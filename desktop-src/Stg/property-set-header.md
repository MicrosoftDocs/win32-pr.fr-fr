---
title: En-tête de jeu de propriétés
description: Au début du jeu de propriétés, le flux est un en-tête. Il se compose d’un indicateur d’ordre d’octet, d’une version de format, de la version du système d’exploitation d’origine, de l’identificateur de classe (CLSID) et d’un champ réservé.
ms.assetid: 6f4531d5-99d8-43ff-b6c1-5975b7527fc0
keywords:
- Stockage structuré d’en-tête de jeu de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506249ae917c6fbf00853a2547188a08ce14ebb29bc24d7e6daaa1aaa830cb3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662219"
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

 

 




