---
title: Message TB_ADDSTRING (commctrl. h)
description: Ajoute une nouvelle chaîne au pool de chaînes de la barre d’outils.
ms.assetid: e22ee2cc-6443-49d3-aea6-a4ab256d4538
keywords:
- TB_ADDSTRING les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_ADDSTRING
- TB_ADDSTRINGA
- TB_ADDSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fba57c298a2b903a65c429ae6b4f9d55fc9ed2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509759"
---
# <a name="tb_addstring-message"></a><span data-ttu-id="0b1a9-104">TO \_ message ADDSTRING</span><span class="sxs-lookup"><span data-stu-id="0b1a9-104">TB\_ADDSTRING message</span></span>

<span data-ttu-id="0b1a9-105">Ajoute une nouvelle chaîne au pool de chaînes de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-105">Adds a new string to the toolbar's string pool.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b1a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b1a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b1a9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b1a9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b1a9-108">Handle de l’instance de module avec un fichier exécutable qui contient la ressource de chaîne.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-108">Handle to the module instance with an executable file that contains the string resource.</span></span> <span data-ttu-id="0b1a9-109">Si *lParam* pointe plutôt vers un tableau de caractères avec une ou plusieurs chaînes, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-109">If *lParam* instead points to a character array with one or more strings, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0b1a9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b1a9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b1a9-111">Identificateur de ressource de la ressource de type chaîne, ou pointeur vers un tableau TCHAR.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-111">Resource identifier for the string resource, or a pointer to a TCHAR array.</span></span> <span data-ttu-id="0b1a9-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-112">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b1a9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b1a9-113">Return value</span></span>

<span data-ttu-id="0b1a9-114">Retourne l’index de la première nouvelle chaîne en cas de réussite, ou-1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-114">Returns the index of the first new string if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b1a9-115">Notes</span><span class="sxs-lookup"><span data-stu-id="0b1a9-115">Remarks</span></span>

<span data-ttu-id="0b1a9-116">Si *wParam* a la **valeur null**, *lParam* pointe vers un tableau de caractères avec une ou plusieurs chaînes se terminant par un caractère null.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-116">If *wParam* is **NULL**, *lParam* points to a character array with one or more null-terminated strings.</span></span> <span data-ttu-id="0b1a9-117">La dernière chaîne dans le tableau doit se terminer par deux caractères null.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-117">The last string in the array must be terminated with two null characters.</span></span>

<span data-ttu-id="0b1a9-118">Si *wParam* est le HINSTANCE de l’application ou d’un autre module contenant une ressource de type chaîne, *lParam* est l’identificateur de ressource de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-118">If *wParam* is the HINSTANCE of the application or of another module containing a string resource, *lParam* is the resource identifier of the string.</span></span> <span data-ttu-id="0b1a9-119">Chaque élément de la chaîne doit commencer par un caractère de séparation arbitraire, et la chaîne doit se terminer par deux caractères.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-119">Each item in the string must begin with an arbitrary separator character, and the string must end with two such characters.</span></span> <span data-ttu-id="0b1a9-120">Par exemple, le texte de trois boutons peut apparaître dans la table de chaînes sous la forme « /New/Open/Save// ».</span><span class="sxs-lookup"><span data-stu-id="0b1a9-120">For example, the text for three buttons might appear in the string table as "/New/Open/Save//".</span></span> <span data-ttu-id="0b1a9-121">Le message retourne l’index de « New » dans le pool de chaînes de la barre d’outils, et les autres éléments se trouvent à des positions consécutives.</span><span class="sxs-lookup"><span data-stu-id="0b1a9-121">The message returns the index of "New" in the toolbar's string pool, and the other items are in consecutive positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b1a9-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b1a9-122">Requirements</span></span>



| <span data-ttu-id="0b1a9-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b1a9-123">Requirement</span></span> | <span data-ttu-id="0b1a9-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b1a9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0b1a9-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b1a9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0b1a9-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b1a9-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0b1a9-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b1a9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0b1a9-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b1a9-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0b1a9-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b1a9-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b1a9-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b1a9-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0b1a9-131">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="0b1a9-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0b1a9-132">**To \_ ADDSTRINGW** (Unicode) et **to \_ ADDSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0b1a9-132">**TB\_ADDSTRINGW** (Unicode) and **TB\_ADDSTRINGA** (ANSI)</span></span><br/>                 |



 

 





