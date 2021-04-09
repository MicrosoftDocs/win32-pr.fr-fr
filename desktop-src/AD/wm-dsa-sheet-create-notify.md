---
title: Message WM_DSA_SHEET_CREATE_NOTIFY
description: Publié dans le composant logiciel enfichable MMC Active Directory pour créer une feuille de propriétés secondaire.
ms.assetid: 878878bf-fb78-4669-b282-1dd3349f35d5
ms.tgt_platform: multiple
keywords:
- Message de WM_DSA_SHEET_CREATE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CREATE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f08424e7b39449861ec654f1ff7891c6e9c60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942206"
---
# <a name="wm_dsa_sheet_create_notify-message"></a><span data-ttu-id="d953c-104">\_Créer un \_ message \_ de \_ notification de la feuille DSA DSA</span><span class="sxs-lookup"><span data-stu-id="d953c-104">WM\_DSA\_SHEET\_CREATE\_NOTIFY message</span></span>

<span data-ttu-id="d953c-105">Le message de notification de création d’une **\_ \_ feuille \_ \_ DSA DSA** est publié dans le composant logiciel enfichable MMC Active Directory pour créer une feuille de propriétés secondaire.</span><span class="sxs-lookup"><span data-stu-id="d953c-105">The **WM\_DSA\_SHEET\_CREATE\_NOTIFY** message is posted to the Active Directory MMC snap-in to create a secondary property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="d953c-106">La valeur de ce message n’est pas définie dans un fichier d’en-tête publié.</span><span class="sxs-lookup"><span data-stu-id="d953c-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="d953c-107">Pour utiliser cette valeur de message, définissez-la dans le format exact indiqué.</span><span class="sxs-lookup"><span data-stu-id="d953c-107">To use this message value, define it in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CREATE_NOTIFY (WM_USER + 6)
LRESULT SendMessage(
    (HWND) hwnd, 
    WM_DSA_SHEET_CREATE_NOTIFY,
    (WPARAM) wParam, 
    (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="d953c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d953c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d953c-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d953c-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d953c-110">Handle de fenêtre de la fenêtre du composant logiciel enfichable qui traitera ce message.</span><span class="sxs-lookup"><span data-stu-id="d953c-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="d953c-111">Ce handle est obtenu à partir du membre **hwndHidden** de la structure [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="d953c-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d953c-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d953c-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d953c-113">Contient un pointeur vers une structure d' [**\_ informations de \_ page \_ DSA sec**](dsa-sec-page-info.md) qui définit la feuille de propriétés secondaire à créer.</span><span class="sxs-lookup"><span data-stu-id="d953c-113">Contains a pointer to a [**DSA\_SEC\_PAGE\_INFO**](dsa-sec-page-info.md) structure that defines the secondary property sheet to create.</span></span> <span data-ttu-id="d953c-114">Le récepteur du message doit libérer cette mémoire avec la fonction [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) lorsqu’il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="d953c-114">The message receiver must free this memory with the [**LocalFree**](/windows/desktop/api/winbase/nf-winbase-localfree) function when it is no longer required.</span></span>

</dd> <dt>

<span data-ttu-id="d953c-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d953c-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d953c-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d953c-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d953c-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d953c-117">Return value</span></span>

<span data-ttu-id="d953c-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="d953c-118">Not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="d953c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d953c-119">Requirements</span></span>



| <span data-ttu-id="d953c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d953c-120">Requirement</span></span> | <span data-ttu-id="d953c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d953c-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="d953c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d953c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d953c-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d953c-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="d953c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d953c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d953c-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d953c-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d953c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d953c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d953c-127">**PROPSHEETCFG**</span><span class="sxs-lookup"><span data-stu-id="d953c-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> <dt>

[<span data-ttu-id="d953c-128">**\_ \_ informations sur la page DSA sec \_**</span><span class="sxs-lookup"><span data-stu-id="d953c-128">**DSA\_SEC\_PAGE\_INFO**</span></span>](dsa-sec-page-info.md)
</dt> <dt>

[<span data-ttu-id="d953c-129">**LocalFree**</span><span class="sxs-lookup"><span data-stu-id="d953c-129">**LocalFree**</span></span>](/windows/desktop/api/winbase/nf-winbase-localfree)
</dt> </dl>

 

