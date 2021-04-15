---
title: Message TB_LOADIMAGES (commctrl. h)
description: Charge les images de bouton définies par le système dans la liste d’images d’un contrôle ToolBar.
ms.assetid: 61146f43-9fd9-4fe3-b85c-cf465f2de769
keywords:
- TB_LOADIMAGES les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_LOADIMAGES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0b0ba6bf75855a0b81ac56438489d7eced3d589
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466223"
---
# <a name="tb_loadimages-message"></a><span data-ttu-id="91f70-104">TO \_ LOADIMAGES message</span><span class="sxs-lookup"><span data-stu-id="91f70-104">TB\_LOADIMAGES message</span></span>

<span data-ttu-id="91f70-105">Charge les images de bouton définies par le système dans la liste d’images d’un contrôle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="91f70-105">Loads system-defined button images into a toolbar control's image list.</span></span>

## <a name="parameters"></a><span data-ttu-id="91f70-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91f70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91f70-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91f70-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91f70-108">Identificateur d’une liste d’images de boutons définie par le système.</span><span class="sxs-lookup"><span data-stu-id="91f70-108">Identifier of a system-defined button image list.</span></span> <span data-ttu-id="91f70-109">Ce paramètre peut être défini sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="91f70-109">This parameter can be set to one of the following values.</span></span>



| <span data-ttu-id="91f70-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="91f70-110">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="91f70-111">Signification</span><span class="sxs-lookup"><span data-stu-id="91f70-111">Meaning</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="IDB_HIST_LARGE_COLOR"></span><span id="idb_hist_large_color"></span><dl> <span data-ttu-id="91f70-112"><dt>**format d' \_ historique des \_ couleurs de grande taille \_**</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-112"><dt>**IDB\_HIST\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="91f70-113">Bitmaps de l’Explorateur Windows en grande taille.</span><span class="sxs-lookup"><span data-stu-id="91f70-113">Windows Explorer bitmaps in large size.</span></span><br/>                                  |
| <span id="IDB_HIST_SMALL_COLOR"></span><span id="idb_hist_small_color"></span><dl> <span data-ttu-id="91f70-114"><dt>**\_couleur de \_ petite taille \_ de IDB hist**</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-114"><dt>**IDB\_HIST\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="91f70-115">Bitmaps de l’Explorateur Windows en petite taille.</span><span class="sxs-lookup"><span data-stu-id="91f70-115">Windows Explorer bitmaps in small size.</span></span><br/>                                  |
| <span id="IDB_STD_LARGE_COLOR"></span><span id="idb_std_large_color"></span><dl> <span data-ttu-id="91f70-116"><dt>**\_taille STD de la \_ grande \_ couleur**</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-116"><dt>**IDB\_STD\_LARGE\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="91f70-117">Images bitmap standard en grande taille.</span><span class="sxs-lookup"><span data-stu-id="91f70-117">Standard bitmaps in large size.</span></span><br/>                                          |
| <span id="IDB_STD_SMALL_COLOR"></span><span id="idb_std_small_color"></span><dl> <span data-ttu-id="91f70-118"><dt>**\_couleur standard de la \_ petite \_ couleur IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-118"><dt>**IDB\_STD\_SMALL\_COLOR**</dt></span></span> </dl>    | <span data-ttu-id="91f70-119">Images bitmap standard de petite taille.</span><span class="sxs-lookup"><span data-stu-id="91f70-119">Standard bitmaps in small size.</span></span><br/>                                          |
| <span id="IDB_VIEW_LARGE_COLOR"></span><span id="idb_view_large_color"></span><dl> <span data-ttu-id="91f70-120"><dt>**\_ \_ grande \_ couleur de la vue IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-120"><dt>**IDB\_VIEW\_LARGE\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="91f70-121">Affichez les bitmaps en grandes tailles.</span><span class="sxs-lookup"><span data-stu-id="91f70-121">View bitmaps in large size.</span></span><br/>                                              |
| <span id="IDB_VIEW_SMALL_COLOR"></span><span id="idb_view_small_color"></span><dl> <span data-ttu-id="91f70-122"><dt>**\_couleur de \_ petite taille \_ de la vue IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-122"><dt>**IDB\_VIEW\_SMALL\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="91f70-123">Affichez les bitmaps dans une petite taille.</span><span class="sxs-lookup"><span data-stu-id="91f70-123">View bitmaps in small size.</span></span><br/>                                              |
| <span id="IDB_HIST_NORMAL"></span><span id="idb_hist_normal"></span><dl> <span data-ttu-id="91f70-124"><dt>**historique des IDB- \_ \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-124"><dt>**IDB\_HIST\_NORMAL**</dt></span></span> </dl>                 | <span data-ttu-id="91f70-125">Les boutons de déplacement de l’Explorateur Windows et les bitmaps favoris sont dans un état normal.</span><span class="sxs-lookup"><span data-stu-id="91f70-125">Windows Explorer travel buttons and favorites bitmaps in normal state.</span></span><br/>   |
| <span id="IDB_HIST_HOT"></span><span id="idb_hist_hot"></span><dl> <span data-ttu-id="91f70-126"><dt>**\_historique \_ chaud de IDB**</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-126"><dt>**IDB\_HIST\_HOT**</dt></span></span> </dl>                          | <span data-ttu-id="91f70-127">Les boutons de déplacement de l’Explorateur Windows et les bitmaps favoris dans un état actif.</span><span class="sxs-lookup"><span data-stu-id="91f70-127">Windows Explorer travel buttons and favorites bitmaps in hot state.</span></span><br/>      |
| <span id="IDB_HIST_DISABLED"></span><span id="idb_hist_disabled"></span><dl> <span data-ttu-id="91f70-128"><dt>**Hist. IDB \_ \_ désactivé**</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-128"><dt>**IDB\_HIST\_DISABLED**</dt></span></span> </dl>           | <span data-ttu-id="91f70-129">Les boutons de déplacement et les bitmaps favoris de l’Explorateur Windows sont en état désactivé.</span><span class="sxs-lookup"><span data-stu-id="91f70-129">Windows Explorer travel buttons and favorites bitmaps in disabled state.</span></span><br/> |
| <span id="IDB_HIST_PRESSED"></span><span id="idb_hist_pressed"></span><dl> <span data-ttu-id="91f70-130"><dt>**historique de IDB \_ \_ enfoncé**</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-130"><dt>**IDB\_HIST\_PRESSED**</dt></span></span> </dl>              | <span data-ttu-id="91f70-131">Les boutons de déplacement et les bitmaps favoris de l’Explorateur Windows sont en état appuyé.</span><span class="sxs-lookup"><span data-stu-id="91f70-131">Windows Explorer travel buttons and favorites bitmaps in pressed state.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="91f70-132">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91f70-132">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91f70-133">Handle d’instance.</span><span class="sxs-lookup"><span data-stu-id="91f70-133">Instance handle.</span></span> <span data-ttu-id="91f70-134">Ce paramètre doit être défini sur HINST \_ COMMCTRL.</span><span class="sxs-lookup"><span data-stu-id="91f70-134">This parameter must be set to HINST\_COMMCTRL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91f70-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91f70-135">Return value</span></span>

