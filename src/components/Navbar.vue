<template>

    <div>
        
        <ul> 
            <li>
                <a href="">Characters</a>
            </li>
        </ul>
    </div>

</template>

<style lang="scss">

@import '@/assets/styles/variables.scss';

    ul {
        list-style: none;
        display: flex;
        list-style: none;
        background-color: white;
        height: 70px;
        padding: 10px 30px 10px 30px;
        margin-bottom: 5rem;
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12); 

        li {
            margin-right: 100px;
            list-style: none; 
            transform: translateY(10px);
        }
    }



   a {
        text-decoration: none;
        color: black;
        font-size: 1.3rem;
    }   

    a:hover {
        /* text-decoration: underline; */
        color: #E73D4C;
    }

 



</style>