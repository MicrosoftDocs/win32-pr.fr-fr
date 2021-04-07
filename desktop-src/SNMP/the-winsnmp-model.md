---
title: Le modèle WinSNMP
description: Le modèle compatible WinSNMP comprend les composants de base suivants.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7ae4fa1c1ee56fc534e4aa4c9bffefb8d7f4d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028866"
---
# <a name="the-winsnmp-model"></a><span data-ttu-id="0505f-103">Le modèle WinSNMP</span><span class="sxs-lookup"><span data-stu-id="0505f-103">The WinSNMP Model</span></span>

<span data-ttu-id="0505f-104">Le modèle compatible WinSNMP comprend les composants de base suivants :</span><span class="sxs-lookup"><span data-stu-id="0505f-104">The WinSNMP-compliant model includes the following basic components:</span></span>

-   <span data-ttu-id="0505f-105">Une application de gestion de réseau SNMP compatible WinSNMP, c’est-à-dire une *application* compatible WinSNMP</span><span class="sxs-lookup"><span data-stu-id="0505f-105">A WinSNMP-enabled SNMP network management application, that is, a WinSNMP-compliant *application*</span></span>
-   <span data-ttu-id="0505f-106">Couche de fonction WinSNMP</span><span class="sxs-lookup"><span data-stu-id="0505f-106">The WinSNMP function layer</span></span>
-   <span data-ttu-id="0505f-107">Un fournisseur de services SNMP compatible avec WinSNMP, c’est-à-dire une *implémentation* conforme à WinSNMP</span><span class="sxs-lookup"><span data-stu-id="0505f-107">A WinSNMP-enabled SNMP service provider, that is, a WinSNMP-compliant *implementation*</span></span>

<span data-ttu-id="0505f-108">Les applications de gestion de réseau qui doivent transmettre des messages SNMP fonctionnent efficacement dans un environnement piloté par les événements.</span><span class="sxs-lookup"><span data-stu-id="0505f-108">Network management applications that must convey SNMP messages operate efficiently in an event-driven environment.</span></span> <span data-ttu-id="0505f-109">Cela est dû au fait que le protocole SNMP est un protocole basé sur des datagrammes ou sans connexion entre les entités distantes qui n’établissent pas de circuits virtuels.</span><span class="sxs-lookup"><span data-stu-id="0505f-109">This is because SNMP is a datagram-based or connectionless protocol between remote entities that do not establish virtual circuits.</span></span>

<span data-ttu-id="0505f-110">Étant donné que les applications Microsoft Windows sont également pilotées par les événements, WinSNMP utilise un modèle de programmation dans lequel la réception et le traitement des applications de gestion des *événements de message* asynchrones.</span><span class="sxs-lookup"><span data-stu-id="0505f-110">Since Microsoft Windows applications are also event-driven, WinSNMP uses a programming model in which the receipt and processing of asynchronous *message-events* drive management applications.</span></span> <span data-ttu-id="0505f-111">Un événement de message asynchrone peut être une demande d’opération SNMP par une application de gestionnaire, ou la réponse à une demande d’une application agent.</span><span class="sxs-lookup"><span data-stu-id="0505f-111">An asynchronous message-event can be an SNMP operation request by a manager application, or the response to a request by an agent application.</span></span>

<span data-ttu-id="0505f-112">SNMP envoie les demandes et les réponses en tant que messages SNMP.</span><span class="sxs-lookup"><span data-stu-id="0505f-112">SNMP sends requests and responses as SNMP messages.</span></span> <span data-ttu-id="0505f-113">Un message SNMP est une unité de données de protocole (PDU) SNMP et des éléments d’en-tête de message supplémentaires définis par la RFC appropriée.</span><span class="sxs-lookup"><span data-stu-id="0505f-113">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="0505f-114">Pour plus d’informations, consultez [à propos des messages SNMP](about-snmp-messages.md), [utilisation des listes de liaisons de variables](working-with-variable-binding-lists.md) et [utilisation des unités de données de protocole](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="0505f-114">For more information, see [About SNMP Messages](about-snmp-messages.md), [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

 

 




