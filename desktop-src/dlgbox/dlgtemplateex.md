---
title: DLGTEMPLATEEX, structure
description: Un modèle de boîte de dialogue étendu commence par un en-tête DLGTEMPLATEEX qui décrit la boîte de dialogue et spécifie le nombre de contrôles dans la boîte de dialogue.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Boîtes de dialogue de la structure DLGTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508958"
---
# <a name="dlgtemplateex-structure"></a><span data-ttu-id="90b35-104">DLGTEMPLATEEX, structure</span><span class="sxs-lookup"><span data-stu-id="90b35-104">DLGTEMPLATEEX structure</span></span>

<span data-ttu-id="90b35-105">Un modèle de boîte de dialogue étendu commence par un en-tête **DLGTEMPLATEEX** qui décrit la boîte de dialogue et spécifie le nombre de contrôles dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-105">An extended dialog box template begins with a **DLGTEMPLATEEX** header that describes the dialog box and specifies the number of controls in the dialog box.</span></span> <span data-ttu-id="90b35-106">Pour chaque contrôle d’une boîte de dialogue, un modèle de boîte de dialogue étendue contient un bloc de données qui utilise le format [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) pour décrire le contrôle.</span><span class="sxs-lookup"><span data-stu-id="90b35-106">For each control in a dialog box, an extended dialog box template has a block of data that uses the [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) format to describe the control.</span></span>

