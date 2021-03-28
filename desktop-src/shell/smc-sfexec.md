---
description: Exécutez l’élément de dossier shell spécifié dans la structure SMDATA associée.
title: Message SMC_SFEXEC (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bb8f6434-0936-460f-b7dc-39be58bb70ce
api_name:
- SMC_SFEXEC
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b4e414cd7dab9968882272b19b9b21b95da0f1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973443"
---
# <a name="smc_sfexec-message"></a><span data-ttu-id="46233-103">\_Message SMC SFEXEC</span><span class="sxs-lookup"><span data-stu-id="46233-103">SMC\_SFEXEC message</span></span>

<span data-ttu-id="46233-104">Exécutez l’élément de dossier shell spécifié dans la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associée.</span><span class="sxs-lookup"><span data-stu-id="46233-104">Execute the Shell folder item specified in the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_SFEXEC
            
```



## <a name="parameters"></a><span data-ttu-id="46233-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46233-105">Parameters</span></span>

<span data-ttu-id="46233-106">Ce message n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="46233-106">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46233-107">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46233-107">Return value</span></span>

<span data-ttu-id="46233-108">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46233-108">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="46233-109">Notes</span><span class="sxs-lookup"><span data-stu-id="46233-109">Remarks</span></span>

<span data-ttu-id="46233-110">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="46233-110">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="46233-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="46233-111">Requirements</span></span>



| <span data-ttu-id="46233-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46233-112">Requirement</span></span> | <span data-ttu-id="46233-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="46233-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46233-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46233-114">Minimum supported client</span></span><br/> | <span data-ttu-id="46233-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46233-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="46233-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46233-116">Minimum supported server</span></span><br/> | <span data-ttu-id="46233-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46233-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46233-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="46233-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="46233-119"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46233-119"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="46233-120">MIDL</span><span class="sxs-lookup"><span data-stu-id="46233-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46233-121"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46233-121"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




