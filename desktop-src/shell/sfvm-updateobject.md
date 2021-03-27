---
description: Met à jour un objet en passant un pointeur vers un tableau de deux pointeurs vers des listes d’identificateurs d’élément (PIDL). Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_UPDATEOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3bd68ace-3ccf-446c-8cf9-52f42444674e
api_name:
- SFVM_UPDATEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4367551cdf2d48a06c633329ad850c3f7c2e0976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210829"
---
# <a name="sfvm_updateobject-message"></a><span data-ttu-id="043b9-104">\_Message SFVM UPDATEOBJECT</span><span class="sxs-lookup"><span data-stu-id="043b9-104">SFVM\_UPDATEOBJECT message</span></span>

<span data-ttu-id="043b9-105">Met à jour un objet en passant un pointeur vers un tableau de deux pointeurs vers des listes d’identificateurs d’élément (PIDL).</span><span class="sxs-lookup"><span data-stu-id="043b9-105">Updates an object by passing a pointer to an array of two pointers to item identifier lists (PIDLs).</span></span> <span data-ttu-id="043b9-106">Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="043b9-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_UPDATEOBJECT 

    lParam = (LPARAM*) ppidl;

            
```



## <a name="parameters"></a><span data-ttu-id="043b9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="043b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="043b9-108">*ppidl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="043b9-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="043b9-109">Adresse d’un tableau de deux PIDL.</span><span class="sxs-lookup"><span data-stu-id="043b9-109">The address of an array of two PIDLs.</span></span> <span data-ttu-id="043b9-110">Le premier PIDL est l’ancien PIDL.</span><span class="sxs-lookup"><span data-stu-id="043b9-110">The first PIDL is the old PIDL.</span></span> <span data-ttu-id="043b9-111">Le deuxième est une copie de l’ancien PIDL avec des informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="043b9-111">The second one is a copy of the old PIDL with updated information.</span></span> <span data-ttu-id="043b9-112">Le contrôle de la durée de vie de la copie appartient à la vue après l’achèvement réussi de cet appel.</span><span class="sxs-lookup"><span data-stu-id="043b9-112">Control over the copy's lifetime belongs to the view after successful completion of this call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="043b9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="043b9-113">Return value</span></span>

<span data-ttu-id="043b9-114">Retourne l’ID ListView de l’objet mis à jour si la mise à jour a réussi ; Sinon, elle retourne-1.</span><span class="sxs-lookup"><span data-stu-id="043b9-114">Returns the listview ID of the updated object if the update was successful; otherwise, it returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="043b9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="043b9-115">Remarks</span></span>

<span data-ttu-id="043b9-116">Si la mise à jour a échoué, l’appelant doit libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="043b9-116">If the update was unsuccessful, the caller must free the memory.</span></span>

## <a name="requirements"></a><span data-ttu-id="043b9-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="043b9-117">Requirements</span></span>



| <span data-ttu-id="043b9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="043b9-118">Requirement</span></span> | <span data-ttu-id="043b9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="043b9-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="043b9-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="043b9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="043b9-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="043b9-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="043b9-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="043b9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="043b9-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="043b9-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="043b9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="043b9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="043b9-125"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="043b9-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




