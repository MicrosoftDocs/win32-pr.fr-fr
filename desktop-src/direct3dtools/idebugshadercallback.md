---
description: Rappel pour retourner les instructions générées à partir de la création d’une trace de nuanceur.
MS-HAID: vspixengine.IDebugShaderCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IDebugShaderCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9A4A3FD3-15E5-4DB5-8777-55797E32ABA3
api_name:
- IDebugShaderCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 676d76a0dbc199880badebc904a4eb66d2ad4d0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106539029"
---
# <a name="span-idvspixengineidebugshadercallbackspanidebugshadercallback-interface"></a><span data-ttu-id="6b336-103"><span id="vspixengine.idebugshadercallback"></span>Interface IDebugShaderCallback</span><span class="sxs-lookup"><span data-stu-id="6b336-103"><span id="vspixengine.idebugshadercallback"></span>IDebugShaderCallback interface</span></span>

<span data-ttu-id="6b336-104">Rappel pour retourner les instructions générées à partir de la création d’une trace de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="6b336-104">Callback to return the instructions generated from creating a shader trace.</span></span>

## <a name="members"></a><span data-ttu-id="6b336-105">Membres</span><span class="sxs-lookup"><span data-stu-id="6b336-105">Members</span></span>

<span data-ttu-id="6b336-106">L’interface **IDebugShaderCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6b336-106">The **IDebugShaderCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6b336-107">**IDebugShaderCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6b336-107">**IDebugShaderCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="6b336-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6b336-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="6b336-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="6b336-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="6b336-110">L’interface **IDebugShaderCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6b336-110">The **IDebugShaderCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="6b336-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="6b336-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="6b336-112">Description</span><span class="sxs-lookup"><span data-stu-id="6b336-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="6b336-113"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ResultInstructions</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b336-113"><a href="/windows/desktop/direct3dtools/idebugshadercallback-resultinstructions-dword-byte-arr"><strong>ResultInstructions</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6b336-114">Rappel qui avertit l’hôte des informations instructrion retournées par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="6b336-114">A callback that notifies the host of instructrion information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="6b336-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b336-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6b336-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b336-116">Header</span></span></p></td><td><span data-ttu-id="6b336-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6b336-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
