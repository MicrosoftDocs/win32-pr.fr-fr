---
title: PLAYLIST. setColumnResizeMode
description: La méthode setColumnResizeMode spécifie le mode de redimensionnement de la colonne indexée.
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- PLAYLIST. setColumnResizeMode Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f356108ff016c404468a9b152b4adac247cd72ee089a9e82ea3206c4c2ffea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335801"
---
# <a name="playlistsetcolumnresizemode"></a>PLAYLIST. setColumnResizeMode

La méthode **setColumnResizeMode** spécifie le mode de redimensionnement de la colonne indexée.

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*chronique*
</dt> <dd>

**Nombre** (**long**) indiquant l’index de la colonne à modifier.

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*mode*
</dt> <dd>

**Chaîne** indiquant le mode de dimensionnement. Contient l'une des valeurs suivantes :



| Valeur          | Description                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | La colonne est redimensionnée pour s’adapter à toutes les données de la colonne et de l’en-tête.                                  |
| AutosizeData   | La colonne est redimensionnée pour s’adapter à toutes les données de la colonne uniquement.                                                 |
| Fixe          | La colonne a une taille fixe.                                                                                    |
| S’étire      | La colonne se redimensionne pour utiliser l’espace restant dans l’élément de **sélection** une fois que toutes les autres colonnes sont redimensionnées. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> </dl>

 

 





