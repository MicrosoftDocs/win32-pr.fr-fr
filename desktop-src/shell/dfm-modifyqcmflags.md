---
description: 'Permet au rappel de modifier les valeurs de CFM \_ xxx passées à IContextMenu :: QueryContextMenu.'
title: Message DFM_MODIFYQCMFLAGS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862122"
---
# <a name="dfm_modifyqcmflags-message"></a><span data-ttu-id="8df69-103">\_Message DFM MODIFYQCMFLAGS</span><span class="sxs-lookup"><span data-stu-id="8df69-103">DFM\_MODIFYQCMFLAGS message</span></span>

<span data-ttu-id="8df69-104">Permet au rappel de modifier les valeurs de CFM \_ xxx passées à [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="8df69-104">Allows the callback to modify the CFM\_XXX values passed to [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="8df69-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8df69-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df69-106">*puNewFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8df69-106">*puNewFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df69-107">Pointeur vers les nouvelles valeurs d’indicateur.</span><span class="sxs-lookup"><span data-stu-id="8df69-107">A pointer to the new flag values.</span></span>

</dd> <dt>

<span data-ttu-id="8df69-108">*uFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8df69-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df69-109">Indicateurs qui spécifient comment le menu contextuel peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="8df69-109">Flags that specify how the context menu can be changed.</span></span> <span data-ttu-id="8df69-110">Ce paramètre utilise les \_ valeurs CMF xxx décrites dans [**IContextMenu :: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="8df69-110">This parameter uses the CMF\_XXX values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8df69-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8df69-111">Requirements</span></span>



| <span data-ttu-id="8df69-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8df69-112">Requirement</span></span> | <span data-ttu-id="8df69-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="8df69-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8df69-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8df69-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8df69-115">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8df69-115">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8df69-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8df69-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8df69-117">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8df69-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8df69-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="8df69-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="8df69-119"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="8df69-119"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




