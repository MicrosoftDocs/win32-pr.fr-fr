---
description: Le périphérique du scanneur d’acquisition d’images Windows (WIA) est implémenté sous la forme d’une arborescence hiérarchique d’objets IWiaItem.
ms.assetid: d716faec-9ace-422d-b6eb-ad4d86c1b0fd
title: Appareils de scanneur WIA dans WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443277b0b580a481b523739cd5bc21642d827252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751757"
---
# <a name="wia-scanner-devices-in-wia-10"></a><span data-ttu-id="788e5-103">Appareils de scanneur WIA dans WIA 1,0</span><span class="sxs-lookup"><span data-stu-id="788e5-103">WIA Scanner Devices in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="788e5-104">Cette rubrique décrit l’arborescence des appareils du scanneur pour les applications qui utilisent le service WIA (Windows Image Acquisition) 1,0 (qui est pris en charge sur Windows XP ou version antérieure).</span><span class="sxs-lookup"><span data-stu-id="788e5-104">This topic discusses the scanner device tree for applications that use the Windows Image Acquisition (WIA) 1.0 service (which is supported on Windows XP or earlier).</span></span> <span data-ttu-id="788e5-105">Pour plus d’informations sur l’arborescence d’appareils des éléments WIA (Windows Image Acquisition) 2,0 (qui sont pris en charge sur Windows Vista ou version ultérieure), consultez [à propos de l’arborescence des éléments IWiaItem2](-wia-about-item-tree.md).</span><span class="sxs-lookup"><span data-stu-id="788e5-105">For information on the device tree of Windows Image Acquisition (WIA) 2.0 items (which are supported on Windows Vista or later), see [About the IWiaItem2 Item Tree](-wia-about-item-tree.md).</span></span>

 

<span data-ttu-id="788e5-106">Le périphérique du scanneur d’acquisition d’images Windows (WIA) est implémenté sous la forme d’une arborescence hiérarchique d’objets [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="788e5-106">The Windows Image Acquisition (WIA) scanner device is implemented as a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) objects.</span></span> <span data-ttu-id="788e5-107">À partir de l’élément racine, une application peut :</span><span class="sxs-lookup"><span data-stu-id="788e5-107">From the root item an application may:</span></span>

-   <span data-ttu-id="788e5-108">Fonctionnalités de l’analyseur de requêtes</span><span class="sxs-lookup"><span data-stu-id="788e5-108">Query scanner capabilities</span></span>
-   <span data-ttu-id="788e5-109">Définir les propriétés d’un périphérique de scanneur</span><span class="sxs-lookup"><span data-stu-id="788e5-109">Set scanner device properties</span></span>
-   <span data-ttu-id="788e5-110">Contrôler le chargeur de documents</span><span class="sxs-lookup"><span data-stu-id="788e5-110">Control the document feeder</span></span>

<span data-ttu-id="788e5-111">Un périphérique de scanneur WIA est différent d’un appareil photo WIA, car, en général, il ne stocke pas plusieurs images en mémoire.</span><span class="sxs-lookup"><span data-stu-id="788e5-111">A WIA scanner device is different from a WIA camera device because, in general, it does not store multiple images in memory.</span></span>

<span data-ttu-id="788e5-112">Sous l’élément racine, un objet scanneur type possède un objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) unique qui représente la fonctionnalité de collecte des données de l’appareil, l’élément d’analyse.</span><span class="sxs-lookup"><span data-stu-id="788e5-112">Underneath the root item, a typical scanner object has a single [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object that represents the data collecting functionality of the device, the Scan Item.</span></span> <span data-ttu-id="788e5-113">L’indicateur [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) est défini pour cet élément pour indiquer que les transferts de données sur cet élément sont possibles.</span><span class="sxs-lookup"><span data-stu-id="788e5-113">This item has the [**WiaItemTypeFile**](-wia-wia-item-type-flags.md) flag set to indicate that data transfers on this item are possible.</span></span> <span data-ttu-id="788e5-114">Une application configure une analyse en définissant les propriétés de l’élément d’analyse, puis effectue l’analyse et transfère les données à l’aide d’une interface de transfert de données.</span><span class="sxs-lookup"><span data-stu-id="788e5-114">An application sets up a scan by setting the properties of the scan item, then performs the scan and transfers the data using a data transfer interface.</span></span>

<span data-ttu-id="788e5-115">Le diagramme suivant illustre l’implémentation WIA pour un scanneur classique :</span><span class="sxs-lookup"><span data-stu-id="788e5-115">The following diagram illustrates the WIA implementation for a typical scanner:</span></span>

![implémentation WIA d’un scanneur classique](images/wiscantr.gif)

<span data-ttu-id="788e5-117">Un scanneur duplex standard est représenté dans WIA en présence d’un objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="788e5-117">A typical duplex scanner is represented in WIA by having one [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span> <span data-ttu-id="788e5-118">Les données de page frontale et de page principale sont accessibles séquentiellement un transfert de données par page.</span><span class="sxs-lookup"><span data-stu-id="788e5-118">Front- and back-page data is accessed sequentially one data transfer per page.</span></span> <span data-ttu-id="788e5-119">Par conséquent, la représentation d’un scanneur duplex est identique à la représentation d’un scanneur classique.</span><span class="sxs-lookup"><span data-stu-id="788e5-119">Therefore, the representation of a duplex scanner is identical to the representation of a typical scanner.</span></span>

<span data-ttu-id="788e5-120">Un scanneur de diapositives permettant d’analyser plusieurs diapositives en une seule opération représente chaque image distincte sous la forme d’un objet [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) distinct.</span><span class="sxs-lookup"><span data-stu-id="788e5-120">A slide scanner capable of scanning multiple slides in a single scan operation represents each separate image as a separate [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object.</span></span>

<span data-ttu-id="788e5-121">Le diagramme suivant illustre la représentation WIA d’un scanneur de diapositive :</span><span class="sxs-lookup"><span data-stu-id="788e5-121">The following diagram illustrates the WIA representation of a slide scanner:</span></span>

![Scanner de diapositive](images/wislscan.gif)

 

 



