---
description: Pour qu’une application s’exécute correctement, les dll appropriées doivent être installées sur l’ordinateur hôte. Ces dll peuvent être fournies par le système d’exploitation ou le package redistribuable des applications.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Liaison de bibliothèques statiques et dynamiques (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513929"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a>Liaison de bibliothèques statiques et dynamiques (Direct3D 10)

Pour qu’une application s’exécute correctement, les dll appropriées doivent être installées sur l’ordinateur hôte. Ces dll peuvent être fournies par le système d’exploitation ou le package redistribuable des applications.

## <a name="libraries-load-appropriate-dlls"></a>Les bibliothèques chargent les dll appropriées

Les bibliothèques incluses avec le kit de développement logiciel (SDK) DirectX chargent automatiquement les dll appropriées au moment de l’exécution. L’exception à cette règle est d3dx10. lib/d3dx10d. lib, qui chargera le d3dx10.dll fourni avec cette version du kit de développement logiciel (SDK). Par exemple, si le kit de développement logiciel (SDK) téléchargé comprend d3dx10 \_33.dll et d3dx10 \_34.dll, la bibliothèque (d3dx10. lib) fournie avec ce kit de développement logiciel (SDK) charge d3dx10 \_34.dll. Si un kit de développement logiciel (SDK) suivant est installé ultérieurement avec d3dx10 \_ 35. lib, le d3dx10. lib du SDK précédent chargera toujours d3dx10 \_34.dll. Le d3dx10. lib du kit de développement logiciel (SDK) le plus récent chargera d3dx10 \_35.dll.

## <a name="redistributing-binaries"></a>Redistribution des binaires

Seules les d3dx10.dll (et les versions ultérieures du même fichier) peuvent être redistribuées. Pour redistribuer ce fichier, vous devez utiliser la fonction **DirectXSetup** . Pour plus d’informations sur l’utilisation de cette fonction et la combinaison d’un package redistribuable, consultez [installation de DirectX avec DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx). Tous les autres fichiers binaires nécessaires sont inclus dans Windows Vista. Les seuls fichiers binaires qui peuvent être redistribués sont ceux qui se trouvent dans le répertoire suivant.


```
(SDK root)\Redist
```



Le tableau suivant décrit les binaires que les développeurs doivent connaître.



| Fichiers binaires Direct3D 10   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d3dx10.dll/d3dx10d.dll | Composants D3DX10 des versions commerciales et de débogage ; les composants de la version commerciale peuvent être redistribués dans le CAB Redist.                                                                                                                                                                                                                                                                                                                                                                                                             |
| d3d10ref.dll           | Rastériseur de référence. Fournit une implémentation logicielle du pipeline Graphics. Inclus uniquement dans le cadre de la SDK Windows ou du SDK DirectX hérité et ne peut pas être redistribué. Le rastériseur de référence est destiné uniquement au débogage. La liaison explicite n’est pas nécessaire. toute tentative de création d’un appareil de référence (voir [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) chargera cette dll si elle est présente.                                                                                                    |
| d3d10sdklayers.dll     | Série d’utilitaires SDK qui agit comme une couche entre les appels d’API et l’exécution du runtime, y compris la couche de [débogage](d3d10-graphics-programming-guide-api-features-layers.md) et la couche Switch-to-Reference. La liaison explicite n’est pas nécessaire. Si un appareil est créé avec l’indicateur de couche approprié, cette DLL est chargée automatiquement. Ce composant est destiné uniquement à des fins de développement et de débogage. Inclus uniquement dans le cadre de la SDK Windows ou du SDK DirectX hérité et ne peut pas être redistribué. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> <dt>

[Graphiques Direct3D 10](d3d10-graphics.md)
</dt> </dl>

 

 



