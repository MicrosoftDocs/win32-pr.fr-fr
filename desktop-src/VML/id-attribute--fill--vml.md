---
title: ID, attribut (Fill) (VML)
description: ID, attribut (Fill) (VML)
ms.assetid: 56865772-51bd-4729-8e56-6b00e3c6bed0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4820c4f7a23cf940c199f27243d8ad5601390a84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031514"
---
# <a name="id-attribute-fillvml"></a><span data-ttu-id="43678-103">ID, attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="43678-103">ID Attribute (Fill)(VML)</span></span>

<span data-ttu-id="43678-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="43678-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="43678-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="43678-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="43678-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="43678-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="43678-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="43678-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="43678-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="43678-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="43678-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="43678-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="43678-110">Nom qui fournit un identificateur unique pour un remplissage.</span><span class="sxs-lookup"><span data-stu-id="43678-110">A name that provides a unique identifier for a fill.</span></span> <span data-ttu-id="43678-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="43678-111">Read/write.</span></span> <span data-ttu-id="43678-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="43678-112">**String**.</span></span>

<span data-ttu-id="43678-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="43678-113">**Applies To**</span></span>

[<span data-ttu-id="43678-114">Complète</span><span class="sxs-lookup"><span data-stu-id="43678-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="43678-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="43678-115">**Tag Syntax**</span></span>

<span data-ttu-id="43678-116"><v : *élément* ID = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="43678-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="43678-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="43678-117">**Script Syntax**</span></span>

<span data-ttu-id="43678-118">*Element* . ID = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="43678-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="43678-119">*expression* = *élément*. ID</span><span class="sxs-lookup"><span data-stu-id="43678-119">*expression*=*element*.id</span></span>

<span data-ttu-id="43678-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="43678-120">**Remarks**</span></span>

<span data-ttu-id="43678-121">Utilisez **ID** pour faire référence à un remplissage spécifique.</span><span class="sxs-lookup"><span data-stu-id="43678-121">Use **ID** to refer to a specific fill.</span></span> <span data-ttu-id="43678-122">Une fois que vous avez créé un remplissage et lui avez attribué un ID, vous pouvez utiliser le nom de l’ID lorsque vous souhaitez manipuler le remplissage.</span><span class="sxs-lookup"><span data-stu-id="43678-122">Once you have created a fill and given it an ID, you can use the ID name when you want to manipulate the fill.</span></span>

<span data-ttu-id="43678-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="43678-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="43678-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="43678-124">**Example**</span></span>

<span data-ttu-id="43678-125">La forme a un ID de remplissage appelé « myfill ».</span><span class="sxs-lookup"><span data-stu-id="43678-125">The shape has a fill ID called "myfill".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill id="myfill"/>
   </v:shape>
```



 

 