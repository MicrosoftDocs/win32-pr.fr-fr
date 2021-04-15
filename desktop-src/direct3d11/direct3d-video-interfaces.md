---
title: Interfaces vidéo Direct3D
description: Cette rubrique répertorie les interfaces vidéo Direct3D disponibles dans Direct3D 9Ex et qui sont prises en charge sur Windows 7 et les versions ultérieures des systèmes d’exploitation clients Windows et sur Windows Server 2008 R2 et les versions ultérieures des systèmes d’exploitation Windows Server.
ms.assetid: 922AC983-B9C0-494C-BADD-CEF20931FC26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d20c86e172308d4be6f4c6218a110f49b033ee
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463254"
---
# <a name="direct3d-video-interfaces"></a>Interfaces vidéo Direct3D

Cette rubrique répertorie les interfaces vidéo Direct3D disponibles dans Direct3D 9Ex et qui sont prises en charge sur Windows 7 et les versions ultérieures des systèmes d’exploitation clients Windows et sur Windows Server 2008 R2 et les versions ultérieures des systèmes d’exploitation Windows Server. Vous pouvez utiliser ces interfaces et leurs méthodes pour obtenir les fonctionnalités de protection du contenu vidéo du pilote graphique et les fonctionnalités matérielles de superposition d’un appareil Direct3D. Vous pouvez également utiliser ces interfaces et leurs méthodes pour protéger le contenu vidéo. Ces interfaces et leurs méthodes sont définies dans d3d9. h et décrites dans la section [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) .



| Interface                                                                                                                                                                                                                             | Description                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)<br/>           | Interroge les fonctionnalités matérielles de superposition d’un appareil Direct3D.<br/>                                                     |
| <span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)<br/> | Fournit un canal de communication avec le pilote Graphics ou le runtime Direct3D.<br/>                                  |
| <span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)<br/>                                    | Représente une session de chiffrement utilisée pour accéder à une surface protégée.<br/>                                      |
| <span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)<br/>                                              | Permet à une application d’utiliser des services de protection et de chiffrement de contenu qui sont implémentés par un pilote Graphics.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[Guide de programmation pour Direct3D 11](dx-graphics-overviews.md)
</dt> </dl>

 

