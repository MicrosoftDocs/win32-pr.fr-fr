---
title: Codes d’erreur WinSNMP
description: Codes d’erreur WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Codes d’erreur WinSNMP SNMP
- Codes d’erreur SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2a9f9dda792008a0e69e6c23e692b4aa4c4e78316eeca015f7b056e2a275df1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142862"
---
# <a name="winsnmp-error-codes"></a>Codes d’erreur WinSNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

> [!Note]  
> Les erreurs décrites dans cette rubrique sont distinctes des codes d’erreur SNMP définis par les RFC pertinentes.

 

Toutes les fonctions WinSNMP retournent la valeur **SNMPAPI \_ Failure** si la fonction échoue. L’application WinSNMP doit immédiatement appeler la fonction [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) pour récupérer les informations d’erreur étendues lorsqu’une fonction WinSNMP échoue. Le tableau suivant répertorie les rubriques qui traitent des codes d’erreur étendus retournés par les fonctions WinSNMP.



| Rubrique                                                        | Description                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [Codes d’erreur courants WinSNMP](winsnmp-common-error-codes.md) | Décrit les codes d’erreur courants pour l’API WinSNMP.       |
| [Erreurs de transport réseau](network-transport-errors.md)     | Décrit les erreurs de transport réseau pour l’API WinSNMP. |



 

Les erreurs WinSNMP qui transmettent des informations spécifiques au contexte sont incluses dans la page de référence de la fonction.

 

 