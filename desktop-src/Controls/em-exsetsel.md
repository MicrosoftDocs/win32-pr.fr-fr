---
title: Message EM_EXSETSEL (RichEdit. h)
description: Sélectionne une plage de caractères ou des objets COM (Component Object Model) dans un contrôle Rich Edit Microsoft.
ms.assetid: 85a0d1d4-1826-4ac5-b823-de81a051441d
keywords:
- EM_EXSETSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_EXSETSEL
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6939156fb1a8f35e03527e64a4c6f5185180668d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843821"
---
# <a name="em_exsetsel-message"></a><span data-ttu-id="1bf94-104">\_Message EXSETSEL em</span><span class="sxs-lookup"><span data-stu-id="1bf94-104">EM\_EXSETSEL message</span></span>

<span data-ttu-id="1bf94-105">Sélectionne une plage de caractères ou des objets COM (Component Object Model) dans un contrôle Rich Edit Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1bf94-105">Selects a range of characters or Component Object Model (COM) objects in a Microsoft Rich Edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1bf94-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bf94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1bf94-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1bf94-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bf94-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1bf94-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="1bf94-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1bf94-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1bf94-110">Structure [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) qui spécifie la plage de sélection.</span><span class="sxs-lookup"><span data-stu-id="1bf94-110">A [**CHARRANGE**](/windows/desktop/api/Richedit/ns-richedit-charrange) structure that specifies the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1bf94-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1bf94-111">Return value</span></span>

<span data-ttu-id="1bf94-112">La valeur de retour est la sélection qui est réellement définie.</span><span class="sxs-lookup"><span data-stu-id="1bf94-112">The return value is the selection that is actually set.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf94-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bf94-113">Requirements</span></span>



| <span data-ttu-id="1bf94-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bf94-114">Requirement</span></span> | <span data-ttu-id="1bf94-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bf94-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf94-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bf94-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1bf94-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bf94-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1bf94-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bf94-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1bf94-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bf94-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1bf94-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bf94-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1bf94-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="1bf94-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





