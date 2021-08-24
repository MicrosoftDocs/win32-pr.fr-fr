---
description: Le chemin d’accès logique permet d’organiser les composants gérés par un writer en groupes bien définis.
ms.assetid: 663c8ca9-8f5b-48bd-af2d-b2d90de9e492
title: Chemin logique des composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ce4feeeb2147a7be736547eb69cbbb1a254c5940b18e904bc3be3290a2c79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767749"
---
# <a name="logical-pathing-of-components"></a>Chemin logique des composants

Le [*chemin d’accès logique*](vssgloss-l.md) permet d’organiser les composants gérés par un writer en groupes bien définis.

Le chemin d’accès logique est analogue à la structure du chemin d’accès de fichier traditionnel, à l’aide de la barre oblique inverse « \\ » pour séparer les éléments dans le chemin d’accès. Contrairement aux chemins d’accès de fichier, la racine d’un chemin d’accès logique est **null** au lieu de « \\ ».

Le chemin d’accès logique est exprimé sous la forme d’une chaîne terminée par le caractère **null**, et il n’existe aucune autre restriction sur les caractères que le chemin d’accès peut contenir.

L’utilisation la plus importante du chemin logique consiste à définir des [*jeux de composants*](vssgloss-c.md), où l' [*inclusion explicite*](vssgloss-e.md) d’un composant dans une opération de sauvegarde ou de restauration d’un composant sélectionnable nécessite l’inclusion d’un certain nombre d’autres composants (sous-[*composant*](vssgloss-s.md)). Le chemin d’accès logique du composant de définition d’un jeu de composants est un parent des chemins logiques de ses sous-composants et :

-   Les sous-composants doivent partager en tant que chemin d’accès racine le chemin d’accès logique du composant sélectionnable qui définit le jeu de composants.
-   Le chemin d’accès racine **null** est valide.
-   Le nom du composant sélectionnable de définition doit être le premier élément de chemin d’accès logique après le chemin d’accès racine pour chaque sous-composant non sélectionnable du jeu de composants.
-   Les ensembles de composants peuvent être imbriqués.
-   La combinaison du chemin d’accès logique et du nom du composant doit être unique pour toutes les instances d’une [*classe de writer*](vssgloss-w.md).

L’exemple hypothétique d’un *MyWriter* d’écriture avec une structure de chemin logique définie ci-dessous illustre le chemin logique.



| Nom du composant | Chemin logique            | Sélectionnable pour la sauvegarde |
|----------------|-------------------------|-----------------------|
| Exécut  | ""                      | N                     |
| "ConfigFiles"  | Exécut           | N                     |
| "LicenseInfo"  | ""                      | O                     |
| « Security »     | ""                      | O                     |
| UserInfo     | « Security »              | N                     |
| EUR.1 | « Security »              | N                     |
| "writerData"   | ""                      | O                     |
| Jeu1         | "writerData"            | N                     |
| Janvier          | « writerData \\ Set1 »      | N                     |
| Decembre          | « writerData \\ Set1 »      | N                     |
| Set2         | "writerData"            | N                     |
| Janvier          | « writerData \\ Set2 »      | N                     |
| Decembre          | « writerData \\ Set2 »      | N                     |
| Demande        | « writerData \\ QueryLogs » | N                     |
| Syntaxe        | "writerData"            | O                     |
| Janvier          | « utilisation de writerData \\ »     | N                     |
| Decembre          | « utilisation de writerData \\ »     | N                     |



 

Notez que les composants « exécutables » et « ConfigFile » ont une relation parent-enfant, mais que les deux ne peuvent pas être sélectionnés. Par conséquent, ils ne forment pas un jeu de composants. Chaque fois que l’enregistreur *MyWriter* est sauvegardé ou restauré, ces deux composants doivent être [*inclus explicitement*](vssgloss-e.md) dans l’opération.

Le composant « LicenseInfo » peut être sélectionné, ni ancêtre, ni descendant. Il peut être inclus explicitement, ou non, dans une opération de sauvegarde ou de restauration, à la discrétion du demandeur.

Le composant « sécurité » définit un ensemble de composants simple, qui ne contient aucun jeu de composants sous-jacents.

Le composant « writerData » définit un jeu de composants, qui contient une collection complexe de composants avec plusieurs hiérarchies de chemins logiques bien définies sous celui-ci.

Un sous-composant, « utilisation », est sélectionnable et définit un jeu de composants.

Plusieurs composants ont le même nom et sont distingués par leurs chemins logiques. Les instances des composants non sélectionnables « DEC » et « Jan » existent sous les composants non sélectionnables « set1 » et « SET2 » et sous le sous-composant sélectionnable « utilisation ».

Si le composant « writerData » est inclus explicitement dans une sauvegarde ou une restauration, tous ses sous-composants, y compris ceux de l’ensemble de composants imbriqués définis par « usage », sont [*implicitement inclus*](vssgloss-e.md)[*implicitement dans l'*](vssgloss-i.md) opération.

Si le jeu de composants défini par « writerData » n’est pas explicitement inclus dans une sauvegarde ou une restauration, les composants « Set1 », « Set2 » et « QueryLogs » (et leurs instances de sous-composants « DEC » et « Jan ») ne sont pas inclus implicitement dans l’opération de sauvegarde ou de restauration.

Toutefois, même si « writerData » n’est pas inclus dans l’opération, le composant « utilisation » est toujours sélectionnable et peut toujours être inclus explicitement dans une opération de sauvegarde ou de restauration. Si c’est le cas, ses sous-composants « Jan » et « DEC » seront inclus implicitement.

Autres points dignes de la note :

-   Les composants sélectionnables « LicenseInfo » et « writerData » et les « exécutables » de composants non sélectionnables se trouvent tous au même niveau dans la hiérarchie des chemins d’accès logiques de *MyWriter*: tous ont le même chemin logique **null** ou «», le chemin logique racine.
-   L’utilisation du composant sélectionnable ne doit jamais être explicitement incluse dans une sauvegarde, si son parent sélectionnable (« writerData ») est explicitement inclus dans une opération de sauvegarde ou de restauration.
-   Les composants qui définissent des ensembles de composants peuvent exister simplement pour des raisons organisationnelles. Par exemple, le composant « writerData » ou « usage », ou les deux, peut être vide. autrement dit, aucun [*jeu de fichiers*](vssgloss-f.md) n’a été ajouté à ces derniers à l’aide de la méthode [**IVssCreateWriterMetadata :: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata :: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) ou [**IVssCreateWriterMetadata :: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) . Les composants définissent toujours un jeu de composants.

 

 



