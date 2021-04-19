---
title: Exemple simple de script dans une page Web
description: Exemple simple de script dans une page Web
ms.assetid: c6d6954e-f684-4dc1-8b9c-c5fc3cab7421
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Contrôle ActiveX du lecteur Windows Media, pages Web
- Windows Media Player Mobile contrôle ActiveX, pages Web
- Contrôle ActiveX, pages Web
- Contrôle ActiveX du lecteur Windows Media, exemple de script
- Contrôle ActiveX mobile pour Windows Media Player, exemple de script
- Contrôle ActiveX, exemple de script
- incorporation, pages Web
- Incorporation de page Web, exemple de script
- exemple de script pour l’incorporation de pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9616bd4032a1b2d7e70916b545db30289995eb4
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "106510850"
---
# <a name="simple-example-of-scripting-in-a-web-page"></a><span data-ttu-id="ef363-119">Exemple simple de script dans une page Web</span><span class="sxs-lookup"><span data-stu-id="ef363-119">Simple Example of Scripting in a Web Page</span></span>

<span data-ttu-id="ef363-120">Vous pouvez facilement incorporer le contrôle du lecteur Windows Media dans un fichier HTML à l’aide de n’importe quel langage de script reconnu par votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="ef363-120">You can easily embed the Windows Media Player control in an HTML file using any scripting language your browser recognizes.</span></span> <span data-ttu-id="ef363-121">L’exemple simple suivant utilise Microsoft JScript pour créer une page qui lit un fichier lorsque vous cliquez sur un bouton et arrête la lecture du fichier lorsque vous cliquez sur un autre bouton.</span><span class="sxs-lookup"><span data-stu-id="ef363-121">The following simple example uses Microsoft JScript to create a page that will play a file when you click on a button, and stop playing the file when you click on another button.</span></span>

<span data-ttu-id="ef363-122">Vous pouvez incorporer le contrôle ActiveX du lecteur Windows Media dans une page Web en suivant les quatre étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ef363-122">You can embed the Windows Media Player ActiveX control in a webpage using the following four steps:</span></span>

1.  <span data-ttu-id="ef363-123">Créez la page Web.</span><span class="sxs-lookup"><span data-stu-id="ef363-123">Create the webpage.</span></span>
2.  <span data-ttu-id="ef363-124">Ajoutez la balise OBJECT.</span><span class="sxs-lookup"><span data-stu-id="ef363-124">Add the OBJECT tag.</span></span>
3.  <span data-ttu-id="ef363-125">Ajoutez une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ef363-125">Add a user interface.</span></span> <span data-ttu-id="ef363-126">Dans ce cas, deux boutons.</span><span class="sxs-lookup"><span data-stu-id="ef363-126">In this case, two buttons.</span></span>
4.  <span data-ttu-id="ef363-127">Ajoutez quelques lignes de code pour répondre quand l’utilisateur clique sur l’un des boutons que vous avez créés.</span><span class="sxs-lookup"><span data-stu-id="ef363-127">Add a few lines of code to respond when the user clicks on one of the buttons you have created.</span></span>

## <a name="creating-the-web-page"></a><span data-ttu-id="ef363-128">Création de la page web</span><span class="sxs-lookup"><span data-stu-id="ef363-128">Creating the Web Page</span></span>

<span data-ttu-id="ef363-129">La première étape consiste à créer une page Web HTML valide.</span><span class="sxs-lookup"><span data-stu-id="ef363-129">The first step is to create a valid HTML webpage.</span></span> <span data-ttu-id="ef363-130">Le code suivant est le minimum nécessaire pour créer une page HTML vide mais valide :</span><span class="sxs-lookup"><span data-stu-id="ef363-130">The following code is the minimum needed to create a blank but valid HTML page:</span></span>


```HTML
<HTML>
    <HEAD>
    </HEAD>
    <BODY>
    </BODY>
</HTML>

```



## <a name="adding-the-object-tag"></a><span data-ttu-id="ef363-131">Ajout de la balise OBJECT</span><span class="sxs-lookup"><span data-stu-id="ef363-131">Adding the OBJECT Tag</span></span>

