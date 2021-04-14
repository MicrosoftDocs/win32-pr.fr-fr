---
title: ID, attribut (image) (VML)
description: ID, attribut (image) (VML)
ms.assetid: d85a6d56-5896-4ac0-85c7-0edc72928c62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40ac489331699ca6fe040cddc0bebb408d524de7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382779"
---
# <a name="id-attribute-imagevml"></a><span data-ttu-id="9ef12-103">ID, attribut (image) (VML)</span><span class="sxs-lookup"><span data-stu-id="9ef12-103">ID Attribute (Image)(VML)</span></span>

<span data-ttu-id="9ef12-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9ef12-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9ef12-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9ef12-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9ef12-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="9ef12-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9ef12-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="9ef12-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9ef12-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9ef12-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9ef12-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9ef12-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9ef12-110">Définit un nom qui fournit un identificateur unique pour une image.</span><span class="sxs-lookup"><span data-stu-id="9ef12-110">Defines a name that provides a unique identifier for an image.</span></span> <span data-ttu-id="9ef12-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9ef12-111">Read/write.</span></span> <span data-ttu-id="9ef12-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="9ef12-112">**String**.</span></span>

<span data-ttu-id="9ef12-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="9ef12-113">**Applies To**</span></span>

[<span data-ttu-id="9ef12-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="9ef12-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="9ef12-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="9ef12-115">**Tag Syntax**</span></span>

<span data-ttu-id="9ef12-116"><v : *élément* ID = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="9ef12-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="9ef12-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="9ef12-117">**Script Syntax**</span></span>

<span data-ttu-id="9ef12-118">*Element* . ID = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="9ef12-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="9ef12-119">*expression* = *élément*. ID</span><span class="sxs-lookup"><span data-stu-id="9ef12-119">*expression*=*element*.id</span></span>

<span data-ttu-id="9ef12-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="9ef12-120">**Remarks**</span></span>

<span data-ttu-id="9ef12-121">Utilisez **ID** pour faire référence à une image spécifique.</span><span class="sxs-lookup"><span data-stu-id="9ef12-121">Use **ID** to refer to a specific image.</span></span> <span data-ttu-id="9ef12-122">Une fois que vous avez créé une image et lui avez attribué un ID, vous pouvez utiliser le nom de l’ID lorsque vous souhaitez manipuler l’image.</span><span class="sxs-lookup"><span data-stu-id="9ef12-122">Once you have created an image and given it an ID, you can use the ID name when you want to manipulate the image.</span></span>

<span data-ttu-id="9ef12-123">**Attribut standard VML**</span><span class="sxs-lookup"><span data-stu-id="9ef12-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="9ef12-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="9ef12-124">**Example**</span></span>

<span data-ttu-id="9ef12-125">La forme a un ID **ImageData** appelé « myImage ».</span><span class="sxs-lookup"><span data-stu-id="9ef12-125">The shape has an **ImageData** ID called "myimage".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata id="myimage" src="kids.jpg"/>
   </v:shape>
```



 

 