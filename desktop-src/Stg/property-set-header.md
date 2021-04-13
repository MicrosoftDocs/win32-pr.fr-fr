---
title: En-tête de jeu de propriétés
description: Au début du jeu de propriétés, le flux est un en-tête. Il se compose d’un indicateur d’ordre d’octet, d’une version de format, de la version du système d’exploitation d’origine, de l’identificateur de classe (CLSID) et d’un champ réservé.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Stockage structuré d’en-tête de jeu de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8d66eeec6525414ba3c6f0a0bb4f4fa34431c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311575"
---
# <a name="property-set-header"></a>En-tête de jeu de propriétés

Au début du jeu de propriétés, le flux est un en-tête. Il se compose d’un indicateur d’ordre d’octet, d’une version de format, de la version du système d’exploitation d’origine, de l’identificateur de classe (CLSID) et d’un champ réservé.

La Pseudo-structure suivante illustre l’en-tête.

``` syntax
typedef struct tagPROPERTYSETHEADER 
{ 
    // Header 
    WORD   wByteOrder ;  // Always 0xFFFE 
    WORD   wFormat ;     // Always 0 
    DWORD   dwOSVer ;    // System version 
    CLSID  clsID ;       // Application CLSID 
    DWORD  reserved ;    // Should be 1 
} PROPERTYSETHEADER;
```

 

 




