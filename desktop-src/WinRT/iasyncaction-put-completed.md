---
description: Définit la méthode qui est appelée lorsque l’action asynchrone se termine.
ms.assetid: 632800E4-D02B-4D45-8A9B-B373AC938558
title: IAsyncAction ::p méthode ut_Completed
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.put_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: ec26401aeeed61445b0f244880864366fd5c6118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951185"
---
# <a name="iasyncactionput_completed-method"></a><span data-ttu-id="28bcc-103">IAsyncAction : méthode :p ut \_ terminée</span><span class="sxs-lookup"><span data-stu-id="28bcc-103">IAsyncAction::put\_Completed method</span></span>

<span data-ttu-id="28bcc-104">Définit la méthode qui est appelée lorsque l’action asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="28bcc-104">Sets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="28bcc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28bcc-105">Syntax</span></span>


```C++
HRESULT put_Completed(
  [out] AsyncActionCompletedHandler *handler
);
```



## <a name="parameters"></a><span data-ttu-id="28bcc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28bcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28bcc-107">*Gestionnaire* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28bcc-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28bcc-108">Tapez : \**[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md) \** _</span><span class="sxs-lookup"><span data-stu-id="28bcc-108">Type: \**[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\** _</span></span>

<span data-ttu-id="28bcc-109">Méthode qui gère la notification d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="28bcc-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28bcc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28bcc-110">Return value</span></span>

<span data-ttu-id="28bcc-111">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="28bcc-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="28bcc-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="28bcc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="28bcc-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="28bcc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="28bcc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28bcc-114">Requirements</span></span>



| <span data-ttu-id="28bcc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28bcc-115">Requirement</span></span> | <span data-ttu-id="28bcc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="28bcc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28bcc-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28bcc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="28bcc-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="28bcc-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="28bcc-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="28bcc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="28bcc-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="28bcc-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="28bcc-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="28bcc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="28bcc-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="28bcc-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28bcc-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28bcc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28bcc-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="28bcc-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
