---
title: Utilisation de Direct3D 11, Direct3D 10 et Direct2D
description: Cette section traite des techniques d’interopérabilité avec les versions antérieures de Direct3D et Direct2D, de l’API Direct3D 11on12 et des instructions de portage de Direct3D 11 vers Direct3D 12.
ms.assetid: 1AB98335-30B1-4244-B244-F8573524B38C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200da0708b9b990b102a77867669217318f1d67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104216"
---
# <a name="working-with-direct3d-11-direct3d-10-and-direct2d"></a><span data-ttu-id="9c514-103">Utilisation de Direct3D 11, Direct3D 10 et Direct2D</span><span class="sxs-lookup"><span data-stu-id="9c514-103">Working with Direct3D 11, Direct3D 10 and Direct2D</span></span>

<span data-ttu-id="9c514-104">Cette section traite des techniques d’interopérabilité avec les versions antérieures de Direct3D et Direct2D, de l’API Direct3D 11on12 et des instructions de portage de Direct3D 11 vers Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9c514-104">This section covers interop techniques with earlier versions of Direct3D and Direct2D, the Direct3D 11on12 API, and porting guidelines from Direct3D 11 to Direct3D 12.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9c514-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="9c514-105">In this section</span></span>



| <span data-ttu-id="9c514-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9c514-106">Topic</span></span>                                                                                             | <span data-ttu-id="9c514-107">Description</span><span class="sxs-lookup"><span data-stu-id="9c514-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c514-108">Interopérabilité Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9c514-108">Direct3D 12 Interop</span></span>](direct3d-12-with-direct3d-11--direct-2d-and-gdi.md)<br/>             | <span data-ttu-id="9c514-109">D3D12 peut être utilisé pour écrire des applications de composants.</span><span class="sxs-lookup"><span data-stu-id="9c514-109">D3D12 can be used to write componentized applications.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="9c514-110">Direct3D 11 sur 12</span><span class="sxs-lookup"><span data-stu-id="9c514-110">Direct3D 11 on 12</span></span>](direct3d-11-on-12.md)<br/>                                             | <span data-ttu-id="9c514-111">D3D11On12 est un mécanisme qui permet aux développeurs d’utiliser des interfaces et des objets D3D11 pour piloter l’API D3D12.</span><span class="sxs-lookup"><span data-stu-id="9c514-111">D3D11On12 is a mechanism by which developers can use D3D11 interfaces and objects to drive the D3D12 API.</span></span> <span data-ttu-id="9c514-112">D3D11on12 permet aux composants écrits à l’aide de D3D11 (par exemple, du texte et de l’interface utilisateur D2D) de fonctionner conjointement avec des composants écrits ciblant l’API D3D12.</span><span class="sxs-lookup"><span data-stu-id="9c514-112">D3D11on12 enables components written using D3D11 (for example, D2D text and UI) to work together with components written targeting the D3D12 API.</span></span> <span data-ttu-id="9c514-113">D3D11on12 permet également le portage incrémentiel d’une application de D3D11 vers D3D12, en permettant aux parties de l’application de continuer à cibler les D3D11 pour plus de simplicité, tandis que d’autres ciblent D3D12 pour les performances, tout en ayant toujours un rendu complet et correct.</span><span class="sxs-lookup"><span data-stu-id="9c514-113">D3D11on12 also enables incremental porting of an application from D3D11 to D3D12, by enabling portions of the app to continue targeting D3D11 for simplicity while others target D3D12 for performance, while always having complete and correct rendering.</span></span> <span data-ttu-id="9c514-114">D3D11On12 simplifie l’utilisation de techniques d’interopérabilité pour partager des ressources et synchroniser le travail entre les deux API.</span><span class="sxs-lookup"><span data-stu-id="9c514-114">D3D11On12 makes it simpler than using interop techniques to share resources and synchronize work between the two APIs.</span></span> <br/> |
| [<span data-ttu-id="9c514-115">Portage de Direct3D 11 sur Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9c514-115">Porting from Direct3D 11 to Direct3D 12</span></span>](porting-from-direct3d-11-to-direct3d-12.md)<br/> | <span data-ttu-id="9c514-116">Cette section fournit des conseils sur le portage d’un moteur graphique Direct3D 11 personnalisé vers Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="9c514-116">This section provides some guidance on porting from a custom Direct3D 11 graphics engine to Direct3D 12.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="9c514-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c514-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c514-118">Guide de programmation Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="9c514-118">Direct3D 12 Programming Guide</span></span>](directx-12-programming-guide.md)
</dt> </dl>

 

 





