---
title: PreferRelative VML (attribut)
description: PreferRelative VML (attribut)
ms.assetid: 7de616e8-4fc3-4bcb-8e5e-ea153d6d4b54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa425321c1937c4df1bb766c554dbd73cc384b3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031334"
---
# <a name="vml-preferrelative-attribute"></a><span data-ttu-id="a3cd4-103">PreferRelative VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="a3cd4-103">VML PreferRelative Attribute</span></span>

<span data-ttu-id="a3cd4-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a3cd4-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a3cd4-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a3cd4-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a3cd4-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a3cd4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a3cd4-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a3cd4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a3cd4-110">Détermine si la taille d’origine d’un objet est enregistrée après le reformatage.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-110">Determines whether the original size of an object is saved after reformatting.</span></span> <span data-ttu-id="a3cd4-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-111">Read/write.</span></span> <span data-ttu-id="a3cd4-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-112">**VgTriState**.</span></span>

<span data-ttu-id="a3cd4-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-113">**Applies To**</span></span>

[<span data-ttu-id="a3cd4-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="a3cd4-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a3cd4-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-115">**Tag Syntax**</span></span>

<span data-ttu-id="a3cd4-116"><v : *Element* o :preferrelative = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a3cd4-116"><v: *element* o:preferrelative=" *expression* "></span></span>

<span data-ttu-id="a3cd4-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-117">**Remarks**</span></span>

<span data-ttu-id="a3cd4-118">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-118">The default is **False**.</span></span> <span data-ttu-id="a3cd4-119">Si la **valeur est true**, la taille d’origine de l’objet sera stockée et tout redimensionnement sera basé sur un pourcentage de cette taille d’origine.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-119">If **True**, the original size of the object will be stored and all resizing will be based on a percentage of that original size.</span></span> <span data-ttu-id="a3cd4-120">Dans le cas contraire, chaque redimensionnement réinitialisera l’échelle à 100%.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-120">Otherwise, each resizing will reset the scale to 100%.</span></span>

<span data-ttu-id="a3cd4-121">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="a3cd4-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="a3cd4-122">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a3cd4-122">**Example**</span></span>

<span data-ttu-id="a3cd4-123">Si la forme est redimensionnée, la taille d’origine ne sera pas stockée.</span><span class="sxs-lookup"><span data-stu-id="a3cd4-123">If the shape is resized, the original size will not be stored.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" preferrelative="False"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 