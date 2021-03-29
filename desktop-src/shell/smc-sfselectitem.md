---
description: L’utilisateur a sélectionné l’élément spécifié par la structure SMDATA qui l’accompagne.
title: Message SMC_SFSELECTITEM (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 82c3dfca-98a8-43ca-bebc-85bfdf640d38
api_name:
- SMC_SFSELECTITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cfb3384fcfff73d264d21c53a91ede554cc7da5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973275"
---
# <a name="smc_sfselectitem-message"></a><span data-ttu-id="0ef33-103">\_Message SMC SFSELECTITEM</span><span class="sxs-lookup"><span data-stu-id="0ef33-103">SMC\_SFSELECTITEM message</span></span>

<span data-ttu-id="0ef33-104">L’utilisateur a sélectionné l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) qui l’accompagne.</span><span class="sxs-lookup"><span data-stu-id="0ef33-104">The user has selected the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFSELECTITEM
            
```



## <a name="parameters"></a><span data-ttu-id="0ef33-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ef33-105">Parameters</span></span>

<span data-ttu-id="0ef33-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="0ef33-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ef33-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ef33-107">Return value</span></span>

<span data-ttu-id="0ef33-108">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0ef33-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ef33-109">Notes</span><span class="sxs-lookup"><span data-stu-id="0ef33-109">Remarks</span></span>

<span data-ttu-id="0ef33-110">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="0ef33-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ef33-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0ef33-111">Requirements</span></span>



| <span data-ttu-id="0ef33-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ef33-112">Requirement</span></span> | <span data-ttu-id="0ef33-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ef33-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ef33-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ef33-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0ef33-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ef33-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0ef33-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ef33-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0ef33-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ef33-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0ef33-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ef33-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ef33-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ef33-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ef33-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="0ef33-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ef33-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ef33-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




