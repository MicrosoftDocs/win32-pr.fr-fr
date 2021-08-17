---
description: ICE74 vérifie que la propriété FASTOEM n’a pas été créée dans la table de propriétés.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3120b0f4cd40acc53a1bcd3623dac33941a7f5da39bc538781e4ffd1d56345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328319"
---
# <a name="ice74"></a>ICE74

ICE74 vérifie que la propriété [**FASTOEM**](fastoem.md) n’a pas été créée dans la [table de propriétés](property-table.md).

la propriété [**FASTOEM**](fastoem.md) permet aux oem de réduire le temps nécessaire pour installer Windows Installer applications pour la première fois. Elle ne peut pas être utilisée après la première installation. La propriété **FASTOEM** ne doit pas être créée dans la table de propriétés, car cela interfère avec les installations suivantes pour la maintenance, la suppression ou la réparation de l’application.

ICE74 vérifie également que la propriété [**UpgradeCode**](upgradecode.md) est créée dans la table de [Propriétés](property-table.md), et que sa valeur n’est pas un GUID null, {00000000-0000-0000-0000-000000000000} .

## <a name="result"></a>Résultat

ICE74 peut poster les erreurs suivantes.



| Erreur ICE74                                                                       | Description                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| La propriété [**FASTOEM**](fastoem.md) ne peut pas être créée dans la table de propriétés. | La propriété [**FASTOEM**](fastoem.md) a été définie dans la table de propriétés.                             |
| ' \[ 2 \] 'n’est pas une [**UpgradeCode**](upgradecode.md)valide.                        | Un GUID null a été entré pour la propriété [**UpgradeCode**](upgradecode.md) dans la table de propriétés. |



 

ICE74 peut poster l’avertissement suivant.



| AVERTISSEMENT ICE74                                                                                                                                                                                             | Description                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| La propriété [**UpgradeCode**](upgradecode.md) n’est pas créée dans la table de propriétés. Il est fortement recommandé que les auteurs des packages d’installation spécifient une **UpgradeCode** pour leur application. | La propriété [**UpgradeCode**](upgradecode.md) n’est pas créée dans la table de propriétés. |



 

## <a name="example"></a>Exemple

ICE74 signale l’erreur suivante si la propriété [**FASTOEM**](fastoem.md) est définie : FASTOEM

``` syntax
 property cannot be authored in the Property table.
```

[Table de propriétés](property-table.md) (partielle)



| Propriété                   | Valeur |
|----------------------------|-------|
| [**FASTOEM**](fastoem.md) | 1     |



 

Pour corriger cette erreur, supprimez la propriété [**FASTOEM**](fastoem.md) de la table de propriétés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**FASTOEM, propriété**](fastoem.md)
</dt> <dt>

[Table de propriétés](property-table.md)
</dt> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



