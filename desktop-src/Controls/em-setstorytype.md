---
title: Message EM_SETSTORYTYPE (RichEdit. h)
description: Définit le type d’histoire.
ms.assetid: 8FA335E1-EE0A-4F31-B800-C79F617A6019
keywords:
- EM_SETSTORYTYPE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be6d1df04f93fca0119b58f978a6a0cb36ddf464
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843362"
---
# <a name="em_setstorytype-message"></a><span data-ttu-id="70201-104">\_Message SETSTORYTYPE em</span><span class="sxs-lookup"><span data-stu-id="70201-104">EM\_SETSTORYTYPE message</span></span>

<span data-ttu-id="70201-105">Définit le type d’histoire.</span><span class="sxs-lookup"><span data-stu-id="70201-105">Sets the story type.</span></span>


```C++
#define EM_SETSTORYTYPE       (WM_USER + 291)
```



## <a name="parameters"></a><span data-ttu-id="70201-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70201-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70201-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70201-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70201-108">Index de l’histoire.</span><span class="sxs-lookup"><span data-stu-id="70201-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="70201-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70201-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70201-110">Type du nouveau récit.</span><span class="sxs-lookup"><span data-stu-id="70201-110">The new story type.</span></span> <span data-ttu-id="70201-111">Pour obtenir la liste des types de récits, consultez [**em \_ GETSTORYTYPE**](em-getstorytype.md).</span><span class="sxs-lookup"><span data-stu-id="70201-111">For a list of story types, see [**EM\_GETSTORYTYPE**](em-getstorytype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70201-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="70201-112">Return value</span></span>

<span data-ttu-id="70201-113">Type d’histoire qui a été défini.</span><span class="sxs-lookup"><span data-stu-id="70201-113">The story type that was set.</span></span>

## <a name="requirements"></a><span data-ttu-id="70201-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70201-114">Requirements</span></span>



| <span data-ttu-id="70201-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70201-115">Requirement</span></span> | <span data-ttu-id="70201-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="70201-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70201-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70201-117">Minimum supported client</span></span><br/> | <span data-ttu-id="70201-118">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70201-118">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="70201-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70201-119">Minimum supported server</span></span><br/> | <span data-ttu-id="70201-120">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70201-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70201-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="70201-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="70201-122"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="70201-122"><dt>Richedit.h</dt></span></span> </dl> |



 

 





