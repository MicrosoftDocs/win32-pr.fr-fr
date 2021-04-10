---
title: ID, attribut (TextBox) (VML)
description: ID, attribut (TextBox) (VML)
ms.assetid: b9eb75cc-4d0a-4e83-a897-e35995ae7c53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b39ac566e7b619c31cb12f4657bd86020dc12cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842449"
---
# <a name="id-attribute-textboxvml"></a><span data-ttu-id="af978-103">ID, attribut (TextBox) (VML)</span><span class="sxs-lookup"><span data-stu-id="af978-103">ID Attribute (TextBox)(VML)</span></span>

<span data-ttu-id="af978-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="af978-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="af978-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="af978-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="af978-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="af978-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="af978-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="af978-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="af978-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="af978-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="af978-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="af978-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="af978-110">Nom qui fournit un identificateur unique pour une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="af978-110">A name that provides a unique identifier for a textbox.</span></span> <span data-ttu-id="af978-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="af978-111">Read/write.</span></span> <span data-ttu-id="af978-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="af978-112">**String**.</span></span>

<span data-ttu-id="af978-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="af978-113">**Applies To**</span></span>

[<span data-ttu-id="af978-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="af978-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="af978-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="af978-115">**Tag Syntax**</span></span>

<span data-ttu-id="af978-116"><v : *élément* ID = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="af978-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="af978-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="af978-117">**Script Syntax**</span></span>

<span data-ttu-id="af978-118">*Element* . ID = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="af978-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="af978-119">*expression* = *élément*. ID</span><span class="sxs-lookup"><span data-stu-id="af978-119">*expression*=*element*.id</span></span>

<span data-ttu-id="af978-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="af978-120">**Remarks**</span></span>

<span data-ttu-id="af978-121">Utilisez **ID** pour faire référence à une zone de texte spécifique.</span><span class="sxs-lookup"><span data-stu-id="af978-121">Use **ID** to refer to a specific textbox.</span></span> <span data-ttu-id="af978-122">Une fois que vous avez créé une zone de texte et lui avez attribué un ID, vous pouvez utiliser le nom de l’ID lorsque vous souhaitez manipuler la zone de texte.</span><span class="sxs-lookup"><span data-stu-id="af978-122">Once you have created a textbox and given it an ID, you can use the ID name when you want to manipulate the textbox.</span></span>

<span data-ttu-id="af978-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="af978-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="af978-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="af978-124">**Example**</span></span>

<span data-ttu-id="af978-125">La forme a un ID de zone de texte appelé « myTextBox ».</span><span class="sxs-lookup"><span data-stu-id="af978-125">The shape has a textbox ID called "mytextbox".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 