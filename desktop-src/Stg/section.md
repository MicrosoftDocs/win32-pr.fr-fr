---
title: Section
description: La section est la troisième partie du flux de jeu de propriétés et contient les valeurs de jeu de propriétés réelles.
ms.assetid: cb392072-116e-4dca-bd70-5f82f86d8c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71796bca5dd2801e437ecfffe663f2702abc4c202d721ecbda8a9b95656e40a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682799"
---
# <a name="section"></a>Section

La section est la troisième partie du flux de jeu de propriétés et contient les valeurs de jeu de propriétés réelles.

Une section contient les éléments suivants :

-   Nombre d’octets pour la section qui est incluse dans le nombre d’octets lui-même.
-   Tableau de paires ID/ID de propriété 32 bits.
-   Tableau d’indicateurs de type de propriété/paires de valeurs.

Les décalages représentent la distance entre le début de la section et le début de la paire propriété (type, valeur). Cela permet de copier une section en tant que tableau d’octets sans traduction de la structure interne.

Les Pseudo-structures suivantes illustrent le format d’une section.

``` syntax
typedef struct tagPROPERTYSECTIONHEADER 
{ 
    DWORD  cbSection ;    // Size of Section 
    DWORD  cProperties ;  // Count of Properties in section 
} PROPERTYSECTIONHEADER; 
 
typedef struct tagPROPERTYIDOFFSET 
{ 
    DWORD  propid;    // Name of property 
    DWORD  dwOffset;  // Offset from start of section to property 
} PROPERTYIDOFFSET; 
 
typedef struct tagSERIALIZEDPROPERTYVALUE 
{ 
    DWORD  dwType;    // Property Type 
    BYTE   rgb[];     // Property Value 
} SERIALIZEDPROPERTYVALUE ;
```

 

 




