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
ms.openlocfilehash: 6f6d70c6a3c2ac2d29c03e6d0518b5e7341f988f41e1bf2f5bb84a7de9f83f68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995909"
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

## <a name="return-value"></a>Valeur retournée

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

**Lecteur Windows Media 10 Mobile :** Cet événement n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



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

 

 





