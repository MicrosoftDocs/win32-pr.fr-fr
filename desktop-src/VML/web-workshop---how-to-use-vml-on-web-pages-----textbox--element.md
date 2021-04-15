---
title: Utilisation de l’élément TextBox
description: Utilisation de l’élément TextBox
ms.assetid: e0022722-a504-47da-aa3f-62aa7fb4ac4d
keywords:
- Atelier Web, élément TextBox
- conception de pages Web, élément TextBox
- Langage VML (VML), élément TextBox
- VML (langage VML), élément TextBox
- Vector Graphics, élément TextBox
- élément TextBox
- Éléments VML, TextBox
- Formes VML, élément TextBox
- Langage VML (VML), joindre du texte
- VML (langage VML), joindre du texte
- graphiques vectoriels, joindre du texte
- Formes VML, joindre du texte
- joindre du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5388a359ca8cf4e320f95d708b4cf7055287d424
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463647"
---
# <a name="using-the-textbox-element"></a><span data-ttu-id="14c87-116">Utilisation de l’élément TextBox</span><span class="sxs-lookup"><span data-stu-id="14c87-116">Using the Textbox Element</span></span>

<span data-ttu-id="14c87-117">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="14c87-117">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="14c87-118">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="14c87-118">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="14c87-119">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="14c87-119">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="14c87-120">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="14c87-120">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="14c87-121">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="14c87-121">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="14c87-122">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="14c87-122">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="examples"></a><span data-ttu-id="14c87-123">Exemples :</span><span class="sxs-lookup"><span data-stu-id="14c87-123">Examples:</span></span>

<span data-ttu-id="14c87-124">Pour attacher du texte à un rectangle, vous pouvez taper les lignes suivantes dans la `<BODY>` région de votre page Web :</span><span class="sxs-lookup"><span data-stu-id="14c87-124">To attach text to a rectangle, you can type the following lines in the `<BODY>` region of your Web page:</span></span>


```HTML
<body>
<v:rect style='width:120pt;height:80pt;' fillcolor="red">
<v:textbox>
I'm attaching some text to this shape!!!
</v:textbox>
</v:rect>
</body>
```





<span data-ttu-id="14c87-125">Pour attacher un lien hypertexte à un rectangle arrondi qui est rempli d’un dégradé, vous pouvez taper les lignes suivantes dans la `<BODY>` région de votre page Web :</span><span class="sxs-lookup"><span data-stu-id="14c87-125">To attach a hyperlink to a rounded rectangle that is gradient-filled, you can type the following lines in the `<BODY>` region of your Web page:</span></span>

![textbox2.gif (1147 octets)](images/textbox2.gif)


```HTML
<body>
<v:roundrect style='width:80pt;height:30pt;' fillcolor="red">
<v:fill type="gradient" />
<v:textbox>
<a href="https://home.microsoft.com/"> Click here</a>
</v:textbox>
</v:roundrect>
</body>
```





<span data-ttu-id="14c87-127">Pour plus d’informations sur cet élément, consultez la [spécification VML](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span><span class="sxs-lookup"><span data-stu-id="14c87-127">For more information about this element, see the [VML specification](https://www.w3.org/TR/NOTE-VML#-toc416858397) .</span></span>

 

 