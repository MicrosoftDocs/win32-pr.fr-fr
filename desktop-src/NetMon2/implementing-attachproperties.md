---
description: Appelle la fonction AttachProperties pour mapper les propriétés qui existent dans une partie des données reconnues.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Implémentation de AttachProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009338"
---
# <a name="implementing-attachproperties"></a>Implémentation de AttachProperties

Moniteur réseau appelle la fonction [**AttachProperties**](attachproperties.md) pour mapper les propriétés qui existent dans une partie des données reconnues. La fonction [**AttachProperties**](attachproperties.md) mappe les propriétés à un emplacement spécifique.

Moniteur réseau utilise le processus suivant pour analyser les données dans un frame.

-   Tout d’abord, Moniteur réseau appelle [RecognizeFrame](recognizeframe.md) pour reconnaître tous les protocoles qui existent dans un frame.
-   Moniteur réseau appelle ensuite [**AttachProperties**](attachproperties.md) pour chaque analyseur qui reconnaît un élément de données.

Lorsque Moniteur réseau appelle la fonction [AttachProperties](attachproperties.md) pour les données reconnues, l’analyseur qui est appelé doit analyser les données, puis mapper chaque propriété existante à un emplacement dans les données reconnues. L’analyseur détermine les propriétés qui existent et l’emplacement où chaque propriété se trouve dans les données. L’illustration suivante montre les données identifiées par l’analyseur.

![données reconnues par l’analyseur](images/attachproperties1.png)

Pendant l’implémentation de [**AttachProperties**](attachproperties.md), vous devez appeler l’une des fonctions suivantes pour chaque propriété qui existe dans une trame de données.

-   Appelez la fonction [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) lorsque vous souhaitez modifier les données de propriété dans un frame.
-   Appelez la fonction [**AttachPropertyInstance**](attachpropertyinstance.md) lorsque vous ne voulez pas modifier les données de propriété dans un frame.

> [!Note]  
> Il est recommandé d’utiliser les données telles qu’elles existent dans la capture.

 

La procédure suivante identifie les étapes nécessaires à l’implémentation de [**AttachProperties**](attachproperties.md).

**Pour implémenter AttachProperties**

1.  Déterminez les propriétés qui existent et l’emplacement de la propriété dans les données.
2.  Appelez [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) pour chaque propriété avec une valeur que vous souhaitez modifier.
3.  Appelez [**AttachPropertyInstance**](attachpropertyinstance.md) pour chaque propriété avec une valeur que vous ne souhaitez pas modifier. En règle générale, il s’agit de la seule fonction que vous devez appeler.

Voici une implémentation de base de [**AttachProperties**](attachproperties.md). N’oubliez pas que l’exemple n’inclut pas le code pour déterminer quelles propriétés existent, soit le code pour localiser les propriétés.

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



