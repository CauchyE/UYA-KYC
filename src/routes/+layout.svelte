<script>
	import '../app.css';
</script>

<div class="w-screen h-screen">
	<!-- ヘッダー -->
	<!-- https://daisyui.com/components/navbar/#navbar-with-dropdown-center-logo-and-icon -->
	<div class="navbar bg-base-200">
		<div class="navbar-start">
			<div class="dropdown">
				<label tabindex="0" class="btn btn-ghost btn-circle">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="h-5 w-5"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						><path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M4 6h16M4 12h16M4 18h7"
						/></svg
					>
				</label>
				<ul
					tabindex="0"
					class="menu menu-compact dropdown-content mt-3 p-2 shadow bg-base-100 rounded-box w-52"
				>
					<li><a>Home</a></li>
					<li><a>Provider</a></li>
					<li><a>About</a></li>
				</ul>
			</div>
		</div>
		<div class="navbar-center">
			<a class="btn btn-ghost normal-case text-xl">CauchyE ASIA</a>
		</div>
		<div class="navbar-end">
			<button class="btn btn-ghost btn-circle">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					class="h-5 w-5"
					fill="none"
					viewBox="0 0 24 24"
					stroke="currentColor"
					><path
						stroke-linecap="round"
						stroke-linejoin="round"
						stroke-width="2"
						d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
					/></svg
				>
			</button>
			<button class="btn btn-ghost btn-circle">
				<div class="indicator">
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="h-5 w-5"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						><path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M15 17h5l-1.405-1.405A2.032 2.032 0 0118 14.158V11a6.002 6.002 0 00-4-5.659V5a2 2 0 10-4 0v.341C7.67 6.165 6 8.388 6 11v3.159c0 .538-.214 1.055-.595 1.436L4 17h5m6 0v1a3 3 0 11-6 0v-1m6 0H9"
						/></svg
					>
					<span class="badge badge-xs badge-primary indicator-item" />
				</div>
			</button>
		</div>
	</div>

	<!-- コンテンツ -->
	<div class="w-full min-h-full p-5">
		<slot />
	</div>

	<!-- フッター -->
	<!-- https://daisyui.com/components/footer/#two-footer -->
	<footer class="footer p-10 bg-base-200 text-base-content">
		<div>
			<span class="footer-title">UnUniFi</span>
			<a class="link link-hover">Landing Page</a>
			<a class="link link-hover">Portal</a>
			<a class="link link-hover">Explorer</a>
		</div>
		<div>
			<span class="footer-title">Company</span>
			<a class="link link-hover">About us</a>
			<a class="link link-hover">Contact</a>
			<a class="link link-hover">Jobs</a>
			<a class="link link-hover">Press kit</a>
		</div>
		<div>
			<span class="footer-title">Legal</span>
			<a class="link link-hover">Terms of use</a>
			<a class="link link-hover">Privacy policy</a>
			<a class="link link-hover">Cookie policy</a>
		</div>
	</footer>
	<footer class="footer px-10 py-4 border-t bg-base-200 text-base-content border-base-300">
		<div class="items-center grid-flow-col">
			<svg
				width="24"
				height="24"
				viewBox="0 0 24 24"
				xmlns="http://www.w3.org/2000/svg"
				fill-rule="evenodd"
				clip-rule="evenodd"
				class="fill-current"
				><path
					d="M22.672 15.226l-2.432.811.841 2.515c.33 1.019-.209 2.127-1.23 2.456-1.15.325-2.148-.321-2.463-1.226l-.84-2.518-5.013 1.677.84 2.517c.391 1.203-.434 2.542-1.831 2.542-.88 0-1.601-.564-1.86-1.314l-.842-2.516-2.431.809c-1.135.328-2.145-.317-2.463-1.229-.329-1.018.211-2.127 1.231-2.456l2.432-.809-1.621-4.823-2.432.808c-1.355.384-2.558-.59-2.558-1.839 0-.817.509-1.582 1.327-1.846l2.433-.809-.842-2.515c-.33-1.02.211-2.129 1.232-2.458 1.02-.329 2.13.209 2.461 1.229l.842 2.515 5.011-1.677-.839-2.517c-.403-1.238.484-2.553 1.843-2.553.819 0 1.585.509 1.85 1.326l.841 2.517 2.431-.81c1.02-.33 2.131.211 2.461 1.229.332 1.018-.21 2.126-1.23 2.456l-2.433.809 1.622 4.823 2.433-.809c1.242-.401 2.557.484 2.557 1.838 0 .819-.51 1.583-1.328 1.847m-8.992-6.428l-5.01 1.675 1.619 4.828 5.011-1.674-1.62-4.829z"
				/></svg
			>
			<p>CauchyE ASIA PTE. LTD.</p>
		</div>
	</footer>
</div>
