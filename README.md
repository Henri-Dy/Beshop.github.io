<!DOCTYPE html>
<html lang="fr" class="flex justify-center items-center flex-col " style="scroll-behavior: smooth; width: 100%; ">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" integrity="sha512-iecdLmaskl7CVkqkXNQ/ZH/XLlvWZOJyj7Yy7tcenmpD1ypASozpmT/E0iPtmFIB46ZmdtAc9eNBvH0H/ZpiBw==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Dosis:wght@300&family=Kablammo&family=Lexend:wght@300&family=Montserrat:wght@300;400&family=Open+Sans:wght@500&family=Poppins:wght@300&display=swap" rel="stylesheet">
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.7.0/jquery.min.js" integrity="sha512-3gJwYpMe3QewGELv8k/BX9vcqhryRdzRMxVfq6ngyWXwo03GFEzjsUm8Q7RZcHPHksttq7/GFoxjCVUjkjvPdw==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
    <title>Beshop</title>
    <style>
        *{
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;           
        }

       
    </style>
</head>
<body class="flex flex-col justify-center items-center min-h-screen  " style="width: 100vw ;">

    <header class="bg-white mb-auto fixed sticky top-0  flex flex-row w-screen  items-center justify-between " style="height:6em ;">
        <img src="https://pbs.twimg.com/media/F1WlsLaXwAEh9XS?format=jpg&name=small" alt="logo de beshop" style="height: 4em; " class="mr-auto ml-5" >
        
        <i class="fa-solid fa-bars text-red-600 mr-5" id="phone_menu_viewer" style="font-size: 24px ;"></i>
        <script>
            $(function(){
                $('.Postuler').click(function(){
                    $('#postuler_section').show();
                    $('#conditions').hide();
                })
                $('.Lire_les_conditions_générales').click(function(){
                    $('#postuler_section').hide();
                    $('#conditions').show();
                })
            });
        </script>
    </header>

    <div class="ml-auto mr-5 p-4  border border-red-400 rounded-md sticky top-20  bg-white  " style="display: none; z-index: 100;" id="phone_menu">

        <ul>
            <li class="hover:text-red-600 Postuler">Postuler</li>
            <li class="hover:text-red-600 Lire_les_conditions_générales">Lire les conditions générales </li>
            <li class="hover:text-red-600"><a href="https://wa.me/68990410?text=">Contactez Beshop</a></li>
        </ul>

        <script>
            $(function(){
                $('#phone_menu_viewer').click(function(){
                    $('#phone_menu').toggle();
                    $('#postuler_section').css('margin-top','-0px  ')
                    
                })
                
            });
        </script>
    </div>


    <section class="min-h-screen flex flex-col justify-center items-center  " id="postuler_section" >
        <div class="shadow-lg   border-red-400 border shadow-red-200 my-2 mx-1 rounded rounded-md">
            <div id="viewed-container" class=" bg-white rounded-md m-8 " style="overflow: hidden ;  transition: 1s ease;">
                <div id="container" class=" bg-white rounded-md    shadow-red-200 w-full flex flex-row duration-1000"   style="width: 200%;  " >
                    <div id="viewed-container" class="bg-white rounded-md     flex flex-col w-full h-full" >
                        <form action="#" class="flex flex-col w-full">
                            <label for="Prenom" style="font-size: 14px;" >Prénom</label>
                            <input type="text" placeholder="Ex:Cloé" class="border border-gray-400 rounded-sm px-2 py-1 hover:border-red-400  duration-200 mt-1 " id="Prenom">
    
                            <label for="nom" style="font-size: 14px;" class="mt-2">Nom</label>
                            <input type="text" placeholder="Ex:DUBOIS" class="border border-gray-400 rounded-sm px-2 py-1 hover:border-red-400  duration-200 mt-1" id="nom">
    
                            <label for="phone_number" style="font-size: 14px;" class="mt-2">Numero de téléphone</label>
                            <input type="number" placeholder="Ex: 01 02 03 04" class="border border-gray-400 rounded-sm px-2 py-1 hover:border-red-400  duration-200 mt-1" id="phone_number">
    
                            <button class="border border-red-400 rounded-sm px-4 py-2 mt-5 text-white bg-red-600 hover:bg-white hover:text-red-500 duration-200 " id="submit-btn" >Soumettre <i class="fa-solid fa-check" ></i></button>
                            
                        </form>
    
                        <script>
                            $(window).on('load', function(){
                                $('#submit-btn').on('click',function(){
                                    $('#container').css('transform','translateX(-50%)');
                    
                                });
                                
                                
                            });
                        </script>
    
                    </div>
    
                    <div id="viewed-container" class="bg-white rounded-md  flex flex-col w-full h-full justify-center items-center mt-20 "   >
                        
                        <p style="font-size: 14px ;">Cliquez pour passer votre entretien <i class="fas fa-hand-point-down text-red-400"></i></p>
    
                        <div class="flex flex-row  rounded-sm mt-5 " id="link_div">
                            <a href="https://wa.me/68990410?text=Salut%20Moi%20C'est"><div><i class="fa-solid fa-up-right-from-square"></i></div></a>
                        </div>
                    </div>
    
                    
                    
                    
                </div>
                
            </div>
        </div>

        <p style="font-size: 12px ; cursor: pointer;" class="text-red-600 mt-4 " id="Veuillez_lire_attentivement">Veuillez lire attentivement les conditions générales avant de postuler !
            <script>
                 $(function(){
                
                    $('#Veuillez_lire_attentivement').click(function(){
                        $('#postuler_section').hide();
                        $('#conditions').show();
                    })
            });
            </script>
        </p>
    
        <script>
       $(function() {
      $('#submit-btn').on('click', function(event) {
        event.preventDefault(); 
        
        var prenom_input = document.getElementById("Prenom").value;
        var nom_input = document.getElementById("nom").value;
        var phone_number_input = document.getElementById("phone_number").value;
    
        var message = "Salut, moi c'est " + prenom_input + " " + nom_input + " et mon numéro de téléphone est " + phone_number_input + ". Je souhaite postuler pour le poste de commercial au compte de l'entreprise Beshop ! Mon lien unique est : https://wa.me/?text=Salut%2C%20je%20viens%20de%20la%20part%20de%20" + prenom_input + nom_input + phone_number_input;
        var encodedMessage = encodeURIComponent(message);
    
        var link = "https://wa.me/68990410?text=" + encodedMessage;
    
        $('#link_div').html('<a href="' + link + '"><div><i class="fa-solid fa-up-right-from-square text-red-400"></div></a>');
      });
    });
    
    </script>
    </section>


    <!-- Voici la section des conditions générales-->


    <section class=" w-full flex justify-center mt-4" id="conditions" style="display: none ;">
        <p class="rounded-md bg-gray-100 p-7 rounded-md " style="width: 80%; ">
            
    
        <span class="text-red-400">Conditions Générales du Programme d'Affiliation</span><br>
    
    1. Définitions<br>
    
    1.1. Dans le cadre des présentes Conditions Générales, les termes suivants auront les significations ci-dessous :<br>
       - "Entreprise" désigne Beshop ;<br>
       - "Affilié" désigne toute personne physique ou morale qui souscrit au Programme d'Affiliation de Beshop ;<br>
       - "Mèche" désigne les produits vendus par Beshop ;<br>
       - "Revenus" désigne les montants générés par les ventes de Mèches ;<br>
       - "Partenaire" désigne un Affilié actif ayant accepté les présentes Conditions Générales.<br><br>
    
    2. Adhésion au Programme d'Affiliation<br>
    
    2.1. Toute personne souhaitant devenir un Partenaire doit s'inscrire via l'application web dédiée développée par Beshop.<br>
    2.2. Beshop se réserve le droit de refuser ou d'accepter une demande d'adhésion au Programme d'Affiliation à sa seule discrétion, sans avoir à fournir de justification.<br><br>
    
    3. Obligations des Partenaires<br>
    
    3.1. Les Partenaires s'engagent à promouvoir les Mèches de Beshop de manière professionnelle, honnête et conforme à la loi.<br>
    3.2. Les Partenaires ne doivent pas engager des pratiques de marketing trompeuses ou mensongères.<br>
    3.3. Les Partenaires sont responsables de la création de leurs propres supports publicitaires, tels que des sites web, des pages de médias sociaux, des publications, etc., pour promouvoir les Mèches de Beshop.<br>
    3.4. Les Partenaires s'engagent à ne pas utiliser de méthodes de promotion illégales, y compris le spamming, le piratage informatique ou toute autre activité répréhensible.<br><br>
    
    4. Commissions et Paiements<br>
    
    4.1. Les Partenaires recevront une commission de 5 % sur le prix de vente de chaque Mèche vendue grâce à leurs efforts de promotion.<br>
    4.2. Les commissions seront calculées sur une base mensuelle.<br>
    4.3. Les paiements des commissions seront effectués [indiquez ici la fréquence des paiements, par exemple, mensuellement/trimestriellement] par Beshop.<br>
    4.4. Les modalités de paiement seront définies par Beshop et communiquées aux Partenaires.<br><br>
    
    5. Propriété Intellectuelle<br>
    
    5.1. Les Partenaires reconnaissent que tous les droits de propriété intellectuelle relatifs aux Mèches, y compris les droits d'auteur, les marques commerciales et les brevets, sont la propriété exclusive de Beshop.<br>
    5.2. Les Partenaires s'engagent à ne pas utiliser les droits de propriété intellectuelle de Beshop sans autorisation préalable et écrite.<br><br>
    
    6. Durée et Résiliation<br>
    
    6.1. Les présentes Conditions Générales entreront en vigueur à la date de l'adhésion du Partenaire et resteront en vigueur jusqu'à leur résiliation conformément aux dispositions ci-dessous.<br>
    6.2. L'une ou l'autre des parties peut résilier le présent contrat d'affiliation à tout moment, moyennant un préavis écrit de [indiquez la durée du préavis, par exemple, 30 jours] à l'autre partie.<br>
    6.3. En cas de non-respect des présentes Conditions Générales, Beshop se réserve le droit de résilier immédiatement le contrat d'affiliation sans préavis.<br><br>
    
    7. Modifications des Conditions Générales<br>
    
    7.1. Beshop se réserve le droit de modifier les présentes Conditions Générales à tout moment et à sa seule discrétion.<br>
    7.2. Les Partenaires seront informés des modifications par le biais de l'application web ou par tout autre moyen jugé approprié par Beshop.<br>
    7.3. En continuant à participer au Programme d'Affiliation après la notification des modifications, les Partenaires acceptent les nouvelles Conditions Générales.<br><br>
    
    8. Loi applicable et juridiction compétente<br>
    
    8.1. Les présentes Conditions Générales seront régies et interprétées conformément aux lois de la République du Bénin.<br>
    8.2. Tout litige découlant des présentes Conditions Générales sera réglé a l'Amiable .<br>
    
    Veuillez vous assurer de bien adapter ce texte en fonction de vos besoins spécifiques. Je recommande également de consulter un professionnel du droit pour vérifier et personnaliser ces documents en fonction des lois en vigueur dans votre pays.<br>
        </p>
    </section>

    

    





<footer class="mt-6" style="font-size: 13px ;">
    © 2023 Beshop. Tous droits réservés.
</footer>
    
    
    
    
    
    
    
    
    

</body>
</html>