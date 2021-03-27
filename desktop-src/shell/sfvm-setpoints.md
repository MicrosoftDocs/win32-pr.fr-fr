---
description: Définit les points des objets actuellement sélectionnés sur l’objet de données sur les commandes copier et couper. Utilisé par le \_ message SHShellFolderView.
title: Message SFVM_SETPOINTS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d2c3e06a-19e4-4b78-9b7c-1a256582786e
api_name:
- SFVM_SETPOINTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1df501f162fb19335fcf1672299a74135672db22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210831"
---
# <a name="sfvm_setpoints-message"></a><span data-ttu-id="ce9f4-104">\_Message SFVM SetPoints</span><span class="sxs-lookup"><span data-stu-id="ce9f4-104">SFVM\_SETPOINTS message</span></span>

<span data-ttu-id="ce9f4-105">Définit les points des objets actuellement sélectionnés sur l’objet de données sur les commandes **copier** et **couper** .</span><span class="sxs-lookup"><span data-stu-id="ce9f4-105">Sets the points of the currently selected objects to the data object on **Copy** and **Cut** commands.</span></span> <span data-ttu-id="ce9f4-106">Utilisé par [**le \_ message SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="ce9f4-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_SETPOINTS 

    lParam = (LPARAM) pdtobj;

            
```



## <a name="parameters"></a><span data-ttu-id="ce9f4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce9f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce9f4-108">*pdtobj* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce9f4-108">*pdtobj* \[in\]</span></span>
</dt> <dd><span data-ttu-id="ce9f4-109">Pointeur vers un <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> des commandes **Copy** et **Cut** .</span><span class="sxs-lookup"><span data-stu-id="ce9f4-109">A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">**IDataObject**</a> of the **Copy** and **Cut** commands.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce9f4-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce9f4-110">Return value</span></span>

<span data-ttu-id="ce9f4-111">Retourne toujours zéro.</span><span class="sxs-lookup"><span data-stu-id="ce9f4-111">Always returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce9f4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ce9f4-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="ce9f4-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ce9f4-113">Requirements</span></span>



| <span data-ttu-id="ce9f4-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce9f4-114">Requirement</span></span> | <span data-ttu-id="ce9f4-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce9f4-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ce9f4-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce9f4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce9f4-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce9f4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ce9f4-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce9f4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce9f4-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce9f4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ce9f4-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce9f4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce9f4-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce9f4-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
