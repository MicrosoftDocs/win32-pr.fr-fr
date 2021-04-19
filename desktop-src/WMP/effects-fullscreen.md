---
title: EFFECTs. fullScreen
description: L’attribut fullScreen spécifie ou récupère une valeur indiquant si la visualisation en cours est affichée en mode plein écran. Cet attribut ne peut être défini qu’au moment de l’exécution.
ms.assetid: 319b46a4-b6c2-4dda-8285-f12af6836b25
keywords:
- EFFECTs. fullScreen Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e1824e35793a083eb88ea42de0eb8858a4b76f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528830"
---
# <a name="effectsfullscreen"></a>EFFECTs. fullScreen

L’attribut **fullscreen** spécifie ou récupère une valeur indiquant si la visualisation en cours est affichée en mode plein écran. Cet attribut ne peut être défini qu’au moment de l’exécution.

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                          |
|-------|------------------------------------------------------|
| true  | La visualisation s’affiche en plein écran.              |
| false | Par défaut. La visualisation n’est pas affichée en mode plein écran. |



 

## <a name="remarks"></a>Notes

Une visualisation peut être placée en mode plein écran uniquement pendant que le média est en cours de diffusion ou en pause. Si *Player*. **currentMedia** est une vidéo, un plug-in vidéo doit être présent. S’il s’agit d’un fichier audio, un plug-in de visualisation qui prend en charge l’affichage plein écran doit être présent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EFFECTs**](effects-element.md)
</dt> </dl>

 

 





