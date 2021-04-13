---
description: WIA représente un appareil photo sous la forme d’une arborescence hiérarchique d’objets IWiaItem.
ms.assetid: fbb2821c-7f13-4fdd-a2ea-582be303855a
title: Appareils photo WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 002a14d8e047019b1af2d2f86c1fd4a2e00d7808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201481"
---
# <a name="wia-camera-devices"></a><span data-ttu-id="b4c46-103">Appareils photo WIA</span><span class="sxs-lookup"><span data-stu-id="b4c46-103">WIA Camera Devices</span></span>

<span data-ttu-id="b4c46-104">WIA représente un appareil photo sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="b4c46-104">WIA represents a camera device as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="b4c46-105">L’élément racine, retourné par un appel à la méthode [**IWiaDevMgr :: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) de l’acquisition d’images Windows (WIA), est utilisé pour obtenir et définir les informations de l’appareil, pour contrôler l’appareil et pour commencer l’énumération des éléments de périphérique.</span><span class="sxs-lookup"><span data-stu-id="b4c46-105">The root item, returned from a call to the Windows Image Acquisition (WIA) device manager [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) method, is used to get and set device information, to control the device, and to begin device item enumeration.</span></span>

> [!Note]  
> <span data-ttu-id="b4c46-106">WIA ne prend pas en charge les caméras dans Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b4c46-106">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="b4c46-107">Pour ces versions de Windows, utilisez l’API Windows Mobile Device (WPD) décrite dans le kit de développement de pilotes (DDK) Windows pour obtenir des images à partir d’appareils photo.</span><span class="sxs-lookup"><span data-stu-id="b4c46-107">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 

<span data-ttu-id="b4c46-108">Le diagramme suivant illustre un exemple d’implémentation d’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="b4c46-108">The following diagram illustrates a sample camera implementation.</span></span> <span data-ttu-id="b4c46-109">L’élément racine de l’appareil photo comporte trois éléments enfants, deux images et un dossier.</span><span class="sxs-lookup"><span data-stu-id="b4c46-109">The camera root item has three child items, two pictures and one folder.</span></span> <span data-ttu-id="b4c46-110">Le dossier contient deux éléments enfants, les deux images.</span><span class="sxs-lookup"><span data-stu-id="b4c46-110">The folder has two child items, both pictures.</span></span>

![exemple d’implémentation d’appareil photo](images/wihierar.gif)

 

 



