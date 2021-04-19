---
title: Message BCM_GETNOTE (commctrl. h)
description: Obtient le texte de la note associée à un bouton de lien de commande. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetNote macro.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527571"
---
# <a name="bcm_getnote-message"></a><span data-ttu-id="43b67-105">\_Message GETNOTE BCM</span><span class="sxs-lookup"><span data-stu-id="43b67-105">BCM\_GETNOTE message</span></span>

<span data-ttu-id="43b67-106">Obtient le texte de la note associée à un bouton de lien de commande.</span><span class="sxs-lookup"><span data-stu-id="43b67-106">Gets the text of the note associated with a command link button.</span></span> <span data-ttu-id="43b67-107">Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) macro.</span><span class="sxs-lookup"><span data-stu-id="43b67-107">You can send this message explicitly or use the [**Button\_GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="43b67-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43b67-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43b67-109">*wParam* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="43b67-109">*wParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="43b67-110">**Valeur DWORD** qui spécifie la taille de la mémoire tampon vers laquelle pointe *lParam*, en caractères.</span><span class="sxs-lookup"><span data-stu-id="43b67-110">A **DWORD** that specifies the size of the buffer pointed to by *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="43b67-111">*lParam* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="43b67-111">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43b67-112">Mémoire tampon de chaîne devant recevoir le texte.</span><span class="sxs-lookup"><span data-stu-id="43b67-112">The string buffer to receive the text.</span></span> <span data-ttu-id="43b67-113">La mémoire tampon doit être suffisamment grande pour contenir le caractère NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="43b67-113">The buffer must be large enough to accommodate the terminating NULL character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43b67-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43b67-114">Return value</span></span>

<span data-ttu-id="43b67-115">Si le message est correctement exécuté, la méthode retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="43b67-115">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="43b67-116">Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="43b67-116">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="43b67-117">Notes</span><span class="sxs-lookup"><span data-stu-id="43b67-117">Remarks</span></span>

<span data-ttu-id="43b67-118">Le **message \_ GETNOTE BCM** fonctionne uniquement avec les boutons qui ont le style de bouton [**BS \_ COMMANDLINK**](button-styles.md) ou [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="43b67-118">The **BCM\_GETNOTE** message works only with buttons that have the [**BS\_COMMANDLINK**](button-styles.md) or [**BS\_DEFCOMMANDLINK**](button-styles.md) button style.</span></span>

<span data-ttu-id="43b67-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) contient les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="43b67-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will contain:</span></span>

-   <span data-ttu-id="43b67-120">ERREUR \_ non \_ prise en charge, si le bouton n’a pas le style [**BS \_ DEFCOMMANDLINK**](button-styles.md) ou [**BS \_ COMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="43b67-120">ERROR\_NOT\_SUPPORTED, if the button does not have the [**BS\_DEFCOMMANDLINK**](button-styles.md) or [**BS\_COMMANDLINK**](button-styles.md) style.</span></span>
-   <span data-ttu-id="43b67-121">ERREUR \_ de \_ mémoire tampon insuffisante, si la mémoire tampon *lParam* est trop petite.</span><span class="sxs-lookup"><span data-stu-id="43b67-121">ERROR\_INSUFFICIENT\_BUFFER, if the *lParam* buffer is too small.</span></span> <span data-ttu-id="43b67-122">Le paramètre *wParam* contient la taille de mémoire tampon requise, en caractères.</span><span class="sxs-lookup"><span data-stu-id="43b67-122">The *wParam* parameter will contain the required buffer size, in characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="43b67-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43b67-123">Requirements</span></span>



| <span data-ttu-id="43b67-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43b67-124">Requirement</span></span> | <span data-ttu-id="43b67-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="43b67-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43b67-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43b67-126">Minimum supported client</span></span><br/> | <span data-ttu-id="43b67-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43b67-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43b67-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43b67-128">Minimum supported server</span></span><br/> | <span data-ttu-id="43b67-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43b67-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43b67-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="43b67-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="43b67-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="43b67-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43b67-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43b67-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="43b67-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="43b67-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="43b67-134">Styles de bouton</span><span class="sxs-lookup"><span data-stu-id="43b67-134">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="43b67-135">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="43b67-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="43b67-136">Types de bouton</span><span class="sxs-lookup"><span data-stu-id="43b67-136">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

