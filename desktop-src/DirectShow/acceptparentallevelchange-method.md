---
description: La méthode AcceptParentalLevelChange accepte ou rejette le nouveau niveau de gestion parental temporaire.
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: Méthode AcceptParentalLevelChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aea4742622ce9a2c65cdce660a8bae7fab6f84171d6bd61cdf88475c2bcd788c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873589"
---
# <a name="acceptparentallevelchange-method"></a>Méthode AcceptParentalLevelChange

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La méthode AcceptParentalLevelChange accepte ou rejette le nouveau niveau de gestion parental temporaire.

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*
</dt> <dd>

Spécifie le nouveau niveau parental en tant que valeur booléenne.



| Valeur | Description                               |
|-------|-------------------------------------------|
| true  | Acceptez le nouveau niveau de gestion parental. |
| false | Rejetez le nouveau niveau de gestion parental. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Appelez cette méthode en réponse à une \_ notification d’événement de modification du niveau parental du DVD EC \_ \_ \_ pour spécifier si le navigateur DVD doit lire le contenu avec le nouveau niveau parental, ou créer une branche vers l’emplacement où le disque spécifie si le nouveau niveau est rejeté.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Application des niveaux de gestion parentale](enforcing-parental-management-levels.md)
</dt> <dt>

[**GetPlayerParentalCountry**](getplayerparentalcountry-method.md)
</dt> <dt>

[**GetPlayerParentalLevel**](getplayerparentallevel-method.md)
</dt> <dt>

[**GetTitleParentalLevels**](gettitleparentallevels-method.md)
</dt> <dt>

[**NotifyParentalLevelChange**](notifyparentallevelchange-method.md)
</dt> <dt>

[**SelectParentalCountry**](selectparentalcountry-method.md)
</dt> <dt>

[**SelectParentalLevel**](selectparentallevel-method.md)
</dt> </dl>

 

 



