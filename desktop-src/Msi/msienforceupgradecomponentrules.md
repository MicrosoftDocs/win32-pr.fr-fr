---
description: Affectez la valeur 1 à la propriété MSIENFORCEUPGRADECOMPONENTRULES sur la ligne de commande ou dans la table de propriétés pour appliquer les règles des composants de mise à niveau pendant les petites mises à jour et les mises à niveau mineures d’un produit particulier.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: Propriété MSIENFORCEUPGRADECOMPONENTRULES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11535beb45ac521e59ec31c5e5231b23549394b75e5df2372ba4295471ea8008
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945043"
---
# <a name="msienforceupgradecomponentrules-property"></a>Propriété MSIENFORCEUPGRADECOMPONENTRULES

Affectez la valeur 1 à la propriété **MSIENFORCEUPGRADECOMPONENTRULES** sur la ligne de commande ou dans la [table de propriétés](property-table.md) pour appliquer les règles des composants de mise à niveau pendant les [petites mises à jour](small-updates.md) et les [mises à niveau mineures](minor-upgrades.md) d’un produit particulier. Pour appliquer les règles pendant les petites mises à jour et les mises à niveau mineures de tous les produits sur l’ordinateur, définissez la stratégie [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) sur 1.

Lorsque la propriété ou la stratégie a la valeur 1, les [mises](small-updates.md) à jour [mineures et les mises à niveau mineures](minor-upgrades.md) peuvent échouer parce que la mise à jour tente d’effectuer les opérations suivantes qui ne respectent pas les règles du composant de mise à niveau :

-   Ajoutez une nouvelle fonctionnalité au sommet ou au milieu d’une arborescence de fonctionnalités existante.

    La nouvelle fonctionnalité doit être ajoutée en tant que nouvelle fonctionnalité feuille à une arborescence de fonctionnalités existante.

    Dans ce cas, la valeur [**ProductCode**](productcode.md) du produit peut être modifiée et la mise à jour peut être traitée comme une [mise à niveau majeure](major-upgrades.md).

-   Supprimer un composant d’une fonctionnalité.

    Cela peut également se produire si vous modifiez le GUID d’un composant. Le composant identifié par le GUID d’origine semble être supprimé et le composant identifié par le nouveau GUID apparaît en tant que nouveau composant.

    **Windows Installer 4,5 et versions ultérieures :** le composant peut être supprimé correctement à l’aide de Windows Installer 4,5 et versions ultérieures, en définissant l’attribut **msidbComponentAttributesUninstallOnSupersedence** dans la [Table des composants](component-table.md) ou en définissant la propriété [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .

    La valeur [**ProductCode**](productcode.md) du produit peut également être modifiée et la mise à jour peut être traitée comme une [mise à niveau majeure](major-upgrades.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




