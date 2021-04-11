---
description: Les boîtes de dialogue sont spécifiées dans la colonne boîte de dialogue de la table boîte de dialogue. Pour plus d’informations sur l’ajout d’une boîte de dialogue ou d’un tableau blanc à une interface utilisateur, consultez Utilisation de l’interface utilisateur.
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: Boîtes de dialogue (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5695a8d936d0933983407ba52a531ea839137c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203589"
---
# <a name="dialog-boxes-windows-installer"></a>Boîtes de dialogue (Windows Installer)

Les boîtes de dialogue sont spécifiées dans la colonne boîte de dialogue de la [table boîte de dialogue](dialog-table.md). Pour plus d’informations sur l’ajout d’une boîte de dialogue ou d’un tableau blanc à une interface utilisateur, consultez [utilisation de l’interface utilisateur](using-the-user-interface.md).

## <a name="reserved-dialog-box-names"></a>Noms de boîte de dialogue réservés

Les noms de boîte de dialogue suivants sont réservés par Windows Installer et ne doivent pas être utilisés pour les boîtes de dialogue personnalisées créées par l’utilisateur. Le programme d’installation requiert que ces boîtes de dialogue soient listées dans la [table de boîte de dialogue](dialog-table.md) en utilisant les noms réservés suivants. Chaque boîte de dialogue et chaque nom ne peuvent être listés qu’une seule fois. Les développeurs doivent créer ces boîtes de dialogue dans l’interface utilisateur. Pour plus d’informations sur l’aperçu des boîtes de dialogue, consultez [importation de l’interface utilisateur](importing-the-user-interface.md).



| Nom de la boîte de dialogue                                      | Brève description de la boîte de dialogue                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Boîte de dialogue FilesInUse](filesinuse-dialog.md)           | Avertit l’utilisateur des processus qui remplacent ou suppriment des fichiers.                                                                                                                 |
| [Boîte de dialogue FirstRun](firstrun-dialog.md)               | Collecte le nom d’utilisateur, le nom de la société et l’ID du produit.                                                                                                                       |
| [Boîte de dialogue MsiRMFilesInUse](msirmfilesinuse-dialog.md) | Avertit l’utilisateur des processus qui remplacent ou suppriment des fichiers et donne à l’utilisateur la possibilité d’utiliser le [Gestionnaire de redémarrage](/windows/desktop/RstMgr/restart-manager-portal) pour fermer et redémarrer les applications. |



 

## <a name="required-dialog-boxes"></a>Boîtes de dialogue obligatoires

Au cours de l’installation, certains événements entraînent l’Windows Installer à vérifier les tables de séquence de l' [interface utilisateur](using-a-sequence-table.md) dans le package et à afficher la boîte de dialogue spécifiée. Par exemple, dans le cas d’une erreur irrécupérable, Windows Installer affiche la boîte de dialogue qui est indiquée avec un numéro de séquence-3 dans la table séquence de l’interface utilisateur, quelle que soit la boîte de dialogue nommée dans la [table boîte de dialogue](dialog-table.md). Le tableau suivant répertorie les événements spécifiques et leur numéro de séquence correspondant dans la table de séquence de l’interface utilisateur :



| Type d’événement                        | Numéro de séquence de la table de séquence de l’interface utilisateur | Description de la boîte de dialogue                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [Erreur irrécupérable](fatalerror-dialog.md) | -3                                            | L’installation a été interrompue par une erreur irrécupérable.      |
| [Fermeture de l’utilisateur](userexit-dialog.md)     | -2                                            | L’installation a été arrêtée à la demande de l’utilisateur. |
| [Quitter](exit-dialog.md)              | -1                                            | L’installation s’est terminée avec succès.               |



 

En outre, l’auteur du package doit créer une boîte de dialogue générique pour afficher Windows Installer des messages d' [erreur](error-dialog.md) . Cette boîte de dialogue peut être nommée tout, mais ce nom doit être spécifié dans la propriété **ErrorDialog** .

## <a name="typical-dialog-boxes"></a>Boîtes de dialogue classiques

Les boîtes de dialogue suivantes sont facultatives et sont généralement incluses dans l’interface utilisateur créée d’un package d’installation. Ces boîtes de dialogue sont typiques de la plupart des [assistants de l’interface utilisateur](user-interface-wizard-behavior.md) pour l’installation de fichiers. Ces boîtes de dialogue peuvent avoir n’importe quel nom dans la table de boîtes de dialogue. Les noms indiqués sont uniquement recommandés pour plus de clarté et peuvent être modifiés en fonction des besoins. Par exemple, deux boîtes de dialogue **LicenseAgreement** personnalisées peuvent être utilisées dans le package et se différencier dans la table de boîtes de dialogue par les noms ProfessionalLicenseAgreement et LimitedLicenseAgreement.



| Type de boîte de dialogue                                             | Brève description de la boîte de dialogue                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [Boîte de dialogue DiskCost](diskcost-dialog.md)                  | Indique que l’espace disque est insuffisant pour l’installation. |
| [Boîte de dialogue Parcourir](browse-dialog.md)                      | Permet à l’utilisateur de sélectionner un répertoire.                     |
| [Boîte de dialogue annuler](cancel-dialog.md)                      | Confirme une demande d’arrêt de l’installation.       |
| [Boîte de dialogue contrat de licence](licenseagreement-dialog.md) | Zone modale affichant le contrat de licence.             |
| [Boîte de dialogue sélection](selection-dialog.md)                | Zone modale permettant à l’utilisateur de sélectionner des éléments.            |



 

 

 