<span data-ttu-id="ef363-132">Une fois que vous avez créé une page Web, vous devez ajouter une balise d’objet.</span><span class="sxs-lookup"><span data-stu-id="ef363-132">Once you have created a webpage, you need to add an OBJECT tag.</span></span> <span data-ttu-id="ef363-133">Cela identifie le contrôle ActiveX dans le navigateur et définit toutes les définitions initiales.</span><span class="sxs-lookup"><span data-stu-id="ef363-133">This identifies the ActiveX control to the browser and sets up any initial definitions.</span></span> <span data-ttu-id="ef363-134">Vous devez placer la balise OBJECT dans le corps du code.</span><span class="sxs-lookup"><span data-stu-id="ef363-134">You must place the OBJECT tag in the BODY of the code.</span></span> <span data-ttu-id="ef363-135">Si vous le placez dans le corps, l’interface utilisateur par défaut du lecteur Windows Media sera visible.</span><span class="sxs-lookup"><span data-stu-id="ef363-135">If you place it in the BODY, the default user interface of Windows Media Player will be visible.</span></span> <span data-ttu-id="ef363-136">Si vous souhaitez créer votre propre interface utilisateur, définissez les attributs Height et Width sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="ef363-136">If you want to create your own user interface, set the height and width attributes to 0 (zero).</span></span> <span data-ttu-id="ef363-137">Vous pouvez également définir le *lecteur*. propriété **UIMODE** sur « invisible » lorsque vous souhaitez masquer le contrôle, tout en réserve de l’espace pour celui-ci sur la page.</span><span class="sxs-lookup"><span data-stu-id="ef363-137">You can also set the *Player*.**uiMode** property to "invisible" when you want to hide the control, but still reserve space for it on the page.</span></span> <span data-ttu-id="ef363-138">Le code suivant est recommandé lorsque vous fournissez une interface utilisateur personnalisée :</span><span class="sxs-lookup"><span data-stu-id="ef363-138">The following code is recommended when you provide a custom user interface:</span></span>


```HTML
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>

```



<span data-ttu-id="ef363-139">Les attributs de balise d’objet suivants sont requis :</span><span class="sxs-lookup"><span data-stu-id="ef363-139">The following OBJECT tag attributes are required:</span></span>

<span data-ttu-id="ef363-140">id</span><span class="sxs-lookup"><span data-stu-id="ef363-140">ID</span></span>

<span data-ttu-id="ef363-141">Nom qui sera utilisé par d’autres parties du code pour identifier et utiliser le contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="ef363-141">The name that will be used by other parts of the code to identify and use the ActiveX control.</span></span> <span data-ttu-id="ef363-142">Vous pouvez choisir le nom de votre choix, à condition qu’il s’agit d’un nom qui n’est pas déjà utilisé par le HTML, les extensions HTML ou le langage de script que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="ef363-142">You can choose any name you want, as long as it is a name that is not already used by HTML, HTML extensions, or the scripting language you are using.</span></span> <span data-ttu-id="ef363-143">Dans cet exemple, le nom « Player » est utilisé, mais vous pouvez également l’appeler « MyPlayer » ou autre chose.</span><span class="sxs-lookup"><span data-stu-id="ef363-143">In this example, the name "Player" is used, but you could also call it "MyPlayer" or something else.</span></span> <span data-ttu-id="ef363-144">Choisissez simplement un nom qui est unique à cette page Web.</span><span class="sxs-lookup"><span data-stu-id="ef363-144">Just pick a name that is unique to that webpage.</span></span>

<span data-ttu-id="ef363-145">CLASSID</span><span class="sxs-lookup"><span data-stu-id="ef363-145">CLASSID</span></span>

