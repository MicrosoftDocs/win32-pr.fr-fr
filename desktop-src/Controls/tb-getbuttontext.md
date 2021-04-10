---
title: Message TB_GETBUTTONTEXT (commctrl. h)
description: Récupère le texte d’affichage d’un bouton dans une barre d’outils.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- TB_GETBUTTONTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ac0b238574cc136f41959b57f3f0e1ec13e3ea1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104182"
---
# <a name="tb_getbuttontext-message"></a><span data-ttu-id="f7d38-104">TO \_ GETBUTTONTEXT message</span><span class="sxs-lookup"><span data-stu-id="f7d38-104">TB\_GETBUTTONTEXT message</span></span>

<span data-ttu-id="f7d38-105">Récupère le texte d’affichage d’un bouton dans une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="f7d38-105">Retrieves the display text of a button on a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f7d38-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7d38-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d38-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f7d38-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d38-108">Identificateur de commande du bouton dont le texte doit être récupéré.</span><span class="sxs-lookup"><span data-stu-id="f7d38-108">Command identifier of the button whose text is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="f7d38-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f7d38-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d38-110">Pointeur vers une mémoire tampon qui reçoit le texte du bouton.</span><span class="sxs-lookup"><span data-stu-id="f7d38-110">Pointer to a buffer that receives the button text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d38-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7d38-111">Return value</span></span>

<span data-ttu-id="f7d38-112">Retourne la longueur, en caractères, de la chaîne désignée par *lParam*.</span><span class="sxs-lookup"><span data-stu-id="f7d38-112">Returns the length, in characters, of the string pointed to by *lParam*.</span></span> <span data-ttu-id="f7d38-113">La longueur n’inclut pas le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="f7d38-113">The length does not include the terminating null character.</span></span> <span data-ttu-id="f7d38-114">En cas d’échec, la valeur de retour est-1.</span><span class="sxs-lookup"><span data-stu-id="f7d38-114">If unsuccessful, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7d38-115">Notes</span><span class="sxs-lookup"><span data-stu-id="f7d38-115">Remarks</span></span>

<span data-ttu-id="f7d38-116">**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="f7d38-116">**Security Warning:** Using this message incorrectly might compromise the security of your program.</span></span> <span data-ttu-id="f7d38-117">Ce message n’offre aucun moyen de connaître la taille de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f7d38-117">This message does not provide a way for you to know the size of the buffer.</span></span> <span data-ttu-id="f7d38-118">Si vous utilisez ce message, appelez tout d’abord le message qui passe **null** dans *lParam*, ce qui renvoie le nombre de caractères, à l’exception de la **valeur null** requise.</span><span class="sxs-lookup"><span data-stu-id="f7d38-118">If you use this message, first call the message passing **NULL** in the *lParam*, this returns the number of characters, excluding **NULL** that are required.</span></span> <span data-ttu-id="f7d38-119">Ensuite, appelez le message une seconde fois pour récupérer la chaîne.</span><span class="sxs-lookup"><span data-stu-id="f7d38-119">Then call the message a second time to retrieve the string.</span></span> <span data-ttu-id="f7d38-120">Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="f7d38-120">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

<span data-ttu-id="f7d38-121">La chaîne retournée correspond au texte actuellement affiché par le bouton.</span><span class="sxs-lookup"><span data-stu-id="f7d38-121">The returned string corresponds to the text that is currently displayed by the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d38-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7d38-122">Requirements</span></span>



| <span data-ttu-id="f7d38-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7d38-123">Requirement</span></span> | <span data-ttu-id="f7d38-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7d38-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d38-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7d38-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d38-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7d38-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f7d38-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f7d38-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d38-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f7d38-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f7d38-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7d38-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7d38-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7d38-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f7d38-131">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="f7d38-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f7d38-132">**To \_ GETBUTTONTEXTW** (Unicode) et **to \_ GETBUTTONTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f7d38-132">**TB\_GETBUTTONTEXTW** (Unicode) and **TB\_GETBUTTONTEXTA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="f7d38-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7d38-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="f7d38-134">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f7d38-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f7d38-135">**TO \_ GETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="f7d38-135">**TB\_GETBUTTONINFO**</span></span>](tb-getbuttoninfo.md)
</dt> <dt>

[<span data-ttu-id="f7d38-136">**TO \_ GETSTRING**</span><span class="sxs-lookup"><span data-stu-id="f7d38-136">**TB\_GETSTRING**</span></span>](tb-getstring.md)
</dt> <dt>

[<span data-ttu-id="f7d38-137">**TO \_ SETBUTTONINFO**</span><span class="sxs-lookup"><span data-stu-id="f7d38-137">**TB\_SETBUTTONINFO**</span></span>](tb-setbuttoninfo.md)
</dt> </dl>

 

 





