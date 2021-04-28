---
description: Shell. ShowBrowserBar, méthode-affiche une barre de navigateur.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Shell. ShowBrowserBar, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d19cd5b98ce39470860cc481ab05e4bb41adc9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083723"
---
# <a name="shellshowbrowserbar-method"></a><span data-ttu-id="bfcdd-103">Shell. ShowBrowserBar, méthode</span><span class="sxs-lookup"><span data-stu-id="bfcdd-103">Shell.ShowBrowserBar method</span></span>

<span data-ttu-id="bfcdd-104">Affiche une barre de navigateur.</span><span class="sxs-lookup"><span data-stu-id="bfcdd-104">Displays a browser bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfcdd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfcdd-105">Syntax</span></span>


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="bfcdd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bfcdd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfcdd-107">*sCLSID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bfcdd-107">*sCLSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfcdd-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="bfcdd-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="bfcdd-109">**Chaîne** qui contient le format de chaîne du CLSID de la barre de navigateur à afficher.</span><span class="sxs-lookup"><span data-stu-id="bfcdd-109">A **String** that contains the string form of the CLSID of the browser bar to be displayed.</span></span> <span data-ttu-id="bfcdd-110">L’objet doit être inscrit en tant qu’objet de barre d’explorateur avec une \_ catégorie de composant INFOBAND CATID.</span><span class="sxs-lookup"><span data-stu-id="bfcdd-110">The object must be registered as an Explorer Bar object with a CATID\_InfoBand component category.</span></span> <span data-ttu-id="bfcdd-111">Pour plus d’informations, consultez [création de barres d’exploration personnalisées, de bandes d’outils et de bandes de bureau](band-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bfcdd-111">For further information, see [Creating Custom Explorer Bars, Tool Bands, and Desk Bands](band-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="bfcdd-112">*vShow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bfcdd-112">*vShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfcdd-113">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="bfcdd-113">Type: **Variant**</span></span>

<span data-ttu-id="bfcdd-114">Affectez la valeur **true** pour afficher la barre de navigateur ou **false** pour la masquer.</span><span class="sxs-lookup"><span data-stu-id="bfcdd-114">Set to **true** to show the browser bar or **false** to hide it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfcdd-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bfcdd-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="bfcdd-116">JScript</span><span class="sxs-lookup"><span data-stu-id="bfcdd-116">JScript</span></span>

<span data-ttu-id="bfcdd-117">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="bfcdd-117">Type: **Variant\***</span></span>

<span data-ttu-id="bfcdd-118">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfcdd-118">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="bfcdd-119">VB</span><span class="sxs-lookup"><span data-stu-id="bfcdd-119">VB</span></span>

<span data-ttu-id="bfcdd-120">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="bfcdd-120">Type: **Variant\***</span></span>

<span data-ttu-id="bfcdd-121">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="bfcdd-121">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfcdd-122">Notes </span><span class="sxs-lookup"><span data-stu-id="bfcdd-122">Remarks</span></span>

<span data-ttu-id="bfcdd-123">Vous pouvez afficher l’une des barres d’exploration standard en définissant le paramètre *sCLSID* sur le CLSID de cette barre d’exploration.</span><span class="sxs-lookup"><span data-stu-id="bfcdd-123">You can display one of the standard Explorer Bars by setting the *sCLSID* parameter to the CLSID of that Explorer Bar.</span></span> <span data-ttu-id="bfcdd-124">Les barres d’exploration standard et leurs chaînes CLSID sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="bfcdd-124">The standard Explorer Bars and their CLSID strings are as follows:</span></span>



| <span data-ttu-id="bfcdd-125">Volet d’exploration</span><span class="sxs-lookup"><span data-stu-id="bfcdd-125">Explorer Bar</span></span> | <span data-ttu-id="bfcdd-126">Chaîne CLSID</span><span class="sxs-lookup"><span data-stu-id="bfcdd-126">CLSID string</span></span>                           |
|--------------|----------------------------------------|
| <span data-ttu-id="bfcdd-127">Favoris</span><span class="sxs-lookup"><span data-stu-id="bfcdd-127">Favorites</span></span>    | <span data-ttu-id="bfcdd-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="bfcdd-128">{EFA24E61-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="bfcdd-129">Dossiers</span><span class="sxs-lookup"><span data-stu-id="bfcdd-129">Folders</span></span>      | <span data-ttu-id="bfcdd-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="bfcdd-130">{EFA24E64-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="bfcdd-131">Historique</span><span class="sxs-lookup"><span data-stu-id="bfcdd-131">History</span></span>      | <span data-ttu-id="bfcdd-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span><span class="sxs-lookup"><span data-stu-id="bfcdd-132">{EFA24E62-B078-11d0-89E4-00C04FC9E26E}</span></span> |
| <span data-ttu-id="bfcdd-133">Recherche</span><span class="sxs-lookup"><span data-stu-id="bfcdd-133">Search</span></span>       | <span data-ttu-id="bfcdd-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span><span class="sxs-lookup"><span data-stu-id="bfcdd-134">{30D02401-6A81-11d0-8274-00C04FD5AE38}</span></span> |



 

<span data-ttu-id="bfcdd-135">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bfcdd-135">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="bfcdd-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="bfcdd-136">Examples</span></span>

<span data-ttu-id="bfcdd-137">Les exemples suivants illustrent l’utilisation de **Shell. ShowBrowserBar** pour afficher la barre de navigateur **favoris** .</span><span class="sxs-lookup"><span data-stu-id="bfcdd-137">The following examples show the use of **Shell.ShowBrowserBar** to display the **Favorites** browser bar.</span></span> <span data-ttu-id="bfcdd-138">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="bfcdd-138">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="bfcdd-139">Langage</span><span class="sxs-lookup"><span data-stu-id="bfcdd-139">JScript:</span></span>


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



<span data-ttu-id="bfcdd-140">VBScript</span><span class="sxs-lookup"><span data-stu-id="bfcdd-140">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="bfcdd-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bfcdd-141">Requirements</span></span>



| <span data-ttu-id="bfcdd-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bfcdd-142">Requirement</span></span> | <span data-ttu-id="bfcdd-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="bfcdd-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcdd-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfcdd-144">Minimum supported client</span></span><br/> | <span data-ttu-id="bfcdd-145">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfcdd-145">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfcdd-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bfcdd-146">Minimum supported server</span></span><br/> | <span data-ttu-id="bfcdd-147">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bfcdd-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bfcdd-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="bfcdd-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfcdd-149"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfcdd-149"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="bfcdd-150">MIDL</span><span class="sxs-lookup"><span data-stu-id="bfcdd-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bfcdd-151"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bfcdd-151"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="bfcdd-152">DLL</span><span class="sxs-lookup"><span data-stu-id="bfcdd-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfcdd-153"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="bfcdd-153"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
