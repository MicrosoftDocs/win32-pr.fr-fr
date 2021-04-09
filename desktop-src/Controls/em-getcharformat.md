---
title: Message EM_GETCHARFORMAT (RichEdit. h)
description: Détermine la mise en forme des caractères dans un contrôle RichEdit.
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- EM_GETCHARFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032944"
---
# <a name="em_getcharformat-message"></a><span data-ttu-id="29c38-104">\_Message GETCHARFORMAT em</span><span class="sxs-lookup"><span data-stu-id="29c38-104">EM\_GETCHARFORMAT message</span></span>

<span data-ttu-id="29c38-105">Détermine la mise en forme des caractères dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="29c38-105">Determines the character formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="29c38-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29c38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29c38-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29c38-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29c38-108">Spécifie la plage de texte à partir de laquelle la mise en forme doit être récupérée.</span><span class="sxs-lookup"><span data-stu-id="29c38-108">Specifies the range of text from which to retrieve formatting.</span></span> <span data-ttu-id="29c38-109">Il peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="29c38-109">It can be one of the following values.</span></span>



| <span data-ttu-id="29c38-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="29c38-110">Value</span></span>                                                                                                                                                         | <span data-ttu-id="29c38-111">Signification</span><span class="sxs-lookup"><span data-stu-id="29c38-111">Meaning</span></span>                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <span data-ttu-id="29c38-112"><dt>**CSAH \_ par défaut**</dt></span><span class="sxs-lookup"><span data-stu-id="29c38-112"><dt>**SCF\_DEFAULT**</dt></span></span> </dl>       | <span data-ttu-id="29c38-113">Mise en forme de caractères par défaut.</span><span class="sxs-lookup"><span data-stu-id="29c38-113">The default character formatting.</span></span><br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <span data-ttu-id="29c38-114"><dt>**\_sélection SCF**</dt></span><span class="sxs-lookup"><span data-stu-id="29c38-114"><dt>**SCF\_SELECTION**</dt></span></span> </dl> | <span data-ttu-id="29c38-115">Mise en forme des caractères de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="29c38-115">The current selection's character formatting.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="29c38-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29c38-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29c38-117">Structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) qui reçoit les attributs du premier caractère.</span><span class="sxs-lookup"><span data-stu-id="29c38-117">A [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure that receives the attributes of the first character.</span></span> <span data-ttu-id="29c38-118">Le membre **dwMask** spécifie les attributs qui sont cohérents dans toute la sélection.</span><span class="sxs-lookup"><span data-stu-id="29c38-118">The **dwMask** member specifies which attributes are consistent throughout the entire selection.</span></span> <span data-ttu-id="29c38-119">Par exemple, si l’ensemble de la sélection est en italique ou non en italique, CFM \_ Italic est défini ; si la sélection est en partie en italique et partiellement non, cfm \_ Italic n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="29c38-119">For example, if the entire selection is either in italics or not in italics, CFM\_ITALIC is set; if the selection is partly in italics and partly not, CFM\_ITALIC is not set.</span></span>

<span data-ttu-id="29c38-120">Microsoft Rich Edit 2,0 et versions ultérieures : ce paramètre peut être un pointeur vers une structure [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , qui est une extension de la structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="29c38-120">Microsoft Rich Edit 2.0 and later: This parameter can be a pointer to a [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) structure, which is an extension of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span> <span data-ttu-id="29c38-121">Avant d’envoyer le message **\_ GETCHARFORMAT em** , définissez le membre **cbSize** de la structure pour indiquer la version de la structure.</span><span class="sxs-lookup"><span data-stu-id="29c38-121">Before sending the **EM\_GETCHARFORMAT** message, set the structure's **cbSize** member to indicate the version of the structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29c38-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29c38-122">Return value</span></span>

<span data-ttu-id="29c38-123">Ce message retourne la valeur du membre **dwMask** de la structure [**Charformat**](/windows/win32/api/richedit/ns-richedit-charformata) .</span><span class="sxs-lookup"><span data-stu-id="29c38-123">This message returns the value of the **dwMask** member of the [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="29c38-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29c38-124">Requirements</span></span>



| <span data-ttu-id="29c38-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29c38-125">Requirement</span></span> | <span data-ttu-id="29c38-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="29c38-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29c38-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29c38-127">Minimum supported client</span></span><br/> | <span data-ttu-id="29c38-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29c38-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29c38-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29c38-129">Minimum supported server</span></span><br/> | <span data-ttu-id="29c38-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29c38-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29c38-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="29c38-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="29c38-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="29c38-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29c38-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29c38-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="29c38-134">**Référence**</span><span class="sxs-lookup"><span data-stu-id="29c38-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="29c38-135">**CHARFORMAT**</span><span class="sxs-lookup"><span data-stu-id="29c38-135">**CHARFORMAT**</span></span>](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[<span data-ttu-id="29c38-136">**CHARFORMAT2**</span><span class="sxs-lookup"><span data-stu-id="29c38-136">**CHARFORMAT2**</span></span>](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





