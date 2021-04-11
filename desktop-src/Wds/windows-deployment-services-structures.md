---
title: Structures des services de déploiement Windows
description: Les structures suivantes sont utilisées avec les services de déploiement Windows.
ms.assetid: 2e52a6ae-cecb-45de-b777-108836ed5264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20f5b369a2bbb5d68bd77dce1751e09fed2e6b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029708"
---
# <a name="windows-deployment-services-structures"></a><span data-ttu-id="3ff50-103">Structures des services de déploiement Windows</span><span class="sxs-lookup"><span data-stu-id="3ff50-103">Windows Deployment Services Structures</span></span>

<span data-ttu-id="3ff50-104">Les structures suivantes sont utilisées avec les services de déploiement Windows.</span><span class="sxs-lookup"><span data-stu-id="3ff50-104">The following structures are used with Windows Deployment Services.</span></span>



| <span data-ttu-id="3ff50-105">Structure</span><span class="sxs-lookup"><span data-stu-id="3ff50-105">Structure</span></span>                                                                         | <span data-ttu-id="3ff50-106">Description</span><span class="sxs-lookup"><span data-stu-id="3ff50-106">Description</span></span>                                                                                                        |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ff50-107">**\_adresse PXE**</span><span class="sxs-lookup"><span data-stu-id="3ff50-107">**PXE\_ADDRESS**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_address)                                               | <span data-ttu-id="3ff50-108">Spécifie l’adresse réseau d’un paquet.</span><span class="sxs-lookup"><span data-stu-id="3ff50-108">Specifies the network address for a packet.</span></span>                                                                        |
| [<span data-ttu-id="3ff50-109">**\_message PXE DHCP \_**</span><span class="sxs-lookup"><span data-stu-id="3ff50-109">**PXE\_DHCP\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_message)                                    | <span data-ttu-id="3ff50-110">Cette structure est utilisée avec l’API du serveur PXE Windows Deployment Services.</span><span class="sxs-lookup"><span data-stu-id="3ff50-110">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="3ff50-111">**PXE \_ DHCP \_ (option)**</span><span class="sxs-lookup"><span data-stu-id="3ff50-111">**PXE\_DHCP\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcp_option)                                      | <span data-ttu-id="3ff50-112">Cette structure est utilisée avec l’API du serveur PXE Windows Deployment Services.</span><span class="sxs-lookup"><span data-stu-id="3ff50-112">This structure is used with the Windows Deployment Services PXE Server API.</span></span>                                        |
| [<span data-ttu-id="3ff50-113">**\_fournisseur PXE**</span><span class="sxs-lookup"><span data-stu-id="3ff50-113">**PXE\_PROVIDER**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_provider)                                             | <span data-ttu-id="3ff50-114">Décrit un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3ff50-114">Describes a provider.</span></span>                                                                                              |
| [<span data-ttu-id="3ff50-115">**\_cred CLI de WDS \_**</span><span class="sxs-lookup"><span data-stu-id="3ff50-115">**WDS\_CLI\_CRED**</span></span>](/windows/win32/api/wdsclientapi/ns-wdsclientapi-wds_cli_cred)                                            | <span data-ttu-id="3ff50-116">Contient les informations d’identification utilisées pour autoriser une session cliente.</span><span class="sxs-lookup"><span data-stu-id="3ff50-116">Contains credentials used to authorize a client session.</span></span>                                                           |
| [<span data-ttu-id="3ff50-117">**\_requête TRANSPORTCLIENT \_ WDS**</span><span class="sxs-lookup"><span data-stu-id="3ff50-117">**WDS\_TRANSPORTCLIENT\_REQUEST**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-wds_transportclient_request)              | <span data-ttu-id="3ff50-118">Utilisé par la fonction [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) .</span><span class="sxs-lookup"><span data-stu-id="3ff50-118">Used by the [**WdsTransportClientStartSession**](/windows/desktop/api/Wdstci/nf-wdstci-wdstransportclientstartsession) function.</span></span>                     |
| [<span data-ttu-id="3ff50-119">**\_informations sur la session TRANSPORTCLIENT \_**</span><span class="sxs-lookup"><span data-stu-id="3ff50-119">**TRANSPORTCLIENT\_SESSION\_INFO**</span></span>](/windows/desktop/api/Wdstci/ns-wdstci-transportclient_session_info)            | <span data-ttu-id="3ff50-120">Utilisé par la fonction de rappel [*PFN \_ WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) .</span><span class="sxs-lookup"><span data-stu-id="3ff50-120">Used by the [*PFN\_WdsTransportClientSessionStartEx*](/windows/desktop/api/Wdstci/nc-wdstci-pfn_wdstransportclientsessionstartex) callback function.</span></span> |
| [<span data-ttu-id="3ff50-121">**\_paramètres d' \_ initialisation de TRANSPORTPROVIDER WDS \_**</span><span class="sxs-lookup"><span data-stu-id="3ff50-121">**WDS\_TRANSPORTPROVIDER\_INIT\_PARAMS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_init_params) | <span data-ttu-id="3ff50-122">Utilisé par la fonction de rappel [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .</span><span class="sxs-lookup"><span data-stu-id="3ff50-122">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |
| [<span data-ttu-id="3ff50-123">**\_paramètres de TRANSPORTPROVIDER WDS \_**</span><span class="sxs-lookup"><span data-stu-id="3ff50-123">**WDS\_TRANSPORTPROVIDER\_SETTINGS**</span></span>](/windows/desktop/api/Wdstpdi/ns-wdstpdi-wds_transportprovider_settings)        | <span data-ttu-id="3ff50-124">Utilisé par la fonction de rappel [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) .</span><span class="sxs-lookup"><span data-stu-id="3ff50-124">Used by the [**WdsTransportProviderInitialize**](/windows/desktop/api/wdstpdi/nf-wdstpdi-wdstransportproviderinitialize) callback function.</span></span>            |



 

<span data-ttu-id="3ff50-125">Les éléments suivants sont disponibles à partir de Windows 8 et de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="3ff50-125">The following is available beginning with Windows 8 and Windows Server 2012.</span></span>

| <span data-ttu-id="3ff50-126">Structure</span><span class="sxs-lookup"><span data-stu-id="3ff50-126">Structure</span></span>                                          | <span data-ttu-id="3ff50-127">Description</span><span class="sxs-lookup"><span data-stu-id="3ff50-127">Description</span></span>                                               |
|----------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="3ff50-128">**PXE \_ DHCPv6 \_ (option)**</span><span class="sxs-lookup"><span data-stu-id="3ff50-128">**PXE\_DHCPV6\_OPTION**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_option)   | <span data-ttu-id="3ff50-129">Utilisé avec l’API du serveur PXE Windows Deployment Services.</span><span class="sxs-lookup"><span data-stu-id="3ff50-129">Used with the Windows Deployment Services PXE Server API.</span></span> |
| [<span data-ttu-id="3ff50-130">**\_Message DHCPv6 \_ PXE**</span><span class="sxs-lookup"><span data-stu-id="3ff50-130">**PXE\_DHCPV6\_MESSAGE**</span></span>](/windows/win32/api/wdspxe/ns-wdspxe-pxe_dhcpv6_message) | <span data-ttu-id="3ff50-131">Message DHCPV6.</span><span class="sxs-lookup"><span data-stu-id="3ff50-131">A DHCPV6 message.</span></span>                                         |



 

 

 




