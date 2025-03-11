<script>
    // 创建星空
    function createStars() {
        const container = document.body;
        for (let i = 0; i < 200; i++) {
            const star = document.createElement('div');
            star.className = 'star';
            star.style.left = Math.random() * 100 + '%';
            star.style.top = Math.random() * 100 + '%';
            star.style.width = Math.random() * 3 + 'px';
            star.style.height = star.style.width;
            star.style.setProperty('--duration', Math.random() * 3 + 1 + 's');
            container.appendChild(star);
        }
    }

    // 创建流星
    function createMeteor() {
        setInterval(() => {
            const meteor = document.createElement('div');
            meteor.className = 'meteor';
            meteor.style.left = Math.random() * 100 + '%';
            meteor.style.top = Math.random() * 100 + '%';
            meteor.style.animationDuration = Math.random() * 0.5 + 0.3 + 's';
            document.body.appendChild(meteor);
            setTimeout(() => meteor.remove(), 1000);
        }, 3000);
    }

    // 初始化特效
    window.onload = () => {
        createStars();
        createMeteor();
    };
</script>
