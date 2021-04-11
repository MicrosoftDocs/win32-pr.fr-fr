---
description: Inscription et chargement du fournisseur de clichés instantanés
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Inscription et chargement du fournisseur de clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725613ff37450075c964b3c66fce3ffba1a70529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318977"
---
# <a name="shadow-copy-provider-registration-and-loading"></a><span data-ttu-id="486ba-103">Inscription et chargement du fournisseur de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="486ba-103">Shadow Copy Provider Registration and Loading</span></span>

## <a name="provider-registration"></a><span data-ttu-id="486ba-104">Inscription du fournisseur</span><span class="sxs-lookup"><span data-stu-id="486ba-104">Provider Registration</span></span>

<span data-ttu-id="486ba-105">Seuls les fournisseurs d’appels VSS.</span><span class="sxs-lookup"><span data-stu-id="486ba-105">Only VSS calls providers.</span></span> <span data-ttu-id="486ba-106">Le fournisseur s’inscrit aux appels en appelant [**IVssAdmin :: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), en passant **le \_ \_ matériel de preuve VSS** pour le paramètre *eProviderType* .</span><span class="sxs-lookup"><span data-stu-id="486ba-106">The provider registers for calls by invoking [**IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passing **VSS\_PROV\_HARDWARE** for the *eProviderType* parameter.</span></span> <span data-ttu-id="486ba-107">Une fois inscrit, le fournisseur est impliqué dans la gestion des clichés instantanés jusqu’à annulation de l’inscription à l’aide de [**IVssAdmin :: UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span><span class="sxs-lookup"><span data-stu-id="486ba-107">Once registered, the provider will be involved in shadow copy management until unregistering using [**IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span></span>

## <a name="provider-loading-and-unloading"></a><span data-ttu-id="486ba-108">Chargement et déchargement du fournisseur</span><span class="sxs-lookup"><span data-stu-id="486ba-108">Provider Loading and Unloading</span></span>

<span data-ttu-id="486ba-109">Les fournisseurs peuvent être souvent chargés et déchargés.</span><span class="sxs-lookup"><span data-stu-id="486ba-109">Providers can be frequently loaded and unloaded.</span></span> <span data-ttu-id="486ba-110">Les fournisseurs peuvent implémenter [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) pour déterminer le moment où VSS charge ou décharge le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="486ba-110">Providers can implement [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) to determine when VSS is loading or unloading the provider.</span></span>

 

 



