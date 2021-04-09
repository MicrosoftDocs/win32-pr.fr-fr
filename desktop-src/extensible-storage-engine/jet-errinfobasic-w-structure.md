---
description: 'En savoir plus sur : structure JET_ERRINFOBASIC_W'
title: Structure JET_ERRINFOBASIC_W
TOCTitle: JET_ERRINFOBASIC_W Structure
ms:assetid: fcc55cb7-718d-419a-a473-15e030c23abd
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475861(v=EXCHG.10)
ms:contentKeyID: 37033567
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 99be77326fe9e037430203bf9744e550e8495fe1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "103954030"
---
# <a name="jet_errinfobasic_w-structure"></a>Structure JET_ERRINFOBASIC_W


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_errinfobasic_w-structure"></a>Structure JET_ERRINFOBASIC_W

La structure **JET_ERRINFOBASIC_W** définit les données retournées à partir de la méthode [JetGetErrorInfo ()](./jetgeterrorinfow-function.md) lorsque la JET_ErrorInfoSpecificErr InfoLevel est passée.

Remarque : cette documentation est basée sur une version préliminaire du moteur de stockage extensible. Ces informations sont susceptibles d’être modifiées.

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

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Requiert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Nécessite Windows 8 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>
