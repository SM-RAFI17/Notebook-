<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ConnectHub — Connect Your World</title>

<style>
:root {
  --bg: #f0f2f5;
  --card: #ffffff;
  --text: #172033;
  --muted: #687386;
  --primary: #2563eb;
  --border: #e4e8ef;
  --shadow: 0 4px 18px rgba(20,35,70,.06);
}
body.dark {
  --bg: #101522;
  --card: #1b2434;
  --text: #f1f5f9;
  --muted: #a8b3c7;
  --primary: #6091ff;
  --border: #303b4e;
  --shadow: 0 4px 18px rgba(0,0,0,.12);
}
* { box-sizing: border-box; }
body {
  margin: 0;
  font-family: Arial, Helvetica, sans-serif;
  background: var(--bg);
  color: var(--text);
  transition: background .2s, color .2s;
}
button, input, textarea { font: inherit; }
button { cursor: pointer; }
.topbar {
  position: sticky;
  top: 0;
  z-index: 10;
  display: flex;
  align-items: center;
  gap: 16px;
  padding: 12px 5%;
  background: var(--card);
  border-bottom: 1px solid var(--border);
}
.logo {
  font-size: 25px;
  font-weight: 800;
  color: var(--primary);
  letter-spacing: -.8px;
}
.search {
  flex: 1;
  max-width: 440px;
  margin-left: auto;
}
.search input {
  width: 100%;
  border: 1px solid var(--border);
  background: var(--bg);
  color: var(--text);
  padding: 11px 15px;
  border-radius: 24px;
  outline: none;
}
.icon-btn {
  border: 1px solid var(--border);
  color: var(--text);
  background: var(--card);
  border-radius: 12px;
  padding: 10px 12px;
}
.layout {
  max-width: 1180px;
  margin: 24px auto;
  padding: 0 16px;
  display: grid;
  grid-template-columns: 225px minmax(0, 620px) 225px;
  gap: 20px;
  align-items: start;
}
.card {
  background: var(--card);
  border: 1px solid var(--border);
  border-radius: 18px;
  box-shadow: var(--shadow);
  overflow: hidden;
  margin-bottom: 18px;
}
.side-card { padding: 18px; }
.profile-cover {
  height: 75px;
  background: linear-gradient(120deg,#2563eb,#8b5cf6,#ec4899);
}
.avatar {
  width: 54px;
  height: 54px;
  border-radius: 50%;
  display: grid;
  place-items: center;
  font-size: 25px;
  font-weight: 700;
  background: linear-gradient(135deg,#dbeafe,#c4b5fd);
  color: #273b76;
  border: 3px solid var(--card);
}
.profile-info {
  padding: 0 16px 18px;
  margin-top: -28px;
}
.name { font-weight: 800; margin-top: 10px; }
.muted { color: var(--muted); font-size: 13px; }
.nav-item {
  padding: 12px 10px;
  border-radius: 11px;
  margin-top: 5px;
  font-weight: 600;
}
.nav-item.active, .nav-item:hover {
  color: var(--primary);
  background: var(--bg);
}
.section-title { font-size: 16px; font-weight: 800; margin: 0 0 14px; }
.composer { padding: 18px; }
.composer-top {
  display: flex;
  align-items: center;
  gap: 12px;
}
.composer textarea {
  flex: 1;
  resize: vertical;
  min-height: 64px;
  padding: 13px;
  border-radius: 14px;
  border: 1px solid var(--border);
  background: var(--bg);
  color: var(--text);
  outline: none;
}
.composer-actions {
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  margin-top: 14px;
}
.btn {
  border: none;
  border-radius: 11px;
  padding: 10px 16px;
  font-weight: 700;
}
.btn-primary { background: var(--primary); color: white; }
.btn-secondary {
  background: var(--bg);
  color: var(--text);
  border: 1px solid var(--border);
}
.post { padding: 18px; }
.post-header {
  display: flex;
  align-items: center;
  gap: 11px;
}
.post-header .avatar { width: 43px; height: 43px; font-size: 20px; }
.post-name { font-weight: 800; }
.post-menu { margin-left: auto; }
.post-text { line-height: 1.6; white-space: pre-wrap; overflow-wrap: anywhere; }
.post-image {
  width: 100%;
  max-height: 460px;
  object-fit: cover;
  border-radius: 13px;
  margin-top: 10px;
}
.post-stats {
  color: var(--muted);
  display: flex;
  justify-content: space-between;
  padding: 12px 0;
  border-bottom: 1px solid var(--border);
  font-size: 13px;
}
.post-actions { display: flex; gap: 7px; margin-top: 8px; }
.post-actions button {
  flex: 1;
  border: none;
  background: transparent;
  color: var(--muted);
  padding: 11px 3px;
  border-radius: 9px;
  font-weight: 700;
}
.post-actions button:hover { background: var(--bg); }
.post-actions .liked { color: #ef4444; }
.comment-box {
  display: flex;
  gap: 8px;
  margin-top: 12px;
}
.comment-box input {
  min-width: 0;
  flex: 1;
  border: 1px solid var(--border);
  background: var(--bg);
  color: var(--text);
  padding: 11px;
  border-radius: 20px;
  outline: none;
}
.comment {
  padding: 10px 12px;
  background: var(--bg);
  border-radius: 12px;
  margin-top: 8px;
  overflow-wrap: anywhere;
}
.stat {
  display: flex;
  justify-content: space-between;
  margin: 12px 0;
  color: var(--muted);
  font-size: 14px;
}
.stat strong { color: var(--text); }
footer {
  text-align: center;
  color: var(--muted);
  padding: 18px;
  font-size: 12px;
}
.empty { padding: 35px 15px; text-align: center; color: var(--muted); }
.hidden { display: none !important; }
#toast {
  position: fixed;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  background: #172033;
  color: white;
  padding: 12px 18px;
  border-radius: 12px;
  z-index: 30;
  display: none;
  box-shadow: var(--shadow);
}
@media (max-width: 900px) {
  .layout { grid-template-columns: 190px minmax(0,1fr); }
  .right-sidebar { display: none; }
}
@media (max-width: 620px) {
  .topbar { padding: 11px 12px; gap: 8px; }
  .logo { font-size: 21px; }
  .search { max-width: none; }
  .search input { padding: 10px; }
  .layout { display: block; margin: 14px auto; padding: 0 10px; }
  .left-sidebar { display: none; }
  .card { border-radius: 15px; }
  .composer, .post { padding: 14px; }
  .icon-btn { padding: 9px; }
}
</style>
</head>

<body>

<header class="topbar">
  <div class="logo">ConnectHub.</div>
  <div class="search">
    <input id="searchInput" type="search" placeholder="🔍 Search posts..." aria-label="Search posts">
  </div>
  <button class="icon-btn" id="themeBtn" title="Toggle theme">🌙</button>
</header>

<div class="layout">

  <aside class="left-sidebar">
    <section class="card">
      <div class="profile-cover"></div>
      <div class="profile-info">
        <div class="avatar">R</div>
        <div class="name" id="sidebarName">ConnectHub User</div>
        <div class="muted">Welcome to your community</div>
      </div>
    </section>

    <section class="card side-card">
      <div class="nav-item active">🏠 &nbsp; Home Feed</div>
      <div class="nav-item" id="profileNav">👤 &nbsp; My Profile</div>
      <div class="nav-item" id="savedNav">💾 &nbsp; Saved Posts</div>
      <div class="nav-item" id="allNav">🌐 &nbsp; All Posts</div>
    </section>
  </aside>

  <main>
    <section class="card composer">
      <h2 class="section-title">Create a post ✨</h2>
      <div class="composer-top">
        <div class="avatar">R</div>
        <textarea id="postText" placeholder="What's on your mind?"></textarea>
      </div>
      <div class="composer-actions">
        <label class="btn btn-secondary" for="imageInput">🖼️ Add photo</label>
        <input class="hidden" id="imageInput" type="file" accept="image/*">
        <span id="fileLabel" class="muted">No photo selected</span>
        <button class="btn btn-primary" id="publishBtn">Publish Post ↗</button>
      </div>
    </section>

    <div id="feed"></div>
  </main>

  <aside class="right-sidebar">
    <section class="card side-card">
      <h3 class="section-title">✨ Your ConnectHub</h3>
      <p class="muted">A place to share ideas, photos and moments.</p>
      <div class="stat"><span>Total posts</span><strong id="totalPosts">0</strong></div>
      <div class="stat"><span>Total likes</span><strong id="totalLikes">0</strong></div>
      <div class="stat"><span>Saved posts</span><strong id="totalSaved">0</strong></div>
    </section>
    <section class="card side-card">
      <h3 class="section-title">💡 Community tips</h3>
      <p class="muted">Be kind, respect others, and share something positive.</p>
      <p class="muted">Your posts are currently saved only in this browser.</p>
    </section>
  </aside>

</div>

<footer>© 2026 ConnectHub · Connect your world 🌐</footer>
<div id="toast" role="status"></div>

<script>
const $ = id => document.getElementById(id);
const STORE_KEY = "connecthub_premium_posts_v1";
const SAVED_KEY = "connecthub_premium_saved_v1";

let posts = loadPosts();
let savedPosts = loadSaved();
let selectedImage = "";
let currentView = "all";
let toastTimer;

function loadPosts() {
  try {
    const data = JSON.parse(localStorage.getItem(STORE_KEY) || "[]");
    return Array.isArray(data) ? data : [];
  } catch { return []; }
}
function loadSaved() {
  try { return JSON.parse(localStorage.getItem(SAVED_KEY) || "[]"); }
  catch { return []; }
}
function saveData() {
  try {
    localStorage.setItem(STORE_KEY, JSON.stringify(posts));
    localStorage.setItem(SAVED_KEY, JSON.stringify(savedPosts));
    return true;
  } catch {
    notify("Storage full. Try removing a large photo.");
    return false;
  }
}
function notify(message) {
  const box = $("toast");
  box.textContent = message;
  box.style.display = "block";
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => box.style.display = "none", 2300);
}
function escapeHTML(value) {
  return String(value).replace(/[&<>"']/g, char => ({
    "&": "&amp;", "<": "&lt;", ">": "&gt;",
    '"': "&quot;", "'": "&#39;"
  })[char]);
}
function safeImage(src) {
  return typeof src === "string" && src.startsWith("data:image/") ? src : "";
}
function render() {
  const query = $("searchInput").value.trim().toLowerCase();
  let visible = posts.filter(post =>
    (post.text || "").toLowerCase().includes(query)
  );

  if (currentView === "saved") {
    visible = visible.filter(post => savedPosts.includes(post.id));
  }
  if (currentView === "profile") {
    visible = visible.filter(post => post.author === "ConnectHub User");
  }

  $("feed").innerHTML = visible.length ? visible.map(post => {
    const liked = !!post.liked;
    const saved = savedPosts.includes(post.id);
    const comments = Array.isArray(post.comments) ? post.comments : [];

    return `
      <article class="card post">
        <div class="post-header">
          <div class="avatar">R</div>
          <div>
            <div class="post-name">${escapeHTML(post.author || "ConnectHub User")}</div>
            <div class="muted">${escapeHTML(post.date || "")}</div>
          </div>
          <button class="icon-btn post-menu" onclick="deletePost('${post.id}')" aria-label="Delete post">🗑️</button>
        </div>

        ${post.text ? `<p class="post-text">${escapeHTML(post.text)}</p>` : ""}
        ${safeImage(post.image) ? `<img class="post-image" src="${post.image}" alt="Post photo">` : ""}

        <div class="post-stats">
          <span>❤️ ${Number(post.likes) || 0} likes</span>
          <span>${comments.length} comments</span>
        </div>

        <div class="post-actions">
          <button class="${liked ? "liked" : ""}" onclick="toggleLike('${post.id}')">
            ${liked ? "❤️ Liked" : "🤍 Like"}
          </button>
          <button onclick="focusComment('${post.id}')">💬 Comment</button>
          <button onclick="toggleSave('${post.id}')">${saved ? "🔖 Saved" : "🔖 Save"}</button>
        </div>

        <div id="comments-${post.id}">
          ${comments.map((comment, index) => `
            <div class="comment">
              <strong>${escapeHTML(comment.author || "User")}</strong><br>
              ${escapeHTML(comment.text || "")}
            </div>
          `).join("")}
        </div>

        <form class="comment-box" onsubmit="addComment(event, '${post.id}')">
          <input id="comment-input-${post.id}" maxlength="500"
            placeholder="Write a comment..." aria-label="Write a comment">
          <button class="btn btn-primary" type="submit">Send</button>
        </form>
      </article>`;
  }).join("") : `<section class="card empty">
      <div style="font-size:35px">🌱</div>
      <h3>Nothing here yet</h3>
      <p>Share the first post or try another search.</p>
    </section>`;

  $("totalPosts").textContent = posts.length;
  $("totalLikes").textContent = posts.reduce((sum, post) => sum + (Number(post.likes) || 0), 0);
  $("totalSaved").textContent = savedPosts.length;
}

