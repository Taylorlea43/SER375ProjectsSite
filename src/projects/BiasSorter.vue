<template>
    <div>
        <twoColumnTemplate :projectTitle="projectTitle" :author="author" :pictures="pictures" :video="video">
            <template v-slot:description>
                <p>
                    This is a bias sorting website for K-Pop fans. A bias in K-Pop is a fan's favorite member(s) within
                    a
                    group.
                    Often, fans will categorize their biases among all of the groups they like. Typically the categories
                    will be "Ults", "Semi-Ult", and "Regular". An "ult bias", short for "ultimate bias", is the
                    person/people that are the fan's most favorite amongst all of their biases. "Semi-ult" is a step
                    down from this and "regular" is all of the other people this fan likes. The categories don't have
                    to be these, though. For example, a fan may have a category called "Birthday Twins", composed of
                    those who share a birthday with the fan.
                    <br><br>
                    The website contains features other than just sorting biases, which can be read about on the site's
                    help page.
                </p>
            </template>
            <template v-slot:story>
                <p>
                    I wanted to make this website because as a K-Pop fan, I like to categorize my favorites into
                    categories. Prior to this website, I would use a spreadsheet. One sheet would display all of my
                    favorites in alphabetical order of the group, and another sheet displayed my favorites in the
                    categories I created. I ran into an issue where I would add someone to one sheet and forget to
                    add them to the other sheet. I thought to myself, "I wish this could just be automated!" This
                    was at the same time we had to think of an idea for this project. So that's what I decided to do!
                    <br><br>
                    In order to make this project, I used the Vue framework, which makes it easier to use HTML, CSS, and
                    JavaScript. My earlier workplans were creating the bare bones of the website with just HTML, CSS,
                    and basic JavaScript. Then halfway through, I transitioned over to the Vue framework. That's when I
                    implemented more of the harder features, like the draggable elements. Since I had a big interest in
                    the website, and I picked up on the code well, I was able to get more done than I had intented, so I
                    was never struggling to complete anything on time.
                </p>
            </template>
            <template v-slot:strugglesAndTriumphs>
                <p>
                    My biggest struggle with this project was making it so users could have their own log-ins to the
                    website. I did this using Firebase Authorization and Firestore. As my project uses the Vue
                    framework, it was hard to find a tutorial that used data as complex as mine. It took many failed
                    attempts and guidance from Professor Thimineur to finally get it to work. I was close to giving up
                    and let the user's data be based on the browser's local storage, but luckily I was able to figure it
                    out. Now, a user can log-in to their account on separate browsers and devices and keep their data.
                    <b>Tip: <i>Don't</i> use the Vuefire API!!!</b>
                    <br><br>
                    Once I was able to get the users to work, that was a big win! My website was finally completed other
                    than little details and extra stuff that I wanted to add.
                </p>
            </template>
            <template v-slot:links>
                <div style="padding-bottom: 10vh;">
                    <a href="https://shanbrick.github.io/Bias-Sorter/">The Website!!!</a><br>
                    <a href="https://github.com/shanbrick/Bias-Sorter">Github Repo</a><br>
                    <a href="https://chromewebstore.google.com/detail/sheets-to-json/enmkalgdnmcaljdfkojckdbhkjmffmoa">Spreadsheet
                        to JSON - Google Sheet Extension</a><br>
                    <a href="https://www.w3schools.com">Lots of HTML, CSS, JS formatting help!!!</a><br>
                    <a href="https://sortablejs.github.io/Vue.Draggable/#/simple">Draggable Vue components</a><br>
                    <a href="https://www.youtube.com/watch?v=WRqEx2kIbaM&ab_channel=ArtofEngineer">Setting up Firebase
                        in Vue project.</a>
                </div>
            </template>
        </twoColumnTemplate>
    </div>
</template>

<script>
import twoColumnTemplate from '../components/templates/twoColumnTemplate.vue'
import home from '../projects/project_images/BrickettHome.png';
import list from '../projects/project_images/BrickettList.png';
import groups from '../projects/project_images/BrickettGroups.png';
import birthdays from '../projects/project_images/BrickettBirthday.png';
import demoVideo from '../projects/project_videos/BrickettDemo.mp4';

export default {
    name: 'BiasSorter',
    components: {
        twoColumnTemplate
    },
    data() {
        return {
            projectTitle: "Bias Sorter",
            author: "Shannon Brickett",
            pictures: [home, list, groups, birthdays],
            video: demoVideo
        }
    },
    info: {
        title: 'Bias Sorter',
        author: 'Shannon Brickett',
        tags: ["Vue", "Website", "JavaScript", "HTML", "CSS", "Spring 2024"]
    }
}
</script>

<style scoped>
a {
    color: white;
}

h1,
h2,
h3 {
    color: white;
    max-width: 90%;
}

h3 {
    padding-bottom: 5vh;
}

p {
    padding-bottom: 10vh;
    text-align: left;
    max-width: 90%;
}

li {
    color: white;
    padding-bottom: 10vh;
    text-align: left;
    padding-bottom: 5px;
    max-width: 90%;
}

h1 {
    padding-bottom: 2vh;
}
</style>