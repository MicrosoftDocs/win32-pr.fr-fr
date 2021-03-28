---
description: Vous informe de l’initialisation de la bande de menu.
title: Message SMC_INITMENU (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 415ee805-2b57-4f8f-85d9-2b38cd05998d
api_name:
- SMC_INITMENU
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ed7f7be1786192fb2be42f6d36cfb4bf222136fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203663"
---
# <a name="smc_initmenu-message"></a><span data-ttu-id="1f605-103">\_Message SMC INITMENU</span><span class="sxs-lookup"><span data-stu-id="1f605-103">SMC\_INITMENU message</span></span>

<span data-ttu-id="1f605-104">Vous informe de l’initialisation de la bande de menu.</span><span class="sxs-lookup"><span data-stu-id="1f605-104">Notifies you to initialize the menu band.</span></span>


```C++
SMC_INITMENU
            
```



## <a name="parameters"></a><span data-ttu-id="1f605-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1f605-105">Parameters</span></span>

<span data-ttu-id="1f605-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="1f605-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1f605-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1f605-107">Return value</span></span>

<span data-ttu-id="1f605-108">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1f605-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f605-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1f605-109">Remarks</span></span>

<span data-ttu-id="1f605-110">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="1f605-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f605-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1f605-111">Requirements</span></span>



| <span data-ttu-id="1f605-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f605-112">Requirement</span></span> | <span data-ttu-id="1f605-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f605-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f605-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f605-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1f605-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f605-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1f605-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f605-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1f605-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f605-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1f605-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f605-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f605-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f605-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f605-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="1f605-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1f605-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f605-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




