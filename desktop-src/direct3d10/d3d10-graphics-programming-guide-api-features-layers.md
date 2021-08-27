---
description: Couches d’API (Direct3D 10)
ms.assetid: 19c81383-6ac7-49ea-98a3-bf761a32ab40
title: Couches d’API (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd452032eda61c49edbf007b5ebaf0314f9054fe0b016cf07e3f4473ae3abee6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119989"
---
# <a name="api-layers-direct3d-10"></a>Couches d’API (Direct3D 10)

Le runtime Direct3D 10 est construit avec des couches, en commençant par les fonctionnalités de base au cœur et en créant des fonctionnalités facultatives et d’assistance aux développeurs dans les couches externes.

## <a name="core-layer"></a>Couche principale

La couche de base existe par défaut ; en fournissant un mappage très étroit entre l’API et le pilote de périphérique, ce qui minimise la surcharge des appels haute fréquence. Étant donné que la couche de base est essentielle pour les performances, elle effectue uniquement une validation critique.

Les couches restantes sont facultatives. En règle générale, les couches ajoutent des fonctionnalités, mais ne modifient pas le comportement existant. Par exemple, les fonctions de base auront les mêmes valeurs de retour que celles de la couche de débogage en cours d’instanciation, bien qu’une sortie de débogage supplémentaire puisse être fournie si la couche de débogage est instanciée.

Créez des couches quand un appareil est créé en appelant [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) et en fournissant une ou plusieurs valeurs d’indicateur de création de l' [**\_ \_ appareil \_ D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) .

## <a name="debug-layer"></a>Couche de débogage

La couche de débogage fournit une validation de paramètres et de cohérence étendues supplémentaires (par exemple, la validation de la liaison de nuanceur et la liaison de ressources, la validation de la cohérence des paramètres et la création de rapports sur les erreurs). La sortie générée par la couche de débogage se compose d’une file d’attente de chaînes qui sont accessibles à l’aide de l' [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) (consultez [personnaliser la sortie de débogage avec ID3D10InfoQueue (Direct3D 10)](d3d10-graphics-programming-guide-api-features-layers-info-queue.md)). Les erreurs générées par la couche de base sont mises en surbrillance avec des avertissements par la couche de débogage.

Pour créer un appareil qui prend en charge la couche de débogage, vous devez installer le kit de développement logiciel (SDK) DirectX (pour obtenir D3D10SDKLayers.DLL), puis spécifier l' \_ indicateur de débogage D3D10 créer un \_ appareil lors de l' \_ appel de [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice). Bien entendu, l’exécution d’une application avec la couche de débogage sera sensiblement plus lente. Pour activer/désactiver les messages de débogage pour les API D3DX10, appelez [**D3DX10DebugMute**](d3dx10debugmute.md).

Lorsque la couche de débogage répertorie les fuites de mémoire, elle génère une liste de pointeurs d’interface d’objet avec leurs noms conviviaux. Le nom convivial par défaut est « sans &lt; nom &gt; ». Vous pouvez définir le nom convivial à l’aide de la méthode [**ID3D10DeviceChild :: SetPrivateData**](/windows/desktop/api/D3D10/nf-d3d10-id3d10devicechild-setprivatedata) et du GUID **WKPDID \_ D3DDebugObjectName** qui se trouve dans D3Dcommon. h. Par exemple, pour nommer pTexture avec le nom de SDKLayer mytexture.jpg, utilisez le code suivant :


```
const char c_szName[] = "mytexture.jpg";
pTexture->SetPrivateData( WKPDID_D3DDebugObjectName, sizeof( c_szName ) - 1, c_szName );
```



En règle générale, vous devez compiler ces appels en dehors de votre version de production.

## <a name="switch-to-reference-layer"></a>Couche Switch-to-Reference

Cette couche permet à une application d’effectuer une transition entre un périphérique matériel (HAL) et une référence ou un périphérique logiciel (REF). Pour basculer un appareil, vous devez d’abord créer un appareil qui prend en charge la couche Switch-to-Reference (voir [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)), puis appeler [**ID3D10SwitchToRef :: SetUseRef**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10switchtoref-setuseref).

Tous les États, les ressources et les objets des appareils sont gérés par le biais de cette transition d’appareil. Toutefois, il est parfois impossible de faire correspondre exactement les données de ressources. Cela est dû au fait que certaines informations sont disponibles pour un périphérique matériel qui n’est pas disponible pour un appareil de référence.

Presque toutes les applications en temps réel utilisent l’implémentation HAL du pipeline. Lorsque le pipeline est basculé d’un périphérique matériel à un appareil de référence, les opérations de rendu sont effectuées simultanément sur le matériel et les logiciels. Lors du rendu de l’appareil logiciel, les ressources sont téléchargées dans la mémoire système. Cela peut nécessiter la suppression d’autres ressources mises en cache dans la mémoire système pour libérer de l’espace.

> [!Note]  
> Cette fonctionnalité de couche de référence est prise en charge uniquement dans Direct3D 10 et Direct3D 10,1 et n’est plus prise en charge dans Direct3D 11 et versions ultérieures.

 

## <a name="thread-safe-layer"></a>Couche Thread-Safe

Cette couche est conçue pour permettre aux applications multithread d’accéder à l’appareil à partir de plusieurs threads.

Une application Direct3D 10 peut contrôler une synchronisation d’appareil à l’aide de fonctions d’appareil. Cela permet à une application d’activer/de désactiver les sections critiques (en activant ou désactivant temporairement la protection de multithreading) et de prendre/libérer un verrou de section critique sur plusieurs points d’entrée de l’API Direct3D 10. La couche thread-safe est activée par défaut. Pour les applications à thread unique, la couche thread-safe n’a aucun impact sur les performances.




Différences entre Direct3D 9 et Direct3D 10 :

- Contrairement à Direct3D 9, l’API Direct3D 10 par défaut est entièrement thread-safe.



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités de l’API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 




