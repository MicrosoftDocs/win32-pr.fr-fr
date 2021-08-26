---
title: Texte de description du point de restauration
description: Quand une application appelle la fonction SRSetRestorePoint, elle peut fournir n’importe quel texte comme description pour le point de restauration. Toutefois, le tableau suivant indique le texte de description recommandé.
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd785d143d3eed243e5d80ec261f121817db6187013f70b6f6cc6be0b1c2b790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111248"
---
# <a name="restore-point-description-text"></a>Texte de description du point de restauration

Quand une application appelle la fonction [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) , elle peut fournir n’importe quel texte comme description pour le point de restauration. Toutefois, le tableau suivant indique le texte de description recommandé.



| Modification du système                            | Type de point de restauration      | Description            |
|------------------------------------------------|-------------------------|------------------------|
| Installation d’application                       | installation de l’APPLICATION \_    | *Appname* installé    |
| Modification de l’application (ajout/suppression de fonctionnalités) | MODIFIER les \_ paramètres        | *Appname* configuré   |
| Suppression de l’application                            | désinstallation de l’APPLICATION \_  | *Appname* supprimé      |
| Installation du pilote de périphérique                     | \_installation du pilote de périphérique \_ | *Nom_pilote* installé |



 

les programmes d’installation, tels que Windows Installer et InstallShield, utilisent les conventions suivantes pour le texte de description :

-   Le nom du produit suit le verbe ; par exemple, l’installation de *appname*.
-   Le nom du produit peut être utilisé seul (*appname*) ou le nom du produit et le nom de la société peuvent tous les deux être utilisés (*MyCompany AppName*).

 

 




