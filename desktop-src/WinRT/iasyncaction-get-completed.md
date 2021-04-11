---
description: Obtient la méthode qui est appelée lorsque l’action asynchrone se termine.
ms.assetid: 5050BF84-F9E0-4B3E-9252-6C5C1060826E
title: 'IAsyncAction :: get_Completed, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAsyncAction.get_Completed
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: bc018912b2b4643cc4ef2f48cc76eb997a2627fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113123"
---
# <a name="iasyncactionget_completed-method"></a><span data-ttu-id="73329-103">IAsyncAction :: méthode d’extraction \_ terminée</span><span class="sxs-lookup"><span data-stu-id="73329-103">IAsyncAction::get\_Completed method</span></span>

<span data-ttu-id="73329-104">Obtient la méthode qui est appelée lorsque l’action asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="73329-104">Gets the method that is called when the asynchronous action completes.</span></span>

## <a name="syntax"></a><span data-ttu-id="73329-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73329-105">Syntax</span></span>


```C++
HRESULT get_Completed(
  [out] AsyncActionCompletedHandler **handler
);
```



## <a name="parameters"></a><span data-ttu-id="73329-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="73329-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73329-107">*Gestionnaire* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="73329-107">*handler* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73329-108">Type : **[ **AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="73329-108">Type: **[**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md)\*\***</span></span>

<span data-ttu-id="73329-109">Méthode qui gère la notification d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="73329-109">The method that handles the completion notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73329-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="73329-110">Return value</span></span>

<span data-ttu-id="73329-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="73329-111">Type: **HRESULT**</span></span>

<span data-ttu-id="73329-112">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="73329-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="73329-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="73329-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="73329-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73329-114">Requirements</span></span>



| <span data-ttu-id="73329-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73329-115">Requirement</span></span> | <span data-ttu-id="73329-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="73329-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73329-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73329-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73329-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="73329-118">Windows 8</span></span><br/>                                                                              |
| <span data-ttu-id="73329-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73329-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73329-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73329-120">Windows Server 2012</span></span><br/>                                                                    |
| <span data-ttu-id="73329-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="73329-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="73329-122"><dt>Windows. Foundation. idl</dt></span><span class="sxs-lookup"><span data-stu-id="73329-122"><dt>Windows.Foundation.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73329-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73329-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73329-124">**IAsyncAction**</span><span class="sxs-lookup"><span data-stu-id="73329-124">**IAsyncAction**</span></span>](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction)
</dt> </dl>

 

 
