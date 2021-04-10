---
title: Utilisation de SAMI avec le contrôle du lecteur Windows Media dans un navigateur
description: Utilisation de SAMI avec le contrôle du lecteur Windows Media dans un navigateur
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
keywords:
- Lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Modèle objet du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX Mobile Player Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX, SAMI (Synchronized Accessible Media Interchange)
- Fichiers de Media Interchange (SAMI) synchronisés, fichiers
- SAMI (Synchronized Accessible Media Interchange), fichiers
- SAMI (Synchronized Accessible Media Interchange), exemple de code
- SAMI (Synchronized Accessible Media Interchange), exemple de code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b651c3af117942d56ffc5334323913d26cdf6f99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940301"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a><span data-ttu-id="a1697-114">Utilisation de SAMI avec le contrôle du lecteur Windows Media dans un navigateur</span><span class="sxs-lookup"><span data-stu-id="a1697-114">Using SAMI with the Windows Media Player Control in a Browser</span></span>

<span data-ttu-id="a1697-115">Au lieu de créer un fichier SAMI pour chaque style ou langage de police, vous pouvez déclarer différentes classes de style dans un fichier à l’aide de scripts de base et du modèle objet de contrôle du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a1697-115">Instead of creating a SAMI file for each font style or language, you can declare different style classes in one file by using basic scripting and the Windows Media Player control object model.</span></span> <span data-ttu-id="a1697-116">Vous pouvez créer des contrôles personnalisés qui permettent à l’utilisateur de choisir entre les différentes options de style et de langue.</span><span class="sxs-lookup"><span data-stu-id="a1697-116">You can create custom controls that enable the user to choose between the different style and language options.</span></span> <span data-ttu-id="a1697-117">En outre, vous disposez d’un contrôle total sur la conception de l’interface du lecteur et la personnalisation de chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="a1697-117">Furthermore, you have complete control over the design of the Player interface and the customization of each function.</span></span>

<span data-ttu-id="a1697-118">Pour plus d’informations sur l’intégration du contrôle du lecteur Windows Media dans une page [Web, consultez exemple simple de script dans une page Web](simple-example-of-scripting-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="a1697-118">For detailed information about embedding the Windows Media Player control in a webpage, see [Simple Example of Scripting in a Web Page](simple-example-of-scripting-in-a-web-page.md).</span></span>

<span data-ttu-id="a1697-119">L’exemple de code suivant montre comment utiliser des sous-titres avec le contrôle du lecteur Windows Media incorporé dans une page Web.</span><span class="sxs-lookup"><span data-stu-id="a1697-119">The following example code demonstrates how to use closed captions with the Windows Media Player control embedded in a webpage.</span></span> <span data-ttu-id="a1697-120">Il comprend des contrôles pour permettre à l’utilisateur de sélectionner le style et la langue de la police.</span><span class="sxs-lookup"><span data-stu-id="a1697-120">It includes controls to allow the user to select font style and language.</span></span>


```C++
<HTML>
<HEAD>

<SCRIPT>
  // The following variable is used to prevent multiple initialization.
  var initialized = false;
  // The following function populates the select boxes.
  // It is called the first time the media file is opened.
  // Before then, the SAMI settings cannot be retrieved.
  function initialize() {
    var newOption;
    for (var i = 0; i < Player.closedCaption.SAMILangCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMILangName(i);
      newOption.value = newOption.text;
      CCLang.options.add(newOption);
    }
    for (var i = 0; i < Player.closedCaption.SAMIStyleCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMIStyleName(i);
      newOption.value = newOption.text;
      CCStyle.options.add(newOption);
    }
    initialized = true;
  }
</SCRIPT>

<!-- The following script code runs when the page is fully loaded. -->
<SCRIPT for="window" event="onload()">
  Player.closedCaption.captioningID = "captions";
  Player.closedCaption.SAMIFileName = "https://www.proseware.com/Media/seattle.smi";
  // The digital media file will open automatically, after which
  // the OpenStateChange event (handled below) will fire.
  Player.URL = "https://www.proseware.com/Media/seattle.wmv";
</SCRIPT>

<!-- The following script code runs when a media file is opened. -->
<SCRIPT for="Player" event="OpenStateChange(NewState)">
  // The first time this event fires, the Player stops and the 
  // initialize function is called. This allows the user to 
  // select a language and style before viewing the file.
  if (13 == NewState && !initialized) {
    Player.controls.stop();
    initialize();
  }
</SCRIPT>

</HEAD>
<BODY>

<OBJECT 
  ID="Player" 
  classID="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"
  height="200" 
  width="250"
>
</OBJECT>

<TABLE height="100" width="250" border="3" bordercolor="blue">
  <TR align="center">
    <TD bgcolor="white">
      <SELECT ID="CCLang" onClick="Player.closedCaption.SAMILang = value"></SELECT>
      <SELECT ID="CCStyle" onClick="Player.closedCaption.SAMIStyle = value"></SELECT>
    </TD>
  </TR>
  <TR height="75">
    <TD bgcolor="blue">
      <DIV id="captions"></DIV>
    </TD>
  </TR>
</TABLE>

</BODY>
</HTML>

```



## <a name="related-topics"></a><span data-ttu-id="a1697-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a1697-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1697-122">**Ajout de sous-titres à des médias numériques**</span><span class="sxs-lookup"><span data-stu-id="a1697-122">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




