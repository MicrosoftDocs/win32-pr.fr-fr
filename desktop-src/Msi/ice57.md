---
description: ICE57 valide le fait que les composants individuels ne mélangent pas les données par ordinateur et par utilisateur. Cette action personnalisée ICE vérifie les entrées de Registre, les fichiers, les chemins d’accès aux clés de répertoire et les raccourcis non publiés.
ms.assetid: 3c82efa7-9cf3-4bcd-8ec4-b81d1d7aa0a6
title: ICE57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59d609e5d7de0011666be0b5cc5e76417d8e67d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021527"
---
# <a name="ice57"></a>ICE57

ICE57 valide le fait que les composants individuels ne mélangent pas les données par ordinateur et par utilisateur. Cette action personnalisée ICE vérifie les entrées de Registre, les fichiers, les chemins d’accès aux clés de répertoire et les raccourcis non publiés.

La combinaison de données par utilisateur et par ordinateur dans le même composant peut entraîner une installation partielle du composant pour certains utilisateurs dans un environnement multi-utilisateur.

Consultez la propriété [**ALLUSERS**](allusers.md) .

## <a name="result"></a>Résultats

ICE57 publie une erreur s’il trouve un composant contenant à la fois des entrées de Registre par ordinateur et par utilisateur, des fichiers, des chemins d’accès de clé de répertoire ou des raccourcis non publiés.

## <a name="example"></a>Exemple

ICE57reports les erreurs suivantes pour l’exemple indiqué.

``` syntax
Component 'Component1' has both per-user and per-machine 
    data with a per-machine KeyPath. 
 
WARNING: Component 'Component2' has both per-user and 
    per-machine data with an HKCU Registry KeyPath. 
 
Component 'Component3' has a registry entry that 
    can be either per-user or per-machine and a per-machine KeyPath. 
 
Component 'Component4' has both per-user data and 
    a keypath that can be either per-user or per-machine.
```

[Table des composants](component-table.md) (partielle)



| Composant  | Répertoire  | Attributs | KeyPath |
|------------|------------|------------|---------|
| Composant1 | Annuaire | 0          | Filea   |
| Component2 | Annuaire | 4          | RegKeyB |
| Component3 | Annuaire | 0          | FileC   |
| Component4 | Annuaire | 4          | RegKeyD |



 

[Table du Registre](registry-table.md) (partielle)



| Registre | Root | Composant\_ |
|----------|------|-------------|
| RegKeyA  | 1    | Composant1  |
| RegKeyB  | 1    | Component2  |
| RegKeyC  | -1   | Component3  |
| RegKeyD  | -1   | Component4  |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier  | Composant\_ |
|-------|-------------|
| Filea | Composant1  |
| FileB | Component2  |
| FileC | Component3  |
| Classer | Component4  |



 

[Table de répertoire](directory-table.md)



| Répertoire  | Répertoire \_ parent | DefaultDir |
|------------|-------------------|------------|
| TARGETDIR  |                   | SourceDir  |
| Annuaire | TARGETDIR         | Annuaire |



 

Pour résoudre les erreurs, réorganisez l’application de sorte que chaque composant ne contienne que les ressources par utilisateur ou par ordinateur, et non les deux.

Le premier message d’erreur est publié, car Composant1 contient Filea (par ordinateur) et la clé de Registre HKCU RegKeyA (Per User).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



