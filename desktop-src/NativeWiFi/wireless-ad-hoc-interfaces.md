---
description: L’interface de programmation ad hoc sans fil est composée des interfaces suivantes.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Interfaces ad hoc sans fil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517599"
---
# <a name="wireless-ad-hoc-interfaces"></a><span data-ttu-id="380fa-103">Interfaces ad hoc sans fil</span><span class="sxs-lookup"><span data-stu-id="380fa-103">Wireless Ad Hoc Interfaces</span></span>

<span data-ttu-id="380fa-104">L’interface de programmation ad hoc sans fil est composée des interfaces suivantes.</span><span class="sxs-lookup"><span data-stu-id="380fa-104">The wireless ad hoc programming interface is composed of the following interfaces.</span></span>



| <span data-ttu-id="380fa-105">Nom de l'interface</span><span class="sxs-lookup"><span data-stu-id="380fa-105">Interface Name</span></span>                                                                       | <span data-ttu-id="380fa-106">Description</span><span class="sxs-lookup"><span data-stu-id="380fa-106">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="380fa-107">**IDot11AdHocInterface**</span><span class="sxs-lookup"><span data-stu-id="380fa-107">**IDot11AdHocInterface**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | <span data-ttu-id="380fa-108">Représente une carte d’interface réseau (NIC) sans fil.</span><span class="sxs-lookup"><span data-stu-id="380fa-108">Represents a wireless network interface card (NIC).</span></span>                                                    |
| [<span data-ttu-id="380fa-109">**IDot11AdHocInterfaceNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="380fa-109">**IDot11AdHocInterfaceNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | <span data-ttu-id="380fa-110">Définit les notifications prises en charge par [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span><span class="sxs-lookup"><span data-stu-id="380fa-110">Defines the notifications supported by [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).</span></span>           |
| [<span data-ttu-id="380fa-111">**IDot11AdHocManager**</span><span class="sxs-lookup"><span data-stu-id="380fa-111">**IDot11AdHocManager**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | <span data-ttu-id="380fa-112">Crée et gère des réseaux ad hoc 802,11.</span><span class="sxs-lookup"><span data-stu-id="380fa-112">Creates and manages 802.11 ad hoc networks.</span></span>                                                            |
| [<span data-ttu-id="380fa-113">**IDot11AdHocManagerNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="380fa-113">**IDot11AdHocManagerNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | <span data-ttu-id="380fa-114">Définit les notifications prises en charge par l’interface [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) .</span><span class="sxs-lookup"><span data-stu-id="380fa-114">Defines the notifications supported by the [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) interface.</span></span> |
| [<span data-ttu-id="380fa-115">**IDot11AdHocNetwork**</span><span class="sxs-lookup"><span data-stu-id="380fa-115">**IDot11AdHocNetwork**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | <span data-ttu-id="380fa-116">Représente une destination de réseau ad hoc disponible dans la plage de connexions.</span><span class="sxs-lookup"><span data-stu-id="380fa-116">Represents an available ad hoc network destination within connection range.</span></span>                            |
| [<span data-ttu-id="380fa-117">**IDot11AdHocNetworkNotificationSink**</span><span class="sxs-lookup"><span data-stu-id="380fa-117">**IDot11AdHocNetworkNotificationSink**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | <span data-ttu-id="380fa-118">Définit les notifications prises en charge par l’interface [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) .</span><span class="sxs-lookup"><span data-stu-id="380fa-118">Defines the notifications supported by the [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) interface.</span></span> |
| [<span data-ttu-id="380fa-119">**IDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="380fa-119">**IDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | <span data-ttu-id="380fa-120">Spécifie les paramètres de sécurité pour un réseau ad hoc sans fil.</span><span class="sxs-lookup"><span data-stu-id="380fa-120">Specifies the security settings for a wireless ad hoc network.</span></span>                                         |
| [<span data-ttu-id="380fa-121">**IEnumDot11AdHocInterfaces**</span><span class="sxs-lookup"><span data-stu-id="380fa-121">**IEnumDot11AdHocInterfaces**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | <span data-ttu-id="380fa-122">Représente la collection des interfaces réseau ad hoc 802,11 actuellement visibles.</span><span class="sxs-lookup"><span data-stu-id="380fa-122">Represents the collection of currently visible 802.11 ad hoc network interfaces.</span></span>                       |
| [<span data-ttu-id="380fa-123">**IEnumDot11AdHocNetworks**</span><span class="sxs-lookup"><span data-stu-id="380fa-123">**IEnumDot11AdHocNetworks**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | <span data-ttu-id="380fa-124">Représente la collection de réseaux ad hoc 802,11 actuellement visibles.</span><span class="sxs-lookup"><span data-stu-id="380fa-124">Represents the collection of currently visible 802.11 ad hoc networks.</span></span>                                 |
| [<span data-ttu-id="380fa-125">**IEnumDot11AdHocSecuritySettings**</span><span class="sxs-lookup"><span data-stu-id="380fa-125">**IEnumDot11AdHocSecuritySettings**</span></span>](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | <span data-ttu-id="380fa-126">Représente la collection de paramètres de sécurité associée à chaque réseau ad hoc sans fil visible.</span><span class="sxs-lookup"><span data-stu-id="380fa-126">Represents the collection of security settings associated with each visible wireless ad hoc network.</span></span>   |



 

> [!Note]  
> <span data-ttu-id="380fa-127">Le mode ad hoc n’est peut-être pas disponible dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="380fa-127">Ad hoc mode might not be available in future versions of Windows.</span></span> <span data-ttu-id="380fa-128">À partir de Windows 8.1 et de Windows Server 2012 R2, utilisez plutôt [le Wi-Fi direct](about-the-wi-fi-direct-api.md) .</span><span class="sxs-lookup"><span data-stu-id="380fa-128">Starting with Windows 8.1 and Windows Server 2012 R2, use [Wi-Fi Direct](about-the-wi-fi-direct-api.md) instead.</span></span>

 

 

 



