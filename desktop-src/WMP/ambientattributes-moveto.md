---
title: AmbientAttributes. moveTo
description: La méthode moveTo déplace le contrôle vers un nouvel emplacement à une vitesse linéaire.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- AmbientAttributes. moveTo lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540420"
---
# <a name="ambientattributesmoveto"></a>AmbientAttributes. moveTo

La méthode **MoveTo** déplace le contrôle vers un nouvel emplacement à une vitesse linéaire.

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*
</dt> <dd>

**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut de **gauche** du contrôle.

</dd> <dt>

<span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*
</dt> <dd>

**Nombre** (**long**) spécifiant la nouvelle valeur de l’attribut **Top** du contrôle.

</dd> <dt>

<span id="time"></span><span id="TIME"></span>*simultanément*
</dt> <dd>

**Nombre** (**long**) spécifiant la durée, en millisecondes, nécessaire au déplacement du contrôle vers son nouvel emplacement.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode est utile pour les éléments de sous- **affichage** animés (par exemple, si l’utilisateur clique sur une barre d’État et les contrôles déroulants).

Cette méthode crée un mouvement linéaire lors du déplacement du contrôle. Cela diffère de **slideTo**, qui crée un mouvement non linéaire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. Left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.slideTo**](ambientattributes-slideto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





