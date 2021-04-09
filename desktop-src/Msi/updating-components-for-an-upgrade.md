---
description: Par défaut, les utilisateurs du produit fictif MNP2000 ne doivent jamais utiliser de fichiers mis à niveau, comme Baseba01.txt.
ms.assetid: 5aca7ff5-c09f-4d00-b319-2b89550686ab
title: Mise à jour des composants d’une mise à niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 920bc955d3d3615941ef03ec885ca8871f79dc86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952725"
---
# <a name="updating-components-for-an-upgrade"></a>Mise à jour des composants d’une mise à niveau

Par défaut, les utilisateurs du produit fictif MNP2000 ne doivent jamais utiliser de fichiers mis à niveau, comme Baseba01.txt. Par conséquent, les fichiers mis à jour sont par définition incompatibles avec le produit d’origine et les composants de Windows Installer, tels que baseball, qui contiennent ces fichiers doivent se voir attribuer de nouveaux codes de composant. De nouveaux fichiers, tels que Opera01.txt, sont introduits dans le cadre d’un nouveau composant avec un code de composant unique. Étant donné que le produit et la mise à niveau d’origine utilisent le même composant bloc-notes, le code du composant de ce composant n’est pas modifié. Pour plus d’informations sur le moment où le code du composant doit être modifié, consultez [modification du code du composant](changing-the-component-code.md).

Utilisez Orca ou un autre éditeur de base de données pour entrer les données suivantes dans la [table des composants](component-table.md) de MNP2001.msi. Ne réutilisez pas les GUID indiqués ci-dessous dans la colonne ComponentId de votre exemple.

[Table des composants](component-table.md)



| Composant  | ComponentId                            | Répertoire\_ | Attributs | Condition | KeyPath      |
|------------|----------------------------------------|-------------|------------|-----------|--------------|
| Chaussures   | {2951190A-6AF8-4D7F-AA16-D256405C277A} | SPORTDIR    | 2          |           | Baseba01.txt |
| Isole | {E1AAB6B0-FEC6-4F18-B765-3B05A81CEACB} | SPORTDIR    | 2          |           | Basket01.txt |
| Concert    | {C28C5064-AA84-4431-AC69-FC1321DF18AF} | ARTSDIR     | 2          |           | Concer01.txt |
| Jongl      | {1AC2B14D-D5F4-4642-9F7A-EE81BF59B3E2} | ARTSDIR     | 2          |           | Dance01.txt  |
| Opera      | {C2DABF7E-1EF6-458D-84B1-AAC1127CED26} | ARTSDIR     | 2          |           | Opera01.txt  |
| Terrain   | {92AA30F4-7AC5-4DFA-801E-988CF3DAA4DC} | SPORTDIR    | 2          |           | Footba01.txt |
| Aide       | {AD10EB50-33C1-11D3-91D6-00C04FD70856} | NOTEPADDIR  | 2          |           | Help.txt     |
| Janvier    | {E90CD0E6-ED8D-4F88-B000-27BD2B482C6C} | MONDIR      | 2          |           | Janua01.txt  |
| NewYears   | {1EEF8C53-F7C0-405C-8FE3-2B0FE54B0114} | HOLDIR      | 2          |           | NewYea01.txt |
| Souvenir   | {BA81ACF7-4D43-424F-93B0-8845A2DF1C02} | HOLDIR      | 2          |           | Memori01.txt |
| Bloc-notes    | {19BED232-30AB-11D3-91D3-00C04FD70856} | NOTEPADDIR  | 2          |           | Redpark.exe  |



 

[Continuer](updating-features-for-an-upgrade.md)

 

 



