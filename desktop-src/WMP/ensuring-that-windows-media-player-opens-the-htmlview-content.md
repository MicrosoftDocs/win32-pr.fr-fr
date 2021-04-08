---
title: S’assurer que le lecteur Windows Media ouvre le contenu HTMLView
description: S’assurer que le lecteur Windows Media ouvre le contenu HTMLView
ms.assetid: 4ec4e027-4f9c-4a86-9f70-b4014971c070
keywords:
- Sélections de métafichiers Windows Media, lecteur Windows Media ouvrant le contenu HTMLView
- sélections, lecteur Windows Media ouvrant le contenu HTMLView
- sélections de métafichiers, lecteur Windows Media ouvrant le contenu HTMLView
- Sélections de métafichiers Windows Media, ouverture de contenu HTMLView
- sélections, ouverture de contenu HTMLView
- sélections de métafichiers, ouverture de contenu HTMLView
- ouverture du contenu HTMLView
- Lecteur Windows Media, ouverture du contenu HTMLView
- Lecteur Windows Media, contenu HTMLView
- HTMLView, ouverture du contenu
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3d3220be44fcc33b3657fb115b0bb57d07d1b928
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673517"
---
# <a name="ensuring-that-windows-media-player-opens-the-htmlview-content"></a><span data-ttu-id="3e301-113">S’assurer que le lecteur Windows Media ouvre le contenu HTMLView</span><span class="sxs-lookup"><span data-stu-id="3e301-113">Ensuring that Windows Media Player Opens the HTMLView Content</span></span>

<span data-ttu-id="3e301-114">Actuellement, le lecteur Windows Media série 9 et le lecteur Windows Media 10 sont les seuls lecteurs qui prennent en charge le paramètre *HTMLView* dans les fichiers. asx.</span><span class="sxs-lookup"><span data-stu-id="3e301-114">Currently, Windows Media Player 9 Series and Windows Media Player 10 are the only players that support the *HTMLView* parameter in .asx files.</span></span> <span data-ttu-id="3e301-115">Cela signifie que vous devez prendre des mesures pour vous assurer que votre contenu HTMLView est lu dans ces versions du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="3e301-115">This means you should take steps to ensure that your HTMLView content plays back in these versions of Windows Media Player.</span></span>

<span data-ttu-id="3e301-116">Vous devez d’abord déterminer si le lecteur Windows Media série 9 ou le lecteur Windows Media 10 est installé sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3e301-116">You must first determine whether Windows Media Player 9 Series or Windows Media Player 10 is installed on the user's computer.</span></span> <span data-ttu-id="3e301-117">Le kit de développement logiciel (SDK) Windows Media Player comprend un exemple complet qui montre comment détecter les différentes versions de Windows Media Player dans différents navigateurs Web.</span><span class="sxs-lookup"><span data-stu-id="3e301-117">The Windows Media Player SDK includes a comprehensive sample that demonstrates how to detect different versions of Windows Media Player in different Web browsers.</span></span> <span data-ttu-id="3e301-118">Bien qu’une analyse complète de l’exemple de détection dépasse le cadre de cette section, vous pouvez suivre certaines étapes de base pour déterminer la version du lecteur Windows Media que l’ordinateur de l’utilisateur exécute.</span><span class="sxs-lookup"><span data-stu-id="3e301-118">Although a complete analysis of the detection sample is beyond the scope of this section, there are some basic steps you can take to determine which version of Windows Media Player the user's computer is running.</span></span>

