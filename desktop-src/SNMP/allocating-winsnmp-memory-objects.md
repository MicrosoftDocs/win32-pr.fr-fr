---
title: Allocation d’objets de mémoire WinSNMP
description: Les descripteurs, les handles de ressource et les chaînes de style C sont les trois types d’objets de mémoire dans l’environnement de programmation WinSNMP.
ms.assetid: 7f51f02b-7c9f-4aa0-b0cf-83551a312e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1188af74e150313cb24b01886d06df9e3ad065039cad9fa4a3e0b3b5ee6a9f4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009787"
---
# <a name="allocating-winsnmp-memory-objects"></a>Allocation d’objets de mémoire WinSNMP

Les descripteurs, les handles de ressource et les chaînes de style C sont les trois types d’objets de mémoire dans l’environnement de programmation WinSNMP.

Le type d’objet détermine si l’implémentation de l’WinSNMP de Microsoft ou l’application WinSNMP alloue et libère la mémoire pour l’objet. Cela réduit l’allocation inutile de l’espace de la mémoire tampon temporaire et la copie inutile des mémoires tampons.

Le tableau suivant résume l’allocation et la désallocation des ressources pour les objets mémoire WinSNMP.



| Type d’objet                                                                   | Description                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| descripteur [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) | Si l’application WinSNMP alloue de la mémoire, elle doit libérer la mémoire avec un appel à une fonction appropriée. Si l’implémentation alloue la mémoire, l’application doit appeler la fonction [**SnmpFreeDescriptor**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreedescriptor) pour libérer la mémoire. |
| [**smiVALUE**](/windows/desktop/api/Winsnmp/ns-winsnmp-smivalue) , structure                                    | Si le membre de **valeur** est un descripteur [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ou [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) , l’application doit s’exécuter comme indiqué ci-dessus pour les descripteurs.                                                                                                     |
| Handle de ressource                                                               | L’implémentation alloue, gère et libère la mémoire.                                                                                                                                                                                                                         |
| Chaîne de style C                                                                | L’application WinSNMP doit gérer et libérer la mémoire allouée.                                                                                                                                                                                                                |



 

Pour plus d’informations, consultez [libération de descripteurs WinSNMP](freeing-winsnmp-descriptors.md).

 

 




