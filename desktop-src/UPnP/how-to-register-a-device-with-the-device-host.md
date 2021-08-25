---
title: Comment inscrire un appareil auprès de l’hôte de l’appareil
description: Vous pouvez inscrire un appareil en cours d’exécution ou un périphérique non en cours d’exécution.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8425578dbd5ccc76685c2a142bee8d2167c4058341c32e4b03bcedca15041579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867579"
---
# <a name="how-to-register-a-device-with-the-device-host"></a>Comment inscrire un appareil auprès de l’hôte de l’appareil

Vous pouvez inscrire un appareil en cours d’exécution ou un périphérique non en cours d’exécution.

## <a name="registering-a-running-device"></a>Inscription d’un appareil en cours d’exécution

Les appareils sont inscrits à l’aide de l’interface [**IUPnPRegistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) . Seuls les administrateurs sont autorisés à inscrire des appareils en cours d’exécution. Pour inscrire un appareil disposant d’un objet contrôle d’appareil en cours d’exécution, une application doit appeler [**IUPnPRegistrar :: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice), en passant ce qui suit :

-   Texte de la description de l’appareil.
-   Pointeur **IUnknown** vers l’objet de contrôle d’appareil.
-   Chaîne d’initialisation qui est transmise à la méthode [**IUPnPDeviceControl :: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) de l’objet de contrôle de périphérique.
-   Emplacement du répertoire de ressources.
-   Durée de vie de l’appareil.
-   Le paramètre d’ID d’appareil (paramètre OUT), qui est la valeur de retour de cet appel ; un pointeur vers l’ID d’appareil est retourné en C++.

## <a name="registering-a-non-running-device"></a>Inscription d’un appareil non en cours d’exécution

Par défaut, seuls les administrateurs et les utilisateurs interactifs sont autorisés à inscrire des appareils non en cours d’exécution. Pour inscrire un appareil auprès d’un objet de contrôle d’appareil qui n’est pas en cours d’exécution, l’application utilise la méthode [**IUPnPRegistrar :: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) .

Pour inscrire un appareil par programme avec un objet de contrôle de périphérique non en cours d’exécution, l’application doit appeler [**IUPnPRegistrar :: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) et lui transmettre les paramètres suivants :

-   Texte de la description de l’appareil.
-   ProgID de l’objet de contrôle d’appareil.
-   Chaîne d’initialisation qui est transmise à la méthode [**IUPnPDeviceControl :: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) de l’objet de contrôle de périphérique.
-   ID de conteneur.
-   Emplacement du répertoire de ressources.
-   Durée de vie de l’appareil.
-   Le paramètre d’ID d’appareil (paramètre OUT), qui est la valeur de retour de cet appel ; un pointeur vers l’ID d’appareil est retourné en C++.

Les inscriptions des appareils non exécutés peuvent être configurées pour être conservées au cours des démarrages du système (les appareils ne sont pas publiés durant la phase d’arrêt). Par conséquent, s’ils sont configurés de cette façon, les appareils sont publiés et annoncés à chaque démarrage de l’ordinateur.

 

 




