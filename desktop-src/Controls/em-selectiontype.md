---
title: Message EM_SELECTIONTYPE (RichEdit. h)
description: Détermine le type de sélection d’un contrôle RichEdit.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- EM_SELECTIONTYPE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509178"
---
# <a name="em_selectiontype-message"></a><span data-ttu-id="c5e49-104">\_Message SELECTIONTYPE em</span><span class="sxs-lookup"><span data-stu-id="c5e49-104">EM\_SELECTIONTYPE message</span></span>

<span data-ttu-id="c5e49-105">Détermine le type de sélection d’un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="c5e49-105">Determines the selection type for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="c5e49-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5e49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5e49-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c5e49-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5e49-108">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c5e49-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c5e49-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c5e49-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c5e49-110">Non utilisé ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c5e49-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5e49-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c5e49-111">Return value</span></span>

<span data-ttu-id="c5e49-112">Si la sélection est vide, la valeur de retour est SEL \_ vide.</span><span class="sxs-lookup"><span data-stu-id="c5e49-112">If the selection is empty, the return value is SEL\_EMPTY.</span></span>

<span data-ttu-id="c5e49-113">Si la sélection n’est pas vide, la valeur de retour est un jeu d’indicateurs contenant une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5e49-113">If the selection is not empty, the return value is a set of flags containing one or more of the following values.</span></span>



| <span data-ttu-id="c5e49-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c5e49-114">Return code</span></span>                                                                                     | <span data-ttu-id="c5e49-115">Description</span><span class="sxs-lookup"><span data-stu-id="c5e49-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="c5e49-116"><dt>**\_texte sel**</dt></span><span class="sxs-lookup"><span data-stu-id="c5e49-116"><dt>**SEL\_TEXT**</dt></span></span> </dl>        | <span data-ttu-id="c5e49-117">Texte.</span><span class="sxs-lookup"><span data-stu-id="c5e49-117">Text.</span></span><br/>                            |
| <dl> <span data-ttu-id="c5e49-118"><dt>**SEL, \_ objet**</dt></span><span class="sxs-lookup"><span data-stu-id="c5e49-118"><dt>**SEL\_OBJECT**</dt></span></span> </dl>      | <span data-ttu-id="c5e49-119">Au moins un objet COM.</span><span class="sxs-lookup"><span data-stu-id="c5e49-119">At least one COM object.</span></span><br/>         |
| <dl> <span data-ttu-id="c5e49-120"><dt>**SEL \_ MULTIchar**</dt></span><span class="sxs-lookup"><span data-stu-id="c5e49-120"><dt>**SEL\_MULTICHAR**</dt></span></span> </dl>   | <span data-ttu-id="c5e49-121">Plusieurs caractères de texte.</span><span class="sxs-lookup"><span data-stu-id="c5e49-121">More than one character of text.</span></span><br/> |
| <dl> <span data-ttu-id="c5e49-122"><dt>**SEL \_ MULTIobject**</dt></span><span class="sxs-lookup"><span data-stu-id="c5e49-122"><dt>**SEL\_MULTIOBJECT**</dt></span></span> </dl> | <span data-ttu-id="c5e49-123">Plusieurs objets COM.</span><span class="sxs-lookup"><span data-stu-id="c5e49-123">More than one COM object.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="c5e49-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c5e49-124">Remarks</span></span>

<span data-ttu-id="c5e49-125">Ce message est utile lors du traitement de la [**\_ taille WM**](/windows/desktop/winmsg/wm-size) pour le parent d’un contrôle Rich Edit sans fin.</span><span class="sxs-lookup"><span data-stu-id="c5e49-125">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5e49-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5e49-126">Requirements</span></span>



| <span data-ttu-id="c5e49-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5e49-127">Requirement</span></span> | <span data-ttu-id="c5e49-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5e49-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c5e49-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5e49-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c5e49-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5e49-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c5e49-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5e49-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c5e49-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5e49-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c5e49-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5e49-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5e49-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5e49-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5e49-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5e49-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e49-136">**taille du WM \_**</span><span class="sxs-lookup"><span data-stu-id="c5e49-136">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

