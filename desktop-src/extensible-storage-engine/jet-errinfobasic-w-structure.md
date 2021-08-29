---
description: 'En savoir plus sur : structure JET_ERRINFOBASIC_W'
title: Structure JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 7652bf39f620322d1c5ebc4b806438d182fd7c64
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477165"
---
# <a name="jet_errinfobasic_w-structure"></a>Structure JET_ERRINFOBASIC_W


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_errinfobasic_w-structure"></a>Structure JET_ERRINFOBASIC_W

La structure **JET_ERRINFOBASIC_W** définit les données retournées à partir de la méthode [JetGetErrorInfo ()](./jetgeterrorinfow-function.md) lorsque la JET_ErrorInfoSpecificErr InfoLevel est passée.

remarque : cette documentation est basée sur une version préliminaire du moteur de Stockage Extensible. Ces informations sont susceptibles d’être modifiées.

```cpp
typedef struct { 
    unsigned long cbStruct; 
    JET_ERR errValue; 
    JET_ERRCAT errcatMostSpecific; 
    unsigned char rgCategoricalHierarchy[8]; 
    unsigned long lSourceLine; 
    WCHAR rgszSourceFile[64]; 
} JET_ERRINFOBASIC_W;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure en octets. Elle doit être définie sur sizeof (JET_ERRINFOBASIC).

**errValue**

Valeur d’erreur qui a été évaluée, comme passé pour l’argument *pvResult* à [JetGetErrorInfo ()](./jetgeterrorinfow-function.md).

**errcatMostSpecific**

La constante [JET_ERRCAT](./jet-errcat.md) de niveau le plus bas qui est associée à l’erreur ; autrement dit, la catégorie de niveau feuille dans la hiérarchie de catégories documentée dans [JET_ERRCAT](./jet-errcat.md).

**rgCategoricalHierarchy \[ 8\]**

La hiérarchie des catégories d’erreur associée à l’erreur. La position 0 est le niveau le plus élevé dans la hiérarchie de [JET_ERRCAT](./jet-errcat.md), et le reste sont des sous-catégories jusqu’à ce que la catégorie la plus spécifique soit définie, après quoi toutes les catégories sont JET_errcatUnknownes.

**lSourceLine**

Réservé.

**rgszSourceFile \[ 64\]**

Réservé.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>Requiert Windows 8.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows 8 Server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 

