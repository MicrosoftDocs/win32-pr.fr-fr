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
ms.openlocfilehash: 252f08c1971b1e8434e3761d87992a7245257c37bcc039650ebf5b7a0a47a884
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134572"
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

## <a name="remarks"></a>Remarques

une préférence est une paire clé/valeur qui peut être stockée dans le registre pour conserver les informations sur l’état de la Lecteur Windows Media entre les exécutions. cette fonctionnalité peut être utilisée, par exemple, pour enregistrer les paramètres de personnalisation afin qu’ils n’aient pas à entrer à nouveau chaque fois que Lecteur Windows Media est démarré.

Les préférences ne sont pas chiffrées et ne sont donc pas une méthode sécurisée pour la persistance des données. N’utilisez pas de préférences pour stocker des données privées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément THEMe**](theme-element.md)
</dt> <dt>

[**THÈME. savePreference**](theme-savepreference.md)
</dt> </dl>

 

 





