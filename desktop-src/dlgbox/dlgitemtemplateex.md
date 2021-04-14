---
title: DLGITEMTEMPLATEEX, structure
description: Bloc de texte utilisé par un modèle de boîte de dialogue étendu pour décrire la boîte de dialogue étendue. Pour obtenir une description du format d’un modèle de boîte de dialogue étendue, consultez DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Boîtes de dialogue de la structure DLGITEMTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385215"
---
# <a name="dlgitemtemplateex-structure"></a><span data-ttu-id="f13e8-105">DLGITEMTEMPLATEEX, structure</span><span class="sxs-lookup"><span data-stu-id="f13e8-105">DLGITEMTEMPLATEEX structure</span></span>

<span data-ttu-id="f13e8-106">Bloc de texte utilisé par un modèle de boîte de dialogue étendu pour décrire la boîte de dialogue étendue.</span><span class="sxs-lookup"><span data-stu-id="f13e8-106">A block of text used by an extended dialog box template to describe the extended dialog box.</span></span> <span data-ttu-id="f13e8-107">Pour obtenir une description du format d’un modèle de boîte de dialogue étendue, consultez [**DLGTEMPLATEEX**](dlgtemplateex.md).</span><span class="sxs-lookup"><span data-stu-id="f13e8-107">For a description of the format of an extended dialog box template, see [**DLGTEMPLATEEX**](dlgtemplateex.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f13e8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f13e8-108">Syntax</span></span>


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="f13e8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="f13e8-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="f13e8-110">**helpID**</span><span class="sxs-lookup"><span data-stu-id="f13e8-110">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-111">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f13e8-111">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-112">Identificateur du contexte d’aide pour le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f13e8-112">The help context identifier for the control.</span></span> <span data-ttu-id="f13e8-113">Lorsque le système envoie un [**message \_ d’aide WM**](../shell/wm-help.md) , il transmet la valeur **HelpID** dans le membre **dwContextId** de la structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .</span><span class="sxs-lookup"><span data-stu-id="f13e8-113">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes the **helpID** value in the **dwContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f13e8-114">**exStyle**</span><span class="sxs-lookup"><span data-stu-id="f13e8-114">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-115">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f13e8-115">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-116">Styles étendus pour une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f13e8-116">The extended styles for a window.</span></span> <span data-ttu-id="f13e8-117">Ce membre n’est pas utilisé pour créer des contrôles dans les boîtes de dialogue, mais les applications qui utilisent des modèles de boîte de dialogue peuvent l’utiliser pour créer d’autres types de fenêtres.</span><span class="sxs-lookup"><span data-stu-id="f13e8-117">This member is not used to create controls in dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="f13e8-118">Pour obtenir la liste des valeurs, consultez [**styles de fenêtre étendus**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="f13e8-118">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="f13e8-119">**style**</span><span class="sxs-lookup"><span data-stu-id="f13e8-119">**style**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-120">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f13e8-120">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-121">Style du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f13e8-121">The style of the control.</span></span> <span data-ttu-id="f13e8-122">Ce membre peut être une combinaison de [valeurs de style de fenêtre](/windows/desktop/winmsg/window-styles) (par exemple, **WS \_ Border**) et une ou plusieurs des [valeurs de style de contrôle](/windows/desktop/Controls/common-control-styles) (par exemple, **BS \_ PUSHBUTTON** et es restantes). **\_**</span><span class="sxs-lookup"><span data-stu-id="f13e8-122">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) (such as **WS\_BORDER**) and one or more of the [control style values](/windows/desktop/Controls/common-control-styles) (such as **BS\_PUSHBUTTON** and **ES\_LEFT**).</span></span>

</dd> <dt>

<span data-ttu-id="f13e8-123">**x**</span><span class="sxs-lookup"><span data-stu-id="f13e8-123">**x**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-124">Type : **short**</span><span class="sxs-lookup"><span data-stu-id="f13e8-124">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-125">Coordonnée x, en unités de boîte de dialogue, du coin supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f13e8-125">The x-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="f13e8-126">Cette coordonnée est toujours relative à l’angle supérieur gauche de la zone cliente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f13e8-126">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="f13e8-127">**y**</span><span class="sxs-lookup"><span data-stu-id="f13e8-127">**y**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-128">Type : **short**</span><span class="sxs-lookup"><span data-stu-id="f13e8-128">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-129">Coordonnée y, en unités de boîte de dialogue, de l’angle supérieur gauche du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f13e8-129">The y-coordinate, in dialog box units, of the upper-left corner of the control.</span></span> <span data-ttu-id="f13e8-130">Cette coordonnée est toujours relative à l’angle supérieur gauche de la zone cliente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f13e8-130">This coordinate is always relative to the upper-left corner of the dialog box's client area.</span></span>

</dd> <dt>

<span data-ttu-id="f13e8-131">**adéquat**</span><span class="sxs-lookup"><span data-stu-id="f13e8-131">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-132">Type : **short**</span><span class="sxs-lookup"><span data-stu-id="f13e8-132">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-133">Largeur, en unités de boîte de dialogue, du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f13e8-133">The width, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="f13e8-134">**CY**</span><span class="sxs-lookup"><span data-stu-id="f13e8-134">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-135">Type : **short**</span><span class="sxs-lookup"><span data-stu-id="f13e8-135">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-136">Hauteur, en unités de boîte de dialogue, du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f13e8-136">The height, in dialog box units, of the control.</span></span>

</dd> <dt>

<span data-ttu-id="f13e8-137">**id**</span><span class="sxs-lookup"><span data-stu-id="f13e8-137">**id**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-138">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="f13e8-138">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-139">Identificateur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f13e8-139">The control identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f13e8-140">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="f13e8-140">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-141">Type : **SZ \_ ou \_ ORD**</span><span class="sxs-lookup"><span data-stu-id="f13e8-141">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-142">Tableau de longueur variable d’éléments 16 bits qui spécifie la classe de fenêtre du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f13e8-142">A variable-length array of 16-bit elements that specifies the window class of the control.</span></span> <span data-ttu-id="f13e8-143">Si le premier élément de ce tableau a une valeur autre que 0xFFFF, le système traite le tableau comme une chaîne Unicode terminée par le caractère null qui spécifie le nom d’une classe de fenêtre inscrite.</span><span class="sxs-lookup"><span data-stu-id="f13e8-143">If the first element of this array is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

<span data-ttu-id="f13e8-144">Si le premier élément est 0xFFFF, le tableau a un élément supplémentaire qui spécifie la valeur ordinale d’une classe système prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="f13e8-144">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system class.</span></span> <span data-ttu-id="f13e8-145">L’ordinal peut être l’une des valeurs Atom suivantes.</span><span class="sxs-lookup"><span data-stu-id="f13e8-145">The ordinal can be one of the following atom values.</span></span>



| <span data-ttu-id="f13e8-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="f13e8-146">Value</span></span>                                                                             | <span data-ttu-id="f13e8-147">Signification</span><span class="sxs-lookup"><span data-stu-id="f13e8-147">Meaning</span></span>               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <span data-ttu-id="f13e8-148"><dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="f13e8-148"><dt>0x0080</dt></span></span> </dl> | <span data-ttu-id="f13e8-149">Bouton</span><span class="sxs-lookup"><span data-stu-id="f13e8-149">Button</span></span><br/>     |
| <dl> <span data-ttu-id="f13e8-150"><dt>0x0081</dt></span><span class="sxs-lookup"><span data-stu-id="f13e8-150"><dt>0x0081</dt></span></span> </dl> | <span data-ttu-id="f13e8-151">Modifier</span><span class="sxs-lookup"><span data-stu-id="f13e8-151">Edit</span></span><br/>       |
| <dl> <span data-ttu-id="f13e8-152"><dt>0x0082</dt></span><span class="sxs-lookup"><span data-stu-id="f13e8-152"><dt>0x0082</dt></span></span> </dl> | <span data-ttu-id="f13e8-153">statique</span><span class="sxs-lookup"><span data-stu-id="f13e8-153">Static</span></span><br/>     |
| <dl> <span data-ttu-id="f13e8-154"><dt>0x0083</dt></span><span class="sxs-lookup"><span data-stu-id="f13e8-154"><dt>0x0083</dt></span></span> </dl> | <span data-ttu-id="f13e8-155">Zone de liste</span><span class="sxs-lookup"><span data-stu-id="f13e8-155">List box</span></span><br/>   |
| <dl> <span data-ttu-id="f13e8-156"><dt>0x0084</dt></span><span class="sxs-lookup"><span data-stu-id="f13e8-156"><dt>0x0084</dt></span></span> </dl> | <span data-ttu-id="f13e8-157">Scroll bar</span><span class="sxs-lookup"><span data-stu-id="f13e8-157">Scroll bar</span></span><br/> |
| <dl> <span data-ttu-id="f13e8-158"><dt>0x0085</dt></span><span class="sxs-lookup"><span data-stu-id="f13e8-158"><dt>0x0085</dt></span></span> </dl> | <span data-ttu-id="f13e8-159">Combo box</span><span class="sxs-lookup"><span data-stu-id="f13e8-159">Combo box</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="f13e8-160">**title**</span><span class="sxs-lookup"><span data-stu-id="f13e8-160">**title**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-161">Type : **SZ \_ ou \_ ORD**</span><span class="sxs-lookup"><span data-stu-id="f13e8-161">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-162">Tableau de longueur variable d’éléments 16 bits qui contient le texte initial ou l’identificateur de ressource du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f13e8-162">A variable-length array of 16-bit elements that contains the initial text or resource identifier of the control.</span></span> <span data-ttu-id="f13e8-163">Si le premier élément de ce tableau est 0xFFFF, le tableau a un élément supplémentaire qui spécifie la valeur ordinale d’une ressource, telle qu’une icône, dans un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="f13e8-163">If the first element of this array is 0xFFFF, the array has one additional element that specifies the ordinal value of a resource, such as an icon, in an executable file.</span></span> <span data-ttu-id="f13e8-164">Vous pouvez utiliser un identificateur de ressource pour les contrôles, tels que les contrôles d’icône statique, qui chargent et affichent une icône ou une autre ressource plutôt que du texte.</span><span class="sxs-lookup"><span data-stu-id="f13e8-164">You can use a resource identifier for controls, such as static icon controls, that load and display an icon or other resource rather than text.</span></span> <span data-ttu-id="f13e8-165">Si le premier élément est une valeur autre que 0xFFFF, le système traite le tableau comme une chaîne Unicode terminée par le caractère null qui spécifie le texte initial.</span><span class="sxs-lookup"><span data-stu-id="f13e8-165">If the first element is any value other than 0xFFFF, the system treats the array as a null-terminated Unicode string that specifies the initial text.</span></span>

</dd> <dt>

<span data-ttu-id="f13e8-166">**extraCount**</span><span class="sxs-lookup"><span data-stu-id="f13e8-166">**extraCount**</span></span>
</dt> <dd>

<span data-ttu-id="f13e8-167">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="f13e8-167">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="f13e8-168">Nombre d’octets de données de création qui suivent ce membre.</span><span class="sxs-lookup"><span data-stu-id="f13e8-168">The number of bytes of creation data that follow this member.</span></span> <span data-ttu-id="f13e8-169">Si cette valeur est supérieure à zéro, les données de création commencent à la limite de **mot** suivante.</span><span class="sxs-lookup"><span data-stu-id="f13e8-169">If this value is greater than zero, the creation data begins at the next **WORD** boundary.</span></span> <span data-ttu-id="f13e8-170">Ces données de création peuvent avoir n’importe quelle taille et n’importe quel format.</span><span class="sxs-lookup"><span data-stu-id="f13e8-170">This creation data can be of any size and format.</span></span> <span data-ttu-id="f13e8-171">La procédure de fenêtre du contrôle doit être en mesure d’interpréter les données.</span><span class="sxs-lookup"><span data-stu-id="f13e8-171">The control's window procedure must be able to interpret the data.</span></span> <span data-ttu-id="f13e8-172">Lorsque le système crée le contrôle, il passe un pointeur vers ces données dans le paramètre *lParam* du message [**WM \_ Create**](/windows/desktop/winmsg/wm-create) qu’il envoie au contrôle.</span><span class="sxs-lookup"><span data-stu-id="f13e8-172">When the system creates the control, it passes a pointer to this data in the *lParam* parameter of the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message that it sends to the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f13e8-173">Notes</span><span class="sxs-lookup"><span data-stu-id="f13e8-173">Remarks</span></span>

<span data-ttu-id="f13e8-174">Un modèle étendu pour une boîte de dialogue se compose d’un en-tête [**DLGTEMPLATEEX**](dlgtemplateex.md) suivi d’une structure **DLGITEMTEMPLATEEX** pour chaque contrôle dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f13e8-174">An extended template for a dialog box consists of a [**DLGTEMPLATEEX**](dlgtemplateex.md) header followed by a **DLGITEMTEMPLATEEX** structure for each control in the dialog box.</span></span>

<span data-ttu-id="f13e8-175">Chaque structure **DLGITEMTEMPLATEEX** doit être alignée sur une limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f13e8-175">Each **DLGITEMTEMPLATEEX** structure must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="f13e8-176">Les tableaux de **WindowClass** de longueur variable et de **titre** doivent être alignés sur les limites de **mots** .</span><span class="sxs-lookup"><span data-stu-id="f13e8-176">The variable-length **windowClass** and **title** arrays must be aligned on **WORD** boundaries.</span></span> <span data-ttu-id="f13e8-177">Le tableau de données de création, le cas échéant, doit être aligné sur une limite de **mot** .</span><span class="sxs-lookup"><span data-stu-id="f13e8-177">The creation data array, if any, must be aligned on a **WORD** boundary.</span></span>

<span data-ttu-id="f13e8-178">Si vous spécifiez des chaînes de caractères dans les tableaux **WindowClass** et **title** , vous devez utiliser des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="f13e8-178">If you specify character strings in the **windowClass** and **title** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="f13e8-179">Utilisez la fonction [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) pour générer des chaînes Unicode à partir de chaînes ANSI.</span><span class="sxs-lookup"><span data-stu-id="f13e8-179">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="f13e8-180">Les membres **x**, **y**, **CX** et **CY** spécifient des valeurs dans les unités de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f13e8-180">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="f13e8-181">Vous pouvez convertir ces valeurs en unités d’écran (pixels) à l’aide de la fonction [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="f13e8-181">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="f13e8-182">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f13e8-182">Requirements</span></span>



| <span data-ttu-id="f13e8-183">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f13e8-183">Requirement</span></span> | <span data-ttu-id="f13e8-184">Valeur</span><span class="sxs-lookup"><span data-stu-id="f13e8-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f13e8-185">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f13e8-185">Minimum supported client</span></span><br/> | <span data-ttu-id="f13e8-186">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f13e8-186">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f13e8-187">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f13e8-187">Minimum supported server</span></span><br/> | <span data-ttu-id="f13e8-188">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f13e8-188">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="f13e8-189">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f13e8-189">See also</span></span>

<dl> <dt>

<span data-ttu-id="f13e8-190">**Référence**</span><span class="sxs-lookup"><span data-stu-id="f13e8-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f13e8-191">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="f13e8-191">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="f13e8-192">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="f13e8-192">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="f13e8-193">**CreateWindowEx**</span><span class="sxs-lookup"><span data-stu-id="f13e8-193">**CreateWindowEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[<span data-ttu-id="f13e8-194">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="f13e8-194">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="f13e8-195">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="f13e8-195">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="f13e8-196">**DLGTEMPLATEEX**</span><span class="sxs-lookup"><span data-stu-id="f13e8-196">**DLGTEMPLATEEX**</span></span>](dlgtemplateex.md)
</dt> <dt>

[<span data-ttu-id="f13e8-197">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="f13e8-197">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="f13e8-198">**création de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f13e8-198">**WM\_CREATE**</span></span>](/windows/desktop/winmsg/wm-create)
</dt> <dt>

<span data-ttu-id="f13e8-199">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f13e8-199">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f13e8-200">Boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="f13e8-200">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="f13e8-201">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="f13e8-201">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f13e8-202">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="f13e8-202">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[<span data-ttu-id="f13e8-203">**\_aide WM**</span><span class="sxs-lookup"><span data-stu-id="f13e8-203">**WM\_HELP**</span></span>](../shell/wm-help.md)
</dt> </dl>

 

