---
title: À propos des messages SNMP
description: Le protocole de gestion de réseau simple utilise des messages pour communiquer et échanger des informations entre les entités SNMP distantes.
ms.assetid: 9ba4b854-fc02-40c1-a92f-7c102c900e95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0426bf44d976ddf9e2eafe2093dcea94956cb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379748"
---
# <a name="about-snmp-messages"></a><span data-ttu-id="8f1fd-103">À propos des messages SNMP</span><span class="sxs-lookup"><span data-stu-id="8f1fd-103">About SNMP Messages</span></span>

<span data-ttu-id="8f1fd-104">Le protocole de gestion de réseau simple utilise des messages pour communiquer et échanger des informations entre les entités SNMP distantes.</span><span class="sxs-lookup"><span data-stu-id="8f1fd-104">The Simple Network Management Protocol uses messages to communicate and exchange information between remote SNMP entities.</span></span> <span data-ttu-id="8f1fd-105">Les messages SNMP contiennent des unités de données de protocole (PDU) et des éléments d’en-tête de message supplémentaires définis par la RFC appropriée.</span><span class="sxs-lookup"><span data-stu-id="8f1fd-105">SNMP messages contain protocol data units (PDUs) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="8f1fd-106">Une PDU est un paquet de données qui contient des composants de données SNMP (ou champs).</span><span class="sxs-lookup"><span data-stu-id="8f1fd-106">A PDU is a data packet that contains SNMP data components (or fields).</span></span>

<span data-ttu-id="8f1fd-107">Le format d’un message SNMP est le même pour SNMPv1 et SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="8f1fd-107">The format of an SNMP message is the same for both SNMPv1 and SNMPv2C.</span></span> <span data-ttu-id="8f1fd-108">Toutefois, SNMPv2C prend en charge des types PDU supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="8f1fd-108">However, SNMPv2C supports additional PDU types.</span></span> <span data-ttu-id="8f1fd-109">Par exemple, il prend en charge le type de demande [ \_ \_ GETBULK PDU](snmp-variable-types-and-request-pdu-types.md) , qui permet à une application de récupérer efficacement des blocs de données volumineux à partir d’entités cibles.</span><span class="sxs-lookup"><span data-stu-id="8f1fd-109">For example, it supports the [SNMP\_PDU\_GETBULK](snmp-variable-types-and-request-pdu-types.md) request type, which enables an application to efficiently retrieve large blocks of data from target entities.</span></span>

 

 