<span data-ttu-id="ef363-146">Nombre hexadécimal très grand qui est unique pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="ef363-146">A very large hexadecimal number that is unique to the control.</span></span> <span data-ttu-id="ef363-147">Un seul contrôle a ce nombre et il s’agit du contrôle ActiveX du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ef363-147">Only one control has this number and it is the Windows Media Player ActiveX control.</span></span> <span data-ttu-id="ef363-148">Pour éviter les erreurs typographiques, vous pouvez copier et coller ce numéro dans la documentation.</span><span class="sxs-lookup"><span data-stu-id="ef363-148">To prevent typographical errors, you can copy and paste this number from the documentation.</span></span> <span data-ttu-id="ef363-149">Les versions du contrôle du lecteur Windows Media antérieures à la version 7,0 ont un CLASSID différent.</span><span class="sxs-lookup"><span data-stu-id="ef363-149">Versions of the Windows Media Player control prior to version 7.0 had a different CLASSID.</span></span>

## <a name="adding-a-user-interface"></a><span data-ttu-id="ef363-150">Ajout d’une interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="ef363-150">Adding a User Interface</span></span>

<span data-ttu-id="ef363-151">HTML offre une multitude d’éléments d’interface utilisateur, ce qui permet à l’utilisateur d’interagir avec votre page Web en cliquant sur les touches et sur les autres actions de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ef363-151">HTML allows a vast wealth of user interface elements, allowing the user to interact with your webpage by clicking, pressing keys, and other user actions.</span></span> <span data-ttu-id="ef363-152">L’ajout de quelques boutons d’entrée est le moyen le plus simple de fournir une interface utilisateur rapide.</span><span class="sxs-lookup"><span data-stu-id="ef363-152">Adding a few INPUT buttons is the easiest way to provide a quick user interface.</span></span> <span data-ttu-id="ef363-153">Le code suivant crée deux boutons qui peuvent répondre à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ef363-153">The following code creates two buttons that can respond to the user.</span></span> <span data-ttu-id="ef363-154">Le fait de cliquer sur un bouton démarre la diffusion du flux multimédia, et l’autre bouton l’arrête :</span><span class="sxs-lookup"><span data-stu-id="ef363-154">Clicking one button starts the media stream playing and the other button stops it:</span></span>


```HTML
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">

```



<span data-ttu-id="ef363-155">Le nom du bouton est utilisé pour identifier le bouton dans votre code ; la valeur est l’étiquette qui s’affiche sur le bouton et l’attribut OnClick identifie la partie de votre code de script qui sera appelée lorsque l’utilisateur clique sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="ef363-155">The name of the button is used to identify the button to your code; the value is the label that will appear on the button, and the OnClick attribute identifies which part of your scripting code will be called when the button is clicked.</span></span>

## <a name="adding-scripting-code"></a><span data-ttu-id="ef363-156">Ajout de code de script</span><span class="sxs-lookup"><span data-stu-id="ef363-156">Adding Scripting Code</span></span>

<span data-ttu-id="ef363-157">Le code de script ajoute l’interactivité à votre page.</span><span class="sxs-lookup"><span data-stu-id="ef363-157">Scripting code adds interactivity to your page.</span></span> <span data-ttu-id="ef363-158">Le code de script peut répondre aux événements, appeler des méthodes et modifier les propriétés au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="ef363-158">Scripting code can respond to events, call methods, and change run-time properties.</span></span> <span data-ttu-id="ef363-159">Les scripts étendus sont placés dans un ensemble de balises de SCRIPT.</span><span class="sxs-lookup"><span data-stu-id="ef363-159">Extended scripts are enclosed in a SCRIPT tag set.</span></span> <span data-ttu-id="ef363-160">La balise SCRIPT indique au navigateur où se trouve votre code de script et identifie le langage de script.</span><span class="sxs-lookup"><span data-stu-id="ef363-160">The SCRIPT tag tells the browser where your scripting code is and identifies the scripting language.</span></span> <span data-ttu-id="ef363-161">Si vous n’identifiez pas une langue, la langue par défaut est Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="ef363-161">If you do not identify a language, the default language will be Microsoft JScript.</span></span>

