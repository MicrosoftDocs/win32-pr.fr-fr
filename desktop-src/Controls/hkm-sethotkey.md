---
title: Message HKM_SETHOTKEY (commctrl. h)
description: Définit la combinaison de touches d’accès rapide pour un contrôle de touche d’accès rapide.
ms.assetid: 372a7b2f-d9d5-43a8-9c06-730f2f5dc56e
keywords:
- HKM_SETHOTKEY les contrôles de message Windows
topic_type:
- apiref
api_name:
- HKM_SETHOTKEY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3672136c44c0268e218e7f87cbbeb3373b76b39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508490"
---
# <a name="hkm_sethotkey-message"></a><span data-ttu-id="08320-104">\_Message hkm SETHOTKEY</span><span class="sxs-lookup"><span data-stu-id="08320-104">HKM\_SETHOTKEY message</span></span>

<span data-ttu-id="08320-105">Définit la combinaison de touches d’accès rapide pour un contrôle de touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="08320-105">Sets the hot key combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="08320-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08320-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08320-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="08320-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08320-108">Le [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) du [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est le code de la touche virtuelle de la touche d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="08320-108">The [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) of the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the virtual key code of the hot key.</span></span> <span data-ttu-id="08320-109">Le [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) du **LOWORD** est le modificateur de clé qui indique les clés qui définissent une combinaison de touches d’accès rapide.</span><span class="sxs-lookup"><span data-stu-id="08320-109">The [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) of the **LOWORD** is the key modifier that indicates the keys that define a hot key combination.</span></span> <span data-ttu-id="08320-110">Pour obtenir la liste des valeurs d’indicateur de modification, consultez la description du message [**hkm \_ GETHOTKEY**](hkm-gethotkey.md) .</span><span class="sxs-lookup"><span data-stu-id="08320-110">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="08320-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="08320-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="08320-112">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="08320-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08320-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08320-113">Return value</span></span>

<span data-ttu-id="08320-114">Retourne toujours zéro.</span><span class="sxs-lookup"><span data-stu-id="08320-114">Always returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="08320-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08320-115">Requirements</span></span>



| <span data-ttu-id="08320-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08320-116">Requirement</span></span> | <span data-ttu-id="08320-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="08320-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="08320-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08320-118">Minimum supported client</span></span><br/> | <span data-ttu-id="08320-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08320-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="08320-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08320-120">Minimum supported server</span></span><br/> | <span data-ttu-id="08320-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08320-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="08320-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="08320-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="08320-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="08320-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

