---
title: ID, attribut (Shadow) (VML)
description: ID, attribut (Shadow) (VML)
ms.assetid: ca20b6b9-a41c-4073-9178-77eb0f918327
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d51a5917f9ef71e3c4acea7ec1ed2e5cf90aef8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728341"
---
# <a name="id-attribute-shadowvml"></a><span data-ttu-id="cfafe-103">ID, attribut (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="cfafe-103">ID Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="cfafe-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cfafe-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cfafe-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cfafe-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cfafe-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="cfafe-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cfafe-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="cfafe-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cfafe-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cfafe-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cfafe-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cfafe-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cfafe-110">Spécifie un nom qui fournit un identificateur unique pour une ombre.</span><span class="sxs-lookup"><span data-stu-id="cfafe-110">Specifies a name that provides a unique identifier for a shadow.</span></span> <span data-ttu-id="cfafe-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="cfafe-111">Read/write.</span></span> <span data-ttu-id="cfafe-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="cfafe-112">**String**.</span></span>

<span data-ttu-id="cfafe-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="cfafe-113">**Applies To**</span></span>

[<span data-ttu-id="cfafe-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="cfafe-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="cfafe-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="cfafe-115">**Tag Syntax**</span></span>

<span data-ttu-id="cfafe-116"><v : *élément* ID = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="cfafe-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="cfafe-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="cfafe-117">**Script Syntax**</span></span>

<span data-ttu-id="cfafe-118">*Element* . ID = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="cfafe-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="cfafe-119">*expression* = *élément*. ID</span><span class="sxs-lookup"><span data-stu-id="cfafe-119">*expression*=*element*.id</span></span>

<span data-ttu-id="cfafe-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="cfafe-120">**Remarks**</span></span>

<span data-ttu-id="cfafe-121">Utilisez **ID** pour faire référence à une ombre spécifique.</span><span class="sxs-lookup"><span data-stu-id="cfafe-121">Use **ID** to refer to a specific shadow.</span></span> <span data-ttu-id="cfafe-122">Une fois que vous avez créé une ombre et donné un ID, vous pouvez utiliser le nom de l’ID lorsque vous souhaitez manipuler l’ombre.</span><span class="sxs-lookup"><span data-stu-id="cfafe-122">Once you have created a shadow and given it an ID, you can use the ID name when you want to manipulate the shadow.</span></span>

<span data-ttu-id="cfafe-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="cfafe-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="cfafe-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="cfafe-124">**Example**</span></span>

<span data-ttu-id="cfafe-125">La forme a un ID d’ombre appelé « myshadow ».</span><span class="sxs-lookup"><span data-stu-id="cfafe-125">The shape has a shadow ID called "myshadow".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow id="myshadow" on="True"/>
   </v:shape>
```



 

 