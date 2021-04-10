---
title: Message TDM_NAVIGATE_PAGE (commctrl. h)
description: Recrée une boîte de dialogue de tâches avec le nouveau contenu, en simulant la fonctionnalité d’un Assistant multipage.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- TDM_NAVIGATE_PAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56fc86e0e4fe457a43e035ed5d568e91303c7fcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942757"
---
# <a name="tdm_navigate_page-message"></a><span data-ttu-id="56019-104">Message de page de \_ navigation TDM \_</span><span class="sxs-lookup"><span data-stu-id="56019-104">TDM\_NAVIGATE\_PAGE message</span></span>

<span data-ttu-id="56019-105">Recrée une boîte de dialogue de tâches avec le nouveau contenu, en simulant la fonctionnalité d’un Assistant multipage.</span><span class="sxs-lookup"><span data-stu-id="56019-105">Recreates a task dialog with new contents, simulating the functionality of a multi-page wizard.</span></span>

## <a name="parameters"></a><span data-ttu-id="56019-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56019-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56019-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56019-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56019-108">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="56019-108">Not used.</span></span> <span data-ttu-id="56019-109">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="56019-109">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="56019-110">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="56019-110">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56019-111">Pointeur vers une structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) qui décrit la boîte de dialogue de tâche à créer.</span><span class="sxs-lookup"><span data-stu-id="56019-111">A pointer to a [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that describes the task dialog to create.</span></span> <span data-ttu-id="56019-112">L’application appelante doit allouer cette structure et définir ses membres.</span><span class="sxs-lookup"><span data-stu-id="56019-112">The calling application must allocate this structure and set its members.</span></span> <span data-ttu-id="56019-113">Les valeurs des membres varient en fonction du type de page vers lequel l’utilisateur accède.</span><span class="sxs-lookup"><span data-stu-id="56019-113">The values of the members vary depending on the kind of page the user navigates to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56019-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="56019-114">Return value</span></span>

<span data-ttu-id="56019-115">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="56019-115">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="56019-116">Notes</span><span class="sxs-lookup"><span data-stu-id="56019-116">Remarks</span></span>

<span data-ttu-id="56019-117">Pour lancer une boîte de dialogue de tâche de l’Assistant, utilisez la fonction [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .</span><span class="sxs-lookup"><span data-stu-id="56019-117">To launch a wizard task dialog, use the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="56019-118">Lorsque l’utilisateur navigue à l’aide de l’Assistant, envoyez ce message à la boîte de dialogue de tâche pour afficher la page suivante.</span><span class="sxs-lookup"><span data-stu-id="56019-118">As the user navigates using the wizard, send this message to the task dialog to display the next page.</span></span> <span data-ttu-id="56019-119">Une nouvelle boîte de dialogue de tâches (qui ressemble à une nouvelle page) est créée avec les éléments spécifiés dans la structure vers laquelle pointe *lParam*.</span><span class="sxs-lookup"><span data-stu-id="56019-119">A new task dialog (looks like a new page) is created with the elements specified in the structure pointed to by *lParam*.</span></span> <span data-ttu-id="56019-120">Au moment de la création, le contenu entier du cadre de la boîte de dialogue est détruit et reconstruit.</span><span class="sxs-lookup"><span data-stu-id="56019-120">At creation, the entire contents of the dialog frame are destroyed and reconstructed.</span></span> <span data-ttu-id="56019-121">Par conséquent, toutes les informations d’État détenues par les contrôles (par exemple, une barre de progression, un bouton de développement ou un bouton de vérification) dans la boîte de dialogue sont perdues.</span><span class="sxs-lookup"><span data-stu-id="56019-121">As a result, any state information held by controls (for example, a progress bar, expando button, or verification checkbox) in the dialog is lost.</span></span>

<span data-ttu-id="56019-122">La disposition de la boîte de dialogue de tâche peut échouer et cela peut ne pas être reflété dans la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="56019-122">The layout of the task dialog may fail and this may not be reflected in the return value.</span></span> <span data-ttu-id="56019-123">Une valeur de retour de S \_ OK reflète uniquement que la boîte de dialogue de tâche a reçu le message et a tenté de le traiter.</span><span class="sxs-lookup"><span data-stu-id="56019-123">A return value of S\_OK reflects only that the task dialog received the message and attempted to process it.</span></span> <span data-ttu-id="56019-124">Si la disposition de la boîte de dialogue de tâche échoue (la boîte de dialogue de tâche ne peut pas être affichée), la boîte de dialogue se ferme et un code **HRESULT** est retourné au niveau de la fonction de rappel enregistrée.</span><span class="sxs-lookup"><span data-stu-id="56019-124">If the layout of the task dialog fails (the task dialog cannot be displayed), the dialog will close and an **HRESULT** code is returned at the registered callback function.</span></span> <span data-ttu-id="56019-125">Pour plus d’informations sur la syntaxe de la fonction de rappel, consultez [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span><span class="sxs-lookup"><span data-stu-id="56019-125">For more information on the callback function syntax, see [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).</span></span>

## <a name="requirements"></a><span data-ttu-id="56019-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56019-126">Requirements</span></span>



| <span data-ttu-id="56019-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56019-127">Requirement</span></span> | <span data-ttu-id="56019-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="56019-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56019-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56019-129">Minimum supported client</span></span><br/> | <span data-ttu-id="56019-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56019-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56019-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="56019-131">Minimum supported server</span></span><br/> | <span data-ttu-id="56019-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="56019-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56019-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="56019-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="56019-134"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="56019-134"><dt>Commctrl.h</dt></span></span> </dl> |



 

