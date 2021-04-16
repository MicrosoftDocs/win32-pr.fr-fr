---
title: Message EM_EXLINEFROMCHAR (RichEdit. h)
description: Détermine la ligne qui contient le caractère spécifié dans un contrôle RichEdit.
ms.assetid: 497482fb-9640-4063-a9f5-e0691b65225d
keywords:
- EM_EXLINEFROMCHAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_EXLINEFROMCHAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce904725c5dc63732bae07cfaa95b41558db11d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479468"
---
# <a name="em_exlinefromchar-message"></a><span data-ttu-id="855da-104">\_Message EXLINEFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="855da-104">EM\_EXLINEFROMCHAR message</span></span>

<span data-ttu-id="855da-105">Détermine la ligne qui contient le caractère spécifié dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="855da-105">Determines which line contains the specified character in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="855da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="855da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="855da-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="855da-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="855da-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="855da-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="855da-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="855da-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="855da-110">Index de base zéro du caractère.</span><span class="sxs-lookup"><span data-stu-id="855da-110">Zero-based index of the character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="855da-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="855da-111">Return value</span></span>

<span data-ttu-id="855da-112">Ce message retourne l’index de base zéro de la ligne.</span><span class="sxs-lookup"><span data-stu-id="855da-112">This message returns the zero-based index of the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="855da-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="855da-113">Requirements</span></span>



| <span data-ttu-id="855da-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="855da-114">Requirement</span></span> | <span data-ttu-id="855da-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="855da-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="855da-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="855da-116">Minimum supported client</span></span><br/> | <span data-ttu-id="855da-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="855da-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="855da-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="855da-118">Minimum supported server</span></span><br/> | <span data-ttu-id="855da-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="855da-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="855da-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="855da-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="855da-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="855da-121"><dt>Richedit.h</dt></span></span> </dl> |



 

 





