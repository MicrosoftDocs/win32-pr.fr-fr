---
title: Codes d’erreur WinSNMP
description: Codes d’erreur WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Codes d’erreur WinSNMP SNMP
- Codes d’erreur SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463570"
---
# <a name="winsnmp-error-codes"></a>Codes d’erreur WinSNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

> [!Note]  
> Les erreurs décrites dans cette rubrique sont distinctes des codes d’erreur SNMP définis par les RFC pertinentes.

 

Toutes les fonctions WinSNMP retournent la valeur **SNMPAPI \_ Failure** si la fonction échoue. L’application WinSNMP doit immédiatement appeler la fonction [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) pour récupérer les informations d’erreur étendues lorsqu’une fonction WinSNMP échoue. Le tableau suivant répertorie les rubriques qui traitent des codes d’erreur étendus retournés par les fonctions WinSNMP.



| Rubrique                                                        | Description                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [Codes d’erreur courants WinSNMP](winsnmp-common-error-codes.md) | Décrit les codes d’erreur courants pour l’API WinSNMP.       |
| [Erreurs de transport réseau](network-transport-errors.md)     | Décrit les erreurs de transport réseau pour l’API WinSNMP. |



 

Les erreurs WinSNMP qui transmettent des informations spécifiques au contexte sont incluses dans la page de référence de la fonction.

 

 