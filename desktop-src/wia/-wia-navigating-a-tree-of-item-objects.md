---
description: 'En savoir plus sur : navigation dans une arborescence d’objets d’élément'
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Navigation dans une arborescence d’objets Item
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515038"
---
# <a name="navigating-a-tree-of-item-objects"></a><span data-ttu-id="68b04-103">Navigation dans une arborescence d’objets Item</span><span class="sxs-lookup"><span data-stu-id="68b04-103">Navigating a Tree of Item Objects</span></span>

> [!Note]  
> <span data-ttu-id="68b04-104">Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="68b04-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="68b04-105">Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="68b04-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="68b04-106">Une application ou un script parcourt l’arborescence d’éléments d’un appareil WIA (Windows Image Acquisition) pour rechercher et sélectionner des images sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="68b04-106">An application or script navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="68b04-107">À l’aide de cette technique, une application sélectionne et acquiert une image sans utiliser de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="68b04-107">Using this technique, an application selects and acquires an image without the use of a dialog box.</span></span>

<span data-ttu-id="68b04-108">Un appareil WIA est représenté en tant qu’élément racine dans une arborescence d’objets d' [**élément**](-wia-item.md) .</span><span class="sxs-lookup"><span data-stu-id="68b04-108">A WIA device is represented as the root item in a tree of [**Item**](-wia-item.md) objects.</span></span> <span data-ttu-id="68b04-109">Les éléments enfants de l’arborescence représentent des dossiers et des images pour un appareil photo ou des lits d’analyse pour un scanneur.</span><span class="sxs-lookup"><span data-stu-id="68b04-109">The child items in the tree represent folders and images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="68b04-110">Après vous être connecté à un appareil, appelez la propriété [**Children**](-wia-iwiadispatchitem-children.md) de l’objet [**Item**](-wia-item.md) qui représente l’appareil (l’élément racine de l’arborescence) pour obtenir une collection des éléments enfants (images ou lits d’analyse) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="68b04-110">After connecting to a device, call the [**Children**](-wia-iwiadispatchitem-children.md) property of the [**Item**](-wia-item.md) object that represents the device (the root item of the tree) to obtain a collection of the child items (the images or scan beds) of the device.</span></span>

<span data-ttu-id="68b04-111">Énumère cette collection (de manière récursive, si nécessaire) pour naviguer dans l’arborescence de l’élément.</span><span class="sxs-lookup"><span data-stu-id="68b04-111">Enumerate this collection (recursively, if necessary) to navigate item tree.</span></span>

 

 
