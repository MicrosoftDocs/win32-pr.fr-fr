---
title: Message TB_SETBOUNDINGSIZE (commctrl. h)
description: Définit la taille limite pour un contrôle de barre d’outils à plusieurs colonnes.
ms.assetid: f406d9e3-1c40-4317-8cf1-51706f4c6adf
keywords:
- TB_SETBOUNDINGSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETBOUNDINGSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 419595da16148f7382da5053d3187e9cce9e00a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843057"
---
# <a name="tb_setboundingsize-message"></a><span data-ttu-id="8c887-104">TO \_ SETBOUNDINGSIZE message</span><span class="sxs-lookup"><span data-stu-id="8c887-104">TB\_SETBOUNDINGSIZE message</span></span>

<span data-ttu-id="8c887-105">\[Destiné à un usage interne ; non recommandé pour une utilisation dans les applications.</span><span class="sxs-lookup"><span data-stu-id="8c887-105">\[Intended for internal use; not recommended for use in applications.</span></span> <span data-ttu-id="8c887-106">Ce message n’est peut-être pas pris en charge dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8c887-106">This message may not be supported in future versions of Windows.\]</span></span>

<span data-ttu-id="8c887-107">Définit la taille limite pour un contrôle de barre d’outils à plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="8c887-107">Sets the bounding size for a multi-column toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c887-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c887-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c887-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8c887-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c887-110">Doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="8c887-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8c887-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8c887-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8c887-112">Pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) dont le membre **CY** contient la hauteur englobante.</span><span class="sxs-lookup"><span data-stu-id="8c887-112">Pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure whose **cy** member contains the bounding height.</span></span> <span data-ttu-id="8c887-113">Le membre **CX** (largeur) est ignoré.</span><span class="sxs-lookup"><span data-stu-id="8c887-113">The **cx** member (the width) is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c887-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c887-114">Return value</span></span>

<span data-ttu-id="8c887-115">La valeur de retour n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="8c887-115">The return value is not used.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="8c887-116">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="8c887-116">Security Considerations</span></span>

<span data-ttu-id="8c887-117">L’utilisation de ce message peut compromettre la sécurité de votre programme.</span><span class="sxs-lookup"><span data-stu-id="8c887-117">Using this message might compromise the security of your program.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c887-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8c887-118">Remarks</span></span>

<span data-ttu-id="8c887-119">La taille limite contrôle la manière dont les boutons sont organisés en colonnes.</span><span class="sxs-lookup"><span data-stu-id="8c887-119">The bounding size controls how buttons are organized into columns.</span></span> <span data-ttu-id="8c887-120">Si le contrôle ToolBar n’a pas le style [**TBSTYLE \_ ex \_ Column**](toolbar-extended-styles.md) , ce message n’a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="8c887-120">If the toolbar control does not have the [**TBSTYLE\_EX\_MULTICOLUMN**](toolbar-extended-styles.md) style, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c887-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c887-121">Requirements</span></span>



| <span data-ttu-id="8c887-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c887-122">Requirement</span></span> | <span data-ttu-id="8c887-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c887-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8c887-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c887-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8c887-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c887-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8c887-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c887-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8c887-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c887-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8c887-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c887-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c887-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c887-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