<span data-ttu-id="3e301-119">Dans sa forme la plus simple, la détection du lecteur Windows Media consiste à incorporer le contrôle du lecteur dans la page Web qui établit un lien vers votre contenu HTMLView, puis à inspecter la valeur récupérée par le *lecteur*. propriété **VERSIONINFO** .</span><span class="sxs-lookup"><span data-stu-id="3e301-119">In its simplest form, detecting Windows Media Player involves embedding the Player control in the webpage that links to your HTMLView content and then inspecting the value retrieved by the *Player*.**versionInfo** property.</span></span> <span data-ttu-id="3e301-120">Une fois que vous avez vérifié que l’utilisateur a installé le lecteur Windows Media série 9 ou le lecteur Windows Media 10, vous pouvez utiliser la méthode [Player. openPlayer](player-openplayer.md) pour ouvrir le contenu dans le lecteur en mode complet.</span><span class="sxs-lookup"><span data-stu-id="3e301-120">Once you have verified that the user has Windows Media Player 9 Series or Windows Media Player 10 installed, you can use the [Player.openPlayer](player-openplayer.md) method to open the content in the full-mode Player.</span></span> <span data-ttu-id="3e301-121">La méthode **openPlayer** garantit que votre contenu est initialement affiché dans la fonctionnalité de **lecture** en cours du lecteur en mode plein, plutôt que dans une apparence, en mode mini lecteur ou dans un autre lecteur qui s’est inscrit comme programme par défaut pour les fichiers avec une extension de nom de fichier. asx, mais ne prend pas en charge HTMLView.</span><span class="sxs-lookup"><span data-stu-id="3e301-121">The **openPlayer** method ensures that your content is initially displayed in the **Now Playing** feature of the full-mode Player, rather than in a skin, in mini Player mode, or in another player that has registered itself as the default program for files with an .asx file name extension, but doesn't support HTMLView.</span></span> <span data-ttu-id="3e301-122">Toutefois, une fois le contenu affiché, l’utilisateur dispose d’un contrôle total sur le lecteur Windows Media, ce qui signifie qu’il peut choisir d’afficher une fonctionnalité autre que **lecture en cours**, passer en mode apparence ou même quitter le lecteur.</span><span class="sxs-lookup"><span data-stu-id="3e301-122">Once the content is displayed, however, the user has complete control of Windows Media Player, meaning that he or she can choose to display a feature other than **Now Playing**, switch to skin mode, or even quit the Player.</span></span>

<span data-ttu-id="3e301-123">L’exemple de code suivant crée une page Web pour Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3e301-123">The following example code creates a webpage for Internet Explorer.</span></span> <span data-ttu-id="3e301-124">Cette page ouvre un fichier. asx, qui spécifie une page Web HTMLView qui s’affiche dans le lecteur en mode complet lorsque le lecteur Windows Media 9 ou une version ultérieure est installé.</span><span class="sxs-lookup"><span data-stu-id="3e301-124">This page opens an .asx file, which specifies an HTMLView webpage that appears in the full-mode Player when Windows Media Player 9 Series or later is installed.</span></span>


```XML
<HTML>
<BODY>

<!-- This code embeds the Player object in invisible mode. -->
<OBJECT id = "Player" 
    CLASSID = "CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6" height = 0 width = 0> 
        <PARAM Name = "AutoStart"  Value = "True">
        <PARAM Name = "uiMode" Value = "invisible">
</OBJECT>

<!-- Create a button to open the content. -->
<INPUT Type = "Button"  ID = "btnPlay"  Value = "Play ASX"  onClick = "PlayASX();"/>

<SCRIPT Language = "JScript">

// This function tests the Player version. If it is Windows Media 
// Player 9 Series or later, the script opens the .asx file in the full-mode 
// Player. Otherwise, the script makes the embedded control visible to 
// the user and opens the .asx file in the webpage. 

function PlayASX()
{
    if(parseInt(Player.versionInfo) >= 9)
        {
            // Open the full-mode Player to show HTMLView.
            Player.openPlayer("https://www.proseware.com/MyHTMLView.asx");
        }
        else
        {
            // Open the .asx file in the embedded Player.
            Player.uiMode = "full";
            Player.height = 200;
            Player.width = 200;
            Player.URL = "https://www.proseware.com/MyHTMLView.asx";
        }
}
</SCRIPT>

</BODY>
</HTML>

```



<span data-ttu-id="3e301-125">Le code de l’exemple précédent incorpore le contrôle du lecteur Windows Media avec la propriété **UIMODE** définie sur « invisible » et les attributs Height et Width du joueur ont la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="3e301-125">The code in the preceding example embeds the Windows Media Player control with the **uiMode** property set to "invisible" and the Player height and width attributes set to zero.</span></span> <span data-ttu-id="3e301-126">Cela est dû au fait que la page Web ne nécessite pas l’affichage initial de l’interface utilisateur du contrôle du lecteur ; elle nécessite uniquement l’accès au modèle objet du lecteur.</span><span class="sxs-lookup"><span data-stu-id="3e301-126">This is because the webpage does not require the Player control user interface to be displayed initially—it only requires access to the Player object model.</span></span> <span data-ttu-id="3e301-127">La page affiche également un bouton d’entrée qui permet à l’utilisateur de lire le fichier. asx.</span><span class="sxs-lookup"><span data-stu-id="3e301-127">The page also displays an input button that enables the user to play the .asx file.</span></span>

