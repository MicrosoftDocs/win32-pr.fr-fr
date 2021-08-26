---
description: Il s’agit d’une stratégie système par ordinateur qui peut être utilisée pour appliquer des règles de composants de mise à niveau lors de petites mises à jour et de mises à niveau mineures.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 882d7df0e794dfb89ab2211db1fada576bd6e056972810d582385c1404e625a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086069"
---
# <a name="enforceupgradecomponentrules"></a>EnforceUpgradeComponentRules

Il s’agit d’une [stratégie système](system-policy.md) par ordinateur qui peut être utilisée pour appliquer des règles de composants de mise à niveau lors de [petites mises à jour](small-updates.md) et de [mises à niveau mineures](minor-upgrades.md).

Définissez la stratégie EnforceUpgradeComponentRules sur 1 pour appliquer les règles des composants de mise à niveau pendant les [petites mises à jour](small-updates.md) et les [mises à niveau mineures](minor-upgrades.md) de tous les produits sur l’ordinateur. Pour appliquer les règles pendant les petites mises à jour et les mises à niveau mineures d’un produit particulier, affectez la valeur 1 à la propriété [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) sur la ligne de commande ou dans la [table des propriétés](property-table.md).

Lorsque la propriété ou la stratégie a la valeur 1, les [petites mises à jour](small-updates.md) et les [mises à niveau mineures](minor-upgrades.md) peuvent échouer parce que la mise à jour tente d’effectuer les opérations suivantes :

-   Ajoutez une nouvelle fonctionnalité au sommet ou au milieu d’une arborescence de fonctionnalités existante.

    La nouvelle fonctionnalité doit être ajoutée en tant que nouvelle fonctionnalité feuille à une arborescence de fonctionnalités existante.

    Dans ce cas, la valeur [**ProductCode**](productcode.md) du produit peut être modifiée et les mises à jour peuvent être traitées comme une [mise à niveau majeure](major-upgrades.md).

-   Supprimer un composant d’une fonctionnalité.

    Cela peut également se produire si vous modifiez le GUID d’un composant. Le composant identifié par le GUID d’origine semble être supprimé et le composant identifié par le nouveau GUID apparaît en tant que nouveau composant.

    **Windows Installer 4,5 et versions ultérieures :** le composant peut être supprimé correctement à l’aide de Windows Installer 4,5 ou version ultérieure en définissant l’attribut **msidbComponentAttributesUninstallOnSupersedence** dans la [table des composants](component-table.md) ou en définissant la propriété [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .

    La valeur [**ProductCode**](productcode.md) du produit peut également être modifiée et les mises à jour peuvent être traitées comme une [mise à niveau majeure](major-upgrades.md).

## <a name="registry-key"></a>Clé de Registre

**HKEY \_ \_** \\ **stratégies logicielles** de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Type de données

**\_valeur DWORD reg**

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



