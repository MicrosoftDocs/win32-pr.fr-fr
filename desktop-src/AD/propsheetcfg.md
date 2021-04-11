---
title: PROPSHEETCFG, structure
description: Utilisé pour contenir les données de configuration de la feuille de propriétés.
ms.assetid: d3bde744-9d85-4506-894f-f8be3463721f
ms.tgt_platform: multiple
keywords:
- Active Directory de la structure PROPSHEETCFG
- Active Directory pointeur de structure PPROPSHEETCFG
topic_type:
- apiref
api_name:
- PROPSHEETCFG
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 33f4a1186cc756435cc49ed7c81592385faaee60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032896"
---
# <a name="propsheetcfg-structure"></a><span data-ttu-id="7a42b-105">PROPSHEETCFG, structure</span><span class="sxs-lookup"><span data-stu-id="7a42b-105">PROPSHEETCFG structure</span></span>

<span data-ttu-id="7a42b-106">La structure **PROPSHEETCFG** est utilisée pour contenir les données de configuration de la feuille de propriétés.</span><span class="sxs-lookup"><span data-stu-id="7a42b-106">The **PROPSHEETCFG** structure is used to contain property sheet configuration data.</span></span> <span data-ttu-id="7a42b-107">Cette structure est contenue dans le format de presse-papiers [**CFSTR \_ DS \_ PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="7a42b-107">This structure is contained in the [**CFSTR\_DS\_PROPSHEETCONFIG**](cfstr-ds-propsheetconfig.md) clipboard format.</span></span>

> [!Note]  
> <span data-ttu-id="7a42b-108">Cette structure n’est pas définie dans un fichier d’en-tête publié.</span><span class="sxs-lookup"><span data-stu-id="7a42b-108">This structure is not defined in a published header file.</span></span> <span data-ttu-id="7a42b-109">Pour utiliser cette structure, vous devez la définir vous-même dans le format exact indiqué.</span><span class="sxs-lookup"><span data-stu-id="7a42b-109">To use this structure, you must define it yourself in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7a42b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a42b-110">Syntax</span></span>


```C++
typedef struct {
  LONG_PTR lNotifyHandle;
  HWND     hwndParentSheet;
  HWND     hwndHidden;
  WPARAM   wParamSheetClose;
} PROPSHEETCFG, *PPROPSHEETCFG;
```



## <a name="members"></a><span data-ttu-id="7a42b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="7a42b-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="7a42b-112">**lNotifyHandle**</span><span class="sxs-lookup"><span data-stu-id="7a42b-112">**lNotifyHandle**</span></span>
</dt> <dd>

<span data-ttu-id="7a42b-113">Contient le handle de notification.</span><span class="sxs-lookup"><span data-stu-id="7a42b-113">Contains the notification handle.</span></span> <span data-ttu-id="7a42b-114">Il est identique au handle passé pour le paramètre de *handle* dans la méthode [**IExtendPropertySheet2 :: CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7a42b-114">This is identical to the handle passed for the *handle* parameter in the [**IExtendPropertySheet2::CreatePropertyPages**](/previous-versions/windows/desktop/legacy/aa814847(v=vs.85)) method.</span></span>

</dd> <dt>

<span data-ttu-id="7a42b-115">**hwndParentSheet**</span><span class="sxs-lookup"><span data-stu-id="7a42b-115">**hwndParentSheet**</span></span>
</dt> <dd>

<span data-ttu-id="7a42b-116">Contient le handle de fenêtre de la feuille de propriétés parente.</span><span class="sxs-lookup"><span data-stu-id="7a42b-116">Contains the window handle of the parent property sheet.</span></span>

</dd> <dt>

<span data-ttu-id="7a42b-117">**hwndHidden**</span><span class="sxs-lookup"><span data-stu-id="7a42b-117">**hwndHidden**</span></span>
</dt> <dd>

<span data-ttu-id="7a42b-118">Contient le handle de la fenêtre masquée.</span><span class="sxs-lookup"><span data-stu-id="7a42b-118">Contains the handle of the hidden window.</span></span>

</dd> <dt>

<span data-ttu-id="7a42b-119">**wParamSheetClose**</span><span class="sxs-lookup"><span data-stu-id="7a42b-119">**wParamSheetClose**</span></span>
</dt> <dd>

<span data-ttu-id="7a42b-120">Contient une valeur 32 bits définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="7a42b-120">Contains an application-defined 32-bit value.</span></span> <span data-ttu-id="7a42b-121">Cette valeur est renvoyée à l’application dans le *wParam* du message de fermeture de la feuille de calcul [**WM \_ DSA \_ \_ \_**](wm-dsa-sheet-close-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="7a42b-121">This value is passed back to the application in the *wParam* of the [**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**](wm-dsa-sheet-close-notify.md) message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a42b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a42b-122">Requirements</span></span>



| <span data-ttu-id="7a42b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a42b-123">Requirement</span></span> | <span data-ttu-id="7a42b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a42b-124">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="7a42b-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a42b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7a42b-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a42b-126">Windows Vista</span></span><br/>       |
| <span data-ttu-id="7a42b-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a42b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7a42b-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a42b-128">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a42b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a42b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a42b-130">**CFSTR \_ DS \_ PROPSHEETCONFIG**</span><span class="sxs-lookup"><span data-stu-id="7a42b-130">**CFSTR\_DS\_PROPSHEETCONFIG**</span></span>](cfstr-ds-propsheetconfig.md)
</dt> <dt>

[<span data-ttu-id="7a42b-131">**notification de fermeture de la \_ feuille du DSA WM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7a42b-131">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
</dt> </dl>

 