<span data-ttu-id="3e301-128">Quand l’utilisateur clique sur le bouton Play ASX, la fonction Microsoft JScript PlayASX s’exécute.</span><span class="sxs-lookup"><span data-stu-id="3e301-128">When the user clicks the Play ASX button, the Microsoft JScript function PlayASX runs.</span></span> <span data-ttu-id="3e301-129">Cette fonction récupère d’abord la valeur de la propriété de joueur **VERSIONINFO** , à l’aide de la méthode JScript **parseInt** pour inspecter la valeur numérique de la chaîne récupérée.</span><span class="sxs-lookup"><span data-stu-id="3e301-129">This function first retrieves the value for the Player **versionInfo** property, using the JScript **parseInt** method to inspect the numerical value of the string retrieved.</span></span> <span data-ttu-id="3e301-130">Si la valeur numérique est supérieure ou égale à 9 (ce qui signifie que l’utilisateur a installé le lecteur Windows Media série 9), le code de script appelle la méthode **openPlayer** , en passant l’URL du fichier. asx qui contient le paramètre HTMLView.</span><span class="sxs-lookup"><span data-stu-id="3e301-130">If the numerical value is greater than or equal to 9 (meaning that the user has Windows Media Player 9 Series installed), the script code calls the **openPlayer** method, passing the URL of the .asx file that contains the HTMLView parameter.</span></span> <span data-ttu-id="3e301-131">Cette méthode ouvre le fichier. asx à l’aide du lecteur Windows Media en mode complet, lit le contenu multimédia numérique dans la sélection. asx et affiche le contenu Web HTMLView dans la fonctionnalité de **lecture** en cours.</span><span class="sxs-lookup"><span data-stu-id="3e301-131">This method opens the .asx file using Windows Media Player in full mode, plays the digital media content in the .asx playlist, and displays the HTMLView Web-based content in the **Now Playing** feature.</span></span>

<span data-ttu-id="3e301-132">Si la valeur numérique de la chaîne de version n’est pas supérieure ou égale à 9 (ce qui signifie que le lecteur Windows Media série 9 ou version ultérieure n’est pas installé sur l’ordinateur), le code de script modifie le **UIMODE** du contrôle Player en « Full », définit une nouvelle largeur et hauteur pour le contrôle, puis ouvre le fichier. asx dans le lecteur incorporé en spécifiant une valeur pour la propriété **URL** .</span><span class="sxs-lookup"><span data-stu-id="3e301-132">If the numerical value of the version string is not greater than or equal to 9 (meaning that the user does not have Windows Media Player 9 Series or later installed on his or her computer), the script code changes the **uiMode** of the Player control to "full", sets a new width and height for the control, and then opens the .asx file in the embedded Player by specifying a value for the **URL** property.</span></span> <span data-ttu-id="3e301-133">Dans ce cas, le contenu multimédia numérique est lu dans la page Web, mais toutes les valeurs HTMLView spécifiées dans le fichier. asx sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="3e301-133">When this happens, the digital media content plays in the webpage, but any HTMLView values specified in the .asx file are ignored.</span></span>

<span data-ttu-id="3e301-134">La façon dont le contenu est lu lorsque l’utilisateur n’a pas le lecteur Windows Media série 9 ou le lecteur Windows Media 10 est installé.</span><span class="sxs-lookup"><span data-stu-id="3e301-134">How content is played back when the user does not have Windows Media Player 9 Series or Windows Media Player 10 installed is up to you.</span></span> <span data-ttu-id="3e301-135">L’exemple précédent montre comment spécifier que le contenu est lu dans la page Web au lieu du lecteur en mode plein, en ignorant tout contenu HTMLView dans le processus.</span><span class="sxs-lookup"><span data-stu-id="3e301-135">The preceding example shows how to specify that the content play in the webpage instead of the full-mode Player, ignoring any HTMLView content in the process.</span></span> <span data-ttu-id="3e301-136">Vous pouvez prendre d’autres approches.</span><span class="sxs-lookup"><span data-stu-id="3e301-136">There are other approaches you might take.</span></span> <span data-ttu-id="3e301-137">Par exemple, vous pouvez inviter l’utilisateur à installer une version plus récente du lecteur Windows Media, ce qui rend cette version du lecteur obligatoire pour la lecture de votre contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="3e301-137">For example, you could prompt the user to install a newer version of Windows Media Player, making that version of the Player a requirement for playing back your digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e301-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e301-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e301-139">**Affichage des pages Web dans le lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="3e301-139">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="3e301-140">**Player. uiMode**</span><span class="sxs-lookup"><span data-stu-id="3e301-140">**Player.uiMode**</span></span>](player-uimode.md)
</dt> <dt>

[<span data-ttu-id="3e301-141">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="3e301-141">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 




