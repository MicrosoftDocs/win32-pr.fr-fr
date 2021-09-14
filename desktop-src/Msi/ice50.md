---
description: ICE50 vérifie que les icônes de raccourci sont spécifiées pour s’afficher correctement et correspondent à l’extension du fichier cible.
ms.assetid: 19288c87-fddb-46c9-8145-59e1b870a261
title: ICE50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de88dda0dd1cdd18a10a35c32ef612acb75c871e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021541"
---
# <a name="ice50"></a>ICE50

ICE50 vérifie que les icônes de raccourci sont spécifiées pour s’afficher correctement et correspondent à l’extension du fichier cible.

## <a name="result"></a>Résultats

ICE50 publie un message d’erreur si l’extension de l’icône et les fichiers cibles ne correspondent pas. ICE50 publie un avertissement si les icônes sont stockées dans des fichiers qui n’ont pas d’extension .exe ou. ico.

## <a name="example"></a>Exemple

ICE50 signale l’erreur suivante pour l’exemple indiqué.



| Erreur ou avertissement ICE50                                                                                                              | Description                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| L’extension de l’icône « Icon2. dat » pour le raccourci « Shortcut2 » ne correspond pas à l’extension du fichier de clé pour le composant « COMPONENT2 ». | Si les extensions de l’icône et du fichier cible ne correspondent pas, le menu contextuel est incorrect lorsque le composant est publié. Pour corriger cette erreur, renommez l’icône pour qu’elle corresponde à l’extension du fichier cible.<br/> |
| L’extension de l’icône' Icon1.bat 'pour le raccourci’Shortcut1 'n’est pas "exe" ou "ico". L’icône ne s’affiche pas correctement.         | Toutes les versions du shell n’affichent pas correctement les icônes stockées dans les fichiers qui n’ont pas d’extension « exe » ou « ico ». Pour résoudre cet avertissement, renommez l’icône avec l’extension « exe » ou « ico ».<br/>                                      |



 

[Table de fichiers](file-table.md) (partielle)



| Fichier  | FileName  |
|-------|-----------|
| Fichier1 | File1.bat |
| Fichier2 | File2.pl  |



 

[Table des fonctionnalités](feature-table.md) (partielle)



| Fonctionnalité  |
|----------|
| Feature1 |



 

[Table des composants](component-table.md) (partielle)



| Composant  | KeyPath |
|------------|---------|
| Composant1 | Fichier1   |
| Component2 | Fichier2   |



 

[Table d’icônes](icon-table.md)



| Nom      | Données            |
|-----------|-----------------|
| Icon1.bat | \[Binary Data\] |
| Icon2. dat | \[Binary Data\] |



 

[Table de raccourcis](shortcut-table.md) (partielle)



| Raccourci  | Composant  | Cible   | Icône\_    |
|-----------|------------|----------|-----------|
| Shortcut1 | Composant1 | Feature1 | Icon1.bat |
| Shortcut2 | Component2 | Feature1 | Icon2. dat |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




