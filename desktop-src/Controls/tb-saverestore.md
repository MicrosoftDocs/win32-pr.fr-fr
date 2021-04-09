---
title: Message TB_SAVERESTORE (commctrl. h)
description: Envoyer ce message pour lancer l’enregistrement ou la restauration de l’état d’une barre d’outils.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- TB_SAVERESTORE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843058"
---
# <a name="tb_saverestore-message"></a><span data-ttu-id="8d152-104">TO \_ SAVERESTORE message</span><span class="sxs-lookup"><span data-stu-id="8d152-104">TB\_SAVERESTORE message</span></span>

<span data-ttu-id="8d152-105">Envoyer ce message pour lancer l’enregistrement ou la restauration de l’état d’une barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="8d152-105">Send this message to initiate saving or restoring a toolbar state.</span></span>

## <a name="parameters"></a><span data-ttu-id="8d152-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d152-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d152-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8d152-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d152-108">Enregistrer ou restaurer l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="8d152-108">Save or restore flag.</span></span> <span data-ttu-id="8d152-109">Si ce paramètre a la **valeur true**, les informations sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="8d152-109">If this parameter is **TRUE**, the information is saved.</span></span> <span data-ttu-id="8d152-110">Si la **valeur est false**, les informations sont restaurées.</span><span class="sxs-lookup"><span data-stu-id="8d152-110">If it is **FALSE**, the information is restored.</span></span>

</dd> <dt>

<span data-ttu-id="8d152-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8d152-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8d152-112">Pointeur vers une structure [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) qui spécifie la clé de Registre, la sous-clé et le nom de la valeur pour les informations d’état de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="8d152-112">Pointer to a [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) structure that specifies the registry key, subkey, and value name for the toolbar state information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d152-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d152-113">Return value</span></span>

<span data-ttu-id="8d152-114">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="8d152-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d152-115">Notes</span><span class="sxs-lookup"><span data-stu-id="8d152-115">Remarks</span></span>

<span data-ttu-id="8d152-116">Pour la version 4,72 et les versions antérieures, afin d’utiliser ce message pour enregistrer ou restaurer une barre d’outils, la fenêtre parente du contrôle ToolBar doit implémenter un gestionnaire pour le code de notification [TBN \_ GETBUTTONINFO](tbn-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="8d152-116">For version 4.72 and earlier, to use this message to save or restore a toolbar, the parent window of the toolbar control must implement a handler for the [TBN\_GETBUTTONINFO](tbn-getbuttoninfo.md) notification code.</span></span> <span data-ttu-id="8d152-117">La barre d’outils émet cette notification pour extraire des informations sur chaque bouton lors de sa restauration.</span><span class="sxs-lookup"><span data-stu-id="8d152-117">The toolbar issues this notification to retrieve information about each button as it is restored.</span></span>

<span data-ttu-id="8d152-118">La version 5,80 comprend une nouvelle option d’enregistrement/restauration.</span><span class="sxs-lookup"><span data-stu-id="8d152-118">Version 5.80 includes a new save/restore option.</span></span> <span data-ttu-id="8d152-119">Au début du processus, lorsque chaque bouton est enregistré ou restauré, votre application reçoit une notification [TBN \_ Save](tbn-save.md) ou [TBN \_ Restore](tbn-restore.md) .</span><span class="sxs-lookup"><span data-stu-id="8d152-119">At the beginning of the process, and as each button is saved or restored, your application will receive a [TBN\_SAVE](tbn-save.md) or [TBN\_RESTORE](tbn-restore.md) notification.</span></span> <span data-ttu-id="8d152-120">Pour utiliser cette option, vous devez implémenter des gestionnaires de notification pour fournir à l’interpréteur de commandes la bitmap et les informations d’État dont il a besoin pour enregistrer ou restaurer l’état de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="8d152-120">To use this option, you must implement notification handlers to provide the Shell with the bitmap and state information it needs to successfully save or restore the toolbar state.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d152-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d152-121">Requirements</span></span>



| <span data-ttu-id="8d152-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d152-122">Requirement</span></span> | <span data-ttu-id="8d152-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d152-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8d152-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d152-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8d152-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d152-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8d152-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d152-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8d152-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d152-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d152-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d152-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d152-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d152-129"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="8d152-130">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="8d152-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8d152-131">**To \_ SAVERESTOREW** (Unicode) et **to \_ SAVERESTOREA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8d152-131">**TB\_SAVERESTOREW** (Unicode) and **TB\_SAVERESTOREA** (ANSI)</span></span><br/>             |



 

 





