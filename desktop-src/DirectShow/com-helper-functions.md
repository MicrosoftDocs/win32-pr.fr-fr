---
description: Ces fonctions assurent la prise en charge de l’implémentation de l’interface IUnknown dans DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Fonctions d’assistance COM (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529020"
---
# <a name="com-helper-functions"></a><span data-ttu-id="b872e-103">Fonctions d’assistance COM</span><span class="sxs-lookup"><span data-stu-id="b872e-103">COM Helper Functions</span></span>

<span data-ttu-id="b872e-104">Ces fonctions assurent la prise en charge de l’implémentation de l’interface **IUnknown** dans DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b872e-104">These functions provide support for implementing the **IUnknown** interface in DirectShow.</span></span>



| <span data-ttu-id="b872e-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="b872e-105">Function</span></span>                                               | <span data-ttu-id="b872e-106">Description</span><span class="sxs-lookup"><span data-stu-id="b872e-106">Description</span></span>                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b872e-107">**DÉCLARER \_ IUnknown**</span><span class="sxs-lookup"><span data-stu-id="b872e-107">**DECLARE\_IUNKNOWN**</span></span>](declare-iunknown.md)          | <span data-ttu-id="b872e-108">Déclare les trois méthodes de l’interface de base pour une nouvelle interface.</span><span class="sxs-lookup"><span data-stu-id="b872e-108">Declares the three methods of the base interface for a new interface.</span></span> |
| [<span data-ttu-id="b872e-109">**GetInterface**</span><span class="sxs-lookup"><span data-stu-id="b872e-109">**GetInterface**</span></span>](getinterface.md)                   | <span data-ttu-id="b872e-110">Récupère un pointeur d’interface vers le client demandé.</span><span class="sxs-lookup"><span data-stu-id="b872e-110">Retrieves an interface pointer to the requested client.</span></span>               |
| [<span data-ttu-id="b872e-111">**INonDelegatingUnknown**</span><span class="sxs-lookup"><span data-stu-id="b872e-111">**INonDelegatingUnknown**</span></span>](inondelegatingunknown.md) | <span data-ttu-id="b872e-112">Version Nondelegating de l’interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="b872e-112">Nondelegating version of the **IUnknown** interface.</span></span>                  |
| [<span data-ttu-id="b872e-113">**LoadOLEAut32**</span><span class="sxs-lookup"><span data-stu-id="b872e-113">**LoadOLEAut32**</span></span>](loadoleaut32.md)                   | <span data-ttu-id="b872e-114">Charge la DLL Automation (OleAut32.dll).</span><span class="sxs-lookup"><span data-stu-id="b872e-114">Loads the Automation DLL (OleAut32.dll).</span></span>                              |



 

## <a name="requirements"></a><span data-ttu-id="b872e-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b872e-115">Requirements</span></span>



| <span data-ttu-id="b872e-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b872e-116">Requirement</span></span> | <span data-ttu-id="b872e-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b872e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b872e-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="b872e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b872e-119"><dt>ComBase. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b872e-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b872e-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b872e-120">Library</span></span><br/> | <dl> <span data-ttu-id="b872e-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b872e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b872e-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b872e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b872e-123">Fonctions utilitaires</span><span class="sxs-lookup"><span data-stu-id="b872e-123">Utility Functions</span></span>](utility-functions.md)
</dt> </dl>

 

 




