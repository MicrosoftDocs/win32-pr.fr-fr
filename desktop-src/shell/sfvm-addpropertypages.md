---
description: 'Permet à l’objet de rappel de fournir une page à ajouter à la feuille de propriétés de propriétés de l’objet sélectionné. Utilisé par IShellFolderViewCB :: MessageSFVCB.'
title: Message SFVM_ADDPROPERTYPAGES (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991665"
---
# <a name="sfvm_addpropertypages-message"></a><span data-ttu-id="c604d-104">\_Message SFVM ADDPROPERTYPAGES</span><span class="sxs-lookup"><span data-stu-id="c604d-104">SFVM\_ADDPROPERTYPAGES message</span></span>

<span data-ttu-id="c604d-105">Permet à l’objet de rappel de fournir une page à ajouter à la feuille de propriétés de **Propriétés** de l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="c604d-105">Allows the callback object to provide a page to add to the **Properties** property sheet of the selected object.</span></span> <span data-ttu-id="c604d-106">Utilisé par [**IShellFolderViewCB :: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="c604d-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a><span data-ttu-id="c604d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c604d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c604d-108">*pData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c604d-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c604d-109">Adresse d’une structure [**de \_ \_ données de PropPage SFVM**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) .</span><span class="sxs-lookup"><span data-stu-id="c604d-109">The address of a [**SFVM\_PROPPAGE\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c604d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c604d-110">Remarks</span></span>

<span data-ttu-id="c604d-111">Ce message sert essentiellement la même fonction que [**IShellPropSheetExt :: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="c604d-111">This message serves essentially the same function as [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span> <span data-ttu-id="c604d-112">Pour plus d’informations, consultez [création de gestionnaires de feuille de propriétés](propsheet-handlers.md) .</span><span class="sxs-lookup"><span data-stu-id="c604d-112">See [Creating Property Sheet Handlers](propsheet-handlers.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="c604d-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c604d-113">Requirements</span></span>



| <span data-ttu-id="c604d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c604d-114">Requirement</span></span> | <span data-ttu-id="c604d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c604d-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c604d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c604d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c604d-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c604d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c604d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c604d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c604d-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c604d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c604d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c604d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c604d-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="c604d-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
