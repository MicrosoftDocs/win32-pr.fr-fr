---
description: ICE38 valide que chaque composant en cours d’installation sous le profil de l’utilisateur actuel spécifie également une clé de Registre sous la \_ racine HKEY Current \_ user dans la colonne keyPath de la table Component.
ms.assetid: f1548b04-78c2-461a-a729-9a8c4856d0d8
title: ICE38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d001d244160f939a73e697e677bf43a1f5f825f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021566"
---
# <a name="ice38"></a>ICE38

ICE38 valide que chaque composant en cours d’installation sous le profil de l’utilisateur actuel spécifie également une clé de Registre sous la racine **HKEY \_ Current \_ User** dans la colonne keyPath de la [table Component](component-table.md).

## <a name="result"></a>Résultats

ICE38 publie une erreur si un composant installé sous le profil de l’utilisateur ne spécifie pas de clé de Registre HKCU.

## <a name="example"></a>Exemple

ICE38 signale les erreurs suivantes pour l’exemple indiqué.



| Erreur ICE38                                                                                                                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le composant Composant1 s’installe dans le profil utilisateur. Il doit utiliser une clé de Registre sous HKCU comme keyPath, et non un fichier.                    | La valeur de la colonne Attributes de Composant1 est 0, ce qui signifie que le composant doit utiliser un fichier comme keyPath. Cela pose des difficultés lorsque plusieurs utilisateurs installent le composant sur le même ordinateur. Pour corriger cette erreur sur Composant1, définissez le bit RegistryKeyPath dans la colonne attributs de la [table Component](component-table.md) et remplacez l’entrée de la colonne keyPath par une valeur indiquée dans la colonne Registry de la [table Registry](registry-table.md).<br/>                                                                                |
| Le composant COMPONENT2 s’installe dans le profil utilisateur. Il doit utiliser une clé de Registre sous HKCU comme keyPath. KeyPath est actuellement NULL. | COMPONENT2 a le bit RegistryKeyPath défini dans la colonne attributs de la [table des composants](component-table.md). Le champ keyPath doit donc contenir une clé pour la colonne Registry de la [table Registry](registry-table.md) , mais la colonne keyPath a la valeur null. Pour corriger cette erreur, remplacez la valeur keyPath par une entrée valide dans la table Registry.<br/>                                                                                                                                                                                                     |
| Le composant Component3 s’installe dans le profil utilisateur. Sa clé de Registre keyPath doit être sous HKCU.                                      | Component3 a le bit RegistryKeyPath défini dans la colonne attributs de la [table de composants](component-table.md) , mais la racine de l’entrée de Registre spécifiée dans la colonne racine de la table du Registre spécifie **HKEY \_ local \_ machine** au lieu de **HKEY \_ Current \_ User**. Pour corriger cette erreur, utilisez une entrée de Registre valide sous **HKEY \_ local \_ machine** comme chemin d’accès au keyPath pour ce composant ou remplacez la valeur de la colonne racine de la [table du Registre](registry-table.md) par-1 ou 1.<br/>                                                                  |
| L’entrée de Registre keyPath pour le composant Component4 n’existe pas.                                                                 | Component4 a le bit RegistryKeyPath défini dans la colonne attributs de la [table des composants](component-table.md) , mais l’entrée dans la colonne keyPath n’existe pas dans la [table du registre](registry-table.md). Pour corriger cette erreur, ajoutez une entrée pour Reg4 à la table de Registre qui est sous **HKEY \_ Current \_ User**.<br/>                                                                                                                                                                                                                                      |
| L’entrée de Registre Reg5 est définie comme le chemin d’accès du composant Component5, mais cette entrée de Registre n’appartient pas à Component5.      | L’entrée de Registre référencée dans la colonne keyPath du composant a été trouvée et se trouve sous l’arborescence HKCU, mais la colonne Component de l’entrée de Registre \_ ne fait pas référence au même composant que le keyPath. Cela signifie que l’entrée de Registre utilisée comme chemin d’accès de clé du composant est créée uniquement quand un autre composant a été installé. Pour corriger cette erreur, modifiez la valeur keyPath pour faire référence à une entrée de Registre qui appartient au composant, ou modifiez l’entrée de Registre pour qu’elle appartienne au composant en l’utilisant comme chemin d’accès de clé.<br/> |



 

[Table de répertoires](directory-table.md) (partielle)



| Répertoire | Répertoire \_ parent | DefaultDir      |
|-----------|-------------------|-----------------|
| Dir1      |                   | StartMenuFolder |
| Dir2      |                   | DesktopFolder   |
| Dir3      | Dir3              | AppData         |
| Dir4      | Dir3              | SubDir          |



 

[Table des composants](component-table.md) (partielle)



| Composant  | Répertoire\_ | Attributs | KeyPath |
|------------|-------------|------------|---------|
| Composant1 | Dir1        | 0          | Fichier1   |
| Component2 | Dir2        | 4          |         |
| Component3 | Dir3        | 4          | Reg3    |
| Component4 | Dir4        | 4          | Reg4    |
| Component5 | Dir5        | 4          | Reg5    |



 

[Table du Registre](registry-table.md) (partielle)



| Registre | Root | Valeur | Composant\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




