---
title: ID, attribut (VML)
description: ID, attribut (VML)
ms.assetid: 39575a1c-f8ea-43e0-9ad5-540e9d803748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a3925166a735b7813efd4cb9bc68f50bb8fa52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463326"
---
# <a name="id-attribute-vml"></a><span data-ttu-id="5ba98-103">ID, attribut (VML)</span><span class="sxs-lookup"><span data-stu-id="5ba98-103">ID Attribute (VML)</span></span>

<span data-ttu-id="5ba98-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5ba98-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5ba98-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5ba98-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5ba98-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="5ba98-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5ba98-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="5ba98-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5ba98-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5ba98-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5ba98-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5ba98-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5ba98-110">Fournit un identificateur unique pour un élément.</span><span class="sxs-lookup"><span data-stu-id="5ba98-110">Provides a unique identifier for an element.</span></span> <span data-ttu-id="5ba98-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5ba98-111">Read/write.</span></span> <span data-ttu-id="5ba98-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="5ba98-112">**String**.</span></span>

<span data-ttu-id="5ba98-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="5ba98-113">**Applies To**</span></span>

<span data-ttu-id="5ba98-114">Tous les éléments VML.</span><span class="sxs-lookup"><span data-stu-id="5ba98-114">All VML elements.</span></span>

<span data-ttu-id="5ba98-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="5ba98-115">**Tag Syntax**</span></span>

<span data-ttu-id="5ba98-116"><v : *ElementName* ID = " *IDname* " ></span><span class="sxs-lookup"><span data-stu-id="5ba98-116"><v: *elementname* id=" *idname* "></span></span>

<span data-ttu-id="5ba98-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="5ba98-117">**Script Syntax**</span></span>

<span data-ttu-id="5ba98-118">*ElementName* . ID = " *IDname* "</span><span class="sxs-lookup"><span data-stu-id="5ba98-118">*elementname* .id =" *idname* "</span></span>

<span data-ttu-id="5ba98-119">*expression* = *ElementName*. ID</span><span class="sxs-lookup"><span data-stu-id="5ba98-119">*expression*=*elementname*.id</span></span>

<span data-ttu-id="5ba98-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="5ba98-120">**Remarks**</span></span>

<span data-ttu-id="5ba98-121">Utilisez **ID** pour faire référence à un élément spécifique.</span><span class="sxs-lookup"><span data-stu-id="5ba98-121">Use **ID** to refer to a specific element.</span></span> <span data-ttu-id="5ba98-122">Une fois que vous avez créé une forme et donné un ID, vous pouvez utiliser le nom de l’ID lorsque vous souhaitez manipuler l’élément.</span><span class="sxs-lookup"><span data-stu-id="5ba98-122">Once you have created a shape and given it an ID, you can use the ID name when you want to manipulate the element.</span></span>

<span data-ttu-id="5ba98-123">L' **ID** est obligatoire pour utiliser l’élément [Typedeforme](msdn-online-vml-shapetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5ba98-123">**ID** is required to use the [ShapeType](msdn-online-vml-shapetype-element.md) element.</span></span>

<span data-ttu-id="5ba98-124">Lorsque VML est généré par Microsoft Office, si un nom de modèle objet est assigné à la forme, **ID** est défini sur ce nom.</span><span class="sxs-lookup"><span data-stu-id="5ba98-124">When VML is generated by Microsoft Office, if an object model name is assigned to the shape, then **ID** is set to this name.</span></span> <span data-ttu-id="5ba98-125">Si le nom du modèle objet n’est pas défini, le nom est généré à l’aide du *SPID* (ID de forme interne) plus un préfixe (S pour forme, M pour la forme principale, T pour Typedeforme).</span><span class="sxs-lookup"><span data-stu-id="5ba98-125">If the object model name is not set, then the name is generated using the *Spid* (internal shape ID) plus a prefix (S for shape, M for master shape, T for shapetype).</span></span>

<span data-ttu-id="5ba98-126">*Attribut standard VML*.</span><span class="sxs-lookup"><span data-stu-id="5ba98-126">*VML Standard Attribute*.</span></span>

<span data-ttu-id="5ba98-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="5ba98-127">**Example**</span></span>

<span data-ttu-id="5ba98-128">Pour modifier les attributs d’une forme, vous devez d’abord attribuer un ID à la forme. par exemple, « myRect ».</span><span class="sxs-lookup"><span data-stu-id="5ba98-128">To change the attributes of a shape, you must first give the shape an ID; for example, "myrect".</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```




```HTML
   myrect.style.width = 80
   myrect.style.height = 80
   myrect.fillColor = "green"
```



<span data-ttu-id="5ba98-129">[Exemple d’attribut d’ID](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span><span class="sxs-lookup"><span data-stu-id="5ba98-129">[ID Attribute Example](/previous-versions/office/developer/speech-technologies/ms872141(v=msdn.10)#example).</span></span> <span data-ttu-id="5ba98-130">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="5ba98-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 