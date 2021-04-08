---
title: Mise à jour d’une PDU
description: Une application WinSNMP peut récupérer et mettre à jour les champs de la PDU sélectionnée à l’aide des fonctions SnmpGetPduData et SnmpSetPduData.
ms.assetid: 001f5252-aa54-490b-8ff0-39a7780baff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678f980882b350669321cf676f9bc69af4369de8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675090"
---
# <a name="updating-a-pdu"></a><span data-ttu-id="80ea0-103">Mise à jour d’une PDU</span><span class="sxs-lookup"><span data-stu-id="80ea0-103">Updating a PDU</span></span>

<span data-ttu-id="80ea0-104">Une application WinSNMP peut récupérer et mettre à jour les champs de la PDU sélectionnée à l’aide des fonctions [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) et [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="80ea0-104">A WinSNMP application can retrieve and update selected PDU fields by using the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) and the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) functions.</span></span>

<span data-ttu-id="80ea0-105">L’application peut récupérer les champs type d’unité d’alimentation, identificateur de la demande, état de l’erreur et index des erreurs d’une PDU spécifique.</span><span class="sxs-lookup"><span data-stu-id="80ea0-105">The application can retrieve the PDU type, request identifier, error status, and error index fields from a specific PDU.</span></span> <span data-ttu-id="80ea0-106">Il peut également récupérer le descripteur de la liste de liaisons de variables.</span><span class="sxs-lookup"><span data-stu-id="80ea0-106">It can also retrieve the handle to the variable binding list.</span></span> <span data-ttu-id="80ea0-107">L’application peut mettre à jour le **\_ type d’unité d’alimentation** et les champs d' **\_ ID de demande** .</span><span class="sxs-lookup"><span data-stu-id="80ea0-107">The application can update the **PDU\_type** and **request\_id** fields.</span></span>

<span data-ttu-id="80ea0-108">Si le type de PDU est égal à la \_ PDU SNMP \_ GETBULK, l’application peut également mettre à jour les champs **non \_ répéteurs** et **nombre maximal de \_ répétitions** de la PDU.</span><span class="sxs-lookup"><span data-stu-id="80ea0-108">If the PDU type is equal to SNMP\_PDU\_GETBULK, the application can also update the **non\_repeaters** and the **max\_repetitions** fields of the PDU.</span></span>

 

 




