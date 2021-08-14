---
title: Gestion des identificateurs d’objets
description: L’API WinSNMP fournit plusieurs fonctions utilitaires WinSNMP qui simplifient la manipulation des identificateurs d’objet pour les applications WinSNMP.
ms.assetid: 6ca5f5bc-aa49-4826-97a7-2ea4a882dc2d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362adbf445901f25307452d67c313ef2a8d0ac5aea038ebfcf61863a72370cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009417"
---
# <a name="managing-object-identifiers"></a>Gestion des identificateurs d’objets

L’API WinSNMP fournit plusieurs [fonctions utilitaires WinSNMP](winsnmp-functions.md) qui simplifient la manipulation des identificateurs d’objet pour les applications winsnmp.

La fonction [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) convertit la représentation binaire interne d’un identificateur d’objet en son format de chaîne numérique en pointillés. Quand vous appelez [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr), spécifiez une mémoire tampon de chaîne de longueur MAXOBJIDSTRSIZE (1408 octets) pour vous assurer que la mémoire tampon de sortie est suffisamment grande pour contenir la chaîne convertie. Pour convertir un identificateur d’objet à partir du format de chaîne numérique avec points en sa représentation binaire interne, appelez la fonction [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) .

Pour copier un identificateur d’objet SNMP, appelez la fonction [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) . Cette fonction alloue la mémoire nécessaire pour le nouvel identificateur d’objet.

Une application WinSNMP doit appeler la fonction [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) pour libérer les ressources allouées pour le membre **ptr** de la structure [**SmiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) spécifiée par les fonctions [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid) et [**SnmpOidCopy**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcopy) .

La fonction [**SnmpOidCompare**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidcompare) compare deux identificateurs d’objet SNMP. L’application WinSNMP peut spécifier le nombre de sous-identificateurs à comparer. Appelez **SnmpOidCompare** pour déterminer si deux identificateurs d’objet ont des préfixes communs.

Pour plus d’informations sur la gestion de la mémoire allouée pour les identificateurs d’objets, consultez [allocation d’objets mémoire WinSNMP](allocating-winsnmp-memory-objects.md).

 

 




