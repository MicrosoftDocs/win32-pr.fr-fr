---
title: Acquisition de licence en mode silencieux
description: Acquisition de licence en mode silencieux
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows Media Format SDK, acquisition de licence en mode silencieux
- Windows Media Format SDK, licences
- gestion des droits numériques (DRM), acquisition de licence en mode silencieux
- DRM (gestion des droits numériques), acquisition de licence en mode silencieux
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- API étendues du client DRM, acquisition de licence silencieuse
- API étendues clientes, acquisition de licence silencieuse
- acquisition de licence en mode silencieux
- licences, acquisition de licence silencieuse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ef92eaf4e347e8eb30f56c1111ec5b27f1e62d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029498"
---
# <a name="silent-license-acquisition"></a>Acquisition de licence en mode silencieux

L’acquisition de licence en mode silencieux requiert un seul appel de méthode qui gère toutes les communications réseau avec le serveur de licences de manière asynchrone.

Ce type d’acquisition de licence est généralement utilisé comme réponse à l’utilisateur final tentant d’accéder au contenu protégé, par exemple en tentant de lire un fichier protégé dans une application de lecteur multimédia. Étant donné que l’acquisition de licence en mode silencieux obtient la licence avec un appel unique, elle ne peut pas être utilisée si une entrée supplémentaire de l’utilisateur, telle que le paiement du contenu, est requise.

Pour effectuer une acquisition de licence en mode silencieux, procédez comme suit :

1.  Appelez la méthode [**IWMDRMLicenseManagement :: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) . Transmettez l’en-tête DRM du fichier protégé en tant que paramètre *bstrHeaderData* . Spécifiez les droits que vous souhaitez accorder à la licence dans le paramètre *bstrActions* . Enfin, définissez le paramètre *dwFlags* sur WMDRM \_ Acquire \_ licence \_ Silent.
2.  Événements d’interruption de l’interface [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) . Quand vous recevez l’événement **MEWMDRMLicenseAcquisitionCompleted** , vérifiez son code de retour en appelant la méthode **IMFMediaEvent :: GetStatus** , qui est documentée dans la documentation de Media Foundation. Si la valeur **HRESULT** Récupérée est un code de réussite, la licence a été téléchargée avec succès et est dans la Banque de licences locale prête à être utilisée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Acquisition de licences**](acquiring-licenses.md)
</dt> <dt>

[**Utilisation du modèle d’événement Media Foundation**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




