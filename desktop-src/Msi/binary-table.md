---
description: La table binaire contient les données binaires pour les éléments tels que les bitmaps, les animations et les icônes. La table binaire est également utilisée pour stocker des données pour les actions personnalisées. Consultez restrictions OLE sur Flux.
ms.assetid: 44c56407-df2e-4cbe-b7a3-b22e8d97eb03
title: Table binaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a70750193b1dc147a9b2b4cfa01bbea410f0e44b7c03f16bd1c992f118a4f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638803"
---
# <a name="binary-table"></a>Table binaire

La table binaire contient les données binaires pour les éléments tels que les bitmaps, les animations et les icônes. La table binaire est également utilisée pour stocker des données pour les actions personnalisées. Consultez [restrictions OLE sur flux](ole-limitations-on-streams.md).

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

 

 