<span data-ttu-id="91f70-136">Nombre d’images dans la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="91f70-136">The count of images in the image list.</span></span> <span data-ttu-id="91f70-137">Retourne zéro si la barre d’outils n’a pas de liste d’images ou si la liste d’images existante est vide.</span><span class="sxs-lookup"><span data-stu-id="91f70-137">Returns zero if the toolbar has no image list or if the existing image list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="91f70-138">Notes</span><span class="sxs-lookup"><span data-stu-id="91f70-138">Remarks</span></span>

<span data-ttu-id="91f70-139">Vous devez utiliser les valeurs d’index d’image appropriées lorsque vous préparez des structures [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) avant d’envoyer le message [**to \_ ADDBUTTONS**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="91f70-139">You must use the proper image index values when you prepare [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structures prior to sending the [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span> <span data-ttu-id="91f70-140">Pour obtenir la liste des valeurs d’index d’image pour ces bitmaps prédéfinies, consultez la rubrique [valeurs d’index d’image du bouton standard de la barre d’outils](toolbar-standard-button-image-index-values.md).</span><span class="sxs-lookup"><span data-stu-id="91f70-140">For a list of image index values for these preset bitmaps, see [Toolbar Standard Button Image Index Values](toolbar-standard-button-image-index-values.md).</span></span>

## <a name="examples"></a><span data-ttu-id="91f70-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="91f70-141">Examples</span></span>

<span data-ttu-id="91f70-142">L’exemple de code suivant charge les images de petite couleur système standard.</span><span class="sxs-lookup"><span data-stu-id="91f70-142">The following sample code loads the system standard small color images.</span></span>


```C++
// hWndToobar is the window handle of the toolbar control.
SendMessage(hWndToolbar, TB_LOADIMAGES, (WPARAM)IDB_STD_SMALL_COLOR, (LPARAM)HINST_COMMCTRL);
```



## <a name="requirements"></a><span data-ttu-id="91f70-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91f70-143">Requirements</span></span>



| <span data-ttu-id="91f70-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91f70-144">Requirement</span></span> | <span data-ttu-id="91f70-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="91f70-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91f70-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91f70-146">Minimum supported client</span></span><br/> | <span data-ttu-id="91f70-147">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91f70-147">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="91f70-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91f70-148">Minimum supported server</span></span><br/> | <span data-ttu-id="91f70-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91f70-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91f70-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="91f70-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="91f70-151"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="91f70-151"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91f70-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91f70-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f70-153">**TO \_ ADDBITMAP**</span><span class="sxs-lookup"><span data-stu-id="91f70-153">**TB\_ADDBITMAP**</span></span>](tb-addbitmap.md)
</dt> </dl>

 

 





