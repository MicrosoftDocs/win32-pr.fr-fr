---
description: Base des demandes qui peuvent être annulées. Les requêtes annulées ne peuvent être annulées que si elles se trouvent toujours dans la file d’attente, une annulation peut donc être ignorée.
MS-HAID: vspixengine.IPixCancelableRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPixCancelableRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5463ADDD-6FE8-428C-A348-3811C6E97E39
api_name:
- IPixCancelableRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 34e80d7dc0e543c041241299dc32f917bc72f3f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515914"
---
# <a name="span-idvspixengineipixcancelablerequestspanipixcancelablerequest-interface"></a><span data-ttu-id="ea0d8-104"><span id="vspixengine.ipixcancelablerequest"></span>Interface IPixCancelableRequest</span><span class="sxs-lookup"><span data-stu-id="ea0d8-104"><span id="vspixengine.ipixcancelablerequest"></span>IPixCancelableRequest interface</span></span>

<span data-ttu-id="ea0d8-105">Base des demandes qui peuvent être annulées.</span><span class="sxs-lookup"><span data-stu-id="ea0d8-105">Base of any request that can be canceled.</span></span> <span data-ttu-id="ea0d8-106">Les requêtes annulées ne peuvent être annulées que si elles se trouvent toujours dans la file d’attente, une annulation peut donc être ignorée.</span><span class="sxs-lookup"><span data-stu-id="ea0d8-106">Canceled requests can only be canceled if they are still in the queue, so a cancelation may be ignored.</span></span>

## <a name="members"></a><span data-ttu-id="ea0d8-107">Membres</span><span class="sxs-lookup"><span data-stu-id="ea0d8-107">Members</span></span>

<span data-ttu-id="ea0d8-108">L’interface **IPixCancelableRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ea0d8-108">The **IPixCancelableRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea0d8-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea0d8-109">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ea0d8-110">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea0d8-110">Header</span></span></p></td><td><span data-ttu-id="ea0d8-111">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ea0d8-111">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
