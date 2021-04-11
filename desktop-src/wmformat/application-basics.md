---
title: Notions de base des applications
description: Notions de base des applications
ms.assetid: 5593d27e-e97d-4f03-99ff-aee856abec8e
keywords:
- SDK Windows Media format, notions de base des applications DRM
- gestion des droits numériques (DRM), principes de base des applications
- DRM (gestion des droits numériques), principes de base des applications
- gestion des droits numériques (DRM), fonction WMDRMStartup
- DRM (gestion des droits numériques), fonction WMDRMStartup
- WMDRMStartup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182a9e54e077c174c4f4cbe74ba392aa44ce5112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190806"
---
# <a name="application-basics"></a>Notions de base des applications

Vous devez effectuer un traitement supplémentaire pour toutes les applications qui utilisent les API étendues du client Windows Media DRM. Cette rubrique décrit la configuration requise pour une application simple.

Tout d’abord, vous devez initialiser les API étendues du client Windows Media DRM en appelant la fonction [**WMDRMStartup**](wmdrmstartup.md) . Les objets du kit de développement logiciel (SDK) sont des objets COM, mais vous n’avez pas besoin d’appeler **CoIntialize**, car la fonction **WMDRMStatup** Initialise com pour vous.

> [!Note]  
> Le kit de développement logiciel (SDK) du format Windows Media utilise uniquement un sous-ensemble de COM. par conséquent, si vous utilisez des objets COM autres que ceux de l’API étendue du client Windows Media DRM, vous devez toujours appeler **CoInitialize**.

 

Tous les objets des API étendues du client Windows Media DRM sont créés à l’aide des fonctions et des méthodes d’assistance. Vous n’avez jamais besoin d’appeler **CoCreateInstance** pour créer un objet. La première interface à instancier pour toute application qui utilise le kit de développement logiciel (SDK) est [**IWMDRMProvider**](iwmdrmprovider.md), que vous pouvez utiliser pour instancier toutes les autres interfaces de base. Pour récupérer une instance de **IWMDRMProvider**, vous devez appeler [**WMDRMCreateProvider**](wmdrmcreateprovider.md) ou [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md). La différence entre ces fonctions est que **WMDRMCreateProvider** crée un objet qui peut à son tour créer uniquement des objets qui ne prennent pas en charge les méthodes qui requièrent la bibliothèque stub.

Une fois que vous disposez d’une instance de **IWMDRMProvider**, vous pouvez créer les autres objets dont vous avez besoin en appelant [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md).

Lorsque vous êtes prêt à quitter votre application, vous devez libérer les ressources du sous-système DRM en appelant la fonction [**WMDRMShutdown**](wmdrmshutdown.md) . Cette fonction arrête également COM pour vous.

L’exemple de code suivant montre comment initialiser et conclure une application qui utilise les API étendues du client Windows Media DRM.


```C++
#include <wmdrmsdk.h>
// TODO: Include other headers here as needed.

// This example demonstrates the code required in a single, simple
// main function. You will most likely break this code up into appropriate
// functions.
void main(void)
{
    HRESULT hr = S_OK;

    IWMDRMProvider*     pProvider     = NULL;
    // For the sake of example, this code will instantiate the
    //  IWMDRMLicenseQuery interface. The process is the same for the
    //  other base interfaces.
    IWMDRMLicenseQuery* pLicenseQuery = NULL;

    // Initialize the DRM subsystem.
    hr = WMDRMStartup();

    // Create a provider object, that can be used to create the other
    //  objects.
    if (SUCCEEDED(hr))
    {
        hr = WMDRMCreateProvider(&pProvider);
    }

    if(SUCCEEDED(hr))
    {
        hr = pProvider->CreateObject(
            IID_IWMDRMLicenseQuery, 
            (void**)&pLicenseQuery);
    }

    // TODO: Use the methods of IWMDRMLicenseQuery as required.

    // Cleanup and shutdown.
    SAFE_RELEASE(pLicenseQuery);
    SAFE_RELEASE(pProvider);

    hr = WMDRMShutdown();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Prise en main**](drm-getting-started.md)
</dt> </dl>

 

 




