---
title: Événement Player. DomainChange
description: L’événement DomainChange se produit lorsque le domaine DVD change. | Événement Player. DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Lecteur Windows Media d’événements DomainChange
- Lecteur Windows Media d’événements DomainChange, classe Player
- Lecteur Windows Media de classe Player, événement DomainChange
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010994"
---
# <a name="playerdomainchange-event"></a>Événement Player. DomainChange

L’événement **DomainChange** se produit lorsque le domaine DVD change.

## <a name="syntax"></a>Syntaxe


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strDomain* 
</dt> <dd>

**Chaîne** indiquant le nouveau domaine. Contient l'une des valeurs suivantes :



| String            | Description                                                          |
|-------------------|----------------------------------------------------------------------|
| firstplay         | Exécution de l’initialisation par défaut d’un disque DVD.                     |
| videoManagerMenu  | Affichage des menus pour la totalité du disque. Également appelé menu racine ou menu principal. |
| videoTitleSetMenu | Affichage des menus pour le jeu de titres actuel. Également appelé titleMenu.     |
| title             | Affichage du titre actuel.                                        |
| stop              | Le navigateur DVD se trouve dans le domaine d’arrêt du DVD.                         |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Notes

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure.<br/>                           |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DVD**](dvd-object.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> </dl>

 

 





