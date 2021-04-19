---
title: Message WM_DSA_SHEET_CLOSE_NOTIFY
description: Publié dans le composant logiciel enfichable MMC Active Directory lorsqu’une feuille de propriétés secondaire est détruite.
ms.assetid: 74271550-e1f7-4576-a04f-52d5b7c619cb
ms.tgt_platform: multiple
keywords:
- Message de WM_DSA_SHEET_CLOSE_NOTIFY Active Directory
topic_type:
- apiref
api_name:
- WM_DSA_SHEET_CLOSE_NOTIFY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36f03cdb6224ae5f55bc995897d766ce61e67693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518079"
---
# <a name="wm_dsa_sheet_close_notify-message"></a><span data-ttu-id="df33d-104">Message de fermeture de la \_ feuille du DSA WM \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="df33d-104">WM\_DSA\_SHEET\_CLOSE\_NOTIFY message</span></span>

<span data-ttu-id="df33d-105">Le message de fermeture de la feuille de calcul **\_ DSA DSA \_ \_ \_** est publié dans le composant logiciel enfichable MMC Active Directory lorsqu’une feuille de propriétés secondaire est détruite.</span><span class="sxs-lookup"><span data-stu-id="df33d-105">The **WM\_DSA\_SHEET\_CLOSE\_NOTIFY** message is posted to the Active Directory MMC snap-in when a secondary property sheet is destroyed.</span></span>

> [!Note]  
> <span data-ttu-id="df33d-106">La valeur de ce message n’est pas définie dans un fichier d’en-tête publié.</span><span class="sxs-lookup"><span data-stu-id="df33d-106">This message value is not defined in a published header file.</span></span> <span data-ttu-id="df33d-107">Pour utiliser cette valeur de message, vous devez la définir vous-même dans le format exact indiqué.</span><span class="sxs-lookup"><span data-stu-id="df33d-107">To use this message value, you must define it yourself in the exact format shown.</span></span>

 


```C++
#define WM_DSA_SHEET_CLOSE_NOTIFY (WM_USER + 5)
```




```C++
LRESULT SendMessage( (HWND)   hwnd, 
                     (UINT)   WM_DSA_SHEET_CLOSE_NOTIFY,
                     (WPARAM) wParam, 
                     (LPARAM) lParam);
```



## <a name="parameters"></a><span data-ttu-id="df33d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df33d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df33d-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="df33d-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="df33d-110">Handle de fenêtre de la fenêtre du composant logiciel enfichable qui traitera ce message.</span><span class="sxs-lookup"><span data-stu-id="df33d-110">The window handle of the snap-in window that will process this message.</span></span> <span data-ttu-id="df33d-111">Ce handle est obtenu à partir du membre **hwndHidden** de la structure [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="df33d-111">This handle is obtained from the **hwndHidden** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="df33d-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="df33d-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df33d-113">Contient une valeur 32 bits définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="df33d-113">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="df33d-114">Elle est obtenue à partir du membre **wParamSheetClose** de la structure [**PROPSHEETCFG**](propsheetcfg.md) .</span><span class="sxs-lookup"><span data-stu-id="df33d-114">This is obtained from the **wParamSheetClose** member of the [**PROPSHEETCFG**](propsheetcfg.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="df33d-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="df33d-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="df33d-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="df33d-116">Not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df33d-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df33d-117">Return value</span></span>

<span data-ttu-id="df33d-118">La valeur de retour de ce message n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="df33d-118">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="df33d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df33d-119">Requirements</span></span>



| <span data-ttu-id="df33d-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df33d-120">Requirement</span></span> | <span data-ttu-id="df33d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="df33d-121">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="df33d-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df33d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="df33d-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="df33d-123">Windows Vista</span></span><br/>       |
| <span data-ttu-id="df33d-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df33d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="df33d-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="df33d-125">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="df33d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df33d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df33d-127">**PROPSHEETCFG**</span><span class="sxs-lookup"><span data-stu-id="df33d-127">**PROPSHEETCFG**</span></span>](propsheetcfg.md)
</dt> </dl>

 

 





