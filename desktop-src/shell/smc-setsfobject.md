---
description: Vous informe de l’enregistrement de l’objet passé.
title: Message SMC_SETSFOBJECT (ShObjIdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 44aeb41ab7dcd271f8c84bff4eb8b5525ac66e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203662"
---
# <a name="smc_setsfobject-message"></a><span data-ttu-id="db7b0-103">\_Message SMC SETSFOBJECT</span><span class="sxs-lookup"><span data-stu-id="db7b0-103">SMC\_SETSFOBJECT message</span></span>

<span data-ttu-id="db7b0-104">Vous informe de l’enregistrement de l’objet passé.</span><span class="sxs-lookup"><span data-stu-id="db7b0-104">Notifies you to save the passed object.</span></span>


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a><span data-ttu-id="db7b0-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db7b0-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db7b0-106">*vaut*</span><span class="sxs-lookup"><span data-stu-id="db7b0-106">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="db7b0-107">IID associé à l’objet.</span><span class="sxs-lookup"><span data-stu-id="db7b0-107">The IID associated with the object.</span></span>

</dd> <dt>

<span data-ttu-id="db7b0-108">*va*</span><span class="sxs-lookup"><span data-stu-id="db7b0-108">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="db7b0-109">Pointeur de l’interface sur l’objet spécifié par *IID*.</span><span class="sxs-lookup"><span data-stu-id="db7b0-109">A pointer the interface on the object specified by *iid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db7b0-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db7b0-110">Return value</span></span>

<span data-ttu-id="db7b0-111">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="db7b0-111">Return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="db7b0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="db7b0-112">Remarks</span></span>

<span data-ttu-id="db7b0-113">Cette notification est reçue par la méthode [**IShellMenuCallback :: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .</span><span class="sxs-lookup"><span data-stu-id="db7b0-113">This notification is received by the [**IShellMenuCallback::CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) method.</span></span>

<span data-ttu-id="db7b0-114">La notification **SMC \_ SETSFOBJECT** est utilisée avec le \_ flux d’iid.</span><span class="sxs-lookup"><span data-stu-id="db7b0-114">The **SMC\_SETSFOBJECT** notification is used with IID\_Stream.</span></span> <span data-ttu-id="db7b0-115">L’objet est enregistré dans un formulaire persistant dans le registre et rien n’est effectué avec le décompte de références sur l’objet passé.</span><span class="sxs-lookup"><span data-stu-id="db7b0-115">The object is saved into a persisted form in the registry and nothing is done with the reference count on the object passed in.</span></span>

## <a name="requirements"></a><span data-ttu-id="db7b0-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="db7b0-116">Requirements</span></span>



| <span data-ttu-id="db7b0-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db7b0-117">Requirement</span></span> | <span data-ttu-id="db7b0-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="db7b0-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db7b0-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db7b0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="db7b0-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db7b0-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="db7b0-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db7b0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="db7b0-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db7b0-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="db7b0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="db7b0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="db7b0-124"><dt>ShObjIdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="db7b0-124"><dt>Shobjidl.h</dt></span></span> </dl>   |
| <span data-ttu-id="db7b0-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="db7b0-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="db7b0-126"><dt>ShObjIdl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="db7b0-126"><dt>Shobjidl.idl</dt></span></span> </dl> |



 

 




