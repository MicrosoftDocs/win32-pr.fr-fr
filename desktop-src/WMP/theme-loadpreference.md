---
title: THÈME. loadPreference
description: La méthode loadPreference charge une préférence à partir du Registre.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- thème. loadPreference Lecteur Windows Media
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228390"
---
# <a name="themeloadpreference"></a>THÈME. loadPreference

La méthode **loadPreference** charge une préférence à partir du Registre.

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

**Chaîne** spécifiant la clé de la valeur de préférence à charger.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne une **chaîne**.

## <a name="remarks"></a>Notes

une préférence est une paire clé/valeur qui peut être stockée dans le registre pour conserver les informations sur l’état de la Lecteur Windows Media entre les exécutions. cette fonctionnalité peut être utilisée, par exemple, pour enregistrer les paramètres de personnalisation afin qu’ils n’aient pas à entrer à nouveau chaque fois que Lecteur Windows Media est démarré.

Les préférences ne sont pas chiffrées et ne sont donc pas une méthode sécurisée pour la persistance des données. N’utilisez pas de préférences pour stocker des données privées.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément THEMe**](theme-element.md)
</dt> <dt>

[**THÈME. savePreference**](theme-savepreference.md)
</dt> </dl>

 

 





