---
title: Message WM_DWMSENDICONICTHUMBNAIL (dwmapi. h)
description: Indique à une fenêtre de fournir une bitmap statique à utiliser comme représentation miniature de cette fenêtre.
ms.assetid: 476c2542-f4d0-4777-93d3-bf50da26d94f
keywords:
- Message de WM_DWMSENDICONICTHUMBNAIL Gestionnaire de fenêtrage
topic_type:
- apiref
api_name:
- WM_DWMSENDICONICTHUMBNAIL
api_location:
- Dwmapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ded5b734278973afe35f5ed3d9fbb5b0aec9242b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466674"
---
# <a name="wm_dwmsendiconicthumbnail-message"></a><span data-ttu-id="71ecc-104">\_Message WM DWMSENDICONICTHUMBNAIL</span><span class="sxs-lookup"><span data-stu-id="71ecc-104">WM\_DWMSENDICONICTHUMBNAIL message</span></span>

<span data-ttu-id="71ecc-105">Indique à une fenêtre de fournir une bitmap statique à utiliser comme représentation miniature de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71ecc-105">Instructs a window to provide a static bitmap to use as a thumbnail representation of that window.</span></span>

## <a name="parameters"></a><span data-ttu-id="71ecc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71ecc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ecc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71ecc-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71ecc-108">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="71ecc-108">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="71ecc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71ecc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71ecc-110">Le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) de cette valeur est la coordonnée x maximale de la miniature.</span><span class="sxs-lookup"><span data-stu-id="71ecc-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) of this value is the maximum x-coordinate of the thumbnail.</span></span> <span data-ttu-id="71ecc-111">Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) est la coordonnée y maximale.</span><span class="sxs-lookup"><span data-stu-id="71ecc-111">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) is the maximum y-coordinate.</span></span> <span data-ttu-id="71ecc-112">Si une miniature a une dimension qui dépasse l’une des deux valeurs ou les deux, le DWM n’accepte pas la miniature.</span><span class="sxs-lookup"><span data-stu-id="71ecc-112">If a thumbnail has a dimension that exceeds one or both of these values, the DWM does not accept the thumbnail.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ecc-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71ecc-113">Return value</span></span>

<span data-ttu-id="71ecc-114">Si une application traite ce message, elle doit retourner la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="71ecc-114">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="71ecc-115">Notes</span><span class="sxs-lookup"><span data-stu-id="71ecc-115">Remarks</span></span>

<span data-ttu-id="71ecc-116">DWM envoie ce message à une fenêtre si toutes les situations suivantes sont vraies :</span><span class="sxs-lookup"><span data-stu-id="71ecc-116">DWM sends this message to a window if all of the following situations are true:</span></span>

-   <span data-ttu-id="71ecc-117">DWM affiche une représentation sous forme de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71ecc-117">DWM is displaying an iconic representation of the window.</span></span>
-   <span data-ttu-id="71ecc-118">[**DWMWA a l’attribut \_ \_ \_ bitmap sous forme**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) est défini dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71ecc-118">The [**DWMWA\_HAS\_ICONIC\_BITMAP**](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute) attribute is set on the window.</span></span>
-   <span data-ttu-id="71ecc-119">La fenêtre n’a pas défini une image bitmap mise en cache.</span><span class="sxs-lookup"><span data-stu-id="71ecc-119">The window did not set a cached bitmap.</span></span>
-   <span data-ttu-id="71ecc-120">Il y a de la place dans le cache pour une autre bitmap.</span><span class="sxs-lookup"><span data-stu-id="71ecc-120">There is room in the cache for another bitmap.</span></span>

<span data-ttu-id="71ecc-121">La fenêtre qui reçoit ce message doit répondre en générant une image bitmap qui n’est pas supérieure à la taille demandée dans les paramètres du message.</span><span class="sxs-lookup"><span data-stu-id="71ecc-121">The window that receives this message should respond by generating a bitmap that is not larger than the size that is requested in the message parameters.</span></span> <span data-ttu-id="71ecc-122">La fenêtre appelle ensuite la fonction [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) pour remplacer la miniature par défaut.</span><span class="sxs-lookup"><span data-stu-id="71ecc-122">The window then calls the [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) function to override the default thumbnail.</span></span> <span data-ttu-id="71ecc-123">Si la fenêtre ne fournit pas de bitmap dans un laps de temps donné, DWM utilise sa propre représentation sous forme par défaut pour la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="71ecc-123">If the window does not supply a bitmap in a given amount of time, DWM uses its own default iconic representation for the window.</span></span>

<span data-ttu-id="71ecc-124">La fenêtre doit appartenir au processus appelant.</span><span class="sxs-lookup"><span data-stu-id="71ecc-124">The window must belong to the calling process.</span></span>

## <a name="examples"></a><span data-ttu-id="71ecc-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="71ecc-125">Examples</span></span>

<span data-ttu-id="71ecc-126">L’exemple de code suivant montre comment répondre au message **WM \_ DWMSENDICONICTHUMBNAIL** .</span><span class="sxs-lookup"><span data-stu-id="71ecc-126">The following code example shows how to respond to the **WM\_DWMSENDICONICTHUMBNAIL** message.</span></span> <span data-ttu-id="71ecc-127">L’exemple appelle [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), avec un handle vers une image bitmap personnalisée indépendante du périphérique à utiliser comme représentation Windows.</span><span class="sxs-lookup"><span data-stu-id="71ecc-127">The example calls [**DwmSetIconicThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail), with a handle to a customized, device-indepedent bitmap to use as the windows' representation.</span></span>


```C++
        case WM_DWMSENDICONICTHUMBNAIL:
        {    
            // This window is being asked to provide its iconic bitmap. This indicates
            // a thumbnail is being drawn.
            hbm = CreateDIB(HIWORD(lParam), LOWORD(lParam)); 
            if (hbm)
            {
                hr = DwmSetIconicThumbnail(hwnd, hbm, 0);
                DeleteObject(hbm);
            }
        }
        break;
```



<span data-ttu-id="71ecc-128">Pour obtenir un exemple complet, consultez les exemples de [miniatures Customize a sous forme et Live Preview](dwm-sample-customizethumbnail.md) .</span><span class="sxs-lookup"><span data-stu-id="71ecc-128">For the complete example, see the [Customize an Iconic Thumbnail and a Live Preview Bitmap](dwm-sample-customizethumbnail.md) sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="71ecc-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71ecc-129">Requirements</span></span>



| <span data-ttu-id="71ecc-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71ecc-130">Requirement</span></span> | <span data-ttu-id="71ecc-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="71ecc-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="71ecc-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71ecc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="71ecc-133">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71ecc-133">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="71ecc-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71ecc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="71ecc-135">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71ecc-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="71ecc-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="71ecc-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="71ecc-137"><dt>Dwmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="71ecc-137"><dt>Dwmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71ecc-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71ecc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ecc-139">**DwmInvalidateIconicBitmaps**</span><span class="sxs-lookup"><span data-stu-id="71ecc-139">**DwmInvalidateIconicBitmaps**</span></span>](/windows/desktop/api/Dwmapi/nf-dwmapi-dwminvalidateiconicbitmaps)
</dt> <dt>

[<span data-ttu-id="71ecc-140">**\_DWMSENDICONICLIVEPREVIEWBITMAP WM**</span><span class="sxs-lookup"><span data-stu-id="71ecc-140">**WM\_DWMSENDICONICLIVEPREVIEWBITMAP**</span></span>](wm-dwmsendiconiclivepreviewbitmap.md)
</dt> </dl>

 

