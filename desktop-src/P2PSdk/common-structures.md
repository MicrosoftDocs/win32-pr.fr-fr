---
description: L’infrastructure homologue utilise les structures communes suivantes.
ms.assetid: b8f290fb-ae0b-44de-87cc-d25f7e0e3ae6
title: Structures communes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fb4afd791d42565202ef55779d1b4ee9260efa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525064"
---
# <a name="common-structures"></a><span data-ttu-id="beb6b-103">Structures communes</span><span class="sxs-lookup"><span data-stu-id="beb6b-103">Common Structures</span></span>

<span data-ttu-id="beb6b-104">L’infrastructure homologue utilise les structures communes suivantes.</span><span class="sxs-lookup"><span data-stu-id="beb6b-104">The Peer Infrastructure uses the following common structures.</span></span>



| <span data-ttu-id="beb6b-105">Structure</span><span class="sxs-lookup"><span data-stu-id="beb6b-105">Structure</span></span>                                                                          | <span data-ttu-id="beb6b-106">Description</span><span class="sxs-lookup"><span data-stu-id="beb6b-106">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="beb6b-107">**adresse HOMOLOGUe \_**</span><span class="sxs-lookup"><span data-stu-id="beb6b-107">**PEER\_ADDRESS**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_address)                                              | <span data-ttu-id="beb6b-108">Spécifie les informations sur l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="beb6b-108">Specifies the information about the IP address.</span></span>                                                                                     |
| [<span data-ttu-id="beb6b-109">**\_informations sur la connexion homologue \_**</span><span class="sxs-lookup"><span data-stu-id="beb6b-109">**PEER\_CONNECTION\_INFO**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_connection_info)                             | <span data-ttu-id="beb6b-110">Contient des informations sur une connexion.</span><span class="sxs-lookup"><span data-stu-id="beb6b-110">Contains information about a connection.</span></span> <span data-ttu-id="beb6b-111">Cette structure est retournée lorsque vous énumérez des connexions de représentation graphique ou de regroupement d’homologues.</span><span class="sxs-lookup"><span data-stu-id="beb6b-111">This structure is returned when you are enumerating peer graphing or grouping connections.</span></span> |
| [<span data-ttu-id="beb6b-112">**données HOMOLOGUes \_**</span><span class="sxs-lookup"><span data-stu-id="beb6b-112">**PEER\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_data)                                                    | <span data-ttu-id="beb6b-113">Contient des données binaires.</span><span class="sxs-lookup"><span data-stu-id="beb6b-113">Contains binary data.</span></span>                                                                                                               |
| [<span data-ttu-id="beb6b-114">**\_données de \_ modification des connexions d’événements homologues \_ \_**</span><span class="sxs-lookup"><span data-stu-id="beb6b-114">**PEER\_EVENT\_CONNECTION\_CHANGE\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_connection_change_data) | <span data-ttu-id="beb6b-115">Contient des informations mises à jour qui incluent des modifications apportées à un voisin ou une connexion directe.</span><span class="sxs-lookup"><span data-stu-id="beb6b-115">Contains updated information that includes changes to a neighbor or direct connection.</span></span>                                              |
| [<span data-ttu-id="beb6b-116">**\_ \_ données entrantes des événements homologues \_**</span><span class="sxs-lookup"><span data-stu-id="beb6b-116">**PEER\_EVENT\_INCOMING\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_incoming_data)                    | <span data-ttu-id="beb6b-117">Contient des informations mises à jour qui incluent des modifications de données qu’un nœud reçoit d’une connexion voisine ou directe.</span><span class="sxs-lookup"><span data-stu-id="beb6b-117">Contains updated information that includes data changes a node receives from a neighbor or direct connection.</span></span>                       |
| [<span data-ttu-id="beb6b-118">**\_données de \_ modification des enregistrements d’événements homologues \_ \_**</span><span class="sxs-lookup"><span data-stu-id="beb6b-118">**PEER\_EVENT\_RECORD\_CHANGE\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_event_record_change_data)         | <span data-ttu-id="beb6b-119">Contient des informations mises à jour qu’une application demande des modifications de données à un enregistrement ou à un type d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="beb6b-119">Contains updated information that an application requests for data changes to a record or record type.</span></span>                              |
| [<span data-ttu-id="beb6b-120">**enregistrement d’HOMOLOGUe \_**</span><span class="sxs-lookup"><span data-stu-id="beb6b-120">**PEER\_RECORD**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_record)                                                | <span data-ttu-id="beb6b-121">Contient l’objet record utilisé par une application.</span><span class="sxs-lookup"><span data-stu-id="beb6b-121">Contains the record object that an application uses.</span></span>                                                                                |
| [<span data-ttu-id="beb6b-122">**\_données de version de l’homologue \_**</span><span class="sxs-lookup"><span data-stu-id="beb6b-122">**PEER\_VERSION\_DATA**</span></span>](/windows/desktop/api/P2P/ns-p2p-peer_version_data)                                   | <span data-ttu-id="beb6b-123">Contient les informations de version sur les API de regroupement et de représentation graphique des homologues.</span><span class="sxs-lookup"><span data-stu-id="beb6b-123">Contains the version information about the Peer Graphing and Grouping APIs.</span></span>                                                         |



 

 

 



