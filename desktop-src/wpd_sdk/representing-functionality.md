---
description: Représentation des fonctionnalités
ms.assetid: 34a4a015-614d-4fac-98d8-29ae43165798
title: Représentation des fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101614592224a1a5ac079b1f9c3dc89cea9afefe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866505"
---
# <a name="representing-functionality"></a><span data-ttu-id="be57b-103">Représentation des fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="be57b-103">Representing Functionality</span></span>

<span data-ttu-id="be57b-104">Il existe des objets fonctionnels permettant d’identifier ou de regrouper logiquement les fonctionnalités d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="be57b-104">Functional objects exist to identify or logically group feature capabilities of a device.</span></span> <span data-ttu-id="be57b-105">Par exemple, une application peut voir qu’un appareil prend en charge SMS en recherchant l’objet fonctionnel SMS.</span><span class="sxs-lookup"><span data-stu-id="be57b-105">For example, an application can see that a device supports SMS by looking for the SMS functional object.</span></span> <span data-ttu-id="be57b-106">De même, l’application peut voir qu’un appareil possède des fonctionnalités d’appareil photo en recherchant l’objet fonctionnel de capture d’image continue.</span><span class="sxs-lookup"><span data-stu-id="be57b-106">Similarly, the application can see that a device has camera capabilities by looking for the Still Image Capture functional object.</span></span>

<span data-ttu-id="be57b-107">Cette représentation d’objet flexible facilite la prise en charge des appareils avec des fonctionnalités multifonction.</span><span class="sxs-lookup"><span data-stu-id="be57b-107">This flexible object representation helps enable easy support for devices with multi-function capabilities.</span></span> <span data-ttu-id="be57b-108">Les pilotes peuvent simplement exposer les objets fonctionnels qui représentent leur appareil, ce qui est plus granulaire que l’utilisation des classes de périphériques traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="be57b-108">Drivers can simply expose whatever functional objects represent their device, which is more granular than using traditional device classes.</span></span> <span data-ttu-id="be57b-109">La représentation d’objet permet également d’isoler les éléments fonctionnels qui se chevauchent. par exemple, certains téléphones peuvent avoir deux caméras ou quatre stockages.</span><span class="sxs-lookup"><span data-stu-id="be57b-109">The object representation also helps isolate overlapping functional pieces; for example, some phones may have two cameras or four storages.</span></span>

<span data-ttu-id="be57b-110">Dans le système d’exploitation Windows 7, les services étendent les objets fonctionnels en fournissant des requêtes riches de fonctionnalités et un regroupement abstrait de contenu.</span><span class="sxs-lookup"><span data-stu-id="be57b-110">In the Windows 7 operating system, services extend functional objects by providing rich queries of capabilities and an abstract grouping of content.</span></span> <span data-ttu-id="be57b-111">Les applications peuvent utiliser des services pour découvrir des fonctionnalités d’appareil et interagir avec le contenu de manière plus efficace.</span><span class="sxs-lookup"><span data-stu-id="be57b-111">Applications can use services to discover device capabilities and to interact with content more efficiently.</span></span> <span data-ttu-id="be57b-112">Par exemple, une application peut voir qu’un appareil prend en charge les fonctionnalités de synchronisation des contacts en recherchant un objet de service de contacts et peut trouver tous les contacts en tant qu’objets enfants de l’objet de service, sans avoir à effectuer une recherche récursive dans la hiérarchie de stockage.</span><span class="sxs-lookup"><span data-stu-id="be57b-112">For example, an application can see that a device supports the contacts-synchronization capabilities by looking for a Contacts service object, and can find all contacts as child objects of the service object, without having to recursively search the storage hierarchy.</span></span>

<span data-ttu-id="be57b-113">Les services permettent également aux applications de découvrir et d’appeler un comportement personnalisé sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="be57b-113">Services also allow applications to discover and invoke custom behavior on a device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be57b-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be57b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be57b-115">**Vue d’ensemble de l’application**</span><span class="sxs-lookup"><span data-stu-id="be57b-115">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



