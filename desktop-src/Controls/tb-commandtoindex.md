---
title: Message TB_COMMANDTOINDEX (commctrl. h)
description: Récupère l’index de base zéro pour le bouton associé à l’identificateur de commande spécifié.
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- TB_COMMANDTOINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0257f55e01db59f1d23d59583f1ef78f44b1dac1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106606"
---
# <a name="tb_commandtoindex-message"></a><span data-ttu-id="81368-104">TO \_ COMMANDTOINDEX message</span><span class="sxs-lookup"><span data-stu-id="81368-104">TB\_COMMANDTOINDEX message</span></span>

<span data-ttu-id="81368-105">Récupère l’index de base zéro pour le bouton associé à l’identificateur de commande spécifié.</span><span class="sxs-lookup"><span data-stu-id="81368-105">Retrieves the zero-based index for the button associated with the specified command identifier.</span></span>

## <a name="parameters"></a><span data-ttu-id="81368-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81368-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81368-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81368-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="81368-108">Identificateur de commande associé au bouton.</span><span class="sxs-lookup"><span data-stu-id="81368-108">Command identifier associated with the button.</span></span>

</dd> <dt>

<span data-ttu-id="81368-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="81368-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="81368-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="81368-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81368-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81368-111">Return value</span></span>

<span data-ttu-id="81368-112">Retourne l’index de base zéro pour le bouton ou-1 si l’identificateur de commande spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="81368-112">Returns the zero-based index for the button or -1 if the specified command identifier is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="81368-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81368-113">Requirements</span></span>



| <span data-ttu-id="81368-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81368-114">Requirement</span></span> | <span data-ttu-id="81368-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="81368-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81368-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81368-116">Minimum supported client</span></span><br/> | <span data-ttu-id="81368-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81368-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81368-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81368-118">Minimum supported server</span></span><br/> | <span data-ttu-id="81368-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="81368-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81368-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="81368-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="81368-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81368-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





