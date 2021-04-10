---
description: Contient des informations pour la fonction CryptUIDlgViewSignerInfo.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: Structure CRYPTUI_VIEWSIGNERINFO_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034504"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a><span data-ttu-id="cc070-103">\_VIEWSIGNERINFO \_ structure de struct CRYPTUI</span><span class="sxs-lookup"><span data-stu-id="cc070-103">CRYPTUI\_VIEWSIGNERINFO\_STRUCT structure</span></span>

<span data-ttu-id="cc070-104">\[La structure du **\_ \_ struct CRYPTUI VIEWSIGNERINFO** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="cc070-104">\[The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cc070-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="cc070-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="cc070-106">La structure du **\_ \_ struct CRYPTUI VIEWSIGNERINFO** contient des informations pour la fonction [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="cc070-106">The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure contains information for the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="cc070-107">Cette structure n’est pas déclarée dans un fichier d’en-tête publié.</span><span class="sxs-lookup"><span data-stu-id="cc070-107">This structure is not declared in a published header file.</span></span> <span data-ttu-id="cc070-108">Pour utiliser cette structure, déclarez-la dans le format exact indiqué.</span><span class="sxs-lookup"><span data-stu-id="cc070-108">To use this structure, declare it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="cc070-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc070-109">Syntax</span></span>


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a><span data-ttu-id="cc070-110">Membres</span><span class="sxs-lookup"><span data-stu-id="cc070-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc070-111">**dwSize nul**</span><span class="sxs-lookup"><span data-stu-id="cc070-111">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-112">Taille, en octets, de cette structure.</span><span class="sxs-lookup"><span data-stu-id="cc070-112">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-113">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="cc070-113">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-114">Handle de la fenêtre qui doit être le parent de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="cc070-114">The handle of the window to be the parent of the dialog box.</span></span> <span data-ttu-id="cc070-115">Ce membre peut avoir la **valeur null** si la boîte de dialogue ne doit pas avoir de parent.</span><span class="sxs-lookup"><span data-stu-id="cc070-115">This member can be **NULL** if the dialog box should have no parent.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="cc070-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-117">Jeu d’indicateurs qui modifie le comportement de la fonction [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="cc070-117">A set of flags that modifies the behavior of the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span> <span data-ttu-id="cc070-118">Aucun indicateur n’est actuellement défini. ce membre doit donc être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="cc070-118">There are no flags currently defined, so this member must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-119">**szTitle**</span><span class="sxs-lookup"><span data-stu-id="cc070-119">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-120">Pointeur vers une chaîne se terminant par un caractère null qui contient le titre à afficher dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="cc070-120">A pointer to a null-terminated string that contains the title to be displayed in the dialog box.</span></span> <span data-ttu-id="cc070-121">Si ce membre a la **valeur null**, un titre par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cc070-121">If this member is **NULL**, a default title is used.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-122">**pSignerInfo**</span><span class="sxs-lookup"><span data-stu-id="cc070-122">**pSignerInfo**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-123">Pointeur vers une structure [**d' \_ \_ informations du signataire CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) qui contient les informations sur le signataire à afficher.</span><span class="sxs-lookup"><span data-stu-id="cc070-123">A pointer to a [**CMSG\_SIGNER\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) structure that contains the signer information to display.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-124">**hMsg**</span><span class="sxs-lookup"><span data-stu-id="cc070-124">**hMsg**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-125">Handle du message à partir duquel les informations du signataire ont été extraites.</span><span class="sxs-lookup"><span data-stu-id="cc070-125">The handle of the message that the signer information was extracted from.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-126">**pszOID**</span><span class="sxs-lookup"><span data-stu-id="cc070-126">**pszOID**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-127">Pointeur vers une chaîne ANSI se terminant par un caractère null qui contient la représentation sous forme de chaîne de l' [*identificateur d’objet*](../secgloss/o-gly.md) (OID) qui indique le certificat pour lequel la signature doit être validée.</span><span class="sxs-lookup"><span data-stu-id="cc070-127">A pointer to a null-terminated ANSI string that contains the string representation of the [*object identifier*](../secgloss/o-gly.md) (OID) that signifies what the certificate that did the signing should be validated for.</span></span> <span data-ttu-id="cc070-128">Par exemple, si cette méthode est appelée pour afficher la signature d’une [*liste de certificats de confiance*](../secgloss/c-gly.md) (CTL), la chaîne d’OID de **\_ \_ \_ \_ signature d’utilisation szOID KP** doit être transmise.</span><span class="sxs-lookup"><span data-stu-id="cc070-128">For example, if this is being called to view the signature of a [*certificate trust list*](../secgloss/c-gly.md) (CTL), the **szOID\_KP\_CTL\_USAGE\_SIGNING** OID string should be passed in.</span></span> <span data-ttu-id="cc070-129">Si ce membre a la **valeur null**, le certificat n’est pas validé pour les utilisations.</span><span class="sxs-lookup"><span data-stu-id="cc070-129">If this member is **NULL**, the certificate is not validated for usages.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-130">**dwReserved**</span><span class="sxs-lookup"><span data-stu-id="cc070-130">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-131">Ce paramètre n’est pas utilisé actuellement.</span><span class="sxs-lookup"><span data-stu-id="cc070-131">This parameter is not currently used.</span></span> <span data-ttu-id="cc070-132">Ce membre doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cc070-132">This member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-133">**cStores**</span><span class="sxs-lookup"><span data-stu-id="cc070-133">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-134">Nombre d’éléments dans le tableau **rghStores** .</span><span class="sxs-lookup"><span data-stu-id="cc070-134">The number of elements in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-135">**rghStores**</span><span class="sxs-lookup"><span data-stu-id="cc070-135">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-136">Tableau de valeurs **HCERTSTORE** qui représentent les autres magasins de certificats pour rechercher le certificat qui a signé le message.</span><span class="sxs-lookup"><span data-stu-id="cc070-136">An array of **HCERTSTORE** values that represent the other certificate stores to search for the certificate that signed the message.</span></span> <span data-ttu-id="cc070-137">Si ce membre a la **valeur null**, aucun autre magasin n’est recherché.</span><span class="sxs-lookup"><span data-stu-id="cc070-137">If this member is **NULL**, no additional stores are searched.</span></span> <span data-ttu-id="cc070-138">Le membre **cStores** contient le nombre d’éléments de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="cc070-138">The **cStores** member contains the number of elements in this array.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-139">**cPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="cc070-139">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-140">Nombre d’éléments dans le tableau **rgPropSheetPages** .</span><span class="sxs-lookup"><span data-stu-id="cc070-140">The number of elements in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="cc070-141">**rgPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="cc070-141">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="cc070-142">Tableau de pointeurs de structure [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) qui définissent les pages supplémentaires à afficher dans la boîte de dialogue standard.</span><span class="sxs-lookup"><span data-stu-id="cc070-142">An array of [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) structure pointers that define any extra pages to display in the standard dialog box.</span></span> <span data-ttu-id="cc070-143">Si ce membre a la **valeur null**, aucune page supplémentaire ne sera affichée.</span><span class="sxs-lookup"><span data-stu-id="cc070-143">If this member is **NULL**, no additional pages will be displayed.</span></span> <span data-ttu-id="cc070-144">Le membre **cPropSheetPages** contient le nombre d’éléments de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="cc070-144">The **cPropSheetPages** member contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc070-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc070-145">Requirements</span></span>



| <span data-ttu-id="cc070-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc070-146">Requirement</span></span> | <span data-ttu-id="cc070-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc070-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc070-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc070-148">Minimum supported client</span></span><br/> | <span data-ttu-id="cc070-149">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc070-149">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="cc070-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc070-150">Minimum supported server</span></span><br/> | <span data-ttu-id="cc070-151">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc070-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cc070-152">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="cc070-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cc070-153">**CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTW** (Unicode) et **CRYPTUI \_ VIEWSIGNERINFO \_ structa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cc070-153">**CRYPTUI\_VIEWSIGNERINFO\_STRUCTW** (Unicode) and **CRYPTUI\_VIEWSIGNERINFO\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc070-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc070-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc070-155">**CryptUIDlgViewSignerInfo**</span><span class="sxs-lookup"><span data-stu-id="cc070-155">**CryptUIDlgViewSignerInfo**</span></span>](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
