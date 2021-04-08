---
title: Objets de descripteur de ressource
description: La structure d’un objet de ressource est limitée à l’implémentation de l’WinSNMP Microsoft. Une application WinSNMP peut accéder à un objet de ressource avec un descripteur.
ms.assetid: c70a03b1-afac-4f1a-81e7-7f31430f5655
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1afe5e6488190f95961bff7ce37f7b719d076d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674906"
---
# <a name="resource-handle-objects"></a>Objets de descripteur de ressource

La structure d’un objet de ressource est limitée à l’implémentation de l’WinSNMP Microsoft. Une application WinSNMP peut accéder à un objet de ressource avec un descripteur.

L’implémentation peut allouer l’un des types de descripteurs de ressources suivants pour une application WinSNMP.

| Type de handle        | Description                       |
|--------------------|-----------------------------------|
| **\_session HSNMP** | Handle vers une session WinSNMP       |
| **\_entité HSNMP**  | Handle vers une entité SNMP          |
| **\_contexte HSNMP** | Handle vers un contexte WinSNMP       |
| **\_PDU HSNMP**     | Handle vers une unité de données de protocole    |
| **HSNMP \_ VBL**     | Handle vers une liste de liaisons de variables |



 

Une application WinSNMP peut demander que l’implémentation crée ou supprime des handles de ressource, mais que l’implémentation effectue l’opération. Pour plus d’informations sur la libération de ressources individuelles, consultez les fonctions [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor), [**SnmpFreeVbl**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreevbl), [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu), [**SnmpFreeEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreeentity)et [**SnmpFreeContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreecontext) .

 

 




