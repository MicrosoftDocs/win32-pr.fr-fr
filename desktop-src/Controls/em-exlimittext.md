---
title: Message EM_EXLIMITTEXT (RichEdit. h)
description: Définit une limite supérieure de la quantité de texte que l’utilisateur peut taper ou coller dans un contrôle RichEdit.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- EM_EXLIMITTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465895"
---
# <a name="em_exlimittext-message"></a><span data-ttu-id="8f4b3-104">\_Message EXLIMITTEXT em</span><span class="sxs-lookup"><span data-stu-id="8f4b3-104">EM\_EXLIMITTEXT message</span></span>

<span data-ttu-id="8f4b3-105">Définit une limite supérieure de la quantité de texte que l’utilisateur peut taper ou coller dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="8f4b3-105">Sets an upper limit to the amount of text the user can type or paste into a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8f4b3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8f4b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f4b3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8f4b3-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f4b3-108">Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="8f4b3-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8f4b3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8f4b3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8f4b3-110">Spécifie la quantité maximale de texte qui peut être entrée.</span><span class="sxs-lookup"><span data-stu-id="8f4b3-110">Specifies the maximum amount of text that can be entered.</span></span> <span data-ttu-id="8f4b3-111">Si ce paramètre est égal à zéro, la valeur maximale par défaut est utilisée, qui est de 64 000 caractères.</span><span class="sxs-lookup"><span data-stu-id="8f4b3-111">If this parameter is zero, the default maximum is used, which is 64K characters.</span></span> <span data-ttu-id="8f4b3-112">Un objet COM compte comme un caractère unique.</span><span class="sxs-lookup"><span data-stu-id="8f4b3-112">A COM object counts as a single character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f4b3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8f4b3-113">Return value</span></span>

<span data-ttu-id="8f4b3-114">Ce message ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8f4b3-114">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8f4b3-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8f4b3-115">Remarks</span></span>

<span data-ttu-id="8f4b3-116">La limite de texte définie par le message **em \_ EXLIMITTEXT** ne limite pas la quantité de texte que vous pouvez diffuser dans un contrôle RichEdit en utilisant le message de [**\_ flux em**](em-streamin.md) avec *lParam* défini sur le \_ texte DF.</span><span class="sxs-lookup"><span data-stu-id="8f4b3-116">The text limit set by the **EM\_EXLIMITTEXT** message does not limit the amount of text that you can stream into a rich edit control using the [**EM\_STREAMIN**](em-streamin.md) message with *lParam* set to SF\_TEXT.</span></span> <span data-ttu-id="8f4b3-117">Toutefois, elle limite la quantité de texte que vous pouvez diffuser dans un contrôle RichEdit à l’aide du message de **\_ flux em** avec *lParam* défini sur DF \_ RTF.</span><span class="sxs-lookup"><span data-stu-id="8f4b3-117">However, it does limit the amount of text that you can stream into a rich edit control using the **EM\_STREAMIN** message with *lParam* set to SF\_RTF.</span></span>

<span data-ttu-id="8f4b3-118">Avant l’appel de **em \_ EXLIMITTEXT** , la limite par défaut de la quantité de texte qu’un utilisateur peut entrer est de 32 767 caractères.</span><span class="sxs-lookup"><span data-stu-id="8f4b3-118">Before **EM\_EXLIMITTEXT** is called, the default limit to the amount of text a user can enter is 32,767 characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f4b3-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8f4b3-119">Requirements</span></span>



| <span data-ttu-id="8f4b3-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8f4b3-120">Requirement</span></span> | <span data-ttu-id="8f4b3-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="8f4b3-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8f4b3-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f4b3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8f4b3-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f4b3-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8f4b3-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8f4b3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8f4b3-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8f4b3-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8f4b3-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="8f4b3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f4b3-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f4b3-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f4b3-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8f4b3-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f4b3-129">**\_flux em**</span><span class="sxs-lookup"><span data-stu-id="8f4b3-129">**EM\_STREAMIN**</span></span>](em-streamin.md)
</dt> </dl>

 

 





