---
title: Méthode ShowPopupMenu
description: Méthode ShowPopupMenu
ms.assetid: 7f964d53-2594-41b1-9450-1ba7e9f85882
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0cfd080adcf0158a628f019b4d48be5cd10b9c5b47d7a4b71ccd2393ad83ce6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600989"
---
# <a name="showpopupmenu-method"></a>Méthode ShowPopupMenu

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Affiche le menu contextuel du caractère à l’emplacement spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agents. ***caractères («**_CharacterID_*_»). ShowPopupMenu_ * _x, y_



| Partie | Description                                                                                                                                          |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x*  | Obligatoire. Valeur entière qui indique la coordonnée d’écran horizontale (*x*) pour afficher le menu. Ces coordonnées doivent être spécifiées en pixels. |
| *y*  | Obligatoire. Valeur entière qui indique la coordonnée d’écran verticale (*y*) pour afficher le menu. Ces coordonnées doivent être spécifiées en pixels.   |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Agent affiche automatiquement le menu contextuel du caractère lorsque l’utilisateur clique avec le bouton droit sur le caractère. Si vous affectez à [**AutoPopupMenu**](autopopupmenu-property.md) la **valeur false**, vous pouvez utiliser cette méthode pour afficher le menu.

Le menu reste affiché jusqu’à ce que l’utilisateur sélectionne une commande ou affiche un autre menu. Un seul menu contextuel peut être affiché à la fois ; par conséquent, les appels à cette méthode annulent (supprime) le menu précédent.

Cette méthode doit être appelée uniquement lorsque votre application cliente est le client actif du caractère ; dans le cas contraire, elle échoue. Pour déterminer la réussite de cette méthode, vous pouvez l’appeler en tant que fonction et retourner une valeur booléenne indiquant si la méthode a réussi.


```
   If Genie.ShowPopupMenu (10,10) = True Then
      ' The menu will be displayed

   Else 
      ' The menu will not be displayed

   End If
```



## <a name="see-also"></a>Voir aussi

[**Propriété AutoPopupMenu**](autopopupmenu-property.md)


 

 




