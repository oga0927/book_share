<template>
  <kodomo @add-book-list="addBooks"></kodomo>
</template>

<script>
const STORAGE_KEY = 'books'

export default {
  name: 'PostsList',
  data(){
    return {
      books: [],
    }
  },
  mounted() {
    // ローカルストレージにアイテムがあれば
    if (localStorage.getItem(STORAGE_KEY)) {
      try {
        // JSON.parseで値を持ってきて、this.booksにデータを渡す
        this.books = JSON.parse(localStorage.getItem(STORAGE_KEY));
      } catch(e) {
        localStorage.removeItem(STORAGE_KEY);
      }
    }
  },
  methods: {
    // (e)で子コンポーネントからデータを受け取る
    addBooks(e) {
      
      // 追加があればpushして
      this.books.push({
        id: this.books.length,
        // 子コンポーネント
        title: e.title,
        image: e.image,
        // 説明
        discription: e.discription,
        // 読んだ日、感想
        readDate: '',
        // メモ
        memo: '',
        learn: '',
        important: '',
        examples: '',
        different: '',
        userId: this.$store.state.userId,
      })
      // this.saveBooksに保存する
      this.saveBooks();

      // 最新のidが入った状態
      this.goToEditPage(this.books.slice(-1)[0].id)

    },
    removeBook(x) {
      this.books.splice(x, 1);
      this.saveBooks();
    },
    saveBooks() {
      const parsed = JSON.stringify(this.books);
      localStorage.setItem(STORAGE_KEY, parsed);
    },
    // 最新のid
    goToEditPage(id) {
      // ページの切り替え
      this.$router.push(`/edit/${id}`)
    },
  }
}
</script>