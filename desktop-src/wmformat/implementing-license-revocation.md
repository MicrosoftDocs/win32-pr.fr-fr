---
title: Implémentation de la révocation des licences
description: Implémentation de la révocation des licences
ms.assetid: 50ecfeaa-89cd-4788-a25a-ee0ae8973bf0
keywords:
- Windows Media Format SDK, implémentation de la révocation des licences
- Windows Media Format SDK, révocation de licence
- Windows Media Format SDK, révocation des licences
- ASF (Advanced Systems Format), implémentation de la révocation des licences
- ASF (format avancé des systèmes), implémentation de la révocation des licences
- ASF (Advanced Systems Format), révocation de licence
- ASF (format de systèmes avancés), révocation de licence
- ASF (Advanced Systems Format), révocation des licences
- ASF (format des systèmes avancés), révocation des licences
- gestion des droits numériques (DRM), implémentation de la révocation des licences
- DRM (gestion des droits numériques), implémentation de la révocation des licences
- gestion des droits numériques (DRM), révocation des licences
- DRM (gestion des droits numériques), révocation de licence
- gestion des droits numériques (DRM), révocation des licences
- DRM (gestion des droits numériques), révocation des licences
- révocation de licence, implémentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e83bfb1a512b031f5b7c297ecede4ed33fba8f2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723570"
---
# <a name="implementing-license-revocation"></a>Implémentation de la révocation des licences

Le kit de développement logiciel (SDK) Windows Media Rights Manager 10 comprend une fonctionnalité appelée révocation de licence. Cette fonctionnalité permet aux serveurs de licences de demander que les licences soient supprimées de l’ordinateur client. Le kit de développement logiciel (SDK) du format Windows Media fournit des méthodes qui traitent les messages de révocation et suppriment les licences du magasin de licences local.

Le processus de révocation de licence est initié par un service fourni par l’émetteur de licence. Votre application peut héberger ce service, ou il peut s’agir d’une application Web. Dans les deux cas, votre application doit être en mesure de recevoir une demande de licence créée par le service.

Pour supprimer des licences du magasin de licences, procédez comme suit :

1.  Lors de la réception d’une demande de licence de l’émetteur de licence, appelez la fonction [**WMCreateLicenseRevocationAgent**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatelicenserevocationagent) pour créer un objet agent de révocation de licence et obtenir un pointeur vers l’interface [**IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent) .
2.  Appelez la méthode [**IWMLicenseRevocationAgent :: GetLRBChallenge**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-getlrbchallenge) pour générer la réponse de stimulation.
3.  Renvoyez la réponse de la demande de remboursement au composant du service de licence à partir duquel vous avez reçu le problème.
4.  Le composant de service de licence envoie un objet blob de révocation de licence (LRB) signé à votre application. Lorsque vous le recevez, appelez la méthode [**IWMLicenseRevocationAgent ::P rocesslrb**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlicenserevocationagent-processlrb) . **ProcessLRB** crée un message d’accusé de réception que vous devez renvoyer au service de licence pour vérifier que les licences ont été supprimées.

> [!Note]  
> DRM n’est pas pris en charge par la version x64 de ce kit de développement logiciel (SDK).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Activation de la prise en charge de DRM**](enabling-drm-support.md)
</dt> <dt>

[**Interface IWMLicenseRevocationAgent**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent)
</dt> </dl>

 

 




