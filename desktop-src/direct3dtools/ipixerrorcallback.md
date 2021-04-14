---
description: Rappel du moteur pour gérer les erreurs.
MS-HAID: vspixengine.IPixErrorCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixErrorCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2FEAB4CF-80C8-4A3F-9D62-DFBAB34DE8C8
api_name:
- IPixErrorCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: df9e34f83f3cdd4c8c36024cf0d4ed042da0070f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392471"
---
# <a name="span-idvspixengineipixerrorcallbackspanipixerrorcallback-interface"></a><span data-ttu-id="ea4f4-103"><span id="vspixengine.ipixerrorcallback"></span>Interface IPixErrorCallback</span><span class="sxs-lookup"><span data-stu-id="ea4f4-103"><span id="vspixengine.ipixerrorcallback"></span>IPixErrorCallback interface</span></span>

<span data-ttu-id="ea4f4-104">Rappel du moteur pour gérer les erreurs.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-104">Callback from engine to handle errors.</span></span>

## <a name="members"></a><span data-ttu-id="ea4f4-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ea4f4-105">Members</span></span>

<span data-ttu-id="ea4f4-106">L’interface **IPixErrorCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ea4f4-106">The **IPixErrorCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ea4f4-107">**IPixErrorCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ea4f4-107">**IPixErrorCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="ea4f4-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ea4f4-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ea4f4-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="ea4f4-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ea4f4-110">L’interface **IPixErrorCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-110">The **IPixErrorCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ea4f4-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="ea4f4-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ea4f4-112">Description</span><span class="sxs-lookup"><span data-stu-id="ea4f4-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ea4f4-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4f4-113"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-errorlistcallback-dword-issue-arr-dword-issue-arr"><strong>ErrorListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ea4f4-114">Rappel qui avertit l’hôte des erreurs retournées par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-114">A callback that notifies the host of errors returned by the associated request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ea4f4-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4f4-115"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-messagescallback-dword-issue-arr"><strong>MessagesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ea4f4-116">Rappel qui avertit l’hôte des messages retournés par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-116">A callback that notifies the host of messages returned by the associated request.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ea4f4-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ea4f4-117"><a href="/windows/desktop/direct3dtools/ipixerrorcallback-warninglistcallback"><strong>WarningListCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ea4f4-118">Rappel qui avertit l’hôte des avertissements retournés par la requête associée.</span><span class="sxs-lookup"><span data-stu-id="ea4f4-118">A callback that notifies the host of warnings returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ea4f4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea4f4-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ea4f4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea4f4-120">Header</span></span></p></td><td><span data-ttu-id="ea4f4-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ea4f4-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
