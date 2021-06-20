---
description: Cette section contient des informations de référence sur les interfaces COM (Component Object Model) fournies par la bibliothèque de l’utilitaire D3DX dans les graphiques Direct3D 10.
ms.assetid: c57d9c39-3f30-4205-9b0a-665fe53f2b14
title: Interfaces D3DX (graphiques Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c064edce5d5841875eb3148bf74b18f50f93081
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408012"
---
# <a name="d3dx-interfaces-direct3d-10-graphics"></a>Interfaces D3DX (graphiques Direct3D 10)

Cette section contient des informations de référence sur les interfaces COM (Component Object Model) fournies par la bibliothèque de l’utilitaire D3DX. Les interfaces suivantes sont utilisées avec la bibliothèque de l’utilitaire D3DX.



| Interfaces                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interface ID3DX10DataLoader**](id3dx10dataloader.md)       | Objet chargeant des données utilisé par l' [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour le chargement des données de façon asynchrone.<br/>                                                                                                                                                                                                                                                                                                   |
| [**Interface ID3DX10DataProcessor**](id3dx10dataprocessor.md) | Objet de traitement de données utilisé par l' [**interface ID3DX10ThreadPump**](id3dx10threadpump.md) pour le traitement des données chargées de façon asynchrone.<br/>                                                                                                                                                                                                                                                                                      |
| [**Interface ID3DX10Font**](id3dx10font.md)                   | L’interface ID3DX10Font encapsule les textures et les ressources nécessaires pour restituer une police spécifique sur un appareil spécifique.<br/>                                                                                                                                                                                                                                                                                                |
| [**Interface ID3DX10Mesh**](id3dx10mesh.md)                   | Les applications utilisent les méthodes de l’interface ID3DX10Mesh pour manipuler les objets de maillage.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**Interface ID3DX10MeshBuffer**](id3dx10meshbuffer.md)       |                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Interface ID3DX10SkinInfo**](id3dx10skininfo.md)           | ID3DX10SkinInfo vous permet d’optimiser, de traiter et de définir manuellement la relation entre les segments et les vertex de vos mailles (voir [animation de squelette sur Wikipédia](https://en.wikipedia.org/wiki/Skeletal_animation)). Il est particulièrement utile pour créer des fichiers. x exportés par des applications DCC (telles que 3DS Max et Maya) plus compatibles avec le matériel et pour améliorer la vitesse de rendu de vos mailles dépouillées en mode de rendu logiciel.<br/> |
| [**Interface ID3DX10Sprite**](id3dx10sprite.md)               | L’interface ID3DX10Sprite fournit un ensemble de méthodes qui simplifient le processus de dessin de sprites à l’aide de Microsoft Direct3D.<br/>                                                                                                                                                                                                                                                                                            |
| [**Interface ID3DX10ThreadPump**](id3dx10threadpump.md)       | Utilisé pour exécuter des tâches de façon asynchrone. Cet objet occupe une quantité importante de ressources. en général, un seul doit être créé par application.<br/>                                                                                                                                                                                                                                                                  |
| [**Interface ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)   | Les applications utilisent les méthodes de l’interface ID3DXMATRIXStack pour manipuler une pile de matrice.<br/>                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur D3DX](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 




