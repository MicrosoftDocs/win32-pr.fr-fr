---
title: TBN_GETBUTTONINFO le code de notification (commctrl. h)
description: Récupère les informations de personnalisation de la barre d’outils et avertit la fenêtre parente de la barre d’outils de toute modification apportée à la barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- Contrôles Windows de code de notification TBN_GETBUTTONINFO
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942533"
---
# <a name="tbn_getbuttoninfo-notification-code"></a><span data-ttu-id="2957a-105">\_Code de notification TBN GETBUTTONINFO</span><span class="sxs-lookup"><span data-stu-id="2957a-105">TBN\_GETBUTTONINFO notification code</span></span>

<span data-ttu-id="2957a-106">Récupère les informations de personnalisation de la barre d’outils et avertit la fenêtre parente de la barre d’outils de toute modification apportée à la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="2957a-106">Retrieves toolbar customization information and notifies the toolbar's parent window of any changes being made to the toolbar.</span></span> <span data-ttu-id="2957a-107">Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="2957a-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="2957a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2957a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2957a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2957a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2957a-110">Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="2957a-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="2957a-111">Le membre **iItem** spécifie un index de base zéro qui fournit le nombre de boutons que la boîte de dialogue Personnaliser la barre d’outils affiche comme étant disponible et présente dans la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="2957a-111">The **iItem** member specifies a zero-based index that provides a count of the buttons the Customize Toolbar dialog box displays as both available and present on the toolbar.</span></span> <span data-ttu-id="2957a-112">Le membre **pszText** spécifie l’adresse du texte du bouton actuel et **cchText** spécifie sa longueur en caractères.</span><span class="sxs-lookup"><span data-stu-id="2957a-112">The **pszText** member specifies the address of the current button text, and **cchText** specifies its length in characters.</span></span> <span data-ttu-id="2957a-113">L’application doit remplir la structure avec des informations sur le bouton.</span><span class="sxs-lookup"><span data-stu-id="2957a-113">The application should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2957a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2957a-114">Return value</span></span>

<span data-ttu-id="2957a-115">Retourne la **valeur true** si les informations sur le bouton ont été copiées dans la structure spécifiée, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2957a-115">Returns **TRUE** if button information was copied to the specified structure, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2957a-116">Notes</span><span class="sxs-lookup"><span data-stu-id="2957a-116">Remarks</span></span>

<span data-ttu-id="2957a-117">Le contrôle ToolBar alloue une mémoire tampon et le récepteur (fenêtre parente) doit copier le texte dans cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="2957a-117">The toolbar control allocates a buffer, and the receiver (parent window) must copy the text into that buffer.</span></span> <span data-ttu-id="2957a-118">Le membre **cchText** contient la longueur de la mémoire tampon allouée par la barre d’outils lorsque TBN \_ GETBUTTONINFO est envoyé à la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="2957a-118">The **cchText** member contains the length of the buffer allocated by the toolbar when TBN\_GETBUTTONINFO is sent to the parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="2957a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2957a-119">Requirements</span></span>



| <span data-ttu-id="2957a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2957a-120">Requirement</span></span> | <span data-ttu-id="2957a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2957a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2957a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2957a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2957a-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2957a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2957a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2957a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2957a-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2957a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2957a-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2957a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2957a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2957a-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="2957a-128">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="2957a-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2957a-129">**TBN \_ GETBUTTONINFOW** (Unicode) et **TBN \_ GETBUTTONINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2957a-129">**TBN\_GETBUTTONINFOW** (Unicode) and **TBN\_GETBUTTONINFOA** (ANSI)</span></span><br/>       |



 

 





