---
description: Contient des informations sur la boîte de dialogue affichée par la fonction CryptUIDlgSelectCertificate.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: Structure CRYPTUI_SELECTCERTIFICATE_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520766"
---
# <a name="cryptui_selectcertificate_struct-structure"></a><span data-ttu-id="1bc62-103">\_SELECTCERTIFICATE \_ structure de struct CRYPTUI</span><span class="sxs-lookup"><span data-stu-id="1bc62-103">CRYPTUI\_SELECTCERTIFICATE\_STRUCT structure</span></span>

<span data-ttu-id="1bc62-104">La structure du **\_ \_ struct CRYPTUI SELECTCERTIFICATE** contient des informations sur la boîte de dialogue affichée par la fonction [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="1bc62-104">The **CRYPTUI\_SELECTCERTIFICATE\_STRUCT** structure contains information about the dialog box displayed by the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bc62-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bc62-105">Syntax</span></span>


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a><span data-ttu-id="1bc62-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1bc62-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1bc62-107">**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="1bc62-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-108">Taille, en octets, de cette structure.</span><span class="sxs-lookup"><span data-stu-id="1bc62-108">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-109">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="1bc62-109">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-110">Handle de la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1bc62-110">The handle of the parent window of the dialog box.</span></span> <span data-ttu-id="1bc62-111">Si cette valeur est **null**, la fenêtre parente est la fenêtre du bureau par défaut.</span><span class="sxs-lookup"><span data-stu-id="1bc62-111">If this value is **NULL**, the parent window is the default desktop window.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="1bc62-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-113">Spécifie des options supplémentaires pour la fonction [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="1bc62-113">Specifies additional options for the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span> <span data-ttu-id="1bc62-114">Il peut s’agir de **zéro ou d’une opération or** au niveau du bit des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1bc62-114">This can be zero or a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="1bc62-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bc62-115">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="1bc62-116">Signification</span><span class="sxs-lookup"><span data-stu-id="1bc62-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <span data-ttu-id="1bc62-117"><dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt></span><span class="sxs-lookup"><span data-stu-id="1bc62-117"><dt>**CRYPTUI\_SELECTCERT\_ADDFROMDS**</dt></span></span> </dl>                              | <span data-ttu-id="1bc62-118">Réservé.</span><span class="sxs-lookup"><span data-stu-id="1bc62-118">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <span data-ttu-id="1bc62-119"><dt>**CRYPTUI \_ SELECTCERT \_ hérité**</dt></span><span class="sxs-lookup"><span data-stu-id="1bc62-119"><dt>**CRYPTUI\_SELECTCERT\_LEGACY**</dt></span></span> </dl>                                       | <span data-ttu-id="1bc62-120">Spécifie que la boîte de dialogue héritée doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="1bc62-120">Specifies that the legacy dialog is to be displayed.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <span data-ttu-id="1bc62-121"><dt>**\_présélection SELECTCERT CRYPTUI \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1bc62-121"><dt>**CRYPTUI\_SELECTCERT\_MULTISELECT**</dt></span></span> </dl>                        | <span data-ttu-id="1bc62-122">Permet à l’utilisateur de sélectionner plusieurs certificats dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1bc62-122">Allows the user to select more than one certificate in the dialog box.</span></span> <span data-ttu-id="1bc62-123">Si cet indicateur est défini, la fonction [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) retourne toujours la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="1bc62-123">If this flag is set, the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function always returns **NULL**.</span></span> <span data-ttu-id="1bc62-124">Le membre **hSelectedCertStore** de cette structure doit contenir un handle vers un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="1bc62-124">The **hSelectedCertStore** member of this structure must contain a handle to a certificate store.</span></span> <span data-ttu-id="1bc62-125">Les certificats sélectionnés par l’utilisateur sont ajoutés à ce magasin.</span><span class="sxs-lookup"><span data-stu-id="1bc62-125">The certificates selected by the user will be added to this store.</span></span><br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <span data-ttu-id="1bc62-126"><dt>**CRYPTUI \_ SELECTCERT \_ put \_ WindowsT \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1bc62-126"><dt>**CRYPTUI\_SELECTCERT\_PUT\_WINDOW\_TOPMOST**</dt></span></span> </dl> | <span data-ttu-id="1bc62-127">Force l’interface utilisateur de chiffrement à être la fenêtre supérieure à l’écran.</span><span class="sxs-lookup"><span data-stu-id="1bc62-127">Forces the cryptography UI to be the top window on the screen.</span></span><br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="1bc62-128">**szTitle**</span><span class="sxs-lookup"><span data-stu-id="1bc62-128">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-129">Titre d’affichage de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1bc62-129">The display title for the dialog box.</span></span> <span data-ttu-id="1bc62-130">Si la valeur de ce membre est **null**, le titre par défaut « sélectionner un certificat » est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1bc62-130">If the value of this member is **NULL**, the default title of "Select Certificate" is used.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-131">**dwDontUseColumn**</span><span class="sxs-lookup"><span data-stu-id="1bc62-131">**dwDontUseColumn**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-132">Indicateurs qui peuvent être combinés pour exclure des colonnes de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="1bc62-132">Flags that can be combined to exclude columns of the display.</span></span>



| <span data-ttu-id="1bc62-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bc62-133">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="1bc62-134">Signification</span><span class="sxs-lookup"><span data-stu-id="1bc62-134">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <span data-ttu-id="1bc62-135"><dt>**CRYPTUI \_ Sélectionnez \_ IssuedTo, \_ colonne**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc62-135"><dt>**CRYPTUI\_SELECT\_ISSUEDTO\_COLUMN**</dt> <dt>1 (0x1)</dt></span></span> </dl>             | <span data-ttu-id="1bc62-136">N’affiche pas d’informations **IssuedTo,** .</span><span class="sxs-lookup"><span data-stu-id="1bc62-136">Do not display **ISSUEDTO** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <span data-ttu-id="1bc62-137"><dt>**CRYPTUI \_ Sélectionnez \_ la \_ colonne IssuedBy,**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc62-137"><dt>**CRYPTUI\_SELECT\_ISSUEDBY\_COLUMN**</dt> <dt>2 (0x2)</dt></span></span> </dl>             | <span data-ttu-id="1bc62-138">N’affiche pas d’informations **IssuedBy,** .</span><span class="sxs-lookup"><span data-stu-id="1bc62-138">Do not display **ISSUEDBY** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <span data-ttu-id="1bc62-139"><dt>**CRYPTUI \_ SÉLECTIONNER \_ la \_ colonne INTENDEDUSE**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc62-139"><dt>**CRYPTUI\_SELECT\_INTENDEDUSE\_COLUMN**</dt> <dt>4 (0x4)</dt></span></span> </dl>    | <span data-ttu-id="1bc62-140">N’affiche pas d’informations **IntendedUse** .</span><span class="sxs-lookup"><span data-stu-id="1bc62-140">Do not display **IntendedUse** information.</span></span><br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <span data-ttu-id="1bc62-141"><dt>**CRYPTUI \_ Sélectionnez \_ la \_ colonne FRIENDLYNAME**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc62-141"><dt>**CRYPTUI\_SELECT\_FRIENDLYNAME\_COLUMN**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="1bc62-142">N’affiche pas d’informations sur le nom.</span><span class="sxs-lookup"><span data-stu-id="1bc62-142">Do not display name information.</span></span><br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <span data-ttu-id="1bc62-143"><dt>**CRYPTUI \_ SÉLECTIONNER l' \_ emplacement \_ colonne**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc62-143"><dt>**CRYPTUI\_SELECT\_LOCATION\_COLUMN**</dt> <dt>16 (0x10)</dt></span></span> </dl>           | <span data-ttu-id="1bc62-144">N’affiche pas les informations relatives à l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="1bc62-144">Do not display location information.</span></span><br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <span data-ttu-id="1bc62-145"><dt>**CRYPTUI \_ Sélectionnez \_ la \_ colonne d’expiration**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="1bc62-145"><dt>**CRYPTUI\_SELECT\_EXPIRATION\_COLUMN**</dt> <dt>32 (0x20)</dt></span></span> </dl>     | <span data-ttu-id="1bc62-146">N’affiche pas les informations d’expiration.</span><span class="sxs-lookup"><span data-stu-id="1bc62-146">Do not display expiration information.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="1bc62-147">**szDisplayString**</span><span class="sxs-lookup"><span data-stu-id="1bc62-147">**szDisplayString**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-148">Texte affiché dans la boîte de dialogue pour indiquer à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1bc62-148">Text that is displayed in the dialog box to instruct the user.</span></span> <span data-ttu-id="1bc62-149">Si la valeur de ce membre est **null**, la chaîne par défaut « sélectionner un certificat que vous souhaitez utiliser » est utilisée.</span><span class="sxs-lookup"><span data-stu-id="1bc62-149">If the value of this member is **NULL**, the default string "Select a certificate you want to use" is used.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-150">**pFilterCallback**</span><span class="sxs-lookup"><span data-stu-id="1bc62-150">**pFilterCallback**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-151">Pointeur vers une fonction de rappel [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) qui filtre les certificats affichés dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1bc62-151">A pointer to a [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) callback function that filters the certificates that are displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-152">**pDisplayCallback**</span><span class="sxs-lookup"><span data-stu-id="1bc62-152">**pDisplayCallback**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-153">Pointeur vers une fonction de rappel [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) qui affiche les certificats que l’utilisateur sélectionne pour afficher.</span><span class="sxs-lookup"><span data-stu-id="1bc62-153">A pointer to a [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) callback function that displays certificates that the user selects to view.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-154">**pvCallbackData**</span><span class="sxs-lookup"><span data-stu-id="1bc62-154">**pvCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-155">Données supplémentaires passées aux fonctions de rappel spécifiées par les membres **pFilterCallback** et **pDisplayCallback** .</span><span class="sxs-lookup"><span data-stu-id="1bc62-155">Additional data that is passed to the callback functions specified by the **pFilterCallback** and **pDisplayCallback** members.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-156">**cDisplayStores**</span><span class="sxs-lookup"><span data-stu-id="1bc62-156">**cDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-157">Nombre de magasins de certificats dans le tableau **rghDisplayStores** .</span><span class="sxs-lookup"><span data-stu-id="1bc62-157">The number of certificate stores in the **rghDisplayStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-158">**rghDisplayStores**</span><span class="sxs-lookup"><span data-stu-id="1bc62-158">**rghDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-159">Pointeur vers un tableau de magasins qui contiennent des certificats disponibles pour la sélection dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1bc62-159">A pointer to an array of stores that contain certificates available for selection in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-160">**cStores**</span><span class="sxs-lookup"><span data-stu-id="1bc62-160">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-161">Nombre de magasins de certificats dans le tableau **rghStores** .</span><span class="sxs-lookup"><span data-stu-id="1bc62-161">The number of certificate stores in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-162">**rghStores**</span><span class="sxs-lookup"><span data-stu-id="1bc62-162">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-163">Pointeur vers un tableau de magasins de certificats à rechercher lors de la création d’une chaîne de certificats et de la vérification de l’approbation pour les certificats affichés dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1bc62-163">A pointer to an array of certificate stores to search when building a certificate chain and verifying trust for the certificates displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-164">**cPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="1bc62-164">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-165">Nombre de pages de propriétés dans le tableau **rgPropSheetPages** .</span><span class="sxs-lookup"><span data-stu-id="1bc62-165">The number of property pages in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-166">**rgPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="1bc62-166">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-167">Pointeur vers un tableau de structures **PROPSHEETPAGE** qui représentent les pages de propriétés qui sont passées à la boîte de dialogue d’affichage du certificat lorsqu’un certificat est sélectionné pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="1bc62-167">A pointer to an array of **PROPSHEETPAGE** structures that represent property pages that are passed to the certificate viewing dialog box when a certificate is selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="1bc62-168">**hSelectedCertStore**</span><span class="sxs-lookup"><span data-stu-id="1bc62-168">**hSelectedCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="1bc62-169">Handle d’un magasin de certificats créé par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="1bc62-169">A handle to a certificate store created by the caller.</span></span> <span data-ttu-id="1bc62-170">Les certificats sélectionnés par l’utilisateur sont ajoutés à ce magasin.</span><span class="sxs-lookup"><span data-stu-id="1bc62-170">The certificates selected by the user are added to this store.</span></span> <span data-ttu-id="1bc62-171">Si le nombre de certificats dans ce magasin est identique avant et après l’appel de [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), l’utilisateur a fermé la boîte de dialogue sans sélectionner de certificats.</span><span class="sxs-lookup"><span data-stu-id="1bc62-171">If the number of certificates in this store is the same before and after calling [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), the user closed the dialog box without selecting any certificates.</span></span>

<span data-ttu-id="1bc62-172">Ce membre n’est pas utilisé si le membre **dwFlags** de cette structure ne contient pas l’indicateur **\_ \_ MultiSelect CRYPTUI SELECTCERT** .</span><span class="sxs-lookup"><span data-stu-id="1bc62-172">This member is not used if the **dwFlags** member of this structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1bc62-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bc62-173">Requirements</span></span>



| <span data-ttu-id="1bc62-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bc62-174">Requirement</span></span> | <span data-ttu-id="1bc62-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bc62-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bc62-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bc62-176">Minimum supported client</span></span><br/> | <span data-ttu-id="1bc62-177">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bc62-177">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="1bc62-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1bc62-178">Minimum supported server</span></span><br/> | <span data-ttu-id="1bc62-179">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1bc62-179">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1bc62-180">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="1bc62-180">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="1bc62-181">**CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTW** (Unicode) et **CRYPTUI \_ SELECTCERTIFICATE \_ structa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="1bc62-181">**CRYPTUI\_SELECTCERTIFICATE\_STRUCTW** (Unicode) and **CRYPTUI\_SELECTCERTIFICATE\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1bc62-182">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bc62-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bc62-183">**CryptUIDlgSelectCertificate**</span><span class="sxs-lookup"><span data-stu-id="1bc62-183">**CryptUIDlgSelectCertificate**</span></span>](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




