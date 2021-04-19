---
description: La table binaire contient les données binaires pour les éléments tels que les bitmaps, les animations et les icônes. La table binaire est également utilisée pour stocker des données pour les actions personnalisées. Consultez Limitations OLE sur les flux.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Table binaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4069c7e684e7d90c94b4b04f3d5839058f3570a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525021"
---
# <a name="binary-table"></a>Table binaire

La table binaire contient les données binaires pour les éléments tels que les bitmaps, les animations et les icônes. La table binaire est également utilisée pour stocker des données pour les actions personnalisées. Consultez [limitations OLE sur les flux](ole-limitations-on-streams.md).

La table binaire contient les colonnes suivantes.



| Colonne | Type                         | Clé | Nullable |
|--------|------------------------------|-----|----------|
| Nom   | [Identificateur](identifier.md) | O   | N        |
| Données   | [Binaire](binary.md)         | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Clé unique qui identifie les données binaires particulières. Si les données binaires sont destinées à un contrôle, la clé apparaît dans la colonne de texte du contrôle associé dans la [table de contrôle](control-table.md). Cette clé doit être unique parmi tous les contrôles nécessitant des données binaires.

</dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée
</dt> <dd>

Données binaires non mises en forme.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE29](ice29.md)  
</dl>

 

 



