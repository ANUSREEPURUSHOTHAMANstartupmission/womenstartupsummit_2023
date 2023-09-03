

<script is:inline>
    import Partners from "../components/Partners.svelte";


let menu_open = false;

let menu_slt = [
{
"label" : "2021",
"link" : "https://startupmission.in/shelovestech/2021.html",
"target" : "_blank"
},
{
"label" : "2020",
"link" : "https://startupmission.in/shelovestech/2020.html",
"target" : "_blank"
},
{
"label" : "2019",
"link" : "https://startupmission.in/shelovestech/2019.html",
"target" : "_blank"
}
];

let menu_wss = [
{
"label" : "2020",
"link" : "https://startupmission.in/womensummit/2020/",
"target" : "_blank"
},
{
"label" : "2019",
"link" : "https://startupmission.in/womensummit/2019/",
"target" : "_blank"
}
]

let videoId = "3D41jkThUbQ";
let player;
let open = false;

let national_partners = [
{
"image" : "startupindia.png"
},
];

let media_partners = [
{
"image" : "herstart.png"
},
];

let eco_partners = [
{
"image" : "tiew.png"
},
{
"image" : "startupindia.png"
},
{
"image" : "yourstory 1.png"
},
{
"image" : "nsrcel.png"
},
{
"image" : "aws.png"
},
{
"image" : "wien.png"
},
{
"image" : "cwe.png"
},
{
"image" : "she.png"
},
{
"image" : "d2c.png"
},
{
"image" : "NSDC.png"
},{
"image" : "We founder Circle.png"
}
];
</script>
<section id="partners" class="py-16 px-5 bg-[#f6f6f6]">
    <div class="container mx-auto">
        <div class="font-other font-bold text-4xl text-center mb-10">Our Partners</div>

        <div class="grid md:grid-cols-2 mb-10">
            <!-- <div class="">
                <div class="font-other font-bold text-xl text-center mb-2">National Partner</div>
                <Partners partners={national_partners} />
            </div>
            <div class="">
                <div class="font-other font-bold text-xl text-center mb-2">Media Partner</div>

                <Partners partners={media_partners}/>
            </div> -->
        </div>

        <div>
            <!-- <div class="font-other font-bold text-xl text-center mb-2">Ecosystem Partners</div> -->
            <Partners  partners={eco_partners}/>
        </div>
    </div>
</section>

