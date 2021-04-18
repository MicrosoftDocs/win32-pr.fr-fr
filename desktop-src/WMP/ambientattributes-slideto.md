---
title: AmbientAttributes.slideTo
description: La méthode slideTo déplace le contrôle vers un nouvel emplacement. Le contrôle se déplace de manière non linéaire sur la période spécifiée.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- Lecteur Windows Media AmbientAttributes. slideTo
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528980"
---
# <a name="ambientattributesslideto"></a>AmbientAttributes.slideTo

La méthode **slideTo** déplace le contrôle vers un nouvel emplacement. Le contrôle se déplace de manière non linéaire sur la période spécifiée.

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut de **gauche** du contrôle.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut **Top** du contrôle.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Nombre** (**long**) spécifiant la durée, en millisecondes, nécessaire au déplacement du contrôle vers son nouvel emplacement.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode est différente de **MoveTo**, qui crée un mouvement linéaire lors du déplacement du contrôle. Le mouvement non linéaire créé par cette méthode est un mouvement coulissant qui accélère à partir d’une vitesse nulle au début du mouvement et ralentit à zéro à la fin, en arrivant à un arrêt sans heurts.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. Left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes. moveTo**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





