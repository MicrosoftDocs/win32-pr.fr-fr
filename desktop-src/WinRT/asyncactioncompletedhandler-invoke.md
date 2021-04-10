---
description: Appelle la méthode qui est appelée lorsque l’action asynchrone spécifiée se termine.
ms.assetid: 97199C1A-7CE3-4BBD-86A3-2CA9B27CC05E
title: 'AsyncActionCompletedHandler :: Invoke, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler.Invoke
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 1cba9c48fa955b82fdc337ba641acbd4c62f6406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113131"
---
# <a name="asyncactioncompletedhandlerinvoke-method"></a><span data-ttu-id="7fdaa-103">AsyncActionCompletedHandler :: Invoke, méthode</span><span class="sxs-lookup"><span data-stu-id="7fdaa-103">AsyncActionCompletedHandler::Invoke method</span></span>

<span data-ttu-id="7fdaa-104">Appelle la méthode qui est appelée lorsque l’action asynchrone spécifiée se termine.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-104">Invokes the method that is called when the specified asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fdaa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7fdaa-105">Syntax</span></span>


```C++
HRESULT Invoke(
  [in] IAsyncAction *asyncInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7fdaa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7fdaa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fdaa-107">*asyncInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7fdaa-107">*asyncInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fdaa-108">Tapez : \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) \** _</span><span class="sxs-lookup"><span data-stu-id="7fdaa-108">Type: \**[**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)\** _</span></span>

<span data-ttu-id="7fdaa-109">Action asynchrone qui signale la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-109">The asynchronous action that reports completion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fdaa-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7fdaa-110">Return value</span></span>

<span data-ttu-id="7fdaa-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="7fdaa-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="7fdaa-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7fdaa-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7fdaa-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7fdaa-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fdaa-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7fdaa-114">Requirements</span></span>



| <span data-ttu-id="7fdaa-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7fdaa-115">Requirement</span></span> | <span data-ttu-id="7fdaa-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7fdaa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fdaa-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fdaa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7fdaa-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="7fdaa-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="7fdaa-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7fdaa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7fdaa-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7fdaa-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="7fdaa-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="7fdaa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fdaa-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7fdaa-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fdaa-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7fdaa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fdaa-124">**AsyncActionCompletedHandler**</span><span class="sxs-lookup"><span data-stu-id="7fdaa-124">**AsyncActionCompletedHandler**</span></span>](asyncactioncompletedhandler.md)
</dt> </dl>

 

