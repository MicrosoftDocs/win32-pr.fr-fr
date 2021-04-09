---
title: ID, attribut (Path) (VML)
description: ID, attribut (Path) (VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101665"
---
# <a name="id-attribute-pathvml"></a><span data-ttu-id="c5a38-103">ID, attribut (Path) (VML)</span><span class="sxs-lookup"><span data-stu-id="c5a38-103">ID Attribute (Path)(VML)</span></span>

<span data-ttu-id="c5a38-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c5a38-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c5a38-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c5a38-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c5a38-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c5a38-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c5a38-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c5a38-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c5a38-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c5a38-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c5a38-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c5a38-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c5a38-110">Nom qui fournit un identificateur unique pour un chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="c5a38-110">A name that provides a unique identifier for a path.</span></span> <span data-ttu-id="c5a38-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c5a38-111">Read/write.</span></span> <span data-ttu-id="c5a38-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="c5a38-112">**String**.</span></span>

<span data-ttu-id="c5a38-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c5a38-113">**Applies To**</span></span>

[<span data-ttu-id="c5a38-114">Chemin d’accès</span><span class="sxs-lookup"><span data-stu-id="c5a38-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="c5a38-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c5a38-115">**Tag Syntax**</span></span>

<span data-ttu-id="c5a38-116"><v : *élément* ID = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="c5a38-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="c5a38-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="c5a38-117">**Script Syntax**</span></span>

<span data-ttu-id="c5a38-118">*Element* . ID = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c5a38-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="c5a38-119">*expression* = *élément*. ID</span><span class="sxs-lookup"><span data-stu-id="c5a38-119">*expression*=*element*.id</span></span>

<span data-ttu-id="c5a38-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c5a38-120">**Remarks**</span></span>

<span data-ttu-id="c5a38-121">Utilisez **ID** pour faire référence à un chemin d’accès spécifique.</span><span class="sxs-lookup"><span data-stu-id="c5a38-121">Use **ID** to refer to a specific path.</span></span> <span data-ttu-id="c5a38-122">Une fois que vous avez créé un chemin d’accès et donné un ID, vous pouvez utiliser le nom de l’ID lorsque vous souhaitez manipuler le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="c5a38-122">Once you have created a path and given it an ID, you can use the ID name when you want to manipulate the path.</span></span>

<span data-ttu-id="c5a38-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="c5a38-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c5a38-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="c5a38-124">**Example**</span></span>

<span data-ttu-id="c5a38-125">La forme a un ID de chemin d’accès appelé « myPath ».</span><span class="sxs-lookup"><span data-stu-id="c5a38-125">The shape has a path ID called "myPath".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 