<span data-ttu-id="ef363-162">Il est recommandé de placer votre script dans des balises de commentaire HTML pour que les navigateurs qui ne prennent pas en charge les scripts n’affichent pas votre code sous forme de texte.</span><span class="sxs-lookup"><span data-stu-id="ef363-162">It is good authoring practice to enclose your script in HTML comment tags so browsers that do not support scripting do not render your code as text.</span></span> <span data-ttu-id="ef363-163">Placez la balise de SCRIPT n’importe où dans le corps de votre fichier HTML et incorporez le code entouré de commentaires dans les balises de SCRIPT d’ouverture et de fermeture.</span><span class="sxs-lookup"><span data-stu-id="ef363-163">Put the SCRIPT tag anywhere within the BODY of your HTML file and embed the comment-surrounded code within the opening and closing SCRIPT tags.</span></span>

<span data-ttu-id="ef363-164">L’exemple de code Microsoft JScript suivant appelle le contrôle du lecteur Windows Media et exécute une action appropriée en réponse au clic de bouton correspondant.</span><span class="sxs-lookup"><span data-stu-id="ef363-164">The following Microsoft JScript code example calls the Windows Media Player control and performs an appropriate action in response to the corresponding button click.</span></span>


```HTML
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>

```



<span data-ttu-id="ef363-165">L’exemple de fonction, StartMeUp, est appelé quand l’utilisateur clique sur le bouton de lecture et que la fonction ShutMeDown est appelée quand l’utilisateur clique sur le bouton arrêter.</span><span class="sxs-lookup"><span data-stu-id="ef363-165">The example function, StartMeUp, is called when the button marked Play is clicked, and the ShutMeDown function is called when the Stop button is clicked.</span></span>

<span data-ttu-id="ef363-166">Le code à l’intérieur de StartMeUp utilise la propriété URL pour définir un chemin d’accès au média.</span><span class="sxs-lookup"><span data-stu-id="ef363-166">The code inside StartMeUp uses the URL property to define a path to the media.</span></span> <span data-ttu-id="ef363-167">Le média commence à s’exécuter immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ef363-167">The media will start playing immediately.</span></span>

<span data-ttu-id="ef363-168">Le code ShutMeDown appelle la méthode **Stop** de l’objet **Controls** .</span><span class="sxs-lookup"><span data-stu-id="ef363-168">The ShutMeDown code calls the **stop** method of the **Controls** object.</span></span> <span data-ttu-id="ef363-169">Notez que l’objet **Controls** est appelé via la propriété **Controls** de l’objet **Player** , qui a la valeur d’ID « Player ».</span><span class="sxs-lookup"><span data-stu-id="ef363-169">Note that the **Controls** object is called through the **controls** property of the **Player** object, which has the ID value of "Player".</span></span>

<span data-ttu-id="ef363-170">L'exemple de code suivant illustre l'exemple complet.</span><span class="sxs-lookup"><span data-stu-id="ef363-170">The following code shows a complete example.</span></span>


```HTML
<HTML>
<HEAD>
</HEAD>
<BODY>
<OBJECT ID="Player" height="0" width="0"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
</OBJECT>
<INPUT TYPE="BUTTON" NAME="BtnPlay" VALUE="Play" OnClick="StartMeUp()">
<INPUT TYPE="BUTTON" NAME="BtnStop" VALUE="Stop" OnClick="ShutMeDown()">
<SCRIPT>
<!--

function StartMeUp ()
{
    Player.URL = "laure.wma";
}

function ShutMeDown ()
{
    Player.controls.stop();
}

-->
</SCRIPT>
</BODY>
</HTML>

```



<span data-ttu-id="ef363-171">Notez que vous devez fournir une URL valide à un nom de fichier valide dans la propriété URL.</span><span class="sxs-lookup"><span data-stu-id="ef363-171">Note that you must provide a valid URL to a valid file name in the URL property.</span></span> <span data-ttu-id="ef363-172">Dans ce cas, il est supposé que le fichier Laure. WMA se trouve dans le même répertoire que le fichier HTML.</span><span class="sxs-lookup"><span data-stu-id="ef363-172">In this case the assumption is that the file laure.wma is in the same directory as the HTML file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef363-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef363-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef363-174">**Utilisation du contrôle du lecteur Windows Media dans une page Web**</span><span class="sxs-lookup"><span data-stu-id="ef363-174">**Using the Windows Media Player Control in a Web Page**</span></span>](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




