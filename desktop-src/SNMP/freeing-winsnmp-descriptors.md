---
title: Libération des descripteurs WinSNMP
description: L’environnement de programmation WinSNMP affecte la désallocation des ressources du descripteur à l’implémentation WinSNMP ou à l’application WinSNMP, en fonction du composant qui alloue la mémoire pour le descripteur.
ms.assetid: 3e4cbbc5-18bc-4731-971c-6e533d904f56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86081a69cd5455bc3c58ca2bcea50154d75920a17655a1feef30ac2d29675d0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009527"
---
# <a name="freeing-winsnmp-descriptors"></a>Libération des descripteurs WinSNMP

L’environnement de programmation WinSNMP affecte la désallocation des ressources du descripteur à l’implémentation WinSNMP ou à l’application WinSNMP, en fonction du composant qui alloue la mémoire pour le descripteur.

Pour libérer les ressources pour un [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou un descripteur [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , les règles suivantes s’appliquent :

-   Pour les paramètres d’entrée

    Étant donné que l’application WinSNMP alloue la mémoire pour les objets d’entrée avec des longueurs variables, l’application doit libérer cette mémoire à l’aide d’une fonction appropriée. Par exemple, si l’application a alloué les ressources avec un appel à la fonction [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) , elle doit utiliser la fonction [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) pour libérer les ressources. Si l’application a alloué les ressources avec un appel à la fonction [**HeapAlloc**](/windows/desktop/api/heapapi/nf-heapapi-heapalloc) , elle doit appeler la fonction [**HeapFree**](/windows/desktop/api/heapapi/nf-heapapi-heapfree) .

-   Pour les paramètres de sortie

    Un appel à l’une des fonctions suivantes permet à l’implémentation d’allouer de la mémoire pour un [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou un descripteur [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) : [**SnmpGetVb**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetvb), [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg), [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy), [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)et [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid).

    Étant donné que l’implémentation alloue la mémoire pour ces objets de sortie, l’application doit appeler la fonction [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) pour libérer les ressources. Cette fonction permet à l’implémentation de libérer la mémoire allouée pour le membre **ptr** de ces structures.

Pour libérer les ressources d’une structure [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) , une application WinSNMP doit vérifier le membre de **syntaxe** d’une structure [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) pour évaluer correctement le membre **value** de la structure. Si le membre de **syntaxe** indique que le membre de **valeur** est un descripteur [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) ou [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) , et que l’implémentation a alloué les ressources pour le descripteur, l’application doit appeler [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor). Cela permet à l’implémentation de libérer de la mémoire. Si l’application a alloué les ressources, elle doit libérer la mémoire à l’aide d’une fonction appropriée, comme indiqué plus haut.

Pour plus d’informations, consultez [allocation d’objets mémoire WinSNMP](allocating-winsnmp-memory-objects.md).

 

 