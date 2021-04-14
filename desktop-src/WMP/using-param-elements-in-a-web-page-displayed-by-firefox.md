---
title: Utilisation d’éléments PARAM dans une page Web affichée par Firefox
description: Utilisation d’éléments PARAM dans une page Web affichée par Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Lecteur Windows Media, éléments PARAM dans l’élément OBJECT
- Windows Media Player Object Model, PARAM, éléments dans l’élément OBJECT
- modèle objet, éléments PARAM dans l’élément OBJECT
- Windows Media Player Mobile, éléments PARAM dans l’élément OBJECT
- Windows Media Player ActiveX Control, PARAM, éléments dans l’élément OBJECT
- Windows Media Player Mobile contrôle ActiveX, éléments PARAM dans l’élément OBJECT
- Contrôle ActiveX, éléments PARAM dans l’élément OBJECT
- incorporation, pages Web
- Incorporation de pages Web, éléments PARAM dans l’élément OBJECT
- PARAM, éléments dans l’élément OBJECT
- Lecteur Windows Media, Firefox
- Windows Media Player Object Model, Firefox
- modèle objet, Firefox
- Windows Media Player Mobile, Firefox
- Contrôle ActiveX du lecteur Windows Media, Firefox
- Windows Media Player Mobile contrôle ActiveX, Firefox
- Contrôle ActiveX, Firefox
- Firefox, éléments PARAM dans l’élément OBJECT
- Incorporation de pages Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "104311680"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="5b8bb-122">Utilisation d’éléments PARAM dans une page Web affichée par Firefox</span><span class="sxs-lookup"><span data-stu-id="5b8bb-122">Using PARAM Elements in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="5b8bb-123">Vous pouvez utiliser des éléments PARAM à l’intérieur d’un élément OBJECT pour définir l’état initial du contrôle Player.</span><span class="sxs-lookup"><span data-stu-id="5b8bb-123">You can use PARAM elements inside an OBJECT element to set the initial state of the Player control.</span></span> <span data-ttu-id="5b8bb-124">Par exemple, les éléments PARAM de l’exemple suivant spécifient que le contrôle doit jouer à Seattle. wmv automatiquement.</span><span class="sxs-lookup"><span data-stu-id="5b8bb-124">For example, the PARAM elements in the following example specify that the control should play seattle.wmv automatically.</span></span>


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



<span data-ttu-id="5b8bb-125">La plupart des éléments PARAM peuvent être interprétés par Internet Explorer et par Firefox.</span><span class="sxs-lookup"><span data-stu-id="5b8bb-125">Most PARAM elements can be interpreted by Internet Explorer and by Firefox.</span></span> <span data-ttu-id="5b8bb-126">Toutefois, il existe quelques éléments PARAM que le plug-in Firefox ne prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="5b8bb-126">However, there are a few PARAM elements that the Firefox plug-in does not support.</span></span> <span data-ttu-id="5b8bb-127">Pour plus d’informations sur les éléments PARAM pris en charge par le plug-in Firefox, consultez [éléments param dans un élément Object](param-elements-in-an-object-element.md).</span><span class="sxs-lookup"><span data-stu-id="5b8bb-127">For information about which PARAM elements are supported by the Firefox plug-in, see [PARAM Elements in an OBJECT Element](param-elements-in-an-object-element.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b8bb-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b8bb-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b8bb-129">**Utilisation du contrôle du lecteur Windows Media avec Firefox**</span><span class="sxs-lookup"><span data-stu-id="5b8bb-129">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




