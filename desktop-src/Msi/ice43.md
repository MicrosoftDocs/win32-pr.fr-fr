---
description: ICE43 vérifie que les raccourcis qui ne font pas référence à une fonctionnalité en tant que cible (raccourcis non publiés) se trouvent dans des composants dont l’entrée de Registre HKCU est le chemin de leur clé.
ms.assetid: 7e58e303-e512-4707-a0bf-2095ec8ec502
title: ICE43
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c69af661b22d851b50a74bdffb9534b1e269dde4e428440882ee2d52813a68c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635205"
---
# <a name="ice43"></a>ICE43

ICE43 vérifie que les raccourcis qui ne font pas référence à une fonctionnalité en tant que cible (raccourcis non publiés) se trouvent dans des composants dont l’entrée de Registre HKCU est le chemin de leur clé.

## <a name="result"></a>Résultat

ICE43 publie un message d’erreur si un raccourci non publié se trouve dans un composant qui n’a pas d’entrée de Registre HKCU comme chemin d’accès de clé.

## <a name="example"></a>Exemple

ICE43 signale les erreurs suivantes pour l’exemple indiqué.



| Erreur ICE43                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Le composant Composant1 a des raccourcis non publiés. Il doit utiliser une clé de Registre sous HKCU comme keyPath, et non un fichier.                    | La colonne Attributes de Composant1 a la valeur 0, ce qui signifie que le composant utilise un fichier comme keyPath. Cela entraîne l’installation de raccourcis non publiés dans ce composant pour le premier utilisateur sur l’ordinateur uniquement. Les utilisateurs qui installent le composant ultérieurement ne voient pas les raccourcis, car le composant s’affiche sur le programme d’installation comme déjà existant sur l’ordinateur. Pour corriger cette erreur, définissez le bit RegistryKeyPath des attributs pour basculer le composant vers une entrée du Registre, puis modifiez la valeur keyPath en spécifiant une entrée valide dans la table Registry.<br/> |
| Le composant COMPONENT2 a des raccourcis non publiés. Il doit utiliser une clé de Registre sous HKCU comme keyPath. KeyPath est actuellement null. | La colonne attributs est définie pour utiliser le registre, mais le keyPath a la valeur null. Le keyPath doit faire référence à une entrée dans la table du Registre. Pour corriger cette erreur, remplacez la valeur keyPath par une entrée valide dans la table Registry.<br/>                                                                                                                                                                                                                                                                                                                               |
| Le composant Component3 a des raccourcis non publiés. Sa clé de Registre keyPath doit être sous HKCU.                                       | La colonne attributs est définie pour utiliser le registre, mais l’entrée de Registre référencée n’est pas sous HKCU. Pour corriger cette erreur, vous pouvez soit basculer vers une autre entrée de registre que le chemin d’accès de clé de ce composant, soit modifier la valeur racine de l’entrée de registre en-1 ou 1.<br/>                                                                                                                                                                                                                                                                             |
| L’entrée de Registre keyPath pour le composant Component4 n’existe pas.                                                                     | L’entrée de Registre référencée dans la colonne keyPath du composant ne figure pas dans la table du Registre. Pour corriger cette erreur, créez une entrée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| L’entrée de Registre Reg5 est définie comme le chemin d’accès du composant Component5, mais cette entrée de Registre n’appartient pas à Component5.          | Une entrée de Registre est référencée dans la colonne keyPath du composant qui se trouve sous l’arborescence HKCU, mais la colonne Component de l’entrée de Registre \_ ne fait pas référence au même composant que celui qui l’a indiquée comme keyPath. Cela signifie que l’entrée de Registre utilisée comme chemin d’accès de clé du composant est créée uniquement si un autre composant a été installé. Pour corriger cette erreur, modifiez la valeur keyPath pour qu’elle fasse référence à une entrée de Registre qui appartient au composant ou modifiez l’entrée du registre de façon à ce qu’elle appartienne au composant en l’utilisant comme chemin d’accès de clé.<br/>   |



 

[Table des composants](component-table.md) (partielle)



| Composant  | Attributs | KeyPath |
|------------|------------|---------|
| Composant1 | 0          | Fichier1   |
| Component2 | 4          |         |
| Component3 | 4          | Reg3    |
| Component4 | 4          | Reg4    |
| Component5 | 4          | Reg5    |



 

[Table du Registre](registry-table.md) (partielle)



| Registre | Root | Valeur | Composant\_ |
|----------|------|-------|-------------|
| Reg3     | 2    |       | Component3  |
| Reg5     | 0    |       | Component4  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




