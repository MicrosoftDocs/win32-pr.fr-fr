---
description: ICE03 valide les types de données et les clés étrangères en fonction de la \_ table de validation et des tables de base de données dans le fichier. msi.
ms.assetid: e9be1c09-8468-4956-9aa0-12383ade4718
title: ICE03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017c13ee568a0efe4d88c28594fb568a7b4a0736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203585"
---
# <a name="ice03"></a>ICE03

ICE03 valide les types de données et les clés étrangères en fonction de la [ \_ table de validation](-validation-table.md) et des tables de base de données dans le fichier. msi.

## <a name="result"></a>Résultats

ICE03 publie les messages suivants pour les erreurs de validation.



| Message d’erreur ICE03                                                       | Description                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dupliquer la clé primaire                                                     | Les clés primaires d’une nouvelle ligne dupliquent les clés primaires d’une ligne existante. La colonne Nullable du [ \_ tableau de validation](-validation-table.md) affiche les clés primaires dans la base de données.                                                                                              |
| N’est pas une colonne Nullable                                                     | Une colonne de table qui n’est pas spécifiée comme Nullable dans la colonne Nullable de la [ \_ table de validation](-validation-table.md) contient une entrée qui a la valeur null.                                                                                                                                |
| Clé étrangère non valide                                                   | Une colonne qui est une clé étrangère dans une deuxième table contient une entrée qui n’existe pas dans la clé primaire de la seconde table.                                                                                                                                                          |
| La valeur est supérieure à MaxValue                                                    | La valeur numérique d’une entrée dans une table de base de données dépasse la limite maximale spécifiée pour ce champ dans la colonne MaxValue de la [ \_ table de validation](-validation-table.md).                                                                                                           |
| Valeur inférieure à MinValue                                                      | La valeur numérique d’une entrée dans une table de base de données est inférieure à la limite minimale spécifiée pour ce champ dans la colonne MinValue de la [ \_ table de validation](-validation-table.md).                                                                                                      |
| La valeur n’est pas un membre de l’ensemble                                             | La valeur d’une entrée dans une table de base de données n’est pas un membre de l’ensemble de valeurs acceptable spécifié pour ce champ dans la colonne set de la [ \_ table de validation](-validation-table.md).                                                                                                  |
| Chaîne de version non valide                                                    | Consultez le type de données [version](version.md) .                                                                                                                                                                                                                                                 |
| Tout en MAJUSCULEs requis                                                   | Consultez le type de données [uppercase](uppercase.md) .                                                                                                                                                                                                                                             |
| Chaîne GUID non valide                                                       | Consultez le type de données [GUID](guid.md) .                                                                                                                                                                                                                                                       |
| Nom de fichier/utilisation des caractères génériques non valide                                      | La base de données contient un nom de fichier non valide ou un caractère générique incorrect. Consultez le type de données [WildCardFilename](wildcardfilename.md) .                                                                                                                                                          |
| Identificateur non valide                                                        | Consultez le type de données [identifier](identifier.md) .                                                                                                                                                                                                                                           |
| ID de langue non valide                                                       | La base de données contient un identificateur de langue numérique (LANGID) non valide. Consultez le type de données [Language](language.md) . Consultez [constantes et chaînes de l’identificateur de langue](../intl/language-identifier-constants-and-strings.md). Par exemple, 1033 pour les États-Unis et 0 pour la langue neutre.<br/> |
| Nom de fichier non valide                                                          | Consultez le type de données [filename](filename.md) .                                                                                                                                                                                                                                               |
| Chemin d’accès complet non valide                                                         | Consultez les types de données [path](path.md), [AnyPath](anypath.md) [et Paths](paths.md) .                                                                                                                                                                                                      |
| Chaîne conditionnelle incorrecte                                                    | La base de données contient une chaîne conditionnelle non valide. Il s’agit d’une chaîne de texte qui doit être évaluée à TRUE ou FALSe en fonction de la syntaxe de l' [instruction conditionnelle](conditional-statement-syntax.md). Consultez le type de données [condition](condition.md) .                                           |
| Chaîne de format non valide                                                     | Consultez le type de données [mis en forme](formatted.md) .                                                                                                                                                                                                                                             |
| Chaîne de modèle non valide                                                   | Consultez le type de données du [modèle](template.md) .                                                                                                                                                                                                                                               |
| Chaîne DefaultDir non valide                                                 | Consultez le type de données [DefaultDir](defaultdir.md) .                                                                                                                                                                                                                                           |
| Chemin du Registre non valide                                                     | Consultez le type de données [regpath](regpath.md) .                                                                                                                                                                                                                                                 |
| Données CustomSource incorrectes                                                     | Consultez le type de données [CustomSource](customsource.md) .                                                                                                                                                                                                                                       |
| Chaîne de propriété non valide                                                   | Consultez le type de données de la [propriété](property.md) .                                                                                                                                                                                                                                               |
| Données manquantes dans la \_ table de validation ou l’ancienne base de données                        | La base de données contient des colonnes qui ne sont pas répertoriées dans la colonne colonne du [ \_ tableau de validation](-validation-table.md). La base de données et la \_ table de validation ne correspondent pas                                                                                                           |
| Syntaxe/nom du fichier CAB erroné                                                   | Consultez le type de données [Cabinet](cabinet.md) .                                                                                                                                                                                                                                                 |
| \_Table de validation : chaîne de catégorie non valide                               | Il s’agit d’une erreur lors de la création du \_ tableau de validation. La validation ne reconnaît pas la chaîne de catégorie utilisée pour cette colonne particulière dans la \_ table de validation. Consultez [types de données des colonnes](column-data-types.md) et spécifiez une catégorie valide.                                           |
| \_Table de validation : les données de la colonne keytable sont incorrectes                  | La colonne keytable du \_ tableau de validation fait référence à une table qui n’existe pas dans la base de données.                                                                                                                                                                                     |
| \_Table de validation : valeur dans la colonne MaxValue < qui est dans la colonne MinValue | Il s’agit d’une erreur lors de la création du [ \_ tableau de validation](-validation-table.md). Min doit toujours être inférieur ou égal à max.                                                                                                                                                              |
| Cible de raccourci incorrecte                                                       | Consultez le type de données [Shortcut](shortcut.md) .                                                                                                                                                                                                                                               |
| Dépassement de capacité de la chaîne (supérieur à la longueur autorisée dans la colonne)                 | La longueur de la chaîne est supérieure à la largeur de colonne spécifiée par la définition de colonne. Notez que le programme d’installation ne limite pas en interne la largeur de colonne à la valeur spécifiée. Consultez [format de définition de colonne](column-definition-format.md).                                         |
| Erreur non définie                                                           | Erreur inconnue.                                                                                                                                                                                                                                                                            |
| La colonne ne peut pas être localisée                                                | Les colonnes de clé primaire ne peuvent pas être localisées.                                                                                                                                                                                                                                                  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 
