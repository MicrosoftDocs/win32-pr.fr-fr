---
title: Utilisation de Moniteur réseau pour afficher les fichiers ETL
description: Moniteur réseau 3,3 permet aux utilisateurs d’analyser, de filtrer et d’afficher un fichier ETL (à l’aide de Windows Vista ou version ultérieure).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "103953289"
---
# <a name="using-network-monitor-to-view-etl-files"></a>Utilisation de Moniteur réseau pour afficher les fichiers ETL

[Moniteur réseau 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) permet aux utilisateurs d’analyser, de filtrer et d’afficher un fichier ETL (à l’aide de Windows Vista ou version ultérieure). (Si vous utilisez Moniteur réseau 3,2, vous devrez télécharger et installer des analyseurs supplémentaires à partir de [CodePlex](https://www.codeplex.com/NMParsers) pour afficher les événements de suivi réseau.)

Les fichiers ETL corrélés regroupent les événements pertinents ensemble. Le défilement ci-dessous montre un fichier corrélé ouvert dans Moniteur réseau, avec la conversation activée.

![Capture d’écran montrant le Moniteur réseau, avec les événements corrélés mis en surbrillance dans la fenêtre de gauche et les UTEvent mis en surbrillance dans la liste déroulante.](images/ut-netmon1.png)

Les événements corrélés sont regroupés par activité dans le volet gauche. Vous pouvez sélectionner un événement dans le volet Résumé des frames, puis cliquer avec le bouton droit pour sélectionner la conversation au niveau de l’événement réseau. Une activité associée s’affiche dans le volet gauche.

La sélection d’une activité particulière dans le volet gauche et son développement affichent la liste des fournisseurs pour les événements corrélés.

![Capture d’écran montrant le Moniteur réseau avec une activité sélectionnée dans le volet gauche et des événements correspondant à cet événement dans le volet droit.](images/ut-netmon2.png)

Lorsque vous sélectionnez un fournisseur spécifique dans le volet gauche, une liste d’événements spécifiques à ce fournisseur et à cette activité s’affiche dans le volet Résumé des frames.

![Capture d’écran montrant un fournisseur spécifique sélectionné dans le volet gauche et une liste d’événements spécifiques au fournisseur mis en surbrillance dans le volet supérieur droit.](images/ut-netmon3.png)

Les filtres peuvent être appliqués dans Moniteur réseau pour faciliter l’affichage et la recherche des événements ou des paquets appropriés. Par exemple, vous pouvez appliquer un filtre aux événements d’erreur sélectionnés (par exemple, **UTEvent. Header. Descriptor. Level = = 2**) pour les afficher dans une certaine couleur.

![Capture d’écran montrant la boîte de dialogue Modifier le filtre de couleurs.](images/ut-netmon4.png)

Des filtres peuvent également être appliqués pour marquer des fournisseurs différents dans des couleurs différentes afin de faciliter l’affichage des résultats.

![Capture d’écran montrant un exemple de différents fournisseurs marqués dans des couleurs différentes.](images/ut-netmon5.png)

Pour appliquer un filtre, cliquez sur **ColorFilters** dans le menu **filtres** .

Le tableau suivant présente quelques exemples de filtres utiles.



| Filtrer                                                                        | Description                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| UTEvent. Header. Descriptor. Level = = 2                                          | Filtre uniquement les événements d’erreur.                                        |
| UTEvent. Header. Descriptor. Level = = 3                                          | Filtre uniquement les événements d’avertissement.                                      |
| UTEvent.Header.Descriptor.Id = = 2001                                          | Filtre uniquement les événements avec l’ID d’événement 2001.                           |
| \_MICROSOFTWINDOWSWLANAUTOCONFIG WLAN                                          | Filtre uniquement les événements du service WLAN.                            |
| N802 \_ MicrosoftWindowsNWiFi                                                   | Filtre uniquement les événements du pilote Wi-Fi natif.                  |
| WLAN \_ MICROSOFTWINDOWSWLANAUTOCONFIG et UTEvent.Header.Descriptor.ID = = 2001 | Filtre uniquement les événements avec l’ID d’événement 2001 émis à partir du service WLAN. |



 

 

 




