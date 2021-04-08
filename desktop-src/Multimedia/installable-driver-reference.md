---
title: Informations de référence sur les pilotes installables
description: Informations de référence sur les pilotes installables
ms.assetid: 869b92f1-2711-4198-9911-3df1ebc58d5f
keywords:
- Windows Multimedia, informations de référence sur les pilotes installables
- Multimedia, informations de référence sur les pilotes
- pilotes installables, référence
- informations de référence sur les pilotes installables, à propos de
- référence pour les pilotes installables, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90475063f9d9211e841902fe73d2f09dc6130d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842145"
---
# <a name="installable-driver-reference"></a><span data-ttu-id="c5d5f-108">Informations de référence sur les pilotes installables</span><span class="sxs-lookup"><span data-stu-id="c5d5f-108">Installable Driver Reference</span></span>

<span data-ttu-id="c5d5f-109">Les fonctions et les messages associés aux pilotes installables sont regroupés comme suit.</span><span class="sxs-lookup"><span data-stu-id="c5d5f-109">The functions and messages associated with installable drivers are grouped as follows.</span></span>

## <a name="loading-and-unloading-drivers"></a><span data-ttu-id="c5d5f-110">Chargement et déchargement des pilotes</span><span class="sxs-lookup"><span data-stu-id="c5d5f-110">Loading and Unloading Drivers</span></span>

-   [<span data-ttu-id="c5d5f-111">GetDriverModuleHandle</span><span class="sxs-lookup"><span data-stu-id="c5d5f-111">GetDriverModuleHandle</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-getdrivermodulehandle)
-   [<span data-ttu-id="c5d5f-112">OpenDriver</span><span class="sxs-lookup"><span data-stu-id="c5d5f-112">OpenDriver</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver)
-   [<span data-ttu-id="c5d5f-113">SendDriverMessage</span><span class="sxs-lookup"><span data-stu-id="c5d5f-113">SendDriverMessage</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage)

## <a name="closedriver"></a><span data-ttu-id="c5d5f-114">CloseDriver</span><span class="sxs-lookup"><span data-stu-id="c5d5f-114">CloseDriver</span></span>

-   [<span data-ttu-id="c5d5f-115">**DRV \_ Fermer**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-115">**DRV\_CLOSE**</span></span>](drv-close.md)
-   [<span data-ttu-id="c5d5f-116">**DRV- \_ Désactiver**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-116">**DRV\_DISABLE**</span></span>](drv-disable.md)
-   [<span data-ttu-id="c5d5f-117">**DRV \_ Enable**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-117">**DRV\_ENABLE**</span></span>](drv-enable.md)
-   [<span data-ttu-id="c5d5f-118">**DRV \_ gratuit**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-118">**DRV\_FREE**</span></span>](drv-free.md)
-   [<span data-ttu-id="c5d5f-119">**chargement du DRV \_**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-119">**DRV\_LOAD**</span></span>](drv-load.md)
-   [<span data-ttu-id="c5d5f-120">**DRV \_ ouvert**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-120">**DRV\_OPEN**</span></span>](drv-open.md)

## <a name="configuring-a-driver"></a><span data-ttu-id="c5d5f-121">Configuration d’un pilote</span><span class="sxs-lookup"><span data-stu-id="c5d5f-121">Configuring a Driver</span></span>

-   [<span data-ttu-id="c5d5f-122">**DRV \_ configurer**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-122">**DRV\_CONFIGURE**</span></span>](drv-configure.md)
-   [<span data-ttu-id="c5d5f-123">**DRV \_ QUERYCONFIGURE**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-123">**DRV\_QUERYCONFIGURE**</span></span>](drv-queryconfigure.md)
-   [<span data-ttu-id="c5d5f-124">**DRVCONFIGINFO**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-124">**DRVCONFIGINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo)

## <a name="installing-a-driver"></a><span data-ttu-id="c5d5f-125">Installation d’un pilote</span><span class="sxs-lookup"><span data-stu-id="c5d5f-125">Installing a Driver</span></span>

-   [<span data-ttu-id="c5d5f-126">**installation de DRV \_**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-126">**DRV\_INSTALL**</span></span>](drv-install.md)
-   [<span data-ttu-id="c5d5f-127">**DRV \_ Supprimer**</span><span class="sxs-lookup"><span data-stu-id="c5d5f-127">**DRV\_REMOVE**</span></span>](drv-remove.md)

## <a name="driver-functions"></a><span data-ttu-id="c5d5f-128">Fonctions du pilote</span><span class="sxs-lookup"><span data-stu-id="c5d5f-128">Driver Functions</span></span>

-   [<span data-ttu-id="c5d5f-129">DefDriverProc</span><span class="sxs-lookup"><span data-stu-id="c5d5f-129">DefDriverProc</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)
-   [<span data-ttu-id="c5d5f-130">DriverCallback</span><span class="sxs-lookup"><span data-stu-id="c5d5f-130">DriverCallback</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback)
-   [<span data-ttu-id="c5d5f-131">DriverProc</span><span class="sxs-lookup"><span data-stu-id="c5d5f-131">DriverProc</span></span>](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc)

## <a name="related-topics"></a><span data-ttu-id="c5d5f-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5d5f-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5d5f-133">Pilotes installables</span><span class="sxs-lookup"><span data-stu-id="c5d5f-133">Installable Drivers</span></span>](installable-drivers.md)
</dt> </dl>

 

 