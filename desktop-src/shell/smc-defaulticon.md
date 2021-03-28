---
description: Retourne l’icône par défaut pour l’élément spécifié par la structure SMDATA associée.
title: Message SMC_DEFAULTICON (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d5f6789a-f160-4fba-ba64-b1a0c491fdaa
api_name:
- SMC_DEFAULTICON
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 10edab26c87dae4b1c9d2d5f06390fc608ba1edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991649"
---
# <a name="smc_defaulticon-message"></a><span data-ttu-id="dfc5c-103">\_Message SMC DEFAULTICON</span><span class="sxs-lookup"><span data-stu-id="dfc5c-103">SMC\_DEFAULTICON message</span></span>

<span data-ttu-id="dfc5c-104">Retourne l’icône par défaut pour l’élément spécifié par la structure [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) associée.</span><span class="sxs-lookup"><span data-stu-id="dfc5c-104">Return the default icon for the item specified by the accompanying [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) structure.</span></span>


```C++
SMC_DEFAULTICON 
    wParam = (WPARAM) (LPWSTR) pwszIcon;
    lParam = (LPARAM) (int) iIcon
            
```



## <a name="parameters"></a><span data-ttu-id="dfc5c-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfc5c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfc5c-106">*pwszIcon*</span><span class="sxs-lookup"><span data-stu-id="dfc5c-106">*pwszIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="dfc5c-107">Pointeur vers une chaîne qui reçoit le chemin d’accès qualifié complet du fichier qui contient l’icône par défaut.</span><span class="sxs-lookup"><span data-stu-id="dfc5c-107">A pointer to a string that receives the fully qualified path of the file that contains the default icon.</span></span>

</dd> <dt>

<span data-ttu-id="dfc5c-108">*Icône*</span><span class="sxs-lookup"><span data-stu-id="dfc5c-108">*iIcon*</span></span> 
</dt> <dd>

<span data-ttu-id="dfc5c-109">Pointeur vers un entier qui reçoit l’index de l’icône dans le fichier spécifié par *pwszIcon*.</span><span class="sxs-lookup"><span data-stu-id="dfc5c-109">A pointer to an integer that receives the index of the icon in the file specified by *pwszIcon*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfc5c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfc5c-110">Return value</span></span>

<span data-ttu-id="dfc5c-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dfc5c-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfc5c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="dfc5c-112">Remarks</span></span>

<span data-ttu-id="dfc5c-113">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="dfc5c-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfc5c-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dfc5c-114">Requirements</span></span>



| <span data-ttu-id="dfc5c-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfc5c-115">Requirement</span></span> | <span data-ttu-id="dfc5c-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfc5c-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfc5c-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfc5c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dfc5c-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfc5c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="dfc5c-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfc5c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dfc5c-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfc5c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dfc5c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="dfc5c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfc5c-122"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfc5c-122"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="dfc5c-123">MIDL</span><span class="sxs-lookup"><span data-stu-id="dfc5c-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dfc5c-124"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dfc5c-124"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




