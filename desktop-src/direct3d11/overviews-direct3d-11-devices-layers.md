---
title: Couches logicielles
description: Le runtime Direct3D 11 est construit avec des couches, en commençant par les fonctionnalités de base au cœur et en créant des fonctionnalités facultatives et d’assistance aux développeurs dans les couches externes. Cette section décrit les fonctionnalités de chaque couche.
ms.assetid: c545983c-5351-42a9-82e5-deea73aa035f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59d0405d53526b8fb0b93e52fd1a53b5c17839f6c58df919bac335b21ad2477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124360"
---
# <a name="software-layers"></a>Couches logicielles

Le runtime Direct3D 11 est construit avec des couches, en commençant par les fonctionnalités de base au cœur et en créant des fonctionnalités facultatives et d’assistance aux développeurs dans les couches externes. Cette section décrit les fonctionnalités de chaque couche.

En règle générale, les couches ajoutent des fonctionnalités, mais ne modifient pas le comportement existant. Par exemple, les fonctions de base auront les mêmes valeurs de retour que celles de la couche de débogage en cours d’instanciation, bien qu’une sortie de débogage supplémentaire puisse être fournie si la couche de débogage est instanciée.

Pour créer des couches quand un appareil est créé, appelez [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) et fournissez une ou plusieurs valeurs d’indicateur de [**\_ création d' \_ appareil \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) .

Direct3D 11 fournit les couches de Runtime suivantes :

-   [Couche principale](#core-layer)
-   [Couche de débogage](#debug-layer)
-   [Rubriques connexes](#related-topics)

## <a name="core-layer"></a>Couche principale

La couche de base existe par défaut ; en fournissant un mappage très étroit entre l’API et le pilote de périphérique, ce qui minimise la surcharge des appels haute fréquence. Étant donné que la couche de base est essentielle pour les performances, elle effectue uniquement une validation critique. Les couches restantes sont facultatives.

## <a name="debug-layer"></a>Couche de débogage

La couche de débogage fournit une validation de paramètres et de cohérence étendues supplémentaires (par exemple, la validation de la liaison de nuanceur et la liaison de ressources, la validation de la cohérence des paramètres et la création de rapports sur les erreurs).

Pour créer un appareil qui prend en charge la couche de débogage, vous devez installer le kit de développement logiciel (SDK) DirectX (pour obtenir D3D11SDKLayers.dll), puis spécifier l’indicateur de **\_ \_ \_ débogage d3d11 créer un appareil** lors de l’appel de la fonction [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou de la fonction [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) . Si vous exécutez votre application avec la couche de débogage activée, l’application sera considérablement plus lente. Toutefois, pour vous assurer que votre application ne nettoie pas les erreurs et les avertissements avant de l’envoyer, utilisez la couche de débogage. Pour plus d’informations, consultez [utilisation de la couche de débogage pour déboguer des applications](using-the-debug-layer-to-test-apps.md).


> [!Note]  
> pour Windows 7 avec la mise à jour de plateforme pour Windows 7 (KB2670838) ou Windows 8. x, pour créer un appareil qui prend en charge la couche de débogage, installez le kit de développement logiciel (SDK) Windows pour Windows 8. x afin d’obtenir D3D11 \_1SDKLayers.dll.


> [!Note]  
> par Windows 10, pour créer un appareil qui prend en charge la couche de débogage, activez la fonctionnalité facultative « outils graphiques ». accédez au panneau Paramètres, sous système, applications & fonctionnalités, gérer les fonctionnalités facultatives, ajouter une fonctionnalité, puis rechercher « outils graphics ».


> [!Note]  
> Pour plus d’informations sur le débogage des applications DirectX à distance, consultez [débogage des applications DirectX à distance](/windows/desktop/direct3dtools/debugging-directx-apps-remotely).

 

Vous pouvez également activer/désactiver l’indicateur de débogage à l’aide du [panneau de configuration DirectX](/previous-versions//bb219725(v=vs.85)) inclus dans le kit de développement logiciel (SDK) DirectX.

Lorsque la couche de débogage répertorie les fuites de mémoire, elle génère une liste de pointeurs d’interface d’objet avec leurs noms conviviaux. Le nom convivial par défaut est « sans &lt; nom &gt; ». Vous pouvez définir le nom convivial à l’aide de la méthode [**ID3D11DeviceChild :: SetPrivateData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicechild-setprivatedata) et du GUID **WKPDID \_ D3DDebugObjectName** qui se trouve dans D3Dcommon. h. Par exemple, pour nommer pTexture avec le nom de SDKLayer mytexture.jpg, utilisez le code suivant :


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



En règle générale, vous devez compiler ces appels en dehors de votre version de production.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appareils](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 