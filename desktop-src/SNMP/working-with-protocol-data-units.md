---
title: Utilisation d’unités de données de protocole
description: Le protocole SNMP (simple Network Management Protocol) envoie des demandes et des réponses d’opération en tant que messages SNMP.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Utilisation d’unités de données de protocole SNMP
- Unités de données de protocole SNMP, utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029529"
---
# <a name="working-with-protocol-data-units"></a><span data-ttu-id="7283e-105">Utilisation d’unités de données de protocole</span><span class="sxs-lookup"><span data-stu-id="7283e-105">Working with Protocol Data Units</span></span>

<span data-ttu-id="7283e-106">Le protocole SNMP (simple Network Management Protocol) envoie des demandes et des réponses d’opération en tant que messages SNMP.</span><span class="sxs-lookup"><span data-stu-id="7283e-106">The Simple Network Management Protocol (SNMP) sends operation requests and responses as SNMP messages.</span></span> <span data-ttu-id="7283e-107">Un message SNMP est une unité de données de protocole (PDU) SNMP et des éléments d’en-tête de message supplémentaires définis par la RFC appropriée.</span><span class="sxs-lookup"><span data-stu-id="7283e-107">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="7283e-108">Une PDU comprend une liste de liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="7283e-108">A PDU includes a variable binding list.</span></span>

<span data-ttu-id="7283e-109">La structure d’une PDU est limitée à l’implémentation de l’WinSNMP Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7283e-109">The structure of a PDU is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="7283e-110">Une application WinSNMP peut accéder à un PDU avec un descripteur de type **HSNMP \_ PDU**.</span><span class="sxs-lookup"><span data-stu-id="7283e-110">A WinSNMP application can access a PDU with a handle of the type **HSNMP\_PDU**.</span></span> <span data-ttu-id="7283e-111">L’application WinSNMP doit créer un PDU avant d’appeler la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) ou la fonction [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .</span><span class="sxs-lookup"><span data-stu-id="7283e-111">The WinSNMP application must create a PDU before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function.</span></span>

<span data-ttu-id="7283e-112">L’application peut extraire et mettre à jour les éléments de données d’une PDU, et libérer les ressources allouées aux PDU.</span><span class="sxs-lookup"><span data-stu-id="7283e-112">The application can extract and update the data elements of a PDU, and release resources allocated for PDUs.</span></span> <span data-ttu-id="7283e-113">Pour effectuer ces opérations, l’application utilise les [fonctions d’rampe d’alimentation](winsnmp-functions.md)winsnmp.</span><span class="sxs-lookup"><span data-stu-id="7283e-113">To perform these operations, the application uses the WinSNMP [PDU functions](winsnmp-functions.md).</span></span> <span data-ttu-id="7283e-114">Le tableau suivant répertorie les rubriques qui traitent de l’utilisation des PDU dans l’environnement de programmation WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="7283e-114">The following table lists topics that discuss working with PDUs in the WinSNMP programming environment.</span></span>



| <span data-ttu-id="7283e-115">Rubrique</span><span class="sxs-lookup"><span data-stu-id="7283e-115">Topic</span></span>                                                                        | <span data-ttu-id="7283e-116">Description</span><span class="sxs-lookup"><span data-stu-id="7283e-116">Description</span></span>                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="7283e-117">Création d’une PDU</span><span class="sxs-lookup"><span data-stu-id="7283e-117">Creating a PDU</span></span>](creating-a-pdu.md)                                         | <span data-ttu-id="7283e-118">Décrit comment créer une PDU.</span><span class="sxs-lookup"><span data-stu-id="7283e-118">Describes how to create a PDU.</span></span>                                     |
| [<span data-ttu-id="7283e-119">Mise à jour d’une PDU</span><span class="sxs-lookup"><span data-stu-id="7283e-119">Updating a PDU</span></span>](updating-a-pdu.md)                                         | <span data-ttu-id="7283e-120">Décrit comment récupérer et mettre à jour les champs de la PDU.</span><span class="sxs-lookup"><span data-stu-id="7283e-120">Describes how to retrieve and update PDU fields.</span></span>                   |
| [<span data-ttu-id="7283e-121">Duplication d’une PDU</span><span class="sxs-lookup"><span data-stu-id="7283e-121">Duplicating a PDU</span></span>](duplicating-a-pdu.md)                                   | <span data-ttu-id="7283e-122">Décrit comment dupliquer une PDU.</span><span class="sxs-lookup"><span data-stu-id="7283e-122">Describes how to duplicate a PDU.</span></span>                                  |
| [<span data-ttu-id="7283e-123">Validation d’une PDU</span><span class="sxs-lookup"><span data-stu-id="7283e-123">Validating a PDU</span></span>](validating-a-pdu.md)                                     | <span data-ttu-id="7283e-124">Décrit la validation d’une PDU.</span><span class="sxs-lookup"><span data-stu-id="7283e-124">Describes the validation of a PDU.</span></span>                                 |
| [<span data-ttu-id="7283e-125">Réponse correspondante et demandes d’alimentation (PDU)</span><span class="sxs-lookup"><span data-stu-id="7283e-125">Matching Response and Request PDUs</span></span>](matching-response-and-request-pdus.md) | <span data-ttu-id="7283e-126">Décrit le processus de correspondance d’un PDU de réponse à un PDU de demande.</span><span class="sxs-lookup"><span data-stu-id="7283e-126">Describes the process of matching a response PDU to a request PDU.</span></span> |



 

<span data-ttu-id="7283e-127">Pour plus d’informations, consultez [utilisation des listes de liaisons de variables](working-with-variable-binding-lists.md) et des objets de handle de [ressource](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7283e-127">For more information, see [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Resource Handle Objects](resource-handle-objects.md).</span></span>

 

 




