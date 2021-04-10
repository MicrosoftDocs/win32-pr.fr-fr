---
title: Message TB_SETWINDOWTHEME (commctrl. h)
description: Définit le style visuel d’un contrôle de barre d’outils.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- TB_SETWINDOWTHEME les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e0c293e974eee2e7827225efb06cc439fdf2c39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106582"
---
# <a name="tb_setwindowtheme-message"></a><span data-ttu-id="4c952-104">TO \_ SETWINDOWTHEME message</span><span class="sxs-lookup"><span data-stu-id="4c952-104">TB\_SETWINDOWTHEME message</span></span>

<span data-ttu-id="4c952-105">Définit le style visuel d’un contrôle de barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="4c952-105">Sets the visual style of a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4c952-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c952-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c952-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4c952-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4c952-108">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="4c952-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4c952-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4c952-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4c952-110">Pointeur vers une chaîne Unicode qui contient le style visuel de la barre d’outils à définir.</span><span class="sxs-lookup"><span data-stu-id="4c952-110">Pointer to a Unicode string that contains the toolbar visual style to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c952-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c952-111">Return value</span></span>

<span data-ttu-id="4c952-112">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="4c952-112">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c952-113">Notes</span><span class="sxs-lookup"><span data-stu-id="4c952-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4c952-114">Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0.</span><span class="sxs-lookup"><span data-stu-id="4c952-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4c952-115">Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4c952-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="4c952-116">L’envoi de ce message revient à appeler [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) dans la barre d’outils et son contrôle ToolTip, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="4c952-116">Sending this message is equivalent to calling [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) on the toolbar and its tooltip control, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c952-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c952-117">Requirements</span></span>



| <span data-ttu-id="4c952-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c952-118">Requirement</span></span> | <span data-ttu-id="4c952-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c952-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c952-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c952-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4c952-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c952-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4c952-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c952-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4c952-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c952-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c952-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c952-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c952-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c952-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





