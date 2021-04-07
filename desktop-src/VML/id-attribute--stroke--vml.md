---
title: ID, attribut (Stroke) (VML)
description: ID, attribut (Stroke) (VML)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efc9cfda1b7ddb359812d9ad28b37b851315da8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728340"
---
# <a name="id-attribute-strokevml"></a><span data-ttu-id="515cf-103">ID, attribut (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="515cf-103">ID Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="515cf-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="515cf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="515cf-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="515cf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="515cf-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="515cf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="515cf-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="515cf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="515cf-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="515cf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="515cf-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="515cf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="515cf-110">Nom qui fournit un identificateur unique pour un trait.</span><span class="sxs-lookup"><span data-stu-id="515cf-110">A name that provides a unique identifier for a stroke.</span></span> <span data-ttu-id="515cf-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="515cf-111">Read/write.</span></span> <span data-ttu-id="515cf-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="515cf-112">**String**.</span></span>

<span data-ttu-id="515cf-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="515cf-113">**Applies To**</span></span>

[<span data-ttu-id="515cf-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="515cf-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="515cf-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="515cf-115">**Tag Syntax**</span></span>

<span data-ttu-id="515cf-116"><v : *élément* ID = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="515cf-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="515cf-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="515cf-117">**Script Syntax**</span></span>

<span data-ttu-id="515cf-118">*Element* . ID = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="515cf-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="515cf-119">*expression* = *élément*. ID</span><span class="sxs-lookup"><span data-stu-id="515cf-119">*expression*=*element*.id</span></span>

<span data-ttu-id="515cf-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="515cf-120">**Remarks**</span></span>

<span data-ttu-id="515cf-121">Utilisez **ID** pour faire référence à un trait spécifique.</span><span class="sxs-lookup"><span data-stu-id="515cf-121">Use **ID** to refer to a specific stroke.</span></span> <span data-ttu-id="515cf-122">Une fois que vous avez créé un trait et lui avez attribué un ID, vous pouvez utiliser le nom de l’ID lorsque vous souhaitez manipuler le trait.</span><span class="sxs-lookup"><span data-stu-id="515cf-122">Once you have created a stroke and given it an ID, you can use the ID name when you want to manipulate the stroke.</span></span>

<span data-ttu-id="515cf-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="515cf-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="515cf-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="515cf-124">**Example**</span></span>

<span data-ttu-id="515cf-125">La forme a un ID de trait appelé « myStroke ».</span><span class="sxs-lookup"><span data-stu-id="515cf-125">The shape has a stroke ID called "mystroke".</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 