---
title: Message SB_GETTIPTEXT (commctrl. h)
description: Récupère le texte d’info-bulle pour un composant dans une barre d’État. La barre d’État doit être créée avec le \_ style info-bulles SBT pour activer les info-bulles.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- SB_GETTIPTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844001"
---
# <a name="sb_gettiptext-message"></a><span data-ttu-id="85534-105">\_Message SB GETTIPTEXT</span><span class="sxs-lookup"><span data-stu-id="85534-105">SB\_GETTIPTEXT message</span></span>

<span data-ttu-id="85534-106">Récupère le texte d’info-bulle pour un composant dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="85534-106">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="85534-107">La barre d’État doit être créée avec le style [**\_ info-bulles SBT**](status-bar-styles.md) pour activer les info-bulles.</span><span class="sxs-lookup"><span data-stu-id="85534-107">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="85534-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85534-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85534-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="85534-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85534-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie l’index de base zéro de la partie qui reçoit le texte info-bulle.</span><span class="sxs-lookup"><span data-stu-id="85534-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the part that receives the tooltip text.</span></span> <span data-ttu-id="85534-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la taille de la mémoire tampon au niveau de *lParam*, en caractères.</span><span class="sxs-lookup"><span data-stu-id="85534-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the size of the buffer at *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="85534-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="85534-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="85534-113">Pointeur vers une mémoire tampon de caractères qui reçoit le texte d’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="85534-113">Pointer to a character buffer that receives the tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85534-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85534-114">Return value</span></span>

<span data-ttu-id="85534-115">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="85534-115">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="85534-116">Notes</span><span class="sxs-lookup"><span data-stu-id="85534-116">Remarks</span></span>

<span data-ttu-id="85534-117">**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut entraîner des problèmes pour votre application.</span><span class="sxs-lookup"><span data-stu-id="85534-117">**Security Warning:** Using this message incorrectly can cause problems for your application.</span></span> <span data-ttu-id="85534-118">Par exemple, si le texte est trop grand pour la mémoire tampon *lParam* , cela peut provoquer un dépassement de capacité de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="85534-118">For example, if the text is too large for the *lParam* buffer, it could cause a buffer overflow.</span></span> <span data-ttu-id="85534-119">Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="85534-119">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="85534-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85534-120">Requirements</span></span>



| <span data-ttu-id="85534-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85534-121">Requirement</span></span> | <span data-ttu-id="85534-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="85534-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85534-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85534-123">Minimum supported client</span></span><br/> | <span data-ttu-id="85534-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85534-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="85534-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85534-125">Minimum supported server</span></span><br/> | <span data-ttu-id="85534-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85534-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="85534-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="85534-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="85534-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="85534-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="85534-129">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="85534-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="85534-130">**SB \_ GETTIPTEXTW** (Unicode) et **SB \_ GETTIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="85534-130">**SB\_GETTIPTEXTW** (Unicode) and **SB\_GETTIPTEXTA** (ANSI)</span></span><br/>               |



 

