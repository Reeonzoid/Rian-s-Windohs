<template>
<div class="menuWrapper">
    <div class="menuHeader">
        <img src="~/static/daisy.jpg" class="menuHeader__img">
        Rian
    </div>
    <div class="menuPrograms">
        <div class="menuLeft">
            <ul>
                <li v-for="item in items" :key="item.title" class="itemList__item">
                    <div class="itemList__icon">
                        <i :class="item.icon" ></i>
                    </div>
                    <div class="itemList__text">
                        <span class="itemList__title">{{item.title}}</span>
                        <span class="itemList__sub">{{item.subtitle}}</span>
                    </div>
                </li>

            </ul>
        </div>
        
        <div class="menuRight">
            <ul>
                <li v-for="folder in documents" :key="folder.title" class="documentList__item">
                    <div class="documentList__icon">
                        <i :class="folder.icon"></i>
                    </div>
                    <div class="documentList__text">
                        <span class="documentList__title">{{folder.title}}</span>
                    </div>
                </li>
            </ul>
        </div>

    </div>

</div>
</template>

<script>

export default {
    data () {
        return {
            items: [
                {
                     title: "Internet",
                     subtitle: "Internet Explorer",
                     icon: "fab fa-internet-explorer"

                },
                {
                    title: "E-mail",
                    subtitle: "Outlook Express",
                    icon: "fas fa-envelope-square"
                },
                {
                    title: "Update",
                    subtitle: "Windohs Update",
                    icon: "fas fa-upload"
                },
                {
                    title: "Messenger",
                    subtitle: "Windohs Live Messenger",
                    icon: "fas fa-user"
                }
                
            ],

            documents: [
                {
                    title: "My Documents",
                    icon: "fas fa-folder-open"
                },
                {
                    title: "My Pictures",
                    icon: "fas fa-folder-open"
                },
                {
                    title: "My computer",
                    icon: "fas fa-desktop"
                }
            ]
        }
    }
}

</script>