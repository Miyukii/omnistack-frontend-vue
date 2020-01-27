<template>
    <li class="dev-item">
        <header>
            <img :src="dev.avatar_url" :alt="dev.name" />
            <div class="user-info">
                <strong>{{dev.name}}</strong>
                <span>{{dev.techs.join(', ')}}</span>
            </div>
        </header>

        <p>{{dev.bio}}</p>
        <a href="{`https://github.com/${dev.github_username}`}">Acessar perfil do GitHub</a>
    </li>
</template>

<script>
    export default {
        name: 'DevItem',
        props: {
            dev: Object
        }
    }
</script>

<style>

    li.dev-item {
        background: #fff;
        box-shadow: 0 0 14px 0 rgba(0, 0, 0, 0.02);
        border-radius: 2px;
        padding: 20px;
    }

    li.dev-item header img {
        width: 54px;
        height: 54px;
        border-radius: 50%;
    }

    li.dev-item header {
        display: flex;
        flex-direction: row;
        align-items: center;
    }

    li.dev-item header .user-info {
        margin-left: 10px;
    }

    .user-info strong {
        display: block;
        font-size: 16px;
        color: #333;
    }

    .user-info span {
        font-size: 13px;
        color: #999;
        margin-top: 2px;
    }

    li.dev-item p {
        color: #666;
        font-size: 14px;
        line-height: 20px;
        margin: 10px 0;
    }

    li.dev-item a {
        color: #8e4dff;
        font-size: 14px;
        text-decoration: none;
    }

    li.dev-item a:hover {
        color: #5a2ea6;
    }
</style>