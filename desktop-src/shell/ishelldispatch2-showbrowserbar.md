---
description: 'Méthode IShellDispatch2. ShowBrowserBar : affiche une barre de navigateur.'
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
ms.openlocfilehash: 7143b55ae59c8fca845d256ddc1f79e69672364b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116937"
---
# <a name="ishelldispatch2showbrowserbar-method"></a><span data-ttu-id="89d70-103">Méthode IShellDispatch2. ShowBrowserBar</span><span class="sxs-lookup"><span data-stu-id="89d70-103">IShellDispatch2.ShowBrowserBar method</span></span>

<span data-ttu-id="89d70-104">Affiche une barre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="89d70-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="89d70-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89d70-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="89d70-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89d70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89d70-107">*sCLSID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89d70-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89d70-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="89d70-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="89d70-109">**Chaîne** qui contient le format de chaîne du CLSID de la barre de navigateur à afficher.</span><span class="sxs-lookup"><span data-stu-id="89d70-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="89d70-110">L’objet doit être inscrit en tant qu’objet de barre d’explorateur avec une \_ catégorie de composant INFOBAND CATID.</span><span class="sxs-lookup"><span data-stu-id="89d70-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="89d70-111">Pour plus d’informations, consultez [création de barres d’exploration personnalisées, de bandes d’outils et de bandes de bureau](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="89d70-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="89d70-112">*vShow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89d70-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89d70-113">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="89d70-113">Type: **Variant**</span></span>

<span data-ttu-id="89d70-114">Affectez la valeur **true** pour afficher la barre de navigateur ou **false** pour la masquer.</span><span class="sxs-lookup"><span data-stu-id="89d70-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89d70-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="89d70-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="89d70-116">JScript</span><span class="sxs-lookup"><span data-stu-id="89d70-116">JScript</span></span>

<span data-ttu-id="89d70-117">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="89d70-117">Type: **Variant\***</span></span>

<span data-ttu-id="89d70-118">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="89d70-118">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="89d70-119">VB</span><span class="sxs-lookup"><span data-stu-id="89d70-119">VB</span></span>

<span data-ttu-id="89d70-120">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="89d70-120">Type: **Variant\***</span></span>

<span data-ttu-id="89d70-121">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="89d70-121">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="89d70-122">Notes </span><span class="sxs-lookup"><span data-stu-id="89d70-122">Remarks</span></span>

<span data-ttu-id="89d70-123">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ShowBrowserBar**](./shell-showbrowserbar.md) .</span><span class="sxs-lookup"><span data-stu-id="89d70-123">This method is implemented and accessed through the [**Shell.ShowBrowserBar**](./shell-showbrowserbar.md) method.</span></span>

<span data-ttu-id="89d70-124">Vous pouvez afficher l’une des barres d’exploration standard en définissant le paramètre *sCLSID* sur le CLSID de cette barre d’exploration.</span><span class="sxs-lookup"><span data-stu-id="89d70-124">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="89d70-125">Les barres d’exploration standard et leurs chaînes CLSID sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="89d70-125">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="89d70-126">Volet d’exploration</span><span class="sxs-lookup"><span data-stu-id="89d70-126">Explorer Bar</span></span> | <span data-ttu-id="89d70-127">Chaîne CLSID</span><span class="sxs-lookup"><span data-stu-id="89d70-127">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="89d70-128">Favoris</span><span class="sxs-lookup"><span data-stu-id="89d70-128">Favorites</span></span>    | <span data-ttu-id="89d70-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="89d70-129">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="89d70-130">Dossiers</span><span class="sxs-lookup"><span data-stu-id="89d70-130">Folders</span></span>      | <span data-ttu-id="89d70-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="89d70-131">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="89d70-132">Historique</span><span class="sxs-lookup"><span data-stu-id="89d70-132">History</span></span>      | <span data-ttu-id="89d70-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="89d70-133">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="89d70-134">Recherche</span><span class="sxs-lookup"><span data-stu-id="89d70-134">Search</span></span>       | <span data-ttu-id="89d70-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="89d70-135">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="89d70-136">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="89d70-136">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="89d70-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="89d70-137">Examples</span></span>

<span data-ttu-id="89d70-138">Les exemples suivants illustrent l’utilisation de **ShowBrowserBar** pour afficher la barre de navigateur **favoris** .</span><span class="sxs-lookup"><span data-stu-id="89d70-138">The following examples show the use of **ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="89d70-139">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="89d70-139">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="89d70-140">Langage</span><span class="sxs-lookup"><span data-stu-id="89d70-140">JScript:</span></span>


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



<span data-ttu-id="89d70-141">VBScript</span><span class="sxs-lookup"><span data-stu-id="89d70-141">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="89d70-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89d70-142">Requirements</span></span>



| <span data-ttu-id="89d70-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89d70-143">Requirement</span></span> | <span data-ttu-id="89d70-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="89d70-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89d70-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89d70-145">Minimum supported client</span></span><br/> | <span data-ttu-id="89d70-146">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89d70-146">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="89d70-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89d70-147">Minimum supported server</span></span><br/> | <span data-ttu-id="89d70-148">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89d70-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="89d70-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="89d70-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="89d70-150"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="89d70-150"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="89d70-151">MIDL</span><span class="sxs-lookup"><span data-stu-id="89d70-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="89d70-152"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="89d70-152"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="89d70-153">DLL</span><span class="sxs-lookup"><span data-stu-id="89d70-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89d70-154"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="89d70-154"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
