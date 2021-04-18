---
title: Activation et désactivation de la retransmission
description: Une application peut définir le mode de retransmission avec un appel à la fonction SnmpSetRetransmitMode. Le nouveau mode de retransmission s’applique aux appels suivants à la fonction SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512236"
---
# <a name="turning-retransmission-on-and-off"></a><span data-ttu-id="a4068-104">Activation et désactivation de la retransmission</span><span class="sxs-lookup"><span data-stu-id="a4068-104">Turning Retransmission On and Off</span></span>

<span data-ttu-id="a4068-105">Une application peut définir le mode de retransmission avec un appel à la fonction [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="a4068-105">An application can set the retransmission mode with a call to the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="a4068-106">Le nouveau mode de retransmission s’applique aux appels suivants à la fonction [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="a4068-106">The new retransmission mode applies to subsequent calls to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span>

<span data-ttu-id="a4068-107">Lorsque l’application appelle **SnmpSetRetransmitMode** avec la valeur du mode de retransmission SNMPAPI \_ sur, l’implémentation de l’WinSNMP Microsoft commence l’exécution de la stratégie de retransmission de l’application.</span><span class="sxs-lookup"><span data-stu-id="a4068-107">When the application calls **SnmpSetRetransmitMode** with the retransmission mode value SNMPAPI\_ON, the Microsoft WinSNMP implementation begins execution of the application's retransmission policy.</span></span> <span data-ttu-id="a4068-108">Le nouveau mode de retransmission n’affecte pas les messages SNMP en suspens.</span><span class="sxs-lookup"><span data-stu-id="a4068-108">The new retransmission mode does not affect outstanding SNMP messages.</span></span> <span data-ttu-id="a4068-109">Un message en attente est un message qui n’a pas de réponse au moment où l’application modifie le mode de retransmission.</span><span class="sxs-lookup"><span data-stu-id="a4068-109">An outstanding message is one that has no response at the time the application changes the retransmission mode.</span></span>

<span data-ttu-id="a4068-110">Lorsque l’application WinSNMP appelle la fonction [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) avec le mode de retransmission valeur SNMPAPI \_ off, l’implémentation cesse d’exécuter la stratégie de retransmission.</span><span class="sxs-lookup"><span data-stu-id="a4068-110">When the WinSNMP application calls the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function with the retransmission mode value SNMPAPI\_OFF, the implementation stops executing the retransmission policy.</span></span> <span data-ttu-id="a4068-111">L’implémentation annule les tentatives de retransmission pour les messages SNMP en attente.</span><span class="sxs-lookup"><span data-stu-id="a4068-111">The implementation cancels retransmission attempts for outstanding SNMP messages.</span></span> <span data-ttu-id="a4068-112">Cela est dû au fait qu’il n’est pas possible que l’implémentation gère toutes les demandes et toutes les opérations SNMP en suspens, ainsi que les nouvelles requêtes, avant qu’un délai d’attente d’application ou un compteur de tentatives ne signale un événement.</span><span class="sxs-lookup"><span data-stu-id="a4068-112">This is because it may not be possible for the implementation to handle all outstanding SNMP requests and operations plus new requests, before an application time-out or retry counter signals an event.</span></span>

 

 




