---
title: Utilisation du modèle d’événement Media Foundation
description: Utilisation du modèle d’événement Media Foundation
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- Windows Media Format SDK, DRM Media Foundation Event Model
- Windows Media Format SDK, Media Foundation Event Model
- Windows Kit de développement logiciel (SDK) Media format, modèle d’événement DRM
- gestion des droits numériques (DRM), Media Foundation modèle d’événement
- DRM (gestion des droits numériques), Media Foundation modèle d’événement
- gestion des droits numériques (DRM), modèle d’événement
- DRM (gestion des droits numériques), modèle d’événement
- gestion des droits numériques (DRM), interface IWMDRMEventGenerator
- DRM (gestion des droits numériques), interface IWMDRMEventGenerator
- Media Foundation
- IWMDRMEventGenerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32c68d1d22c6b3d95c34efb5a919c82ecf5dd3755943e96f2507ae9f3391f48
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707389"
---
# <a name="using-the-media-foundation-event-model"></a>Utilisation du modèle d’événement Media Foundation

les méthodes asynchrones prises en charge par le Windows les api étendues du Client Media DRM utilisent le même modèle d’événement que celui utilisé par le kit de développement logiciel (SDK) Media Foundation. Chaque objet qui prend en charge des méthodes asynchrones implémente l’interface [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) , qui peut être utilisée pour récupérer un événement lorsqu’une opération asynchrone est terminée.

L’interface **IWMDRMEventGenerator** hérite de l’interface **IMFMediaEventGenerator** , qui est décrite dans la documentation du kit de développement logiciel (SDK) Media Foundation.

L’exemple de code de l’exemple de l' [individualisation DRM](drm-individualization-example.md) utilise la méthode **IMFMediaEventGenerator :: GetEvent** pour récupérer les événements de la file d’attente un par un. L’utilisation de **GetEvent** est plus simple que l’utilisation de **IMFMediaEventGenerator :: BeginGetEvent** et **IMFMediaEventGenerator :: EndGetEvent** avec un rappel, ce qui rend les exemples de code plus faciles à comprendre. Que vous utilisiez **GetEvent** dans votre code ou implémentiez **IMFAsyncCallback** et que vous utilisiez **BeginGetEvent** et **EndGetEvent**, la logique de gestion de l’événement après sa réception est la même.

Plusieurs méthodes asynchrones génèrent des événements qui contiennent des références à des objets qui peuvent être utilisés pour obtenir des informations d’État plus détaillées. Dans ces cas, l’événement généré a un pointeur **IUnknown** comme valeur, qui peut être interrogé pour récupérer l’interface d’État. La liste suivante résume les relations entre les appels asynchrones, les événements générés et d’autres interfaces.

-   La méthode [**IWMDRMLicenseManagement :: BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) génère des événements **MEWMDRMLicenseBackupProgress** avec les interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) associées.
-   La méthode [**IWMDRMLicenseManagement :: RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) génère des événements **MEWMDRMLicenseRestoreProgress** avec les interfaces [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) associées.
-   La méthode [**IWMDRMSecurity ::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , lorsqu’elle est utilisée pour effectuer une individualisation, génère des événements **MEWMDRMIndividualizationProgress** avec les interfaces [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) associées.
-   La méthode [**IWMDRMLicenseManagement :: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , lorsqu’elle est utilisée pour préparer des données pour une acquisition de licence non silencieuse, génère un événement **MEWMDRMLicenseAcquisitionCompleted** avec une interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) associée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple d’individualisation DRM**](drm-individualization-example.md)
</dt> <dt>

[**Prise en main**](drm-getting-started.md)
</dt> <dt>

[Documentation du kit de développement logiciel Media Foundation](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




