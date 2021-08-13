---
description: La table ModuleSubstitution spécifie les champs configurables d’une base de données de module et fournit un modèle pour la configuration de chaque champ.
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: Table ModuleSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66fbbb0898a254b181d02eca78f33709f8c0e037de140a37893ea3887af6390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628586"
---
# <a name="modulesubstitution-table"></a>Table ModuleSubstitution

La table ModuleSubstitution spécifie les champs configurables d’une base de données de module et fournit un modèle pour la configuration de chaque champ. L’utilisateur ou l’outil de fusion peut interroger cette table pour déterminer quelles opérations de configuration doivent avoir lieu. Cette table n’est pas fusionnée dans la base de données cible.

Les tables suivantes ne peuvent pas contenir de champs configurables et ne doivent pas être listés dans ce tableau :

Table ModuleSubstitution

[Table ModuleConfiguration](moduleconfiguration-table.md)

[Table ModuleExclusion](moduleexclusion-table.md)

[ModuleSignature, table](modulesignature-table.md)

La table ModuleSubstitution contient les colonnes suivantes.



| Colonne | Type                         | Clé | Nullable |
|--------|------------------------------|-----|----------|
| Table de charge de travail  | [Identificateur](identifier.md) | O   | N        |
| Ligne    | [Text](text.md)             | O   | N        |
| Colonne | [Identificateur](identifier.md) | O   | N        |
| Valeur  | [Text](text.md)             | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau
</dt> <dd>

Cette colonne spécifie le nom de la table en cours de modification dans la base de données du module.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Haut
</dt> <dd>

Ce champ spécifie les clés primaires de la ligne cible dans la table nommée dans la colonne de table. Plusieurs clés primaires sont séparées par des points-virgules. Les lignes cibles sont sélectionnées pour être modifiées avant toute modification apportée à la table cible. Si un enregistrement de la table ModuleSubstitution modifie le champ de clé primaire d’une ligne cible, les autres enregistrements de la table ModuleSubstitution sont appliqués en fonction des données de clé primaire d’origine, et non des substitutions de clé primaire. L’ordre de substitution de ligne n’est pas défini.

Les valeurs de cette colonne sont toujours au [format spécial CMSM](cmsm-special-format.md). Un point-virgule littéral ('; ') ou un signe égal (' = ') peut être ajouté en préfixant le caractère par une barre oblique inverse. '\\'. Une valeur null pour une clé est indiquée par une valeur null, un point-virgule de début, deux points-virgules consécutifs ou un point-virgule de fin, selon que la valeur null est une valeur de colonne clé unique, première, centrale ou finale.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Chronique
</dt> <dd>

Ce champ spécifie la colonne cible dans la ligne nommée dans la colonne de ligne. Si plusieurs lignes de la table ModuleSubstitution changent différentes colonnes de la même ligne cible, toutes les substitutions de colonne sont effectuées avant que la ligne modifiée soit insérée dans la base de données. L’ordre de substitution de colonne n’est pas défini.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Ajoutée
</dt> <dd>

Cette colonne contient une chaîne qui fournit un modèle de mise en forme pour les données qui sont remplacées dans le champ cible spécifié par la table, la ligne et la colonne. Lorsqu’une chaîne de substitution de la forme \[ = ITEMA \] est rencontrée, la chaîne, y compris les crochets, est remplacée par la valeur de l’élément configurable « ITEMA ». L’élément configurable « ITEMA » est spécifié dans la colonne Name de la [table ModuleConfiguration](moduleconfiguration-table.md) et sa valeur est fournie par l’outil Merge Tool. Si l’outil de fusion refuse de fournir une valeur pour un élément d’une chaîne de remplacement, la valeur par défaut spécifiée dans la colonne DefaultValue de la table ModuleConfiguration est remplacée. Si une chaîne fait référence à un élément qui n’est pas dans la table ModuleConfiguration, la fusion échoue.