<span data-ttu-id="90b35-107">La structure **DLGTEMPLATEEX** n’est définie dans aucun fichier d’en-tête standard.</span><span class="sxs-lookup"><span data-stu-id="90b35-107">The **DLGTEMPLATEEX** structure is not defined in any standard header file.</span></span> <span data-ttu-id="90b35-108">La définition de structure est fournie ici pour expliquer le format d’un modèle étendu pour une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-108">The structure definition is provided here to explain the format of an extended template for a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="90b35-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90b35-109">Syntax</span></span>


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a><span data-ttu-id="90b35-110">Membres</span><span class="sxs-lookup"><span data-stu-id="90b35-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="90b35-111">**dlgVer**</span><span class="sxs-lookup"><span data-stu-id="90b35-111">**dlgVer**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-112">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="90b35-112">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-113">Numéro de version du modèle de boîte de dialogue étendue.</span><span class="sxs-lookup"><span data-stu-id="90b35-113">The version number of the extended dialog box template.</span></span> <span data-ttu-id="90b35-114">Ce membre doit avoir la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="90b35-114">This member must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-115">**signature**</span><span class="sxs-lookup"><span data-stu-id="90b35-115">**signature**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-116">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="90b35-116">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-117">Indique si un modèle est un modèle de boîte de dialogue étendue.</span><span class="sxs-lookup"><span data-stu-id="90b35-117">Indicates whether a template is an extended dialog box template.</span></span> <span data-ttu-id="90b35-118">Si la **signature** est 0xFFFF, il s’agit d’un modèle de boîte de dialogue étendue.</span><span class="sxs-lookup"><span data-stu-id="90b35-118">If **signature** is 0xFFFF, this is an extended dialog box template.</span></span> <span data-ttu-id="90b35-119">Dans ce cas, le membre **dlgVer** spécifie le numéro de version du modèle.</span><span class="sxs-lookup"><span data-stu-id="90b35-119">In this case, the **dlgVer** member specifies the template version number.</span></span> <span data-ttu-id="90b35-120">Si la **signature** correspond à une valeur autre que 0xFFFF, il s’agit d’un modèle de boîte de dialogue standard qui utilise les structures [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) et [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) .</span><span class="sxs-lookup"><span data-stu-id="90b35-120">If **signature** is any value other than 0xFFFF, this is a standard dialog box template that uses the [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) and [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) structures.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-121">**helpID**</span><span class="sxs-lookup"><span data-stu-id="90b35-121">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-122">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="90b35-122">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-123">Identificateur de contexte d’aide pour la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-123">The help context identifier for the dialog box window.</span></span> <span data-ttu-id="90b35-124">Lorsque le système envoie un [**message \_ d’aide WM**](../shell/wm-help.md) , il transmet cette valeur dans le membre **WContextId** de la structure [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .</span><span class="sxs-lookup"><span data-stu-id="90b35-124">When the system sends a [**WM\_HELP**](../shell/wm-help.md) message, it passes this value in the **wContextId** member of the [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) structure.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-125">**exStyle**</span><span class="sxs-lookup"><span data-stu-id="90b35-125">**exStyle**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-126">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="90b35-126">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-127">Styles Windows étendus.</span><span class="sxs-lookup"><span data-stu-id="90b35-127">The extended windows styles.</span></span> <span data-ttu-id="90b35-128">Ce membre n’est pas utilisé lors de la création de boîtes de dialogue, mais les applications qui utilisent des modèles de boîte de dialogue peuvent l’utiliser pour créer d’autres types de fenêtres.</span><span class="sxs-lookup"><span data-stu-id="90b35-128">This member is not used when creating dialog boxes, but applications that use dialog box templates can use it to create other types of windows.</span></span> <span data-ttu-id="90b35-129">Pour obtenir la liste des valeurs, consultez [**styles de fenêtre étendus**](/windows/desktop/winmsg/extended-window-styles).</span><span class="sxs-lookup"><span data-stu-id="90b35-129">For a list of values, see [**Extended Window Styles**](/windows/desktop/winmsg/extended-window-styles).</span></span>

</dd> <dt>

<span data-ttu-id="90b35-130">**style**</span><span class="sxs-lookup"><span data-stu-id="90b35-130">**style**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-131">Type : **DWORD**</span><span class="sxs-lookup"><span data-stu-id="90b35-131">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-132">Style de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-132">The style of the dialog box.</span></span> <span data-ttu-id="90b35-133">Ce membre peut être une combinaison de [valeurs de style de fenêtre](/windows/desktop/winmsg/window-styles) et de [valeurs de style de boîte de dialogue](dialog-box-styles.md).</span><span class="sxs-lookup"><span data-stu-id="90b35-133">This member can be a combination of [window style values](/windows/desktop/winmsg/window-styles) and [dialog box style values](dialog-box-styles.md).</span></span>

<span data-ttu-id="90b35-134">Si **style** inclut le style de boîte de dialogue **DS \_ SetFont** ou **DS \_ SHELLFONT** , l’en-tête **DLGTEMPLATEEX** du modèle de boîte de dialogue étendue contient quatre membres **supplémentaires (taille**, **épaisseur**, **italique** et **police**) qui décrivent la police à utiliser pour le texte dans la zone cliente et les contrôles de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-134">If **style** includes the **DS\_SETFONT** or **DS\_SHELLFONT** dialog box style, the **DLGTEMPLATEEX** header of the extended dialog box template contains four additional members ( **pointsize**, **weight**, **italic**, and **typeface**) that describe the font to use for the text in the client area and controls of the dialog box.</span></span> <span data-ttu-id="90b35-135">Si possible, le système crée une police en fonction des valeurs spécifiées dans ces membres.</span><span class="sxs-lookup"><span data-stu-id="90b35-135">If possible, the system creates a font according to the values specified in these members.</span></span> <span data-ttu-id="90b35-136">Le système envoie ensuite un message [**WM \_ SetFont**](/windows/desktop/winmsg/wm-setfont) à la boîte de dialogue et à chaque contrôle pour fournir un handle à la police.</span><span class="sxs-lookup"><span data-stu-id="90b35-136">Then the system sends a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to the dialog box and to each control to provide a handle to the font.</span></span>

<span data-ttu-id="90b35-137">Pour plus d’informations, consultez polices de boîte de [dialogue](about-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="90b35-137">For more information, see [Dialog Box Fonts](about-dialog-boxes.md).</span></span>

</dd> <dt>

<span data-ttu-id="90b35-138">**cDlgItems**</span><span class="sxs-lookup"><span data-stu-id="90b35-138">**cDlgItems**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-139">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="90b35-139">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-140">Nombre de contrôles dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-140">The number of controls in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-141">**x**</span><span class="sxs-lookup"><span data-stu-id="90b35-141">**x**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-142">Type : **short**</span><span class="sxs-lookup"><span data-stu-id="90b35-142">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-143">Coordonnée x, en unités de boîte de dialogue, de l’angle supérieur gauche de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-143">The x-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-144">**y**</span><span class="sxs-lookup"><span data-stu-id="90b35-144">**y**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-145">Type : **short**</span><span class="sxs-lookup"><span data-stu-id="90b35-145">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-146">Coordonnée y, en unités de boîte de dialogue, de l’angle supérieur gauche de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-146">The y-coordinate, in dialog box units, of the upper-left corner of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-147">**adéquat**</span><span class="sxs-lookup"><span data-stu-id="90b35-147">**cx**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-148">Type : **short**</span><span class="sxs-lookup"><span data-stu-id="90b35-148">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-149">Largeur, en unités de boîte de dialogue, de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-149">The width, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-150">**CY**</span><span class="sxs-lookup"><span data-stu-id="90b35-150">**cy**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-151">Type : **short**</span><span class="sxs-lookup"><span data-stu-id="90b35-151">Type: **short**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-152">Hauteur, en unités de boîte de dialogue, de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-152">The height, in dialog box units, of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-153">**menus**</span><span class="sxs-lookup"><span data-stu-id="90b35-153">**menu**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-154">Type : **SZ \_ ou \_ ORD**</span><span class="sxs-lookup"><span data-stu-id="90b35-154">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-155">Tableau de longueur variable d’éléments 16 bits qui identifie une ressource de menu pour la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-155">A variable-length array of 16-bit elements that identifies a menu resource for the dialog box.</span></span> <span data-ttu-id="90b35-156">Si le premier élément de ce tableau est 0x0000, la boîte de dialogue n’a pas de menu et le tableau n’a pas d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="90b35-156">If the first element of this array is 0x0000, the dialog box has no menu and the array has no other elements.</span></span> <span data-ttu-id="90b35-157">Si le premier élément est 0xFFFF, le tableau a un élément supplémentaire qui spécifie la valeur ordinale d’une ressource de menu dans un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="90b35-157">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a menu resource in an executable file.</span></span> <span data-ttu-id="90b35-158">Si le premier élément a une autre valeur, le système traite le tableau comme une chaîne Unicode terminée par le caractère null qui spécifie le nom d’une ressource de menu dans un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="90b35-158">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a menu resource in an executable file.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-159">**windowClass**</span><span class="sxs-lookup"><span data-stu-id="90b35-159">**windowClass**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-160">Type : **SZ \_ ou \_ ORD**</span><span class="sxs-lookup"><span data-stu-id="90b35-160">Type: **sz\_Or\_Ord**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-161">Tableau de longueur variable d’éléments 16 bits qui identifie la classe de fenêtre de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-161">A variable-length array of 16-bit elements that identifies the window class of the dialog box.</span></span> <span data-ttu-id="90b35-162">Si le premier élément du tableau est 0x0000, le système utilise la classe de boîte de dialogue prédéfinie pour la boîte de dialogue et le tableau n’a pas d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="90b35-162">If the first element of the array is 0x0000, the system uses the predefined dialog box class for the dialog box and the array has no other elements.</span></span> <span data-ttu-id="90b35-163">Si le premier élément est 0xFFFF, le tableau a un élément supplémentaire qui spécifie la valeur ordinale d’une classe de fenêtre système prédéfinie.</span><span class="sxs-lookup"><span data-stu-id="90b35-163">If the first element is 0xFFFF, the array has one additional element that specifies the ordinal value of a predefined system window class.</span></span> <span data-ttu-id="90b35-164">Si le premier élément a une autre valeur, le système traite le tableau comme une chaîne Unicode terminée par le caractère null qui spécifie le nom d’une classe de fenêtre inscrite.</span><span class="sxs-lookup"><span data-stu-id="90b35-164">If the first element has any other value, the system treats the array as a null-terminated Unicode string that specifies the name of a registered window class.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-165">**title**</span><span class="sxs-lookup"><span data-stu-id="90b35-165">**title**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-166">Type : **WCHAR \[ titleLen \]**</span><span class="sxs-lookup"><span data-stu-id="90b35-166">Type: **WCHAR\[titleLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-167">Titre de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-167">The title of the dialog box.</span></span> <span data-ttu-id="90b35-168">Si le premier élément de ce tableau est 0x0000, la boîte de dialogue n’a pas de titre et le tableau n’a pas d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="90b35-168">If the first element of this array is 0x0000, the dialog box has no title and the array has no other elements.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-169">**pointsize**</span><span class="sxs-lookup"><span data-stu-id="90b35-169">**pointsize**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-170">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="90b35-170">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-171">Taille en points de la police à utiliser pour le texte dans la boîte de dialogue et ses contrôles.</span><span class="sxs-lookup"><span data-stu-id="90b35-171">The point size of the font to use for the text in the dialog box and its controls.</span></span>

<span data-ttu-id="90b35-172">Ce membre est présent uniquement si le membre de **style** spécifie **DS \_ SetFont** ou **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="90b35-172">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-173">**weight**</span><span class="sxs-lookup"><span data-stu-id="90b35-173">**weight**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-174">Type : **Word**</span><span class="sxs-lookup"><span data-stu-id="90b35-174">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-175">Poids de la police.</span><span class="sxs-lookup"><span data-stu-id="90b35-175">The weight of the font.</span></span> <span data-ttu-id="90b35-176">Notez que, bien qu’il peut s’agir de l’une des valeurs énumérées pour le membre **lfWeight** de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , toute valeur utilisée sera automatiquement remplacée par le **FW \_ normal**.</span><span class="sxs-lookup"><span data-stu-id="90b35-176">Note that, although this can be any of the values listed for the **lfWeight** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure, any value that is used will be automatically changed to **FW\_NORMAL**.</span></span>

<span data-ttu-id="90b35-177">Ce membre est présent uniquement si le membre de **style** spécifie **DS \_ SetFont** ou **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="90b35-177">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-178">**italique**</span><span class="sxs-lookup"><span data-stu-id="90b35-178">**italic**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-179">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="90b35-179">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-180">Indique si la police est en italique.</span><span class="sxs-lookup"><span data-stu-id="90b35-180">Indicates whether the font is italic.</span></span> <span data-ttu-id="90b35-181">Si cette valeur est **true**, la police est en italique.</span><span class="sxs-lookup"><span data-stu-id="90b35-181">If this value is **TRUE**, the font is italic.</span></span>

<span data-ttu-id="90b35-182">Ce membre est présent uniquement si le membre de **style** spécifie **DS \_ SetFont** ou **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="90b35-182">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-183">**caractères**</span><span class="sxs-lookup"><span data-stu-id="90b35-183">**charset**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-184">Type : **Byte**</span><span class="sxs-lookup"><span data-stu-id="90b35-184">Type: **BYTE**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-185">Jeu de caractères à utiliser.</span><span class="sxs-lookup"><span data-stu-id="90b35-185">The character set to be used.</span></span> <span data-ttu-id="90b35-186">Pour plus d’informations, consultez le membre **lfCharSet** de [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span><span class="sxs-lookup"><span data-stu-id="90b35-186">For more information, see the **lfcharset** member of [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).</span></span>

<span data-ttu-id="90b35-187">Ce membre est présent uniquement si le membre de **style** spécifie **DS \_ SetFont** ou **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="90b35-187">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> <dt>

<span data-ttu-id="90b35-188">**certain**</span><span class="sxs-lookup"><span data-stu-id="90b35-188">**typeface**</span></span>
</dt> <dd>

<span data-ttu-id="90b35-189">Type : **WCHAR \[ stringLen \]**</span><span class="sxs-lookup"><span data-stu-id="90b35-189">Type: **WCHAR\[stringLen\]**</span></span>

</dd> <dd>

<span data-ttu-id="90b35-190">Nom de la police de la police.</span><span class="sxs-lookup"><span data-stu-id="90b35-190">The name of the typeface for the font.</span></span>

<span data-ttu-id="90b35-191">Ce membre est présent uniquement si le membre de **style** spécifie **DS \_ SetFont** ou **DS \_ SHELLFONT**.</span><span class="sxs-lookup"><span data-stu-id="90b35-191">This member is present only if the **style** member specifies **DS\_SETFONT** or **DS\_SHELLFONT**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="90b35-192">Notes</span><span class="sxs-lookup"><span data-stu-id="90b35-192">Remarks</span></span>

<span data-ttu-id="90b35-193">Vous pouvez utiliser un modèle de boîte de dialogue étendu à la place d’un modèle de boîte de dialogue standard dans les fonctions [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)et [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .</span><span class="sxs-lookup"><span data-stu-id="90b35-193">You can use an extended dialog box template instead of a standard dialog box template in the [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta), and [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) functions.</span></span>

<span data-ttu-id="90b35-194">Le fait de suivre l’en-tête **DLGTEMPLATEEX** dans un modèle de boîte de dialogue étendue est une ou plusieurs structures [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) qui décrivent les contrôles de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-194">Following the **DLGTEMPLATEEX** header in an extended dialog box template is one or more [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structures that describe the controls of the dialog box.</span></span> <span data-ttu-id="90b35-195">Le membre **cDlgItems** de la structure **DLGITEMTEMPLATEEX** spécifie le nombre de structures **DLGITEMTEMPLATEEX** qui suivent dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="90b35-195">The **cDlgItems** member of the **DLGITEMTEMPLATEEX** structure specifies the number of **DLGITEMTEMPLATEEX** structures that follow in the template.</span></span>

<span data-ttu-id="90b35-196">Chaque structure [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) du modèle doit être alignée sur une limite **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="90b35-196">Each [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) structure in the template must be aligned on a **DWORD** boundary.</span></span> <span data-ttu-id="90b35-197">Si le membre de **style** spécifie le style **DS \_ SetFont** ou **DS \_ SHELLFONT** , la première structure **DLGITEMTEMPLATEEX** commence sur la première limite **DWORD** après la chaîne de **police** .</span><span class="sxs-lookup"><span data-stu-id="90b35-197">If the **style** member specifies the **DS\_SETFONT** or **DS\_SHELLFONT** style, the first **DLGITEMTEMPLATEEX** structure begins on the first **DWORD** boundary after the **typeface** string.</span></span> <span data-ttu-id="90b35-198">Si ces styles ne sont pas spécifiés, la première structure commence sur la première limite **DWORD** après la chaîne de **titre** .</span><span class="sxs-lookup"><span data-stu-id="90b35-198">If these styles are not specified, the first structure begins on the first **DWORD** boundary after the **title** string.</span></span>

<span data-ttu-id="90b35-199">Les tableaux **menu**, **WindowClass**, **title** et **Typeface** doivent être alignés sur les limites de **mots** .</span><span class="sxs-lookup"><span data-stu-id="90b35-199">The **menu**, **windowClass**, **title**, and **typeface** arrays must be aligned on **WORD** boundaries.</span></span>

<span data-ttu-id="90b35-200">Si vous spécifiez des chaînes de caractères dans les tableaux **menu**, **WindowClass**, **title** et **Typeface** , vous devez utiliser des chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="90b35-200">If you specify character strings in the **menu**, **windowClass**, **title**, and **typeface** arrays, you must use Unicode strings.</span></span> <span data-ttu-id="90b35-201">Utilisez la fonction [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) pour générer ces chaînes Unicode à partir de chaînes ANSI.</span><span class="sxs-lookup"><span data-stu-id="90b35-201">Use the [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) function to generate these Unicode strings from ANSI strings.</span></span>

<span data-ttu-id="90b35-202">Les membres **x**, **y**, **CX** et **CY** spécifient des valeurs dans les unités de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="90b35-202">The **x**, **y**, **cx**, and **cy** members specify values in dialog box units.</span></span> <span data-ttu-id="90b35-203">Vous pouvez convertir ces valeurs en unités d’écran (pixels) à l’aide de la fonction [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .</span><span class="sxs-lookup"><span data-stu-id="90b35-203">You can convert these values to screen units (pixels) by using the [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="90b35-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90b35-204">Requirements</span></span>



| <span data-ttu-id="90b35-205">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90b35-205">Requirement</span></span> | <span data-ttu-id="90b35-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="90b35-206">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="90b35-207">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90b35-207">Minimum supported client</span></span><br/> | <span data-ttu-id="90b35-208">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90b35-208">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="90b35-209">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="90b35-209">Minimum supported server</span></span><br/> | <span data-ttu-id="90b35-210">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="90b35-210">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="90b35-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90b35-211">See also</span></span>

<dl> <dt>

<span data-ttu-id="90b35-212">**Référence**</span><span class="sxs-lookup"><span data-stu-id="90b35-212">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="90b35-213">**CreateDialogIndirect**</span><span class="sxs-lookup"><span data-stu-id="90b35-213">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[<span data-ttu-id="90b35-214">**CreateDialogIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="90b35-214">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[<span data-ttu-id="90b35-215">**DialogBoxIndirect**</span><span class="sxs-lookup"><span data-stu-id="90b35-215">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[<span data-ttu-id="90b35-216">**DialogBoxIndirectParam**</span><span class="sxs-lookup"><span data-stu-id="90b35-216">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[<span data-ttu-id="90b35-217">**DLGITEMTEMPLATEEX**</span><span class="sxs-lookup"><span data-stu-id="90b35-217">**DLGITEMTEMPLATEEX**</span></span>](dlgitemtemplateex.md)
</dt> <dt>

[<span data-ttu-id="90b35-218">**MapDialogRect**</span><span class="sxs-lookup"><span data-stu-id="90b35-218">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[<span data-ttu-id="90b35-219">**\_SetFont WM**</span><span class="sxs-lookup"><span data-stu-id="90b35-219">**WM\_SETFONT**</span></span>](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

<span data-ttu-id="90b35-220">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="90b35-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="90b35-221">Boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="90b35-221">Dialog Boxes</span></span>](dialog-boxes.md)
</dt> <dt>

<span data-ttu-id="90b35-222">**Autres ressources**</span><span class="sxs-lookup"><span data-stu-id="90b35-222">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="90b35-223">**LOGFONT**</span><span class="sxs-lookup"><span data-stu-id="90b35-223">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="90b35-224">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="90b35-224">**MultiByteToWideChar**</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