function publishPost() {
  const text = $("postText").value.trim();
  if (!text && !selectedImage) {
    notify("Write something or choose a photo first.");
    return;
  }

  const post = {
    id: Date.now().toString(36) + Math.random().toString(36).slice(2, 7),
    author: "ConnectHub User",
    text,
    image: selectedImage,
    date: new Date().toLocaleString(),
    likes: 0,
    liked: false,
    comments: []
  };

  posts.unshift(post);
  if (!saveData()) {
    posts.shift();
    return;
  }

  $("postText").value = "";
  $("imageInput").value = "";
  $("fileLabel").textContent = "No photo selected";
  selectedImage = "";
  currentView = "all";
  render();
  notify("Your post was published! 🎉");
}

function toggleLike(id) {
  const post = posts.find(item => item.id === id);
  if (!post) return;
  post.liked = !post.liked;
  post.likes = Math.max(0, (Number(post.likes) || 0) + (post.liked ? 1 : -1));
  saveData();
  render();
}
function toggleSave(id) {
  savedPosts = savedPosts.includes(id)
    ? savedPosts.filter(item => item !== id)
    : [...savedPosts, id];
  saveData();
  render();
  notify(savedPosts.includes(id) ? "Post saved 🔖" : "Post removed from saved posts");
}
function deletePost(id) {
  const post = posts.find(item => item.id === id);
  if (!post) return;
  if (!confirm("Delete this post?")) return;
  posts = posts.filter(item => item.id !== id);
  savedPosts = savedPosts.filter(item => item !== id);
  saveData();
  render();
  notify("Post deleted.");
}
function addComment(event, id) {
  event.preventDefault();
  const input = $("comment-input-" + id);
  const text = input.value.trim();
  if (!text) return;

  const post = posts.find(item => item.id === id);
  if (!post) return;
  if (!Array.isArray(post.comments)) post.comments = [];
  post.comments.push({ author: "You", text });
  saveData();
  render();
  notify("Comment added 💬");
}
function focusComment(id) {
  const input = $("comment-input-" + id);
  if (input) input.focus();
}
$("imageInput").addEventListener("change", event => {
  const file = event.target.files[0];
  if (!file) return;
  if (!file.type.startsWith("image/")) {
    notify("Please select an image file.");
    event.target.value = "";
    return;
  }
  if (file.size > 1.5 * 1024 * 1024) {
    notify("Please choose an image smaller than 1.5 MB.");
    event.target.value = "";
    return;
  }
  const reader = new FileReader();
  reader.onload = () => {
    selectedImage = String(reader.result);
    $("fileLabel").textContent = file.name;
  };
  reader.onerror = () => notify("Could not read this image.");
  reader.readAsDataURL(file);
});
$("publishBtn").addEventListener("click", publishPost);
$("searchInput").addEventListener("input", render);
$("themeBtn").addEventListener("click", () => {
  document.body.classList.toggle("dark");
  const dark = document.body.classList.contains("dark");
  $("themeBtn").textContent = dark ? "☀️" : "🌙";
  try { localStorage.setItem("connecthub_theme", dark ? "dark" : "light"); } catch {}
});
$("profileNav").addEventListener("click", () => {
  currentView = "profile";
  render();
  window.scrollTo({ top: 0, behavior: "smooth" });
});
$("savedNav").addEventListener("click", () => {
  currentView = "saved";
  render();
  window.scrollTo({ top: 0, behavior: "smooth" });
});
$("allNav").addEventListener("click", () => {
  currentView = "all";
  render();
  window.scrollTo({ top: 0, behavior: "smooth" });
});

try {
  if (localStorage.getItem("connecthub_theme") === "dark") {
    document.body.classList.add("dark");
    $("themeBtn").textContent = "☀️";
  }
} catch {}

render();
</script>
</body>
</html>
