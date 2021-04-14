---
description: Les programmeurs qui utilisent Windows Update Agent (WUA) commencent par ajouter une référence à Wuapi.dll à leur projet actuel (dans Visual C++, Microsoft Visual Basic ou C \# ) ou en référençant wuapi. h et Wuguid. lib dans un projet C ou C++.
ms.assetid: ec9cbb0b-b5d4-41f2-8a25-143130d08a3b
title: Windows Update le modèle objet de l’agent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5060a76c850ea9ad97e9132f661d4b64f4f4fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564921"
---
# <a name="windows-update-agent-object-model"></a>Windows Update le modèle objet de l’agent

Les programmeurs qui utilisent Windows Update Agent (WUA) commencent par ajouter une référence à Wuapi.dll à leur projet actuel (dans Visual C++, Microsoft Visual Basic ou C \# ) ou en référençant wuapi. h et Wuguid. lib dans un projet C ou C++. La première étape de l’utilisation de l’API WUA consiste à créer une instance de l’une des interfaces en créant un objet à partir de la coclasse appropriée.

L’illustration suivante décrit le modèle objet WUA. Pour plus d’informations, consultez la section «[objets WUA et tâches associées](#wua-objects-and-associated-tasks)». Pour obtenir la liste complète de toutes les interfaces WUA, consultez [interfaces](interfaces.md).

![modèle objet de l’agent Windows Update](images/wua-object-model.png)

## <a name="wua-objects-and-associated-tasks"></a>Objets WUA et tâches associées

Le tableau suivant répertorie les objets WUA et les tâches typiques associées aux objets WUA.



| Object                                                                | Description                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AutomaticUpdates**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)                         | Commencez, interrompez ou reprenez Mises à jour automatiques.                                                                                                                                                                                                  |
| [**AutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)         | Récupérer ou définir le jour et l’heure d’installation des mises à jour. Spécifiez comment les utilisateurs sont avertis d’un événement Mises à jour automatiques.                                                                                                                          |
| [**Category**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)                                         | Récupérez les informations relatives à la catégorie de la mise à jour, notamment le nom, l’ID, la description, le propriétaire et le produit souhaité. Récupérer une collection de mises à jour qui appartiennent à cette catégorie. Récupère une collection de catégories parent ou enfant. |
| [**CategoryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)                     | Accédez à une collection d’objets Category.                                                                                                                                                                                                    |
| [**DownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadresult)                             | Récupérez des informations sur le résultat d’un téléchargement.                                                                                                                                                                                        |
| [**InstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult)                     | Récupérez des informations sur le résultat d’une installation ou d’une désinstallation. Déterminez si un redémarrage du système est nécessaire pour terminer l’installation ou la désinstallation.                                                                  |
| [**SearchResult**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)                                 | Récupérez des informations sur le résultat d’une recherche de catégories ou de mises à jour. Récupère une collection de catégories détectées sur l’ordinateur de destination à l’aide de la recherche. Récupère une collection de mises à jour trouvées par la recherche.                     |
| [**SystemInformation**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)                       | Récupérez des informations sur la configuration requise pour le système OEM et le redémarrage du système sur l’ordinateur de destination.                                                                                                                                        |
| [**Mise à jour**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)                                             | Récupérer la plupart des informations sur la mise à jour, y compris les mises à jour regroupées, les spécifications source, l’identité, la description, les options de désinstallation, la priorité de téléchargement, la taille et l’échéance.                                                                |
| [**UpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)                         | Accédez à une collection d’objets de mise à jour.                                                                                                                                                                                                      |
| [**UpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)                         | Démarrez un téléchargement asynchrone ou synchrone des fichiers associés aux mises à jour.                                                                                                                                            |
| [**UpdateDownloadResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadresult)                 | Récupérez des informations sur le résultat du téléchargement pour une seule mise à jour.                                                                                                                                                                       |
| [**UpdateException**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)                           | Récupère la description et le contexte d’une exception qui est levée lorsqu’une erreur de mise à jour se produit.                                                                                                                                            |
| [**UpdateExceptionCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)       | Accédez à une collection d’objets UpdateException.                                                                                                                                                                                             |
| [**UpdateHistoryEntry**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)                     | Récupérez des informations sur une mise à jour qui a été installée ou désinstallée, y compris l’application, la date et la description traitées.                                                                                                    |
| [**UpdateHistoryEntryCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection) | Accédez à une collection d’objets UpdateHistoryEntry.                                                                                                                                                                                          |
| [**UpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult)         | Récupérez des informations sur le résultat de l’installation ou de la désinstallation d’une mise à jour.                                                                                                                                                  |
| [**UpdateInstaller**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)                           | Démarrez une installation asynchrone ou synchrone ou une désinstallation d’une mise à jour. Démarrer une séquence de dialogue interactive pour guider l’utilisateur tout au long des étapes d’installation des mises à jour.                                                              |
| [**UpdateSearcher**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)                             | Recherche des mises à jour sur le serveur en fonction de critères tels que le type de mise à jour, l’ID ou la catégorie.                                                                                                                                            |
| [**UpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)                               | Démarrez une session pour rechercher, télécharger, installer ou désinstaller les mises à jour pour une application.                                                                                                                                                  |
| [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy)                                         | Récupérez et définissez les paramètres du proxy HTTP.                                                                                                                                                                                                       |



 

 

 



