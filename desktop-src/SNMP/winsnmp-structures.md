---
title: Structures WinSNMP
description: Les fonctions de l’API WinSNMP utilisent les structures suivantes.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- SNMP structures WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b409b6d12063ebd3feb9c663f2d607bc5ceead0462b2945334f1e7e691c9be63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142752"
---
# <a name="winsnmp-structures"></a>Structures WinSNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Les fonctions de l’API WinSNMP utilisent les structures suivantes.



| Structure                                  | Description                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Contient une valeur d’entier non signé 64 bits qui représente un compteur.                                                    |
| [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Contient un pointeur vers une chaîne d’octets SNMP de longueur variable.                                                         |
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Contient un pointeur vers un tableau de longueur variable des sous-identificateurs associés à un objet nommé spécifié. |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Représente la valeur associée à un nom de variable dans une entrée de liaison de variable.                              |
| [**smiVENDORINFO**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Contient des informations sur l’implémentation Microsoft de WinSNMP.                                                    |



 

 

 