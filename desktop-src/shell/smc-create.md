---
description: Vous avertit qu’une bande de menu a été créée.
title: Message SMC_CREATE (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8eeca6f6-1718-4ff6-b4a7-4b68b9527468
api_name:
- SMC_CREATE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 59219f376288431fa20e198d8c427ff40c7fba62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991656"
---
# <a name="smc_create-message"></a><span data-ttu-id="54d45-103">\_Créer un message SMC</span><span class="sxs-lookup"><span data-stu-id="54d45-103">SMC\_CREATE message</span></span>

<span data-ttu-id="54d45-104">Vous avertit qu’une bande de menu a été créée.</span><span class="sxs-lookup"><span data-stu-id="54d45-104">Notifies you that a menu band has been created.</span></span>


```C++
SMC_CREATE 
    lParam = (LPARAM) (LPSMDATA) psmd
            
```



## <a name="parameters"></a><span data-ttu-id="54d45-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54d45-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54d45-106">*psmd*</span><span class="sxs-lookup"><span data-stu-id="54d45-106">*psmd*</span></span> 
</dt> <dd>

<span data-ttu-id="54d45-107">Pointeur vers le membre **pvUserData** d’une structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) .</span><span class="sxs-lookup"><span data-stu-id="54d45-107">A pointer to the **pvUserData** member of an [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54d45-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54d45-108">Return value</span></span>

<span data-ttu-id="54d45-109">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54d45-109">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="54d45-110">Notes</span><span class="sxs-lookup"><span data-stu-id="54d45-110">Remarks</span></span>

<span data-ttu-id="54d45-111">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="54d45-111">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="54d45-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="54d45-112">Requirements</span></span>



| <span data-ttu-id="54d45-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54d45-113">Requirement</span></span> | <span data-ttu-id="54d45-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="54d45-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54d45-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54d45-115">Minimum supported client</span></span><br/> | <span data-ttu-id="54d45-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54d45-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="54d45-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54d45-117">Minimum supported server</span></span><br/> | <span data-ttu-id="54d45-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54d45-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54d45-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="54d45-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="54d45-120"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="54d45-120"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="54d45-121">MIDL</span><span class="sxs-lookup"><span data-stu-id="54d45-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54d45-122"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54d45-122"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




