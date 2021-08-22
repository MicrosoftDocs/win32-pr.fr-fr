---
description: ICE30 vérifie que l’installation des composants contenant le même fichier n’installe jamais le fichier plus d’une fois dans le même répertoire.
ms.assetid: 74cb455b-a53e-4c6b-98ff-08cf0858f11f
title: ICE30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba807ec1eb3bde54b1f115e93c531f24414b75e7a293c8ff1b7d7ff1d3abca8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528659"
---
# <a name="ice30"></a>ICE30

ICE30 vérifie que l’installation des composants contenant le même fichier n’installe jamais le fichier plus d’une fois dans le même répertoire.

ICE30 accède à chaque composant de la [table des composants](component-table.md) , puis détermine le répertoire cible du composant à partir de la [table de répertoires](directory-table.md). Il vérifie ensuite quels composants s’installent dans le même répertoire cible. Enfin, elle utilise la [table file](file-table.md) pour vérifier qu’aucun des fichiers de ces composants n’a le même nom.

ICE30 vérifie les noms de fichiers longs (LFN) et les noms de fichiers courts (SFN).

ICE30 n’évalue pas les propriétés dans la résolution des répertoires, car ces propriétés peuvent changer au moment de l’exécution et modifier le schéma de résolution d’annuaire. Cela signifie que ICE30 peut détecter des collisions de fichiers en raison des répertoires ayant la même propriété dans leurs chemins d’accès, mais ne détecte pas les collisions résultant de deux propriétés ayant la même valeur.

## <a name="result"></a>Résultat

ICE30 publie un message d’erreur pour chaque paire de composants qui installe le même fichier dans le même répertoire.

## <a name="example"></a>Exemples

L’exemple présenté retourne chaque erreur suivante deux fois.



| Erreur ou avertissement ICE30                                                                                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERREUR : le fichier cible’README. 1re’est installé dans le’TARGETDIR \\ Product’par deux composants différents sur un système SFN : 'Composant1 'et’COMPONENT2 '. Cela interrompt le décompte de références de composants.                                                                                           | Composant1 et COMPONENT2 ont tous les deux un fichier nommé « READEME. 1er ». Lorsque vous utilisez des noms de fichiers courts, le programme d’installation installe à la fois Dir1 et dir2 dans le même répertoire, TARGETDIR \\ Product.<br/> ICE30 génère deux erreurs, une pour chaque fichier. Dans un environnement de création qui affiche des emplacements d’erreur, la première erreur se trouve à l’entrée d’un fichier dans la [table de fichiers](file-table.md)et la seconde à l’emplacement de l’autre fichier.<br/> |
| ERREUR : l’installation d’un composant conditionnel entraînerait l’installation du fichier cible « README. 1er » dans « TARGETDIR \\ Common Tools » par deux composants différents sur un système LFN : « Component3 » et « Component4 ». Cela rompt le décompte de références de composants.                      | Component4 a une entrée dans la colonne condition de la [table Component](component-table.md) et Component3 ne le fait pas. Si [**VersionNT**](versionnt.md) a la valeur true, Component4 est installé et il y a une collision avec le fichier Readme. la première est toujours installée par Component3.<br/> ICE30 génère 4 erreurs, une paire pour SFN, une pour LFN.<br/>                                                                                            |
| AVERTISSEMENT : le fichier cible « README. premier » peut être installé dans « TARGETDIR \\ Common Tools » par deux composants conditionnels différents sur un système SFN : « Component4 » et « Component5 ». Si les conditions ne s’excluent pas mutuellement, le système de comptage des références du composant sera rompu. | Étant donné que Component4 et Component5 ont tous les deux des entrées dans la colonne condition de la [table des composants](component-table.md) , cette collision de fichier peut ne pas se produire. ICE30 publie un avertissement uniquement parce que les conditions doivent être déterminées au moment de l’installation.<br/> ICE30 génère 4 avertissements, une paire pour SFN, un pour LFN.<br/>                                                                                            |



 

[Table des composants](component-table.md) (partielle)



| Composant  | Répertoire | Condition |
|------------|-----------|-----------|
| Composant1 | Dir1      |           |
| Component2 | Dir2      |           |
| Component3 | Dir3      |           |
| Component4 | Dir3      | VersionNT |
| Component5 | Dir3      | Version9X |



 

[Table de répertoire](directory-table.md)



| Répertoire | \_Répertoire parent | DefaultDir                    |
|-----------|-------------------|-------------------------------|
| SOURCEDIR |                   | TARGETDIR                     |
| Dir1      | SOURCEDIR         | Produit \| Composant1 produit :. |
| Dir2      | SOURCEDIR         | Produit :.                     |
| Dir3      | SOURCEDIR         | \|Outils courants courants :         |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Composant\_ | FileName   |
|-------|-------------|------------|
| Fichier1 | Composant1  | Lisez-moi. 1re |
| Fichier2 | Component2  | Lisez-moi. 1re |
| Fichier3 | Component3  | Lisez-moi. 1re |
| Fichier4 | Component4  | Lisez-moi. 1re |
| Fichier5 | Component5  | Lisez-moi. 1re |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




