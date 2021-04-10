---
title: Message EM_SETTARGETDEVICE (RichEdit. h)
description: Définit l’appareil cible et la largeur de ligne utilisés pour \ 0034 ; ce que vous voyez est ce que vous obtenez \ 0034 ; (WYSIWYG) mise en forme dans un contrôle RichEdit.
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- EM_SETTARGETDEVICE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104215"
---
# <a name="em_settargetdevice-message"></a><span data-ttu-id="5db3b-104">\_Message SETTARGETDEVICE em</span><span class="sxs-lookup"><span data-stu-id="5db3b-104">EM\_SETTARGETDEVICE message</span></span>

<span data-ttu-id="5db3b-105">Définit l’appareil cible et la largeur de ligne utilisés pour la mise en forme de type « que vous obtenez » (WYSIWYG) dans un contrôle RichEdit.</span><span class="sxs-lookup"><span data-stu-id="5db3b-105">Sets the target device and line width used for "what you see is what you get" (WYSIWYG) formatting in a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5db3b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5db3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db3b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5db3b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5db3b-108">HDC pour l’appareil cible.</span><span class="sxs-lookup"><span data-stu-id="5db3b-108">HDC for the target device.</span></span>

</dd> <dt>

<span data-ttu-id="5db3b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5db3b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5db3b-110">Largeur de ligne à utiliser pour la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="5db3b-110">Line width to use for formatting.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5db3b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5db3b-111">Return value</span></span>

<span data-ttu-id="5db3b-112">La valeur de retour est égale à zéro si l’opération échoue, ou différente de zéro si elle réussit.</span><span class="sxs-lookup"><span data-stu-id="5db3b-112">The return value is zero if the operation fails, or nonzero if it succeeds.</span></span>

## <a name="remarks"></a><span data-ttu-id="5db3b-113">Notes</span><span class="sxs-lookup"><span data-stu-id="5db3b-113">Remarks</span></span>

<span data-ttu-id="5db3b-114">Le HDC pour l’imprimante par défaut peut être obtenu comme suit.</span><span class="sxs-lookup"><span data-stu-id="5db3b-114">The HDC for the default printer can be obtained as follows.</span></span>


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



<span data-ttu-id="5db3b-115">Si *lParam* est égal à zéro, aucun saut de ligne n’est créé.</span><span class="sxs-lookup"><span data-stu-id="5db3b-115">If *lParam* is zero, no line breaks are created.</span></span>

## <a name="requirements"></a><span data-ttu-id="5db3b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5db3b-116">Requirements</span></span>



| <span data-ttu-id="5db3b-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5db3b-117">Requirement</span></span> | <span data-ttu-id="5db3b-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5db3b-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5db3b-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5db3b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5db3b-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5db3b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5db3b-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5db3b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5db3b-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5db3b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5db3b-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="5db3b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5db3b-124"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5db3b-124"><dt>Richedit.h</dt></span></span> </dl> |



 

 





