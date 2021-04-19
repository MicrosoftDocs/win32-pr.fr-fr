---
title: THÈME. savePreference
description: La méthode savePreference enregistre une préférence dans le registre.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- THEMe. savePreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529958"
---
# <a name="themesavepreference"></a>THÈME. savePreference

La méthode **savePreference** enregistre une préférence dans le registre.

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*
</dt> <dd>

**Chaîne** spécifiant la clé de la valeur de préférence à enregistrer.

</dd> <dt>

<span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*Valeurreprésentant*
</dt> <dd>

**Chaîne** spécifiant la valeur à enregistrer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Une préférence est une paire clé/valeur qui peut être stockée dans le registre pour conserver les informations sur l’état du lecteur Windows Media entre les exécutions. Cette fonctionnalité peut être utilisée, par exemple, pour enregistrer les paramètres de personnalisation afin qu’ils n’aient pas à entrer à nouveau chaque fois que le lecteur Windows Media est démarré.

Les préférences ne sont pas chiffrées et ne sont donc pas une méthode sécurisée pour la persistance des données. N’utilisez pas de préférences pour stocker des données privées.

## <a name="examples"></a>Exemples


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément THEMe**](theme-element.md)
</dt> <dt>

[**THÈME. loadPreference**](theme-loadpreference.md)
</dt> </dl>

 

 





