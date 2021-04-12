---
title: Message EM_FILELINEFROMCHAR (CommCtrl. h)
description: Obtient l’index de la ligne qui contient l’index de caractère spécifié dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_FILELINEFROMCHAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FILELINEFROMCHAR
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a083d7e12822eacfb1e29a7d4bfd2ea705f2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465718"
---
# <a name="em_filelinefromchar-message"></a><span data-ttu-id="4e5e9-104">\_Message FILELINEFROMCHAR em</span><span class="sxs-lookup"><span data-stu-id="4e5e9-104">EM\_FILELINEFROMCHAR message</span></span>

<span data-ttu-id="4e5e9-105">Obtient l’index de la ligne qui contient l’index de caractère spécifié dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-105">Gets the index of the line that contains the specified character index in a multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="4e5e9-106">Un index de caractère est l’index de base zéro du caractère à partir du début du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e5e9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e5e9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e5e9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4e5e9-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e5e9-109">Index de caractère du caractère contenu dans la ligne dont le nombre doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-109">The character index of the character contained in the line whose number is to be retrieved.</span></span> <span data-ttu-id="4e5e9-110">Si ce paramètre a la valeur-1, **em \_ FILELINEFROMCHAR** récupère le numéro de ligne de la ligne active (la ligne qui contient le signe insertion) ou, s’il y a une sélection, le numéro de ligne de la ligne contenant le début de la sélection.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-110">If this parameter is -1, **EM\_FILELINEFROMCHAR** retrieves either the line number of the current line (the line containing the caret) or, if there is a selection, the line number of the line containing the beginning of the selection.</span></span>

</dd> <dt>

<span data-ttu-id="4e5e9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4e5e9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4e5e9-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e5e9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e5e9-113">Return value</span></span>

<span data-ttu-id="4e5e9-114">La valeur de retour est le numéro de ligne de base zéro de la ligne contenant l’index de caractère spécifié par *wParam*, indépendamment de la façon dont les lignes sont affichées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-114">The return value is the zero-based line number of the line containing the character index specified by *wParam*, independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e5e9-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e5e9-115">Requirements</span></span>



| <span data-ttu-id="4e5e9-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e5e9-116">Requirement</span></span> | <span data-ttu-id="4e5e9-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e5e9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e5e9-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e5e9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4e5e9-119">Applications de bureau Windows 10, 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e5e9-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4e5e9-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4e5e9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4e5e9-121">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4e5e9-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4e5e9-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e5e9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e5e9-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4e5e9-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e5e9-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e5e9-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e5e9-125">**Référence**</span><span class="sxs-lookup"><span data-stu-id="4e5e9-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="4e5e9-126">**\_FILELINEINDEX em**</span><span class="sxs-lookup"><span data-stu-id="4e5e9-126">**EM\_FILELINEINDEX**</span></span>](em-filelineindex.md)
</dt> </dl>

 

 





