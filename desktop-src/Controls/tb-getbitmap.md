---
title: Message TB_GETBITMAP (commctrl. h)
description: Récupère l’index de l’image bitmap associée à un bouton dans une barre d’outils.
ms.assetid: 64878cca-7d71-48ad-b2ed-d2bdc3067592
keywords:
- TB_GETBITMAP les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771073b67b1421a5d9bda9d162bc234400c85885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942910"
---
# <a name="tb_getbitmap-message"></a><span data-ttu-id="0700c-104">TO \_ GETBITMAP message</span><span class="sxs-lookup"><span data-stu-id="0700c-104">TB\_GETBITMAP message</span></span>

<span data-ttu-id="0700c-105">Récupère l’index de l’image bitmap associée à un bouton dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="0700c-105">Retrieves the index of the bitmap associated with a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0700c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0700c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0700c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0700c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0700c-108">Identificateur de commande du bouton dont l’index bitmap doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="0700c-108">Command identifier of the button whose bitmap index is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="0700c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0700c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="0700c-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0700c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0700c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0700c-111">Return value</span></span>

<span data-ttu-id="0700c-112">Retourne l’index de l’image bitmap en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0700c-112">Returns the index of the bitmap if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0700c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0700c-113">Requirements</span></span>



| <span data-ttu-id="0700c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0700c-114">Requirement</span></span> | <span data-ttu-id="0700c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0700c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0700c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0700c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0700c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0700c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0700c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0700c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0700c-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0700c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0700c-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="0700c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0700c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0700c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





