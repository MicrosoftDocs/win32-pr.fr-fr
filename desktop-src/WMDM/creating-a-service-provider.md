---
title: Création d’un fournisseur de services
description: Création d’un fournisseur de services
ms.assetid: 7da27fe2-8a57-4adb-94b2-448b6362dc33
keywords:
- Gestionnaire de périphériques Windows Media, création de fournisseurs de services
- Gestionnaire de périphériques, création de fournisseurs de services
- Gestionnaire de périphériques Windows Media, Guide de programmation
- Gestionnaire de périphériques, Guide de programmation
- Guide de programmation, fournisseurs de services
- Guide de programmation, Windows Media Gestionnaire de périphériques
- Guide de programmation, création de fournisseurs de services
- Gestionnaire de périphériques Windows Media, fournisseurs de services
- Gestionnaire de périphériques, fournisseurs de services
- fournisseurs de services, création
- créer des fournisseurs de services, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8469c3d656d151457ed818ea6b4192a3c79ed061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510686"
---
# <a name="creating-a-service-provider"></a>Création d’un fournisseur de services

Un fournisseur de services est un composant qui sert de intermédiaire entre une application et un appareil. Windows Media Gestionnaire de périphériques achemine les demandes de l’application vers le fournisseur de services, qui est ensuite responsable de la communication avec l’appareil ou de l’exécution de l’action demandée. Un fournisseur de services communique généralement avec un pilote pour permettre la communication avec l’appareil. Un fournisseur de services est un composant COM qui implémente les interfaces appelées par les Gestionnaire de périphériques Windows Media. L’interface racine de l’objet fournisseur de services est [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider). Après avoir obtenu cette interface, les Gestionnaire de périphériques Windows Media peuvent obtenir d’autres interfaces via l’implémentation du fournisseur de services de différentes méthodes. Les interfaces qu’un fournisseur de services doit implémenter sont répertoriées dans [interfaces obligatoires et facultatives](mandatory-and-optional-interfaces.md). La hiérarchie des interfaces est indiquée dans [interfaces pour les fournisseurs de services](interfaces-for-service-providers.md).

> [!Note]  
> Vous ne devez pas essayer de créer un fournisseur de services MTP. au lieu de cela, vous devez utiliser le fournisseur de services MTP et les pilotes fournis par Microsoft.

 

Avant d’essayer de créer un fournisseur de services, vous devez comprendre soigneusement les appels effectués par une application sur un fournisseur de services. Lisez [création d’une application Windows Media gestionnaire de périphériques](creating-a-windows-media-device-manager-application.md) pour obtenir une idée des tâches de base et des appels qu’une application fera sur un fournisseur de services lorsqu’il tente de communiquer avec un appareil.

La liste suivante présente les principales étapes du développement d’un fournisseur de services :

1.  Incluez (et éventuellement compilez) l’en-tête et les fichiers de bibliothèque requis pour votre projet. Consultez les [bibliothèques et en-têtes requis pour un fournisseur de services](required-libraries-and-headers-for-a-service-provider.md) pour obtenir la liste des fichiers requis.
2.  Implémentez toutes les autres interfaces requises ou facultatives du fournisseur de services (consultez [interfaces obligatoires et facultatives](mandatory-and-optional-interfaces.md)). En règle générale, les interfaces sont appelées dans cet ordre :
    -   [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
    -   [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)/2
    -   [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)
    -   [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)/2
    -   [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)
    -   [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)/2/3
3.  Vérifiez que votre fournisseur de services ou appareil installe les clés de Registre appropriées lors de l’installation. Ces clés spécifient les paramètres de l’appareil, inscrivent le fournisseur de services en tant que plug-in et activent Plug-and-Play notifications pour l’arrivée et la suppression de l’appareil. Consultez [paramètres](device-parameters.md)de l’appareil, [inscription du fournisseur de services](registering-the-service-provider.md)et [activation de PNP pour les appareils](enabling-pnp-for-devices.md).
4.  Sur l’instanciation de votre classe, authentifiez le fournisseur de services dans le constructeur. Pour ce faire, créez une classe [CSecureChannelServer](csecurechannelserver-class.md) et définissez le certificat. Implémentez l’interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) et appelez les méthodes de la classe CSecureChannelServer instanciées précédemment. Consultez [authentification du fournisseur de services](authenticating-the-service-provider.md) pour savoir comment instancier la classe CSecureChannelServer et implémenter les méthodes IComponentAuthenticate.
5.  Windows Media Gestionnaire de périphériques interroge votre fournisseur de services pour obtenir la liste des appareils connectés en appelant [**IMDServiceProvider2 :: CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) ou [**IMDServiceProvider :: EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices), selon que le fournisseur de services gère plug-and-Play appareils. Le fournisseur de services doit retourner une liste d’objets [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice) représentant des appareils connectés. Pour plus d’informations, consultez [énumération des appareils](enumerating-devices-service-provider.md) .
6.  Avant de gérer un appel, vérifiez qu’un canal sécurisé a été établi. Appelez [**CSecureChannelServer :: fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) avant d’effectuer des actions. Si cet appel échoue, retournez WMDM \_ E \_ NOTCERTIFIED.
7.  Vous aurez besoin d’une paire certificat/clé émise par Microsoft pour être en mesure de gérer les documents DRM protégés. Pour plus d’informations, consultez [gestion du contenu protégé dans le fournisseur de services](handling-protected-content-in-the-service-provider.md) .
8.  Pour permettre à votre appareil de se synchroniser automatiquement avec le lecteur Windows Media, il doit respecter les conditions requises indiquées dans activation de la [synchronisation avec le lecteur Windows Media](enabling-synchronization-with-windows-media-player.md).
9.  Pour que votre appareil s’affiche dans l’Explorateur Windows, vous devez effectuer quelques étapes spéciales, détaillées dans [Configuration requise pour que les lecteurs audio portables s’affichent dans l’Explorateur Windows](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation**](programming-guide.md)
</dt> </dl>

 

 