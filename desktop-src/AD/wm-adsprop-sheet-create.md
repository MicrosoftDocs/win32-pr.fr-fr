---
title: Message WM_ADSPROP_SHEET_CREATE
description: Envoyé à l’objet de notification pour créer une feuille de propriétés secondaire dans un composant logiciel enfichable MMC Active Directory.
ms.assetid: 3efa25f2-cd39-44f8-952e-203f1519ce2c
ms.tgt_platform: multiple
keywords:
- Message de WM_ADSPROP_SHEET_CREATE Active Directory
topic_type:
- apiref
api_name:
- WM_ADSPROP_SHEET_CREATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b540ffd87d4350a323577ff5fa317e94f9271f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508614"
---
# <a name="wm_adsprop_sheet_create-message"></a><span data-ttu-id="97bf1-104">Créer un message de la \_ feuille ADSPROP WM \_ \_</span><span class="sxs-lookup"><span data-stu-id="97bf1-104">WM\_ADSPROP\_SHEET\_CREATE message</span></span>

<span data-ttu-id="97bf1-105">Le message de création de la **\_ \_ feuille \_ ADSPROP WM** est envoyé à l’objet notification pour créer une feuille de propriétés secondaire dans un composant logiciel enfichable MMC Active Directory.</span><span class="sxs-lookup"><span data-stu-id="97bf1-105">The **WM\_ADSPROP\_SHEET\_CREATE** message is sent to the notification object to create a secondary property sheet in an Active Directory MMC snap-in.</span></span>

> [!Note]  
> <span data-ttu-id="97bf1-106">La valeur de ce message n’est pas définie dans un fichier d’en-tête publié.</span><span class="sxs-lookup"><span data-stu-id="97bf1-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="97bf1-107">Pour utiliser cette valeur de message, vous devez la définir vous-même dans le format exact indiqué.</span><span class="sxs-lookup"><span data-stu-id="97bf1-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_ADSPROP_SHEET_CREATE (WM_USER + 1108)
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_ADSPROP_SHEET_CREATE,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="97bf1-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97bf1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97bf1-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="97bf1-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="97bf1-110">Handle de l’objet de notification.</span><span class="sxs-lookup"><span data-stu-id="97bf1-110">The handle of the notification object.</span></span> <span data-ttu-id="97bf1-111">Pour obtenir ce handle, appelez [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span><span class="sxs-lookup"><span data-stu-id="97bf1-111">To obtain this handle, call [**ADsPropCreateNotifyObj**](/windows/desktop/api/Adsprop/nf-adsprop-adspropcreatenotifyobj).</span></span>

</dd> <dt>

<span data-ttu-id="97bf1-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="97bf1-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97bf1-113">Contient un pointeur vers une structure d' [**\_ informations de \_ page \_ DSA sec**](dsa-sec-page-info.md) qui définit la page secondaire à créer.</span><span class="sxs-lookup"><span data-stu-id="97bf1-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary page to create.</span></span> <span data-ttu-id="97bf1-114">Une seule feuille de propriétés secondaire peut être créée avec le message de **\_ \_ \_ création de feuille ADSPROP WM** , de sorte que la structure [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) ne peut contenir qu’une seule structure [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) .</span><span class="sxs-lookup"><span data-stu-id="97bf1-114">Only one secondary property sheet can be created with the **WM\_ADSPROP\_SHEET\_CREATE** message, so the [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) structure can only contain one [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) structure.</span></span>

</dd> <dt>

<span data-ttu-id="97bf1-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97bf1-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97bf1-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="97bf1-116">Not used.</span></span> <span data-ttu-id="97bf1-117">Doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="97bf1-117">Must be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97bf1-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97bf1-118">Return value</span></span>

<span data-ttu-id="97bf1-119">La valeur de retour de ce message est toujours égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="97bf1-119">The return value for this message is always zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="97bf1-120">Notes</span><span class="sxs-lookup"><span data-stu-id="97bf1-120">Remarks</span></span>

<span data-ttu-id="97bf1-121">L’appelant doit allouer la structure des informations de la [**\_ \_ page \_ DSA sec**](dsa-sec-page-info.md) , la chaîne de titre et toutes les chaînes [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) à l’aide d’un appel unique à la fonction [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) .</span><span class="sxs-lookup"><span data-stu-id="97bf1-121">The caller must allocate the [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure, the title string and all [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) strings using a single call to the [**LocalAlloc**](/windows/desktop/api/winbase/nf-winbase-localalloc) function.</span></span> <span data-ttu-id="97bf1-122">Le message de création de la **\_ feuille de ADSPROP \_ \_ WM** est un message asynchrone. il retournera donc avant la création de la feuille secondaire.</span><span class="sxs-lookup"><span data-stu-id="97bf1-122">The **WM\_ADSPROP\_SHEET\_CREATE** message is an asynchronous message, so it will return before the secondary sheet is created.</span></span> <span data-ttu-id="97bf1-123">Pour cette raison, la mémoire doit rester intacte après le retour du message.</span><span class="sxs-lookup"><span data-stu-id="97bf1-123">Because of this, the memory must remain intact after the message returns.</span></span> <span data-ttu-id="97bf1-124">Le récepteur libère cette mémoire avec un appel unique à la fonction [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) après la création de la feuille secondaire.</span><span class="sxs-lookup"><span data-stu-id="97bf1-124">The receiver will free this memory with a single call to the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function after the secondary sheet is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="97bf1-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97bf1-125">Requirements</span></span>



| <span data-ttu-id="97bf1-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97bf1-126">Requirement</span></span> | <span data-ttu-id="97bf1-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="97bf1-127">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="97bf1-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97bf1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="97bf1-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97bf1-129">Windows Vista</span></span><br/>       |
| <span data-ttu-id="97bf1-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97bf1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="97bf1-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97bf1-131">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97bf1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97bf1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97bf1-133">**CFSTR \_ DS \_ PARENTHWND**</span><span class="sxs-lookup"><span data-stu-id="97bf1-133">**CFSTR\_DS\_PARENTHWND**</span></span>](cfstr-ds-parenthwnd.md)
</dt> <dt>

[<span data-ttu-id="97bf1-134">**\_ \_ informations sur la page DSA sec \_**</span><span class="sxs-lookup"><span data-stu-id="97bf1-134">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="97bf1-135">**DSOBJECTNAMES**</span><span class="sxs-lookup"><span data-stu-id="97bf1-135">**DSOBJECTNAMES**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames)
</dt> <dt>

[<span data-ttu-id="97bf1-136">**DSOBJECT**</span><span class="sxs-lookup"><span data-stu-id="97bf1-136">**DSOBJECT**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsobject)
</dt> <dt>

[<span data-ttu-id="97bf1-137">**LocalAlloc**</span><span class="sxs-lookup"><span data-stu-id="97bf1-137">**LocalAlloc**</span></span>](/windows/desktop/api/winbase/nf-winbase-localalloc)
</dt> <dt>

[<span data-ttu-id="97bf1-138">**LocalFree**</span><span class="sxs-lookup"><span data-stu-id="97bf1-138">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

