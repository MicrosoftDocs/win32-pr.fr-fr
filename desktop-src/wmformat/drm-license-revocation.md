---
title: Révocation de licence (client Microsoft Windows Media DRM)
description: Révocation de licence (client Microsoft Windows Media DRM)
ms.assetid: 615ddddf-4f2f-400d-9c4d-ff3a2851d699
keywords:
- Windows Media Format SDK, licences
- Windows Media Format SDK, révocation de licence
- gestion des droits numériques (DRM), licences
- DRM (gestion des droits numériques), licences
- gestion des droits numériques (DRM), révocation des licences
- DRM (gestion des droits numériques), révocation de licence
- API étendues du client DRM, licences
- API étendues clientes, licences
- API étendues du client DRM, révocation de licence
- API étendues clientes, révocation de licence
- licences, révocation
- révocation de licence, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90388a7392c79f583143e06fb78ecfe45e188612
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "104211176"
---
# <a name="license-revocation-microsoft-windows-media-drm-client"></a>Révocation de licence (client Microsoft Windows Media DRM)

La révocation de licence fait référence à la suppression de licences d’un magasin de licences local. Un scénario courant de révocation de licence se produit lorsqu’un fournisseur de services, tel qu’un service d’abonnement musical, doit désactiver le service sur l’ordinateur d’un utilisateur.

Le processus de révocation de licence est initié par un service fourni par l’émetteur de licence. Votre application peut héberger ce service ou une application Web. Dans les deux cas, votre application doit être en mesure de recevoir une demande de licence créée par le service.

Pour supprimer des licences du magasin de licences, procédez comme suit :

1.  Lors de la réception d’une demande de licence de l’émetteur de licence, créez une demande de révocation à l’aide de la méthode [**IWMDRMLicenseManagement :: CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) . Cette méthode alloue une mémoire tampon contenant des données de stimulation de révocation, qui est transmise à votre application par le biais du paramètre *ppbChallengeOutput* .
2.  Envoyez la demande de révocation de licence à un service de révocation de licence. Le serveur génère un objet BLOB de révocation de licence (LRB) en réponse.
3.  Supprimez la licence du magasin local à l’aide de la méthode [**IWMDRMLicenseManagement ::P rocesslicenserevocationresponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) , en passant le LRB retourné par le serveur de licences.
4.  Libérez la mémoire tampon allouée par **CreateLicenseRevocationChallenge** à l’aide de la fonction **CoTaskMemFree** .

Pour plus d’informations sur le fonctionnement de la révocation des licences ou sur l’écriture d’un service de révocation, consultez Implémentation de la révocation des [licences](/documentation/?url=%2flibrary%2fwmrm10%2fhtm%2fhowlicenserevokationworks.asp).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> <dt>

[**Magasin de licences local**](local-license-store.md)
</dt> <dt>

[**Guide de programmation**](drm-programming-guide.md)
</dt> </dl>

 

 