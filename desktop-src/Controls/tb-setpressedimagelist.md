---
title: Message TB_SETPRESSEDIMAGELIST (commctrl. h)
description: Définit la liste d’images utilisée par la barre d’outils pour afficher les boutons qui sont dans un état appuyé.
ms.assetid: d0e061ec-3a89-4c2d-b7f7-5f2061098428
keywords:
- TB_SETPRESSEDIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETPRESSEDIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a3c6dafed6dbfdf2a654f4f95f1cef636ba762
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519305"
---
# <a name="tb_setpressedimagelist-message"></a><span data-ttu-id="23c85-104">TO \_ SETPRESSEDIMAGELIST message</span><span class="sxs-lookup"><span data-stu-id="23c85-104">TB\_SETPRESSEDIMAGELIST message</span></span>

<span data-ttu-id="23c85-105">Définit la liste d’images utilisée par la barre d’outils pour afficher les boutons qui sont dans un état appuyé.</span><span class="sxs-lookup"><span data-stu-id="23c85-105">Sets the image list that the toolbar uses to display buttons that are in a pressed state.</span></span>

## <a name="parameters"></a><span data-ttu-id="23c85-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23c85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23c85-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23c85-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23c85-108">Index de la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="23c85-108">The index of the image list.</span></span> <span data-ttu-id="23c85-109">Si vous n’utilisez qu’une seule liste d’images, définissez ce paramètre sur zéro.</span><span class="sxs-lookup"><span data-stu-id="23c85-109">If you use only one image list, set this parameter to zero.</span></span> <span data-ttu-id="23c85-110">Pour plus d’informations sur l’utilisation de plusieurs listes d’images, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="23c85-110">See Remarks for details on using multiple image lists.</span></span>

</dd> <dt>

<span data-ttu-id="23c85-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23c85-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="23c85-112">Handle de la liste d’images à définir.</span><span class="sxs-lookup"><span data-stu-id="23c85-112">Handle to the image list to set.</span></span> <span data-ttu-id="23c85-113">Si ce paramètre a la **valeur null**, aucune image ne s’affiche dans les boutons.</span><span class="sxs-lookup"><span data-stu-id="23c85-113">If this parameter is **NULL**, no images are displayed in the buttons.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23c85-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23c85-114">Return value</span></span>

<span data-ttu-id="23c85-115">Retourne le handle de la liste d’images utilisée précédemment pour afficher les boutons dans un état appuyé, ou **null** si aucune liste d’images n’a été définie précédemment.</span><span class="sxs-lookup"><span data-stu-id="23c85-115">Returns the handle to the image list previously used to display buttons in their pressed state, or **NULL** if no such image list was previously set.</span></span>

## <a name="remarks"></a><span data-ttu-id="23c85-116">Notes</span><span class="sxs-lookup"><span data-stu-id="23c85-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23c85-117">Votre application est chargée de libérer la liste d’images après la destruction de la barre d’outils.</span><span class="sxs-lookup"><span data-stu-id="23c85-117">Your application is responsible for freeing the image list after the toolbar is destroyed.</span></span>

 

<span data-ttu-id="23c85-118">Le **message \_ SETPRESSEDIMAGELIST to** ne peut pas être combiné avec [**to \_ ADDBITMAP**](tb-addbitmap.md).</span><span class="sxs-lookup"><span data-stu-id="23c85-118">The **TB\_SETPRESSEDIMAGELIST** message cannot be combined with [**TB\_ADDBITMAP**](tb-addbitmap.md).</span></span> <span data-ttu-id="23c85-119">Elle ne peut pas non plus être utilisée avec les barres d’outils créées avec [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), qui appelle **to \_ ADDBITMAP** en interne.</span><span class="sxs-lookup"><span data-stu-id="23c85-119">It also cannot be used with toolbars created with [**CreateToolbarEx**](/windows/desktop/api/Commctrl/nf-commctrl-createtoolbarex), which calls **TB\_ADDBITMAP** internally.</span></span> <span data-ttu-id="23c85-120">Lorsque vous créez une barre d’outils avec **CreateToolbarEx** ou utilisez **to \_ ADDBITMAP** pour ajouter des images, la barre d’outils gère la liste d’images en interne.</span><span class="sxs-lookup"><span data-stu-id="23c85-120">When you create a toolbar with **CreateToolbarEx** or use **TB\_ADDBITMAP** to add images, the toolbar manages the image list internally.</span></span> <span data-ttu-id="23c85-121">Toute tentative de modification avec **to \_ SETPRESSEDIMAGELIST** a des conséquences imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="23c85-121">Attempting to modify it with **TB\_SETPRESSEDIMAGELIST** has unpredictable consequences.</span></span>

