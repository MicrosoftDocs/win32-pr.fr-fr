---
description: Rappel pour retourner les données de pile des appels.
MS-HAID: vspixengine.ICallStackCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface ICallStackCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AF380634-A284-4DCA-B746-FB1D8BE099B4
api_name:
- ICallStackCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6b2aa72008d11891c211512308290a3393ee49
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746757"
---
# <a name="span-idvspixengineicallstackcallbackspanicallstackcallback-interface"></a><span data-ttu-id="b6626-103"><span id="vspixengine.icallstackcallback"></span>Interface ICallStackCallback</span><span class="sxs-lookup"><span data-stu-id="b6626-103"><span id="vspixengine.icallstackcallback"></span>ICallStackCallback interface</span></span>

<span data-ttu-id="b6626-104">Rappel pour retourner les données de pile des appels.</span><span class="sxs-lookup"><span data-stu-id="b6626-104">Callback to return callstack data.</span></span>

## <a name="members"></a><span data-ttu-id="b6626-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b6626-105">Members</span></span>

<span data-ttu-id="b6626-106">L’interface **ICallStackCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b6626-106">The **ICallStackCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b6626-107">**ICallStackCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b6626-107">**ICallStackCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="b6626-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b6626-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="b6626-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="b6626-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="b6626-110">L’interface **ICallStackCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b6626-110">The **ICallStackCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="b6626-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="b6626-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="b6626-112">Description</span><span class="sxs-lookup"><span data-stu-id="b6626-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="b6626-113"><a href="/windows/desktop/direct3dtools/icallstackcallback-resultcallback-dword-callstackframe-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="b6626-113"><a href="/windows/desktop/direct3dtools/icallstackcallback-resultcallback-dword-callstackframe-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="b6626-114">Fonction de rappel utilisée pour informer l’hôte des informations de la pile des appels.</span><span class="sxs-lookup"><span data-stu-id="b6626-114">A callback function used to notify the host of call stack information.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="b6626-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6626-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="b6626-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6626-116">Header</span></span></p></td><td><span data-ttu-id="b6626-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="b6626-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
