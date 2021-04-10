---
title: Message EM_FILELINEINDEX (CommCtrl. h)
description: Obtient l’index de caractère du premier caractère d’une ligne spécifiée dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.
ms.assetid: vs|controls|~\controls\editcontrols\editcontrolreference\editcontrolmessages\em_lineindex.htm
keywords:
- EM_FILELINEINDEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FILELINEINDEX
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4ce5f5ca07fc9fb9869898965422c7c8a6aa3fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104227"
---
# <a name="em_filelineindex-message-commctrlh"></a><span data-ttu-id="702bf-104">Message EM_FILELINEINDEX (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="702bf-104">EM_FILELINEINDEX message (CommCtrl.h)</span></span>

<span data-ttu-id="702bf-105">Obtient l’index de caractère du premier caractère d’une ligne spécifiée dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.</span><span class="sxs-lookup"><span data-stu-id="702bf-105">Gets the character index of the first character of a specified line in a multiline edit control, independently of how lines are displayed on the screen..</span></span> <span data-ttu-id="702bf-106">Un index de caractère est l’index de base zéro du caractère à partir du début du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="702bf-106">A character index is the zero-based index of the character from the beginning of the edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="702bf-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="702bf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="702bf-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="702bf-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="702bf-109">Numéro de ligne de base zéro.</span><span class="sxs-lookup"><span data-stu-id="702bf-109">The zero-based line number.</span></span> <span data-ttu-id="702bf-110">La valeur-1 spécifie le numéro de la ligne active (la ligne qui contient le signe insertion).</span><span class="sxs-lookup"><span data-stu-id="702bf-110">A value of -1 specifies the current line number (the line that contains the caret).</span></span>

</dd> <dt>

<span data-ttu-id="702bf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="702bf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="702bf-112">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="702bf-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="702bf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="702bf-113">Return value</span></span>

<span data-ttu-id="702bf-114">La valeur de retour est l’index de caractère de la ligne spécifiée dans le paramètre *wParam* , indépendamment de la façon dont les lignes sont affichées à l’écran, ou a la valeur-1 si le numéro de ligne spécifié est supérieur au nombre de lignes dans le contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="702bf-114">The return value is the character index of the line specified in the *wParam* parameter, independently of how lines are displayed on the screen, or it is -1 if the specified line number is greater than the number of lines in the edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="702bf-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="702bf-115">Requirements</span></span>



| <span data-ttu-id="702bf-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="702bf-116">Requirement</span></span> | <span data-ttu-id="702bf-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="702bf-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="702bf-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="702bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="702bf-119">Applications de bureau Windows 10, 1809 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="702bf-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="702bf-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="702bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="702bf-121">Applications de bureau Windows Server 2019 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="702bf-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="702bf-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="702bf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="702bf-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="702bf-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="702bf-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="702bf-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="702bf-125">**\_FILELINEFROMCHAR em**</span><span class="sxs-lookup"><span data-stu-id="702bf-125">**EM\_FILELINEFROMCHAR**</span></span>](em-filelinefromchar.md)
</dt> </dl>

 

 





