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
# <a name="direct3d-video-interfaces"></a><span data-ttu-id="ac1c6-103">Interfaces vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="ac1c6-103">Direct3D Video Interfaces</span></span>

<span data-ttu-id="ac1c6-104">Cette rubrique répertorie les interfaces vidéo Direct3D disponibles dans Direct3D 9Ex et qui sont prises en charge sur Windows 7 et les versions ultérieures des systèmes d’exploitation clients Windows et sur Windows Server 2008 R2 et les versions ultérieures des systèmes d’exploitation Windows Server.</span><span class="sxs-lookup"><span data-stu-id="ac1c6-104">This topic lists the Direct3D video interfaces that are available in Direct3D 9Ex and that are supported on Windows 7 and later versions of Windows client operating systems and on Windows Server 2008 R2 and later versions of Windows server operating systems.</span></span> <span data-ttu-id="ac1c6-105">Vous pouvez utiliser ces interfaces et leurs méthodes pour obtenir les fonctionnalités de protection du contenu vidéo du pilote graphique et les fonctionnalités matérielles de superposition d’un appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ac1c6-105">You can use these interfaces and their methods to obtain the video content protection capabilities of the graphics driver and the overlay hardware capabilities of a Direct3D device.</span></span> <span data-ttu-id="ac1c6-106">Vous pouvez également utiliser ces interfaces et leurs méthodes pour protéger le contenu vidéo.</span><span class="sxs-lookup"><span data-stu-id="ac1c6-106">You can also use these interfaces and their methods to protect video content.</span></span> <span data-ttu-id="ac1c6-107">Ces interfaces et leurs méthodes sont définies dans d3d9. h et décrites dans la section [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) .</span><span class="sxs-lookup"><span data-stu-id="ac1c6-107">These interfaces and their methods are defined in D3d9.h and described in the [Microsoft Media Foundation](/windows/desktop/medfound/microsoft-media-foundation-sdk) section.</span></span>



| <span data-ttu-id="ac1c6-108">Interface</span><span class="sxs-lookup"><span data-stu-id="ac1c6-108">Interface</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="ac1c6-109">Description</span><span class="sxs-lookup"><span data-stu-id="ac1c6-109">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac1c6-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span><span class="sxs-lookup"><span data-stu-id="ac1c6-110"><span id="IDirect3D9ExOverlayExtension"></span><span id="idirect3d9exoverlayextension"></span><span id="IDIRECT3D9EXOVERLAYEXTENSION"></span>[**IDirect3D9ExOverlayExtension**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9exoverlayextension)</span></span><br/>           | <span data-ttu-id="ac1c6-111">Interroge les fonctionnalités matérielles de superposition d’un appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ac1c6-111">Queries the overlay hardware capabilities of a Direct3D device.</span></span><br/>                                                     |
| <span data-ttu-id="ac1c6-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span><span class="sxs-lookup"><span data-stu-id="ac1c6-112"><span id="IDirect3DAuthenticatedChannel9"></span><span id="idirect3dauthenticatedchannel9"></span><span id="IDIRECT3DAUTHENTICATEDCHANNEL9"></span>[**IDirect3DAuthenticatedChannel9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9)</span></span><br/> | <span data-ttu-id="ac1c6-113">Fournit un canal de communication avec le pilote Graphics ou le runtime Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ac1c6-113">Provides a communication channel with the graphics driver or the Direct3D runtime.</span></span><br/>                                  |
| <span data-ttu-id="ac1c6-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span><span class="sxs-lookup"><span data-stu-id="ac1c6-114"><span id="IDirect3DCryptoSession9"></span><span id="idirect3dcryptosession9"></span><span id="IDIRECT3DCRYPTOSESSION9"></span>[**IDirect3DCryptoSession9**](/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9)</span></span><br/>                                    | <span data-ttu-id="ac1c6-115">Représente une session de chiffrement utilisée pour accéder à une surface protégée.</span><span class="sxs-lookup"><span data-stu-id="ac1c6-115">Represents a cryptographic session that is used to access a protected surface.</span></span><br/>                                      |
| <span data-ttu-id="ac1c6-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span><span class="sxs-lookup"><span data-stu-id="ac1c6-116"><span id="IDirect3DDevice9Video"></span><span id="idirect3ddevice9video"></span><span id="IDIRECT3DDEVICE9VIDEO"></span>[**IDirect3DDevice9Video**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9video)</span></span><br/>                                              | <span data-ttu-id="ac1c6-117">Permet à une application d’utiliser des services de protection et de chiffrement de contenu qui sont implémentés par un pilote Graphics.</span><span class="sxs-lookup"><span data-stu-id="ac1c6-117">Enables an application to use content protection and encryption services that are implemented by a graphics driver.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ac1c6-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ac1c6-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac1c6-119">Effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="ac1c6-119">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="ac1c6-120">Guide de programmation pour Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ac1c6-120">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

