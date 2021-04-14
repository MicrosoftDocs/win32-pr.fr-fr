---
title: Message ACM_OPEN (commctrl. h)
description: Ouvre un clip AVI et affiche sa première image dans un contrôle d’animation. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro animer \_ ouvrir ou animer \_ OpenEx. Nous vous recommandons d’utiliser la version Unicode de ce message, ACM \_ OPENW.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- ACM_OPEN les contrôles de message Windows
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0588c0e321efe5cace63baf4016dbaa97f735252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384131"
---
# <a name="acm_open-message"></a><span data-ttu-id="54b0b-106">\_Message d’ouverture ACM</span><span class="sxs-lookup"><span data-stu-id="54b0b-106">ACM\_OPEN message</span></span>

<span data-ttu-id="54b0b-107">Ouvre un clip AVI et affiche sa première image dans un contrôle d’animation.</span><span class="sxs-lookup"><span data-stu-id="54b0b-107">Opens an AVI clip and displays its first frame in an animation control.</span></span> <span data-ttu-id="54b0b-108">Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**animer \_ ouvrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ou [**animer \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) .</span><span class="sxs-lookup"><span data-stu-id="54b0b-108">You can send this message explicitly or use the [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) or [**Animate\_OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) macro.</span></span> <span data-ttu-id="54b0b-109">Nous vous recommandons d’utiliser la version Unicode de ce message, ACM \_ OPENW.</span><span class="sxs-lookup"><span data-stu-id="54b0b-109">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

## <a name="parameters"></a><span data-ttu-id="54b0b-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54b0b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54b0b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54b0b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54b0b-112">[Version 4,71](common-control-versions.md) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="54b0b-112">[Version 4.71](common-control-versions.md) and later.</span></span> <span data-ttu-id="54b0b-113">Handle d’instance du module à partir duquel la ressource doit être chargée.</span><span class="sxs-lookup"><span data-stu-id="54b0b-113">An instance handle to the module from which the resource should be loaded.</span></span> <span data-ttu-id="54b0b-114">Définissez cette valeur sur **null** pour que le contrôle utilise la valeur HINSTANCE utilisée pour créer la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="54b0b-114">Set this value to **NULL** to have the control use the HINSTANCE value used to create the window.</span></span> <span data-ttu-id="54b0b-115">Notez que si la fenêtre est créée par une DLL, la valeur par défaut de *wParam* est la valeur HINSTANCE de la dll, et non celle de l’application qui appelle la dll.</span><span class="sxs-lookup"><span data-stu-id="54b0b-115">Note that if the window is created by a DLL, the default value for *wParam* is the HINSTANCE value of the DLL, not of the application that calls the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="54b0b-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54b0b-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54b0b-117">Pointeur vers une mémoire tampon qui contient le chemin d’accès du fichier AVI ou le nom d’une ressource AVI.</span><span class="sxs-lookup"><span data-stu-id="54b0b-117">A pointer to a buffer that contains the path of the AVI file or the name of an AVI resource.</span></span> <span data-ttu-id="54b0b-118">Ce paramètre peut également être constitué de l’identificateur de ressource AVI dans [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et de zéro dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="54b0b-118">Alternatively, this parameter can consist of the AVI resource identifier in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and zero in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span> <span data-ttu-id="54b0b-119">Pour créer cette valeur, utilisez la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) .</span><span class="sxs-lookup"><span data-stu-id="54b0b-119">To create this value, use the [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) macro.</span></span> <span data-ttu-id="54b0b-120">Le contrôle charge la ressource AVI à partir du module spécifié par le handle d’instance passé à la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) , à la macro de création d' [**animation \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) ou à la fonction de création de boîte de dialogue qui a créé le contrôle.</span><span class="sxs-lookup"><span data-stu-id="54b0b-120">The control loads the AVI resource from the module specified by the instance handle passed to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function, the [**Animate\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) macro, or the dialog box creation function that created the control.</span></span> <span data-ttu-id="54b0b-121">Dans la [Version 4,71](common-control-versions.md) et les versions ultérieures, la ressource est chargée à partir du module spécifié par *wParam*.</span><span class="sxs-lookup"><span data-stu-id="54b0b-121">In [Version 4.71](common-control-versions.md) and later, the resource is loaded from the module specified by *wParam*.</span></span> <span data-ttu-id="54b0b-122">Une ressource AVI doit avoir le type « AVI ».</span><span class="sxs-lookup"><span data-stu-id="54b0b-122">An AVI resource must have the "AVI" type.</span></span> <span data-ttu-id="54b0b-123">Si ce paramètre a la **valeur null**, le système ferme le fichier AVI précédemment ouvert pour le contrôle d’animation spécifié, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="54b0b-123">If this parameter is **NULL**, the system closes the AVI file that was previously opened for the specified animation control, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54b0b-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54b0b-124">Return value</span></span>

<span data-ttu-id="54b0b-125">Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="54b0b-125">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="54b0b-126">Notes</span><span class="sxs-lookup"><span data-stu-id="54b0b-126">Remarks</span></span>

<span data-ttu-id="54b0b-127">Le fichier ou la ressource AVI spécifié par *lpszName* ne doit pas contenir de données audio.</span><span class="sxs-lookup"><span data-stu-id="54b0b-127">The AVI file or resource specified by *lpszName* must not contain audio.</span></span>

<span data-ttu-id="54b0b-128">Nous vous recommandons d’utiliser la version Unicode de ce message, ACM \_ OPENW.</span><span class="sxs-lookup"><span data-stu-id="54b0b-128">We recommend using the Unicode version of this message, ACM\_OPENW.</span></span>

<span data-ttu-id="54b0b-129">Vous ne pouvez ouvrir que des clips AVI en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="54b0b-129">You can only open silent AVI clips.</span></span> <span data-ttu-id="54b0b-130">Le composant ACM \_ Open et [**Animate \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) échoue si *lParam* spécifie un clip AVI contenant du son.</span><span class="sxs-lookup"><span data-stu-id="54b0b-130">ACM\_OPEN and [**Animate\_Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) fail if *lParam* specifies an AVI clip that contains sound.</span></span>

<span data-ttu-id="54b0b-131">Vous pouvez utiliser l' [**animation \_ Fermer**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) pour fermer un fichier AVI ou une ressource AVI précédemment ouverte pour le contrôle d’animation spécifié.</span><span class="sxs-lookup"><span data-stu-id="54b0b-131">You can use [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) to close an AVI file or AVI resource that was previously opened for the specified animation control.</span></span>

## <a name="requirements"></a><span data-ttu-id="54b0b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54b0b-132">Requirements</span></span>



| <span data-ttu-id="54b0b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54b0b-133">Requirement</span></span> | <span data-ttu-id="54b0b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="54b0b-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54b0b-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54b0b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="54b0b-136">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54b0b-136">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54b0b-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54b0b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="54b0b-138">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54b0b-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54b0b-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="54b0b-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="54b0b-140"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="54b0b-140"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="54b0b-141">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="54b0b-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="54b0b-142">**ACM \_ OPENW** (Unicode) et **ACM \_ Opena** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="54b0b-142">**ACM\_OPENW** (Unicode) and **ACM\_OPENA** (ANSI)</span></span><br/>                         |



 

