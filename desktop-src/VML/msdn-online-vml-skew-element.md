---
title: Élément pivot incliné
description: Élément pivot incliné
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e317d03fc0bbef361df56282bec55ea2a9e708f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463163"
---
# <a name="vml-skew-element"></a><span data-ttu-id="523ce-103">Élément pivot incliné</span><span class="sxs-lookup"><span data-stu-id="523ce-103">VML Skew Element</span></span>

<span data-ttu-id="523ce-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="523ce-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="523ce-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="523ce-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="523ce-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="523ce-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="523ce-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="523ce-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="523ce-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="523ce-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="523ce-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="523ce-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="523ce-110">Définit une inclinaison pour une forme.</span><span class="sxs-lookup"><span data-stu-id="523ce-110">Defines a skew for a shape.</span></span>

<span data-ttu-id="523ce-111">Les attributs suivants modifient un décalage.</span><span class="sxs-lookup"><span data-stu-id="523ce-111">The following attributes modify a skew.</span></span>



| <span data-ttu-id="523ce-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="523ce-112">Attribute</span></span>                                 | <span data-ttu-id="523ce-113">Description</span><span class="sxs-lookup"><span data-stu-id="523ce-113">Description</span></span>                                    |
|-------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="523ce-114">Ext</span><span class="sxs-lookup"><span data-stu-id="523ce-114">Ext</span></span>](ext-attribute--skew--vml.md)       | <span data-ttu-id="523ce-115">Définit le mode d’affichage d’une inclinaison.</span><span class="sxs-lookup"><span data-stu-id="523ce-115">Defines the way a skew is displayed.</span></span>           |
| [<span data-ttu-id="523ce-116">Identifiant</span><span class="sxs-lookup"><span data-stu-id="523ce-116">ID</span></span>](id-attribute--skew--vml.md)         | <span data-ttu-id="523ce-117">Définit un identificateur unique pour une inclinaison.</span><span class="sxs-lookup"><span data-stu-id="523ce-117">Defines a unique identifier for a skew.</span></span>        |
| [<span data-ttu-id="523ce-118">Matrice</span><span class="sxs-lookup"><span data-stu-id="523ce-118">Matrix</span></span>](matrix-attribute--skew--vml.md) | <span data-ttu-id="523ce-119">Définit une transformation de perspective pour une inclinaison.</span><span class="sxs-lookup"><span data-stu-id="523ce-119">Defines a perspective transform for a skew.</span></span>    |
| [<span data-ttu-id="523ce-120">Offset</span><span class="sxs-lookup"><span data-stu-id="523ce-120">Offset</span></span>](offset-attribute--skew--vml.md) | <span data-ttu-id="523ce-121">Définit le décalage d’une inclinaison.</span><span class="sxs-lookup"><span data-stu-id="523ce-121">Defines the offset of a skew.</span></span>                  |
| [<span data-ttu-id="523ce-122">Activé</span><span class="sxs-lookup"><span data-stu-id="523ce-122">On</span></span>](on-attribute--skew--vml.md)         | <span data-ttu-id="523ce-123">Détermine si l’inclinaison sera affichée.</span><span class="sxs-lookup"><span data-stu-id="523ce-123">Determines whether the skew will be displayed.</span></span> |
| [<span data-ttu-id="523ce-124">Origine</span><span class="sxs-lookup"><span data-stu-id="523ce-124">Origin</span></span>](origin-attribute--skew--vml.md) | <span data-ttu-id="523ce-125">Détermine l’origine d’un décalage.</span><span class="sxs-lookup"><span data-stu-id="523ce-125">Determines the origin of a skew.</span></span>               |



 

<span data-ttu-id="523ce-126">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="523ce-126">**Remarks**</span></span>

<span data-ttu-id="523ce-127">Cet élément doit être défini dans un élément [Shape](shape-element--vml.md) .</span><span class="sxs-lookup"><span data-stu-id="523ce-127">This element must be defined within a [Shape](shape-element--vml.md) element.</span></span>

<span data-ttu-id="523ce-128">En outre, la [matrice](matrix-attribute--skew--vml.md) et [les](on-attribute--skew--vml.md) attributs doivent avoir la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="523ce-128">In addition, the [Matrix](matrix-attribute--skew--vml.md) and [On](on-attribute--skew--vml.md) attributes must be set to **True**.</span></span>

<span data-ttu-id="523ce-129">Voici le code minimal nécessaire pour produire un décalage.</span><span class="sxs-lookup"><span data-stu-id="523ce-129">The following is the minimum code needed to produce a skew.</span></span>


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



<span data-ttu-id="523ce-130">L’élément **skew** est une Extension de Microsoft Office à Vml.</span><span class="sxs-lookup"><span data-stu-id="523ce-130">The **Skew** element is a Microsoft Office Extension to VML.</span></span>

<span data-ttu-id="523ce-131">**Exemples**</span><span class="sxs-lookup"><span data-stu-id="523ce-131">**Examples**</span></span>

-   <span data-ttu-id="523ce-132">[Exemple d’inclinaison simple](/previous-versions/bb229482(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="523ce-132">[Simple Skew Example](/previous-versions/bb229482(v=vs.85))</span></span>
-   [<span data-ttu-id="523ce-133">Exemple d’inclinaison dynamique</span><span class="sxs-lookup"><span data-stu-id="523ce-133">Dynamic Skew Example</span></span>](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 