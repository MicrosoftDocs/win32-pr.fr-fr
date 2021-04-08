---
title: Message HDM_EDITFILTER (commctrl. h)
description: Déplace le focus d’entrée vers la zone d’édition lorsqu’un bouton de filtre a le focus.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- HDM_EDITFILTER les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742284"
---
# <a name="hdm_editfilter-message"></a><span data-ttu-id="c4a3a-104">\_Message HDM EDITFILTER</span><span class="sxs-lookup"><span data-stu-id="c4a3a-104">HDM\_EDITFILTER message</span></span>

<span data-ttu-id="c4a3a-105">Déplace le focus d’entrée vers la zone d’édition lorsqu’un bouton de filtre a le focus.</span><span class="sxs-lookup"><span data-stu-id="c4a3a-105">Moves the input focus to the edit box when a filter button has the focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="c4a3a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4a3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4a3a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c4a3a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4a3a-108">Valeur qui spécifie la colonne à modifier.</span><span class="sxs-lookup"><span data-stu-id="c4a3a-108">A value specifying the column to edit.</span></span>

</dd> <dt>

<span data-ttu-id="c4a3a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c4a3a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c4a3a-110">Indicateur qui spécifie comment gérer les modifications de modification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4a3a-110">A flag that specifies how to handle the user's editing changes.</span></span> <span data-ttu-id="c4a3a-111">Utilisez cet indicateur pour spécifier la procédure à suivre si l’utilisateur est en train de modifier le filtre lorsque le message est envoyé.</span><span class="sxs-lookup"><span data-stu-id="c4a3a-111">Use this flag to specify what to do if the user is in the process of editing the filter when the message is sent.</span></span>



| <span data-ttu-id="c4a3a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4a3a-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="c4a3a-113">Signification</span><span class="sxs-lookup"><span data-stu-id="c4a3a-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="c4a3a-114"><dt></dt><dt> **True**</dt></span><span class="sxs-lookup"><span data-stu-id="c4a3a-114"><dt></dt> <dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="c4a3a-115">Ignorez les modifications apportées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4a3a-115">Discard the changes made by the user.</span></span> <br/> |
| <dl> <span data-ttu-id="c4a3a-116"><dt></dt><dt> **Valeur false**</dt></span><span class="sxs-lookup"><span data-stu-id="c4a3a-116"><dt></dt> <dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="c4a3a-117">Accepter les modifications apportées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c4a3a-117">Accept the changes made by the user.</span></span> <br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4a3a-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4a3a-118">Return value</span></span>

<span data-ttu-id="c4a3a-119">Retourne un entier.</span><span class="sxs-lookup"><span data-stu-id="c4a3a-119">Returns an integer.</span></span> <span data-ttu-id="c4a3a-120">La propriété **LRESULT** est castée en un entier qui indique **true**(1) ou **false**(0).</span><span class="sxs-lookup"><span data-stu-id="c4a3a-120">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4a3a-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4a3a-121">Requirements</span></span>



| <span data-ttu-id="c4a3a-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4a3a-122">Requirement</span></span> | <span data-ttu-id="c4a3a-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4a3a-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4a3a-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4a3a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c4a3a-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4a3a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4a3a-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4a3a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c4a3a-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4a3a-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c4a3a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4a3a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4a3a-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4a3a-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4a3a-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4a3a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4a3a-131">**HDM \_ CLEARFILTER**</span><span class="sxs-lookup"><span data-stu-id="c4a3a-131">**HDM\_CLEARFILTER**</span></span>](hdm-clearfilter.md)
</dt> </dl>

 

 





