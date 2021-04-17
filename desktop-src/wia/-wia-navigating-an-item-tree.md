---
description: Une application parcourt l’arborescence d’éléments d’un appareil WIA (Windows Image Acquisition) pour rechercher et sélectionner des images sur cet appareil. À l’aide de cette technique, une application sélectionne et acquiert une image sans présenter une boîte de dialogue à l’utilisateur.
ms.assetid: 1f124b4a-45fb-4181-b45a-e810a61ac37d
title: Navigation dans une arborescence d’éléments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787ff3b53690ae7db4ff69fd5de2f4f4186f8e43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526433"
---
# <a name="navigating-an-item-tree"></a><span data-ttu-id="09ed8-104">Navigation dans une arborescence d’éléments</span><span class="sxs-lookup"><span data-stu-id="09ed8-104">Navigating an Item Tree</span></span>

<span data-ttu-id="09ed8-105">Une application parcourt l’arborescence d’éléments d’un appareil WIA (Windows Image Acquisition) pour rechercher et sélectionner des images sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="09ed8-105">An application navigates a Windows Image Acquisition (WIA) device's item tree to find and select images on that device.</span></span> <span data-ttu-id="09ed8-106">À l’aide de cette technique, une application sélectionne et acquiert une image sans présenter une boîte de dialogue à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="09ed8-106">Using this technique, an application selects and acquires an image without presenting a dialog box to the user.</span></span>

<span data-ttu-id="09ed8-107">Un appareil WIA est représenté en tant qu’élément racine dans une arborescence d’objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="09ed8-107">A WIA device is represented as the root item in a tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects.</span></span> <span data-ttu-id="09ed8-108">Les éléments enfants de l’arborescence représentent les images d’un scanneur ou d’un appareil photo.</span><span class="sxs-lookup"><span data-stu-id="09ed8-108">The child items in the tree represent images for a camera or scan beds for a scanner.</span></span>

<span data-ttu-id="09ed8-109">Une fois qu’un appareil WIA est sélectionné, une application appelle la méthode [**IWiaItem :: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) de l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) de l’appareil pour énumérer les éléments enfants (les images ou les lits d’analyse) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="09ed8-109">After a WIA device is selected, an application calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method of the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface of the device to enumerate the child items (the images or scan beds) of the device.</span></span> <span data-ttu-id="09ed8-110">Pour obtenir des instructions, consultez [sélection d’un appareil](-wia-selecting-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="09ed8-110">For instructions, see [Selecting a Device](-wia-selecting-a-device.md).</span></span>

<span data-ttu-id="09ed8-111">La méthode [**IWiaItem :: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) crée un objet d’énumération pour les éléments enfants de l’appareil et retourne un pointeur vers l’interface [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) de cet objet.</span><span class="sxs-lookup"><span data-stu-id="09ed8-111">The [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) method creates an enumeration object for the child items of the device, and returns a pointer to that object's [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) interface.</span></span> <span data-ttu-id="09ed8-112">L’application peut ensuite utiliser les méthodes de l’interface **IEnumWiaItem** pour obtenir des pointeurs vers les éléments de l’arborescence d’éléments de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="09ed8-112">The application can then use the methods of the **IEnumWiaItem** interface to obtain pointers to the items in the device's item tree.</span></span>

 

 



