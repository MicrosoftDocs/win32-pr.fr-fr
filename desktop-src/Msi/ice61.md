---
description: ICE61 valide la table de mise à niveau d’une base de données Windows Installer.
ms.assetid: 9f6834c6-74eb-4219-8111-7b722ea41a3a
title: ICE61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f5a685d5b0a4f2bd5ce8dac70a738cbe2e0b9b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021520"
---
# <a name="ice61"></a>ICE61

ICE61 vérifie la table de mise à niveau pour s’assurer que les conditions suivantes sont remplies :

-   Toutes les propriétés ActionProperty ne sont pas pré-créées dans la table de propriétés.
-   Toutes les propriétés ActionProperty sont des propriétés publiques.
-   Toutes les propriétés ActionProperty sont incluses dans la propriété [**SecureCustomProperties**](securecustomproperties.md) .
-   Toutes les propriétés ActionProperty sont uniques à chaque enregistrement dans la table de mise à niveau.
-   Toutes les valeurs VersionMax ne sont pas inférieures aux valeurs VersionMin correspondantes.
-   Les valeurs VersionMin et VersionMax sont des versions de produit valides. Consultez la propriété [**ProductVersion**](productversion.md) pour le format de version de produit valide.
-   Aucune tentative n’est faite pour supprimer une version plus récente ou égale du produit actuel.

Si vous ne corrigez pas un avertissement ou une erreur signalée par ICE61, les problèmes liés à la mise à niveau de votre application sont généralement problématiques. En fonction de l’erreur exacte, il peut y avoir n’importe quoi, en laissant les fichiers de l’ancienne version en arrière-plan, en supprimant les fichiers de l’ancienne version, même s’ils sont requis par la nouvelle application, ou en cas de défaillance complète de la mise à niveau.

## <a name="result"></a>Résultats

ICE61 publie un avertissement ou une erreur si l’une des conditions ci-dessus n’est pas remplie.

## <a name="example"></a>Exemple

ICE61 signale les erreurs et avertissements suivants pour les exemples indiqués.

``` syntax
This product should remove only older versions of itself. The Maximum version is not less than the current product. (2.01.0000 2.01.0000)
```

Dans ce cas, la première ligne essaiera de supprimer un produit de la même version. (La colonne VersionMax est égale à la version du produit dans la table de propriétés).

Pour corriger cette erreur, utilisez une version de la colonne VersionMax inférieure à la version actuelle spécifiée dans la table de propriétés. Supprimez le bit **msidbUpgradeAttributesVersionMaxInclusive** de la colonne attributs si le VersionMax est égal à la version actuelle. Si l’objectif est uniquement de détecter le produit et de ne pas le supprimer, l’ajout du bit **msidbUpgradeAttributesOnlyDetect** à la colonne attributs corrigera également cette erreur.

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must be added to the SecureCustomProperties property.
```

À moins que la propriété ne soit listée dans la propriété [**SecureCustomProperties**](securecustomproperties.md) , la propriété n’est pas transmise au côté serveur de l’installation lorsque la propriété est trouvée.

Pour corriger cette erreur, ajoutez la propriété à [**SecureCustomProperties**](securecustomproperties.md).

``` syntax
Upgrade.ActionProperty EnglishAPPFOUND must not contain lowercase letters.
```

Les propriétés de mise à niveau doivent être des propriétés publiques pour que le résultat soit transmis au côté serveur de l’installation.

Pour corriger cette erreur, utilisez toutes les lettres majuscules dans le nom de la propriété.

``` syntax
Upgrade.ActionProperty OLDAPPFOUND may be used in only one record of the Upgrade table.
```

Une propriété ne peut être utilisée que sur une seule ligne de la table de mise à niveau.

Pour corriger cette erreur, utilisez une autre propriété pour la deuxième ligne.

``` syntax
Upgrade.VersionMax cannot be less than Upgrade.VersionMin. (OLDAPPFOUND)
```

La version minimale doit être inférieure à la version maximale.

Pour corriger cette erreur, vérifiez que les numéros de version ne sont pas corrects. S’ils sont corrects et que vous souhaitez utiliser la plage entre les deux versions, changez-les afin que VersionMin soit inférieur à VersionMax.

[Table de propriétés](property-table.md)



| Propriété                                                 | Valeur                                  |
|----------------------------------------------------------|----------------------------------------|
| [**UpgradeCode**](upgradecode.md)                       | {61AA4C55-E17F-11D2-93BB-0060089A76DB} |
| [**ProductVersion**](productversion.md)                 | 2.01.0000                              |
| [**SecureCustomProperties**](securecustomproperties.md) | OLDAPPFOUND                            |



 

[Mettre à niveau la table](upgrade-table.md)



| UpgradeCode                            | VersionMin | VersionMax | Langage | Attributs | Supprimer                | ActionProperty  |
|----------------------------------------|------------|------------|----------|------------|-----------------------|-----------------|
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} |            | 2.01.0000  |          | 513        |                       | OLDAPPFOUND     |
| {61AA4C55-E17F-11D2-93BB-0060089A76DB} | 2.01.0001  | 2.01.0000  |          |            |                       | OLDAPPFOUND     |
| {C6CB4596-D8E8-D5A4-635F-9FE456D682EB} | 1.00.0000  | 2.00.0000  | 1033     |            | \[AppFeatureEnglish\] | EnglishAPPFOUND |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