<span data-ttu-id="23c85-122">Il n’est pas nécessaire que les images de bouton proviennent de la même liste d’images.</span><span class="sxs-lookup"><span data-stu-id="23c85-122">Button images need not come from the same image list.</span></span> <span data-ttu-id="23c85-123">Pour utiliser plusieurs listes d’images pour vos images de bouton de barre d’outils :</span><span class="sxs-lookup"><span data-stu-id="23c85-123">To use multiple image lists for your toolbar button images:</span></span>

1.  <span data-ttu-id="23c85-124">Activez plusieurs listes d’images en envoyant le contrôle ToolBar à un message [**\_ SETVERSION CCM**](ccm-setversion.md) avec *wParam* (le numéro de version) défini sur 5.</span><span class="sxs-lookup"><span data-stu-id="23c85-124">Enable multiple image lists by sending the toolbar control a [**CCM\_SETVERSION**](ccm-setversion.md) message with *wParam* (the version number) set to 5.</span></span>
2.  <span data-ttu-id="23c85-125">Pour chaque liste d’images que vous souhaitez utiliser, envoyez au contrôle ToolBar un message **\_ SETPRESSEDIMAGELIST to** .</span><span class="sxs-lookup"><span data-stu-id="23c85-125">For each image list you want to use, send the toolbar control a **TB\_SETPRESSEDIMAGELIST** message.</span></span> <span data-ttu-id="23c85-126">Affectez à *wParam* une valeur *wParam* définie par l’application qui sera utilisée pour identifier la liste.</span><span class="sxs-lookup"><span data-stu-id="23c85-126">Set *wParam* to an application-defined *wParam* value that will be used to identify the list.</span></span> <span data-ttu-id="23c85-127">Affectez à *lParam* la valeur du handle HIMAGELIST de la liste.</span><span class="sxs-lookup"><span data-stu-id="23c85-127">Set *lParam* to the list's HIMAGELIST handle.</span></span>
3.  <span data-ttu-id="23c85-128">Pour chaque bouton, définissez le membre **iBitmap** de la structure [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) du bouton sur MAKELONG (*iIndex*, *iImageID*).</span><span class="sxs-lookup"><span data-stu-id="23c85-128">For each button, set the **iBitmap** member of the button's [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) structure to MAKELONG(*iIndex*, *iImageID*).</span></span> <span data-ttu-id="23c85-129">La valeur *iImageID* est l’ID de la liste d’images appropriée définie à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="23c85-129">The *iImageID* value is the ID of the appropriate image list that was defined in step two.</span></span> <span data-ttu-id="23c85-130">La valeur *iIndex* est l’index de l’image particulière dans cette liste.</span><span class="sxs-lookup"><span data-stu-id="23c85-130">The *iIndex* value is the index of the particular image within that list.</span></span>
4.  <span data-ttu-id="23c85-131">Ajoutez les boutons en envoyant le contrôle de barre d’outils à un message [**\_ ADDBUTTONS to**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="23c85-131">Add the buttons by sending the toolbar control a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>

<span data-ttu-id="23c85-132">Le fragment de code suivant montre comment ajouter cinq boutons à une barre d’outils, avec des images de trois listes d’images différentes.</span><span class="sxs-lookup"><span data-stu-id="23c85-132">The following code fragment illustrates how to add five buttons to a toolbar, with images from three different image lists.</span></span> <span data-ttu-id="23c85-133">La prise en charge de plusieurs listes d’images est activée avec un message [**CCM \_ SETVERSION**](ccm-setversion.md) .</span><span class="sxs-lookup"><span data-stu-id="23c85-133">Support for multiple image lists is enabled with a [**CCM\_SETVERSION**](ccm-setversion.md) message.</span></span> <span data-ttu-id="23c85-134">Les listes d’images sont ensuite définies et les ID attribués de 0-2.</span><span class="sxs-lookup"><span data-stu-id="23c85-134">The image lists are then set and assigned IDs of 0-2.</span></span> <span data-ttu-id="23c85-135">Les boutons sont affectés aux images à partir des listes d’images comme suit :</span><span class="sxs-lookup"><span data-stu-id="23c85-135">The buttons are assigned images from the image lists as follows:</span></span>

-   <span data-ttu-id="23c85-136">Le bouton 0 provient de la liste d’images zéro (ahimd \[ 0 \] ) avec l’index 1.</span><span class="sxs-lookup"><span data-stu-id="23c85-136">Button 0 is from image list zero (ahim\[0\]) with index of 1.</span></span>
-   <span data-ttu-id="23c85-137">Le bouton 1 est issu de la liste d’images 1 (Ahim \[ 1 \] ) avec un index de 1.</span><span class="sxs-lookup"><span data-stu-id="23c85-137">Button 1 is from image list one (ahim\[1\]) with an index of 1.</span></span>
-   <span data-ttu-id="23c85-138">Le bouton 2 provient de la liste d’images deux (Ahim \[ 2 \] ) avec un index de 1.</span><span class="sxs-lookup"><span data-stu-id="23c85-138">Button 2 is from image list two (ahim\[2\]) with an index of 1.</span></span>
-   <span data-ttu-id="23c85-139">Le bouton 3 est issu de la liste d’images zéro (ahimd \[ 0 \] ) avec un index de 2.</span><span class="sxs-lookup"><span data-stu-id="23c85-139">Button 3 is from image list zero (ahim\[0\]) with an index of 2.</span></span>
-   <span data-ttu-id="23c85-140">Le bouton 4 est issu de la liste d’images 1 (Ahim \[ 1 \] ) avec un index de 3.</span><span class="sxs-lookup"><span data-stu-id="23c85-140">Button 4 is from image list one (ahim\[1\]) with an index of 3.</span></span>

<span data-ttu-id="23c85-141">Enfin, les boutons sont ajoutés au contrôle Toolbar avec un message [**\_ ADDBUTTONS to**](tb-addbuttons.md) .</span><span class="sxs-lookup"><span data-stu-id="23c85-141">Finally, the buttons are added to the toolbar control with a [**TB\_ADDBUTTONS**](tb-addbuttons.md) message.</span></span>


```
// Enable multiple image lists
    SendMessage(hwndTB, CCM_SETVERSION, (WPARAM) 5, 0); 

    //Set the image lists and assign them IDs of 0-2
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 0, (LPARAM)ahiml[0]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 1, (LPARAM)ahiml[1]);
    SendMessage(hwndTB, TB_SETPRESSEDIMAGELIST, 2, (LPARAM)ahiml[2]);

    // Create the five buttons
    TBBUTTON rgtb[5];
    
    //... initialize the TBBUTTON structures as usual ...
    
    //Assign images to each button
    rgtb[0].iBitmap = MAKELONG(1, 0);
    rgtb[1].iBitmap = MAKELONG(1, 1);
    rgtb[2].iBitmap = MAKELONG(1, 2);
    rgtb[3].iBitmap = MAKELONG(2, 0);
    rgtb[4].iBitmap = MAKELONG(3, 1);

    // Add the five buttons to the toolbar control
    SendMessage(hwndTB, TB_ADDBUTTONS, 5, (LPARAM)(&rgtb);
```



## <a name="requirements"></a><span data-ttu-id="23c85-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23c85-142">Requirements</span></span>



| <span data-ttu-id="23c85-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23c85-143">Requirement</span></span> | <span data-ttu-id="23c85-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="23c85-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23c85-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23c85-145">Minimum supported client</span></span><br/> | <span data-ttu-id="23c85-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23c85-146">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23c85-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23c85-147">Minimum supported server</span></span><br/> | <span data-ttu-id="23c85-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23c85-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23c85-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="23c85-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="23c85-150"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="23c85-150"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23c85-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23c85-151">See also</span></span>

<dl> <dt>

<span data-ttu-id="23c85-152">**Référence**</span><span class="sxs-lookup"><span data-stu-id="23c85-152">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="23c85-153">**TO \_ GETPRESSEDIMAGELIST**</span><span class="sxs-lookup"><span data-stu-id="23c85-153">**TB\_GETPRESSEDIMAGELIST**</span></span>](tb-getpressedimagelist.md)
</dt> <dt>

<span data-ttu-id="23c85-154">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="23c85-154">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="23c85-155">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="23c85-155">[**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))</span></span>
</dt> </dl>

 

