<script>
  import ExpandableList from '../../components/ExpandableList.svelte';
  const items = [
    {
      title: 'A Philosphy of Software Design',
      links: [
        { text: 'Ch. 2 (home)', href: '/' },
        { text: 'Ch. 3 (home)', href: '/' },
        { text: 'Ch. 4 (art)', href: '/art' },
      ],
    },
    {
      title: 'Learning How to Learn',
      links: [
        { text: 'programming', href: '/programming' },
        { text: 'art', href: '/art' },
        { text: 'blog', href: '/blog' },
      ],
    },
  ];
</script>
<main>
  <a href='/'>Back</a>
  <h1>Blog</h1>
  <p>Here is the list of entries</p>
  <ExpandableList {items} />
</main>