-   Cette colonne utilise le [format spécial CMSM](cmsm-special-format.md). Il est possible d’ajouter un point-virgule littéral ('; ') ou un signe égal (' = ') à la table en ajoutant une barre oblique inverse au caractère. '\\'.
-   Le champ valeur peut contenir plusieurs chaînes de substitution. Par exemple, la configuration des éléments « Food1 » et « Food2 » dans la chaîne : « \[ = Food1 \] est bonne, mais \[ = Food2 \] est préférable, car \[ = Food2 \] est plus Nutritious ».
-   Les chaînes de remplacement ne doivent pas être imbriquées. Le modèle « \[ = AB \[ = CDE \] \] » n’est pas valide.
-   Si le champ de valeur prend la valeur null et que le champ cible n’accepte pas la valeur null, la fusion échoue et un objet d’erreur de type msmErrorBadNullSubstitution est créé et ajouté à la liste d’erreurs. Pour plus d’informations, consultez les types d’erreurs décrits dans la [**fonction obtenir le \_ type**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).
-   Si le champ de valeur prend la valeur du GUID NULL : {00000000-0000-0000-0000-000000000000} , le GUID null est remplacé par le nom de la fonctionnalité avant que la ligne ne soit fusionnée dans le module. Pour plus d’informations, consultez [référencement des fonctionnalités dans les modules de fusion](referencing-features-in-merge-modules.md).
-   Le modèle dans le champ de valeur est évalué avant d’être inséré dans le champ cible. La substitution dans une ligne est effectuée avant le remplacement de toutes les fonctionnalités.
-   Si la colonne valeur prend la valeur d’une chaîne de caractères entiers uniquement (avec une valeur facultative + ou-), la chaîne est convertie en un entier avant d’être substituée dans un champ cible du [type de format entier](integer-format-types.md). Si le modèle prend la valeur d’une chaîne qui ne se compose pas uniquement de caractères entiers (et d’une valeur + ou-), le résultat ne peut pas être substitué dans un champ cible entier. Toute tentative d’insertion d’un entier non entier dans un champ entier provoque l’échec de la fusion et ajoute un objet d’erreur msmErrorBadSubstitutionType à la liste d’erreurs.
-   Si la colonne cible spécifiée dans les champs de table et de colonne est un [type de format texte](text-format-types.md)et que l’évaluation du champ de valeur donne un [type de format entier](integer-format-types.md), une représentation décimale du nombre est insérée dans le champ de texte cible.
-   Si le champ cible est un [type de format entier](integer-format-types.md), et le champ de valeur se compose d’une liste non délimitée d’éléments dans le [format](bitfield-format-types.md)de champ de bits, la valeur du champ cible est combinée à l’aide de l’opérateur de bits **and** avec l’inverse de l’opération de bits or de toutes les valeurs de masque des éléments, puis combinées à l’aide de **l’opérateur de** bits or avec chacun des éléments entiers **ou de champ** de bits Fondamentalement, cela définit explicitement les bits des propriétés sur les valeurs fournies, mais laisse tous les autres bits dans la cellule uniquement.
-   Si le champ de valeur prend la valeur d’un [type de format de clé](key-format-types.md)et qu’il s’agit d’une clé dans une table qui utilise plusieurs clés primaires, le nom de l’élément peut être suivi d’un point-virgule et d’une valeur entière qui indique l’index de base 1 dans l’ensemble de valeurs qui forment une clé primaire. Si aucun entier n’est spécifié, la valeur 1 est utilisée. Par exemple, la [table de contrôle](control-table.md) comporte deux colonnes de clé primaire, la boîte de dialogue \_ et le contrôle. La valeur d’un élément « Item1 » qui est une clé dans la table de contrôle se présente sous la forme «DialogName ; NomContrôle», où DialogName est la valeur dans la table de boîtes de dialogue \_ et NomContrôle est la valeur dans la colonne de contrôle. Pour remplacer simplement NomContrôle, la chaîne de substitution \[ = Item1 ; 2 \] doit être utilisée.

</dd> </dl>

## <a name="remarks"></a>Remarques

La table ModuleSubstition est utilisée par les [modules de fusion configurables](configurable-merge-modules.md). Mergemod.dll version 2,0 ou ultérieure est nécessaire pour créer un module de fusion configurable.

Pour garantir la compatibilité avec les versions de Mergemod.dll antérieures à la version 2,0, la [table ModuleConfiguration](moduleconfiguration-table.md) et les tables ModuleSubstitution doivent être incluses dans la [table ModuleIgnoreTable](moduleignoretable-table.md) de chaque module.

 

 
