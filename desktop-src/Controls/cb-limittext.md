---
title: Message CB_LIMITTEXT (winuser. h)
description: Limite la longueur du texte que l’utilisateur peut taper dans le contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- CB_LIMITTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032847"
---
# <a name="cb_limittext-message"></a><span data-ttu-id="7e3b6-104">\_Message LIMITTEXT CB</span><span class="sxs-lookup"><span data-stu-id="7e3b6-104">CB\_LIMITTEXT message</span></span>

<span data-ttu-id="7e3b6-105">Limite la longueur du texte que l’utilisateur peut taper dans le contrôle d’édition d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-105">Limits the length of the text the user may type into the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e3b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e3b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e3b6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e3b6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e3b6-108">Nombre maximal de **TCHARs** que l’utilisateur peut entrer, à l’exclusion du caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-108">The maximum number of **TCHARs** the user can enter, not including the terminating null character.</span></span> <span data-ttu-id="7e3b6-109">Si ce paramètre est égal à zéro, la longueur du texte est limitée à 0x7FFFFFFE caractères.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-109">If this parameter is zero, the text length is limited to 0x7FFFFFFE characters.</span></span>

</dd> <dt>

<span data-ttu-id="7e3b6-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e3b6-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e3b6-111">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e3b6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e3b6-112">Return value</span></span>

<span data-ttu-id="7e3b6-113">La valeur de retour est toujours **true**.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e3b6-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7e3b6-114">Remarks</span></span>

<span data-ttu-id="7e3b6-115">Si la zone de liste déroulante n’a pas le style [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) , la définition de la limite du texte sur une valeur supérieure à la taille du contrôle d’édition n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-115">If the combo box does not have the [**CBS\_AUTOHSCROLL**](combo-box-styles.md) style, setting the text limit to be larger than the size of the edit control has no effect.</span></span>

<span data-ttu-id="7e3b6-116">Le **message \_ LIMITTEXT CB** limite uniquement le texte que l’utilisateur peut entrer.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-116">The **CB\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="7e3b6-117">Elle n’a aucun effet sur le texte déjà présent dans le contrôle d’édition lorsque le message est envoyé, ni sur la longueur du texte copié dans le contrôle d’édition lorsqu’une chaîne de la zone de liste est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-117">It has no effect on any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control when a string in the list box is selected.</span></span>

<span data-ttu-id="7e3b6-118">La limite par défaut du texte qu’un utilisateur peut entrer dans le contrôle d’édition est 30 000 **TCHARs**.</span><span class="sxs-lookup"><span data-stu-id="7e3b6-118">The default limit to the text a user can enter in the edit control is 30,000 **TCHARs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e3b6-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e3b6-119">Requirements</span></span>



| <span data-ttu-id="7e3b6-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e3b6-120">Requirement</span></span> | <span data-ttu-id="7e3b6-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e3b6-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e3b6-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e3b6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7e3b6-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e3b6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7e3b6-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e3b6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7e3b6-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e3b6-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7e3b6-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e3b6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e3b6-127"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e3b6-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





