---
title: External. saveCurrentViewToLibrary, méthode
description: La méthode saveCurrentViewToLibrary crée une sélection à partir des éléments multimédias dans l’affichage actuel et enregistre la sélection dans la bibliothèque locale.
ms.assetid: cd87e932-d599-4298-bbee-6755999dda15
keywords:
- méthode saveCurrentViewToLibrary lecteur Windows Media
- méthode saveCurrentViewToLibrary lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, méthode saveCurrentViewToLibrary
topic_type:
- apiref
api_name:
- External.saveCurrentViewToLibrary
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 212f590f03c32821c0774c4898720c92558ecc73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537362"
---
# <a name="externalsavecurrentviewtolibrary-method"></a>External. saveCurrentViewToLibrary, méthode

La méthode **saveCurrentViewToLibrary** crée une sélection à partir des éléments multimédias dans l’affichage actuel et enregistre la sélection dans la bibliothèque locale.

## <a name="syntax"></a>Syntaxe


```JScript
External.saveCurrentViewToLibrary(
  FriendlyListName,
  Local
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FriendlyListName* \[ dans\]
</dt> <dd>

**Chaîne** qui spécifie un nom convivial pour la sélection. Le lecteur Windows Media affiche ce nom dans son interface utilisateur.

</dd> <dt>

*Local* \[ dans\]
</dt> <dd>

**Valeur booléenne** qui spécifie si la sélection est dynamique ou statique. **True** spécifie Dynamic, et **false** spécifie static.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





