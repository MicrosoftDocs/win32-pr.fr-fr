---
title: DTN_FORMATQUERY le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) pour récupérer la taille maximale autorisée de la chaîne qui s’affichera dans un champ de rappel. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0f00086a-0ab8-4f6f-9c3e-6e77008aa088
keywords:
- Contrôles Windows de code de notification DTN_FORMATQUERY
topic_type:
- apiref
api_name:
- DTN_FORMATQUERY
- DTN_FORMATQUERYA
- DTN_FORMATQUERYW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e9653f369f13e0ef4a775265d763e854db4de7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941716"
---
# <a name="dtn_formatquery-notification-code"></a><span data-ttu-id="52fd9-105">\_Code de notification DTN FORMATQUERY</span><span class="sxs-lookup"><span data-stu-id="52fd9-105">DTN\_FORMATQUERY notification code</span></span>

<span data-ttu-id="52fd9-106">Envoyé par un contrôle de sélecteur de date et heure (PAO) pour récupérer la taille maximale autorisée de la chaîne qui s’affichera dans un champ de rappel.</span><span class="sxs-lookup"><span data-stu-id="52fd9-106">Sent by a date and time picker (DTP) control to retrieve the maximum allowable size of the string that will be displayed in a callback field.</span></span> <span data-ttu-id="52fd9-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="52fd9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
DTN_FORMATQUERY

    lpDTFormatQuery = (LPNMDATETIMEFORMATQUERY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="52fd9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52fd9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52fd9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52fd9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52fd9-110">Pointeur vers une structure [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) contenant des informations sur le champ de rappel.</span><span class="sxs-lookup"><span data-stu-id="52fd9-110">A pointer to an [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure containing information about the callback field.</span></span> <span data-ttu-id="52fd9-111">La structure contient une sous-chaîne qui définit un champ de rappel et reçoit la taille maximale autorisée de la chaîne qui s’affichera dans le champ de rappel.</span><span class="sxs-lookup"><span data-stu-id="52fd9-111">The structure contains a substring that defines a callback field and receives the maximum allowable size of the string that will be displayed in the callback field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52fd9-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52fd9-112">Return value</span></span>

<span data-ttu-id="52fd9-113">Le propriétaire du contrôle doit calculer la largeur maximale possible du texte qui sera affiché dans le champ de rappel, définir le membre **szMax** de la structure [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) et retourner zéro.</span><span class="sxs-lookup"><span data-stu-id="52fd9-113">The owner of the control must calculate the maximum possible width of the text that will be displayed in the callback field, set the **szMax** member of the [**NMDATETIMEFORMATQUERY**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimeformatquerya) structure, and return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="52fd9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="52fd9-114">Remarks</span></span>

<span data-ttu-id="52fd9-115">La gestion de ce code de notification prépare le contrôle pour la taille maximale de la chaîne qui s’affiche dans un champ de rappel particulier.</span><span class="sxs-lookup"><span data-stu-id="52fd9-115">Handling this notification code prepares the control to adjust for the maximum size of the string that will be displayed in a particular callback field.</span></span> <span data-ttu-id="52fd9-116">Cela permet au contrôle d’afficher correctement la sortie à tout moment, ce qui réduit le scintillement dans l’affichage du contrôle.</span><span class="sxs-lookup"><span data-stu-id="52fd9-116">This enables the control to properly display output at all times, reducing flicker within the control's display.</span></span> <span data-ttu-id="52fd9-117">(Pour plus d’informations sur les champs de rappel, consultez [champs de rappel](date-and-time-picker-controls.md).)</span><span class="sxs-lookup"><span data-stu-id="52fd9-117">(For additional information about callback fields, see [Callback fields](date-and-time-picker-controls.md).)</span></span>

## <a name="requirements"></a><span data-ttu-id="52fd9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52fd9-118">Requirements</span></span>



| <span data-ttu-id="52fd9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52fd9-119">Requirement</span></span> | <span data-ttu-id="52fd9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="52fd9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52fd9-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52fd9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="52fd9-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52fd9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52fd9-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52fd9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="52fd9-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52fd9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52fd9-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="52fd9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="52fd9-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52fd9-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="52fd9-127">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="52fd9-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="52fd9-128">**DTN \_ FORMATQUERYW** (Unicode) et **DTN \_ FORMATQUERYA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="52fd9-128">**DTN\_FORMATQUERYW** (Unicode) and **DTN\_FORMATQUERYA** (ANSI)</span></span><br/>           |



 

 





