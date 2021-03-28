---
description: Affiche une barre de navigateur.
ms.assetid: 5776370c-3bbf-449b-a8fe-2dbc7d89dd25
title: Méthode IShellDispatch2. ShowBrowserBar (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e1df729401dd12b8221ba98a3b81ea65569113e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972379"
---
# <a name="ishelldispatch2showbrowserbar-method"></a><span data-ttu-id="c4e1a-103">Méthode IShellDispatch2. ShowBrowserBar</span><span class="sxs-lookup"><span data-stu-id="c4e1a-103">IShellDispatch2.ShowBrowserBar method</span></span>

<span data-ttu-id="c4e1a-104">Affiche une barre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4e1a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4e1a-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

IShellDispatch2.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="c4e1a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c4e1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4e1a-107">*sCLSID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4e1a-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e1a-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c4e1a-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c4e1a-109">**Chaîne** qui contient le format de chaîne du CLSID de la barre de navigateur à afficher.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="c4e1a-110">L’objet doit être inscrit en tant qu’objet de barre d’explorateur avec une \_ catégorie de composant INFOBAND CATID.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="c4e1a-111">Pour plus d’informations, consultez [création de barres d’exploration personnalisées, de bandes d’outils et de bandes de bureau](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="c4e1a-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4e1a-112">*vShow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c4e1a-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4e1a-113">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="c4e1a-113">Type: **Variant**</span></span>

<span data-ttu-id="c4e1a-114">Affectez la valeur **true** pour afficher la barre de navigateur ou **false** pour la masquer.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4e1a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c4e1a-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="c4e1a-116">JScript</span><span class="sxs-lookup"><span data-stu-id="c4e1a-116">JScript</span></span>

<span data-ttu-id="c4e1a-117">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="c4e1a-117">Type: \**Variant\** _</span></span>

<span data-ttu-id="c4e1a-118">Retourne _ *true*\* en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-118">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="c4e1a-119">VB</span><span class="sxs-lookup"><span data-stu-id="c4e1a-119">VB</span></span>

<span data-ttu-id="c4e1a-120">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="c4e1a-120">Type: \**Variant\** _</span></span>

<span data-ttu-id="c4e1a-121">Retourne _ *true*\* en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-121">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4e1a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="c4e1a-122">Remarks</span></span>

<span data-ttu-id="c4e1a-123">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ShowBrowserBar**](./shell-showbrowserbar.md) .</span><span class="sxs-lookup"><span data-stu-id="c4e1a-123">This method is implemented and accessed through the [**Shell.ShowBrowserBar**](./shell-showbrowserbar.md) method.</span></span>

<span data-ttu-id="c4e1a-124">Vous pouvez afficher l’une des barres d’exploration standard en définissant le paramètre *sCLSID* sur le CLSID de cette barre d’exploration.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-124">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="c4e1a-125">Les barres d’exploration standard et leurs chaînes CLSID sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="c4e1a-125">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="c4e1a-126">Volet d’exploration</span><span class="sxs-lookup"><span data-stu-id="c4e1a-126">Explorer Bar</span></span> | <span data-ttu-id="c4e1a-127">Chaîne CLSID</span><span class="sxs-lookup"><span data-stu-id="c4e1a-127">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="c4e1a-128">Favoris</span><span class="sxs-lookup"><span data-stu-id="c4e1a-128">Favorites</span></span>    | <span data-ttu-id="c4e1a-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="c4e1a-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="c4e1a-130">Dossiers</span><span class="sxs-lookup"><span data-stu-id="c4e1a-130">Folders</span></span>      | <span data-ttu-id="c4e1a-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="c4e1a-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="c4e1a-132">Historique</span><span class="sxs-lookup"><span data-stu-id="c4e1a-132">History</span></span>      | <span data-ttu-id="c4e1a-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="c4e1a-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="c4e1a-134">Rechercher</span><span class="sxs-lookup"><span data-stu-id="c4e1a-134">Search</span></span>       | <span data-ttu-id="c4e1a-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="c4e1a-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="c4e1a-136">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-136">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="c4e1a-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="c4e1a-137">Examples</span></span>

<span data-ttu-id="c4e1a-138">Les exemples suivants illustrent l’utilisation de **ShowBrowserBar** pour afficher la barre de navigateur **favoris** .</span><span class="sxs-lookup"><span data-stu-id="c4e1a-138">The following examples show the use of **ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="c4e1a-139">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="c4e1a-139">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="c4e1a-140">Langage</span><span class="sxs-lookup"><span data-stu-id="c4e1a-140">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



<span data-ttu-id="c4e1a-141">VBScript</span><span class="sxs-lookup"><span data-stu-id="c4e1a-141">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="c4e1a-142">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c4e1a-142">Requirements</span></span>



| <span data-ttu-id="c4e1a-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4e1a-143">Requirement</span></span> | <span data-ttu-id="c4e1a-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4e1a-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4e1a-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4e1a-145">Minimum supported client</span></span><br/> | <span data-ttu-id="c4e1a-146">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4e1a-146">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c4e1a-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4e1a-147">Minimum supported server</span></span><br/> | <span data-ttu-id="c4e1a-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4e1a-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c4e1a-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4e1a-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4e1a-150"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4e1a-150"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c4e1a-151">MIDL</span><span class="sxs-lookup"><span data-stu-id="c4e1a-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c4e1a-152"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c4e1a-152"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c4e1a-153">DLL</span><span class="sxs-lookup"><span data-stu-id="c4e1a-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4e1a-154"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c4e1a-154"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
