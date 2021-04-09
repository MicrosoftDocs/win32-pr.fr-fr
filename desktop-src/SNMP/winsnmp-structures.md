---
title: Structures WinSNMP
description: Les fonctions de l’API WinSNMP utilisent les structures suivantes.
ms.assetid: ec74217e-8d02-4bda-b365-7b8f6c14cffb
keywords:
- SNMP structures WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b263f6078171c096eb7208ae4c7ef29847aead9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842489"
---
# <a name="winsnmp-structures"></a>Structures WinSNMP

\[SNMP peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures. Utilisez plutôt [Windows Remote Management](/windows/desktop/WinRM/portal), qui est l’implémentation Microsoft de WS-Man.\]

Les fonctions de l’API WinSNMP utilisent les structures suivantes.



| Structure                                  | Description                                                                                                            |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**smiCNTR64**](/windows/desktop/api/Winsnmp/ns-winsnmp-smicntr64)         | Contient une valeur d’entier non signé 64 bits qui représente un compteur.                                                    |
| [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)         | Contient un pointeur vers une chaîne d’octets SNMP de longueur variable.                                                         |
| [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid)               | Contient un pointeur vers un tableau de longueur variable des sous-identificateurs associés à un objet nommé spécifié. |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue)           | Représente la valeur associée à un nom de variable dans une entrée de liaison de variable.                              |
| [**smiVENDORINFO**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivendorinfo) | Contient des informations sur l’implémentation Microsoft de WinSNMP.                                                    |



 

 

 