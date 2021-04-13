---
title: Message TB_GETHOTITEM (commctrl. h)
description: Récupère l’index de l’élément réactif dans une barre d’outils.
ms.assetid: a87dbfc3-c6be-4a0a-9b6a-301b900d7929
keywords:
- TB_GETHOTITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829864cc9223ba15b49b1ecc623f294fd4a6b4fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465031"
---
# <a name="tb_gethotitem-message"></a><span data-ttu-id="191dc-104">TO \_ GETHOTITEM message</span><span class="sxs-lookup"><span data-stu-id="191dc-104">TB\_GETHOTITEM message</span></span>

<span data-ttu-id="191dc-105">Récupère l’index de l’élément réactif dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="191dc-105">Retrieves the index of the hot item in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="191dc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="191dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="191dc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="191dc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="191dc-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="191dc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="191dc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="191dc-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="191dc-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="191dc-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="191dc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="191dc-111">Return value</span></span>

<span data-ttu-id="191dc-112">Retourne l’index de l’élément réactif, ou-1 si aucun élément réactif n’est défini.</span><span class="sxs-lookup"><span data-stu-id="191dc-112">Returns the index of the hot item, or -1 if no hot item is set.</span></span> <span data-ttu-id="191dc-113">Les contrôles Toolbar qui n’ont pas le style [**TBSTYLE \_ Flat**](toolbar-control-and-button-styles.md) n’ont pas d’éléments chauds.</span><span class="sxs-lookup"><span data-stu-id="191dc-113">Toolbar controls that do not have the [**TBSTYLE\_FLAT**](toolbar-control-and-button-styles.md) style do not have hot items.</span></span>

## <a name="requirements"></a><span data-ttu-id="191dc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="191dc-114">Requirements</span></span>



| <span data-ttu-id="191dc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="191dc-115">Requirement</span></span> | <span data-ttu-id="191dc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="191dc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="191dc-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="191dc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="191dc-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="191dc-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="191dc-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="191dc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="191dc-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="191dc-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="191dc-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="191dc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="191dc-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="191dc-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





