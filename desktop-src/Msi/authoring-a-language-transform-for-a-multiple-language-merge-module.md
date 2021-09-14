---
description: Lorsqu’un module est fusionné dans une base de données qui a une autre langue par défaut, l’outil de fusion peut avoir besoin d’appliquer une transformation de langage au module pour fournir le dernier langage. Pour plus d’informations, consultez modules de fusion multilingues.
ms.assetid: 51e8774e-f358-423f-a283-ad7beeabbbdb
title: Création d’une transformation de langue pour un module de fusion à plusieurs langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 970c8908ddbf89e31f0fc7a415358bb887f0838e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092526"
---
# <a name="authoring-a-language-transform-for-a-multiple-language-merge-module"></a>Création d’une transformation de langue pour un module de fusion à plusieurs langues

Lorsqu’un module est fusionné dans une base de données qui a une autre langue par défaut, l’outil de fusion peut avoir besoin d’appliquer une transformation de langage au module pour fournir le dernier langage. Pour plus d’informations, consultez [modules de fusion multilingues](multiple-language-merge-modules.md).

Les transformations de langage sont stockées dans le fichier. msm du module et doivent avoir le nom et le format : MergeModule. lang \# \# \# \# . Le \# \# \# \# représente l' [ID de langue](localizing-the-error-and-actiontext-tables.md) (en anglais) jusqu’à quatre chiffres du dernier langage. Par exemple, MergeModule. Lang1033, MergeModule. Lang9 et MergeModule. Lang0 pour les transformations en anglais (États-Unis), anglais du monde et indépendant de la langue. Ils sont identiques aux [transformations incorporées](embedded-transforms.md) et vous pouvez les ajouter à des sous-stockages dans le fichier. msm.

La transformation de langage doit effectuer les opérations suivantes :

-   Remplacez la langue par défaut dans la colonne Language de la [table ModuleSignature](modulesignature-table.md) par la nouvelle langue du module.
-   Remplacez la langue par défaut dans la colonne Language de la [table ModuleComponents](modulecomponents-table.md) par la nouvelle langue du module. La transformation peut ajouter ou supprimer des lignes dans cette table.
-   Si nécessaire, modifiez la langue dans la colonne RequiredLanguage ou ajoutez ou supprimez des lignes dans la [table ModuleDependency](moduledependency-table.md).
-   Si nécessaire, modifiez la langue dans la colonne ExcludedLanguage ou ajoutez ou supprimez des lignes dans la [table ModuleExclusion](moduleexclusion-table.md).
-   La transformation peut effectuer n’importe quelle opération de transformation valide sur le module, y compris l’ajout ou la suppression de composants, de fichiers, d’entrées de registre ou d’actions.

Notez que l’application d’une transformation de langage lors de l’ouverture du module ne modifie pas la langue par défaut ni les langues prises en charge par le module. il modifie simplement la langue demandée. Par conséquent, la propriété [**Résumé du modèle**](template-summary.md) ne change pas, elle doit déjà répertorier toutes les langues prises en charge par le module avec la langue par défaut répertoriée en premier.

Tous les fichiers nécessaires à toutes les transformations de langage possibles sont généralement stockés dans un fichier CAB unique inclus dans le module. Comme il n’est pas pratique que la transformation de langage modifie ce fichier CAB, il est préférable d’utiliser une séquence de fichiers globale dans le fichier CAB, la [table de fichiers](file-table.md)et la transformation de langue. Pour plus d’informations, consultez [classement de la séquence de fichiers dans le fichier cab d’un module de fusion de plusieurs langues](ordering-the-file-sequence-in-the-cab-of-a-multiple-language-merge-module.md)

 

 



