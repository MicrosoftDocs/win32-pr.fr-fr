---
title: Message TDM_CLICK_RADIO_BUTTON (commctrl. h)
description: Simule l’action d’un clic sur une case d’option dans une boîte de dialogue de tâche.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- TDM_CLICK_RADIO_BUTTON les contrôles de message Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b76d465b1b937359a3d312a401914d497f9c9b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942759"
---
# <a name="tdm_click_radio_button-message"></a><span data-ttu-id="ea0f7-104">Message de case d' \_ option de clic TDM \_ \_</span><span class="sxs-lookup"><span data-stu-id="ea0f7-104">TDM\_CLICK\_RADIO\_BUTTON message</span></span>

<span data-ttu-id="ea0f7-105">Simule l’action d’un clic sur une case d’option dans une boîte de dialogue de tâche.</span><span class="sxs-lookup"><span data-stu-id="ea0f7-105">Simulates the action of a radio button click in a task dialog.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea0f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea0f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea0f7-107">*wParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea0f7-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea0f7-108">Valeur **int** qui spécifie l’ID de la case d’option sur laquelle cliquer.</span><span class="sxs-lookup"><span data-stu-id="ea0f7-108">An **int** value that specifies the ID of the radio button to be clicked.</span></span>

</dd> <dt>

<span data-ttu-id="ea0f7-109">*lParam* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea0f7-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea0f7-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="ea0f7-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea0f7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea0f7-111">Return value</span></span>

<span data-ttu-id="ea0f7-112">La valeur de retour est ignorée.</span><span class="sxs-lookup"><span data-stu-id="ea0f7-112">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea0f7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ea0f7-113">Remarks</span></span>

<span data-ttu-id="ea0f7-114">L’ID de case d’option spécifié est envoyé à la fonction de rappel [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) dans le cadre d’un [ \_ \_ \_ clic sur](tdn-radio-button-clicked.md) le code de notification de TDN.</span><span class="sxs-lookup"><span data-stu-id="ea0f7-114">The specified radio button ID is sent to the [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) callback function as part of a [TDN\_RADIO\_BUTTON\_CLICKED](tdn-radio-button-clicked.md) notification code.</span></span> <span data-ttu-id="ea0f7-115">Une fois la fonction de rappel retournée, la case d’option est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="ea0f7-115">After the callback function returns, the radio button will be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea0f7-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea0f7-116">Requirements</span></span>



| <span data-ttu-id="ea0f7-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea0f7-117">Requirement</span></span> | <span data-ttu-id="ea0f7-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea0f7-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea0f7-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea0f7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ea0f7-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea0f7-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea0f7-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ea0f7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ea0f7-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ea0f7-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea0f7-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea0f7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea0f7-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea0f7-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

