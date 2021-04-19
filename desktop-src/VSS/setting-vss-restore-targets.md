---
description: L’interface IVssComponent permet à un enregistreur d’ajuster précisément la manière dont les fichiers sont restaurés composant par composant.
ms.assetid: 362c6f44-ca67-4043-8d2c-4e46b5c8edd3
title: Définition des cibles de restauration VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e8815e552db518c447bd63b9f02ba9228850384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544795"
---
# <a name="setting-vss-restore-targets"></a>Définition des cibles de restauration VSS

L’interface [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) permet à un enregistreur d’ajuster précisément la manière dont les fichiers sont restaurés composant par composant.

Étant donné qu’il est possible que la configuration du système pendant la restauration soit autre que celle prévue lors de la sauvegarde, le mécanisme de la cible de restauration est fourni.

Elle permet aux rédacteurs d’appeler [**IVssComponent :: SetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setrestoretarget) pour modifier la façon dont les composants qui sont [*explicitement inclus*](vssgloss-e.md) dans le document des composants de sauvegarde sont restaurés. Cela modifie également le mécanisme de restauration utilisé sur les composants qui sont [*implicitement inclus*](vssgloss-i.md).

La restauration de fichiers qui a lieu lors d’un redémarrage du système (sous les valeurs d’énumération VSS [**\_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) VSS \_ RME \_ Restore \_ au \_ redémarrage et VSS \_ RME \_ Restore \_ au \_ redémarrage \_ si \_ ne peut pas \_ être remplacé) ne peut pas être affectée par les cibles de restauration, car il n’existe aucun service VSS en cours d’exécution lorsque **MoveFileEx** copie les fichiers à leur emplacement final.

De même, \_ \_ les restaurations personnalisées de VSS RME peuvent être affectées, car chaque restauration personnalisée est spécifique à un writer donné et peut choisir de respecter ou d’ignorer les cibles de restauration.

Les demandeurs et les enregistreurs peuvent utiliser [**IVssComponent :: GetRestoreTarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getrestoretarget) pour vérifier la cible de restauration d’un jeu de composants.

[**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent) prend en charge les cibles de restauration suivantes, qui peuvent être définies sur un composant défini à l’aide d’un jeu de composants :

-   \_ \_ version d’origine de VSS RT. La méthode Restore spécifiée par l’énumération [**VSS \_ RESTOREMETHOD \_ enum**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) est respectée.
-   alternative à VSS \_ RT \_ . Les fichiers sont restaurés à un emplacement déterminé à partir d’un mappage d’emplacement de remplacement existant. Si un mappage d’emplacement secondaire correspondant à un chemin d’accès dans un sous-composant de jeu de composants existe, restaurez-le dans un autre emplacement, si possible ; Sinon, retourne une erreur.

 

 



