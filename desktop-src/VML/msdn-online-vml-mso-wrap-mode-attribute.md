---
title: VML DCL-attribut de mode habillage
description: VML DCL-attribut de mode habillage
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315599"
---
# <a name="vml-mso-wrap-mode-attribute"></a><span data-ttu-id="bc8b1-103">VML DCL-attribut de mode habillage</span><span class="sxs-lookup"><span data-stu-id="bc8b1-103">VML MSO-Wrap-Mode Attribute</span></span>

<span data-ttu-id="bc8b1-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bc8b1-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bc8b1-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bc8b1-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bc8b1-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bc8b1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bc8b1-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bc8b1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bc8b1-110">Définit le mode d’habillage pour le texte.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-110">Defines the wrapping mode for text.</span></span> <span data-ttu-id="bc8b1-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-111">Read/write.</span></span> <span data-ttu-id="bc8b1-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-112">**String**.</span></span>

<span data-ttu-id="bc8b1-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="bc8b1-113">**Applies To**</span></span>

[<span data-ttu-id="bc8b1-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="bc8b1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="bc8b1-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="bc8b1-115">**Tag Syntax**</span></span>

<span data-ttu-id="bc8b1-116"><v : *Element* style = "mso-Wrap-mode : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="bc8b1-116"><v: *element* style="mso-wrap-mode: *expression* "></span></span>

<span data-ttu-id="bc8b1-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="bc8b1-117">**Remarks**</span></span>

<span data-ttu-id="bc8b1-118">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="bc8b1-118">Values include:</span></span>



| <span data-ttu-id="bc8b1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc8b1-119">Value</span></span>          | <span data-ttu-id="bc8b1-120">Description</span><span class="sxs-lookup"><span data-stu-id="bc8b1-120">Description</span></span>                          |
|----------------|--------------------------------------|
| <span data-ttu-id="bc8b1-121">square</span><span class="sxs-lookup"><span data-stu-id="bc8b1-121">square</span></span>         | <span data-ttu-id="bc8b1-122">Encapsule le texte autour de la forme dans un carré.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-122">Wraps text around shape in a square.</span></span> |
| <span data-ttu-id="bc8b1-123">raccords</span><span class="sxs-lookup"><span data-stu-id="bc8b1-123">tight</span></span>          | <span data-ttu-id="bc8b1-124">Le texte est renvoyé à la fin de la forme.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-124">Text is wrapped close to the shape.</span></span>  |
| <span data-ttu-id="bc8b1-125">haut et bas</span><span class="sxs-lookup"><span data-stu-id="bc8b1-125">top-and-bottom</span></span> | <span data-ttu-id="bc8b1-126">Le texte se déplace de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-126">Text jumps from top to bottom.</span></span>       |
| <span data-ttu-id="bc8b1-127">jusqu'à</span><span class="sxs-lookup"><span data-stu-id="bc8b1-127">through</span></span>        | <span data-ttu-id="bc8b1-128">Le texte s’affiche dans la forme.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-128">Text displays through the shape.</span></span>     |
| <span data-ttu-id="bc8b1-129">aucun</span><span class="sxs-lookup"><span data-stu-id="bc8b1-129">none</span></span>           | <span data-ttu-id="bc8b1-130">Le texte n’est pas renvoyé à la ligne.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-130">Text doesn't wrap.</span></span>                   |



 

<span data-ttu-id="bc8b1-131">Utilisé par Microsoft PowerPoint pour l’enregistrement au format HTML pour indiquer si le retour automatique à la ligne dans une forme automatique est activé (**carré**) ou désactivé (**aucun**).</span><span class="sxs-lookup"><span data-stu-id="bc8b1-131">Used by Microsoft PowerPoint for saving to HTML to indicate whether word wrap inside an AutoShape is on (**square**) or off (**none**).</span></span>

<span data-ttu-id="bc8b1-132">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="bc8b1-132">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="bc8b1-133">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="bc8b1-133">**Example**</span></span>

<span data-ttu-id="bc8b1-134">Le code suivant indique que les retours automatique à l’intérieur d’une forme automatique sont activés dans PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="bc8b1-134">The following code indicates that wordwrap inside an AutoShape is turned on in PowerPoint.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 