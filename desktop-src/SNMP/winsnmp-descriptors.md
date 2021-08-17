---
title: Descripteurs WinSNMP
description: Dans l’environnement de programmation WinSNMP, un descripteur est l’une des deux structures suivantes.
ms.assetid: a329963b-cdb9-40d2-9a82-6f0d9f4ac73a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875112d8519f93f4b5ae6729401f2689294a84c55dc729f0ffa24d05076e300b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142912"
---
# <a name="winsnmp-descriptors"></a>Descripteurs WinSNMP

Dans l’environnement de programmation WinSNMP, un *descripteur* est l’une des deux structures suivantes :

-   Une structure [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) qui décrit une variable de chaîne d’octets
-   Une structure [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) qui décrit une variable d’identificateur d’objet SNMP

Un descripteur WinSNMP est une structure qui a deux membres : un membre de longueur, **Len** et un membre de pointeur, **ptr**. Le membre **ptr** pointe vers la chaîne d’octets ou l’identificateur d’objet qui vous intéresse. Le membre **ptr** peut être le type de données **smiLPBYTE** ou **smiLPUINT32** .

Un descripteur [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) ou un descripteur [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) peut être le membre **value** d’une structure **smiVALUE** . La structure [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) décrit la valeur associée à un nom de variable dans une entrée de liaison de variable.

L’implémentation de l’WinSNMP Microsoft alloue et libère de la mémoire pour toutes les structures **smiOCTETS** et **smiOID** de sortie. Par conséquent, l’application doit appeler la fonction [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) pour libérer la mémoire pour le membre **ptr** de ces structures.

Les membres de chaîne dans les descripteurs ne requièrent pas d’octet de fin **null** . Pour plus d’informations sur la gestion de la mémoire allouée pour les descripteurs, consultez [allocation d’objets mémoire WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




