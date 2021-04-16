---
title: Acquisition de licence non silencieuse
description: Acquisition de licence non silencieuse
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows Media Format SDK, acquisition de licence non silencieuse
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), acquisition de licence non silencieuse
- DRM (gestion des droits numériques), acquisition de licence non silencieuse
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- API étendues du client DRM, acquisition de licence non silencieuse
- API étendues clientes, acquisition de licence non silencieuse
- acquisition de licence non silencieuse
- licences, acquisition de licence non silencieuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507427"
---
# <a name="non-silent-license-acquisition"></a>Acquisition de licence non silencieuse

L’acquisition de licence non silencieuse permet au fournisseur de licences d’interagir avec l’utilisateur final par le biais d’une page Web, comme étape intermédiaire du processus d’acquisition de licence. Une acquisition de licence non silencieuse est lancée en réponse à un utilisateur qui tente d’accéder à du contenu protégé.

Pour effectuer une acquisition de licence non silencieuse, procédez comme suit :

1.  Appelez la méthode [**IWMDRMLicenseManagement :: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) . Transmettez l’en-tête DRM du fichier protégé en tant que paramètre *bstrHeaderData* . Spécifiez les droits que vous souhaitez accorder à la licence dans le paramètre *bstrActions* . Enfin, définissez le paramètre *dwFlags* sur WMDRM \_ Acquire \_ License No \_ Silent.
2.  Événements d’interruption de l’interface **IWMDRMLicenseManagement** . Quand vous recevez l’événement **MEWMDRMLicenseAcquisitionCompleted** , obtenez sa valeur associée en appelant **IMFMediaEvent :: GetValue**. La valeur doit être de type VT \_ inconnu, un pointeur vers une interface **IUnknown** .
3.  Appelez la méthode **QueryInterface** de l’interface **IUnknown** Récupérée à l’étape 2 pour obtenir l’interface [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) .
4.  Appelez [**IWMDRMNonSilentLicenseAquisition :: GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) pour récupérer la demande de licence. Appelez également [**IWMDRMNonSilentLicenseAquisition :: getURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) si vous n’avez pas déjà l’URL du serveur de licences.
5.  Envoyez la stimulation à la page Web spécifiée par l’URL.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Acquisition de licences**](acquiring-licenses.md)
</dt> <dt>

[**Utilisation du modèle d’événement Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




