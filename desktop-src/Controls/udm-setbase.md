---
title: Message UDM_SETBASE (commctrl. h)
description: Définit la base de base pour un contrôle up-up. La valeur de base détermine si la fenêtre associée affiche des nombres en chiffres décimaux ou hexadécimaux. Les nombres hexadécimaux sont toujours non signés et les nombres décimaux sont signés.
ms.assetid: c76cdec1-e73b-4b4b-89be-9a00ff2ea172
keywords:
- UDM_SETBASE les contrôles de message Windows
topic_type:
- apiref
api_name:
- UDM_SETBASE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6bcd7d6154b4ba732e5ffbbec889b326ec8176
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942452"
---
# <a name="udm_setbase-message"></a><span data-ttu-id="54301-106">\_Message SETBASE UDM</span><span class="sxs-lookup"><span data-stu-id="54301-106">UDM\_SETBASE message</span></span>

<span data-ttu-id="54301-107">Définit la base de base pour un contrôle up-up.</span><span class="sxs-lookup"><span data-stu-id="54301-107">Sets the radix base for an up-down control.</span></span> <span data-ttu-id="54301-108">La valeur de base détermine si la fenêtre associée affiche des nombres en chiffres décimaux ou hexadécimaux.</span><span class="sxs-lookup"><span data-stu-id="54301-108">The base value determines whether the buddy window displays numbers in decimal or hexadecimal digits.</span></span> <span data-ttu-id="54301-109">Les nombres hexadécimaux sont toujours non signés et les nombres décimaux sont signés.</span><span class="sxs-lookup"><span data-stu-id="54301-109">Hexadecimal numbers are always unsigned, and decimal numbers are signed.</span></span>

## <a name="parameters"></a><span data-ttu-id="54301-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54301-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54301-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54301-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54301-112">Nouvelle valeur de base pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="54301-112">New base value for the control.</span></span> <span data-ttu-id="54301-113">Ce paramètre peut avoir la valeur 10 pour Decimal ou 16 pour hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="54301-113">This parameter can be 10 for decimal or 16 for hexadecimal.</span></span>

</dd> <dt>

<span data-ttu-id="54301-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54301-114">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="54301-115">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="54301-115">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54301-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54301-116">Return value</span></span>

<span data-ttu-id="54301-117">La valeur de retour est la valeur de base précédente.</span><span class="sxs-lookup"><span data-stu-id="54301-117">The return value is the previous base value.</span></span> <span data-ttu-id="54301-118">Si une base non valide est spécifiée, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="54301-118">If an invalid base is given, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="54301-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54301-119">Requirements</span></span>



| <span data-ttu-id="54301-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54301-120">Requirement</span></span> | <span data-ttu-id="54301-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="54301-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54301-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54301-122">Minimum supported client</span></span><br/> | <span data-ttu-id="54301-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54301-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54301-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54301-124">Minimum supported server</span></span><br/> | <span data-ttu-id="54301-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54301-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54301-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="54301-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="54301-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="54301-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





