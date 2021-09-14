---
description: ICEM09 vérifie que le module de fusion gère les répertoires prédéfinis en toute sécurité.
ms.assetid: 747ae5ee-adc1-4aa7-8239-2379f76bfd0f
title: ICEM09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30542ead9a47ab5e92074227b1ae47fa6de0e643
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021427"
---
# <a name="icem09"></a>ICEM09

ICEM09 vérifie que le module de fusion gère les répertoires prédéfinis en toute sécurité. Pour ce faire, il vérifie qu’aucun composant du module n’installe un répertoire dans un répertoire système prédéfini comme « ProgramFilesFolder » ou « StartMenuFolder ». Au lieu de cela, les modules doivent utiliser des répertoires avec des noms uniques (créés avec la Convention de nommage des modules de fusion) et utiliser des actions personnalisées pour cibler le répertoire cible approprié. Cette approche empêche les modules d’entrer en conflit avec une structure de répertoires existante dans la base de données finale. ICEM09 vérifie que les actions personnalisées nécessaires à cette technique pour fonctionner n’existent pas (afin que l’outil de fusion puisse les générer) ou qu’elles existent dans le format approprié (afin qu’elles fonctionnent comme prévu).

L’échec de la résolution d’un avertissement ou d’une erreur signalée par ICEM09 peut provoquer des problèmes pour les clients de votre module de fusion. Les lignes de la table de répertoires avec des clés primaires telles que ProgramFilesFolder existent souvent dans une base de données ; par conséquent, si les composants de votre module s’installent directement dans des répertoires prédéfinis tels que ProgramFilesFolder, les entrées de répertoire dans le module peuvent entrer en conflit avec des lignes déjà existantes. Cette condition oblige l’utilisateur de votre module à fractionner les fichiers sources de votre module afin qu’il corresponde au répertoire source existant.

## <a name="result"></a>Résultats

ICEM09 signale une erreur ou un avertissement lorsqu’un composant de module installe un répertoire dans un répertoire système prédéfini, provoquant ainsi un conflit de noms avec la structure de répertoires existante.

## <a name="example"></a>Exemple

ICEM09 publie les avertissements suivants pour un module contenant les entrées de base de données affichées.

``` syntax
Warning: The component 'Component1.<GUID>' installs directly into the pre-defined 
directory 'ProgramFilesFolder'. It is recommended that merge modules alias 
all such directories to unique names.
```

renommez le répertoire du module de fusion afin qu’il ne corresponde pas à une propriété Windows Installer et qu’il soit unique. affectez ensuite à une propriété du même nom la valeur de l’Windows Installer directory. Lorsque la résolution de répertoire a lieu, le répertoire a une propriété du même nom, donc l’emplacement d’installation du répertoire est la valeur de la propriété. Les fichiers sont déplacés de l’emplacement source distinct vers le même emplacement cible. Ce processus doit supprimer complètement les conflits de fusion.

``` syntax
Warning: The 'ModuleInstallExecuteSequence' table contains a type 51 action 
(StartMenuFolder.<GUID>) for a pre-defined directory, but this action 
does not have sequence number '1'
```

Si l’action n’a pas le numéro de séquence 1, il est possible qu’elle n’effectue pas de fusion dans la base de données cible suffisamment tôt dans la séquence pour fonctionner efficacement.

Pour résoudre cet avertissement, définissez le numéro de séquence sur 1. Notez que la plupart des outils de fusion actuels (mais pas certaines versions antérieures) génèrent ces actions personnalisées au moment de la fusion. par conséquent, il n’est pas toujours nécessaire de créer explicitement les actions dans le module de fusion.

``` syntax
Warning: The 'CustomAction' table contains a type 51 action (MyAppDataFolderAction) 
for a pre-defined directory, but the name is not the same as the target directory. 
Many merge tools will generate duplicate actions."
```

Étant donné que la colonne CustomAction est la clé primaire de la table CustomAction, certains outils de fusion peuvent générer des actions en double, car le nom de l’action précréée est différent.

Pour résoudre cet avertissement, nommez l’action de la même façon que le répertoire cible. Notez que la plupart des outils de fusion actuels (mais pas certaines versions antérieures) génèrent ces actions personnalisées au moment de la fusion. il n’est donc pas toujours nécessaire de créer explicitement les actions dans le module de fusion.

[Table de répertoire](directory-table.md)



| Répertoire          | Répertoire \_ parent | DefaultDir |
|--------------------|-------------------|------------|
| ProgramFilesFolder | Répertoire1        | Un          |
| StartMenuFolder    | Directory2        | B:C        |
| AppDataFolder      | Directory3        | D          |
| MyPicturesFolder   | Directory4        | E          |



 

[Table des composants](component-table.md)



| Composant               | Répertoire          |
|-------------------------|--------------------|
| Composant1. &lt; UNIQUES&gt; | ProgramFilesFolder |
| COMPONENT2. &lt; UNIQUES&gt; | StartMenuFolder    |
| Component3. &lt; UNIQUES&gt; | AppDataFolder      |
| Component4. &lt; UNIQUES&gt; | MyPicturesFolder   |



 

[Table CustomAction](customaction-table.md)



| CustomAction                 | Type | Source                       | Cible              |
|------------------------------|------|------------------------------|---------------------|
| StartMenuFolder. &lt; UNIQUES&gt; | 51   | StartMenuFolder. &lt; UNIQUES&gt; | \[StartMenuFolder\] |
| MyAppDataFolderAction        | 51   | AppDataFolder. &lt; UNIQUES&gt;   | \[AppDataFolder\]   |



 

[Table ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md)



| Action                       | Séquence | BaseAction | Après | Condition |
|------------------------------|----------|------------|-------|-----------|
| StartMenuFolder. &lt; UNIQUES&gt; | 100      |            |       |           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE du module de fusion](merge-module-ice-reference.md)
</dt> </dl>

 

 



