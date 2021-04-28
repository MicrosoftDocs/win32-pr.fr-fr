---
description: 'Méthode IShellDispatch2. GetSystemInformation : récupère les informations système.'
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: Méthode IShellDispatch2. GetSystemInformation (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a81ac091dc1905c1cbcd2c41575c907ce957e60c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117107"
---
# <a name="ishelldispatch2getsysteminformation-method"></a><span data-ttu-id="821dd-103">Méthode IShellDispatch2. GetSystemInformation</span><span class="sxs-lookup"><span data-stu-id="821dd-103">IShellDispatch2.GetSystemInformation method</span></span>

<span data-ttu-id="821dd-104">Récupère des informations système.</span><span class="sxs-lookup"><span data-stu-id="821dd-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="821dd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="821dd-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="821dd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="821dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="821dd-107">*sName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="821dd-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="821dd-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="821dd-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="821dd-109">**Chaîne** qui spécifie les informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="821dd-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="821dd-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="821dd-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="821dd-111">JScript</span><span class="sxs-lookup"><span data-stu-id="821dd-111">JScript</span></span>

<span data-ttu-id="821dd-112">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="821dd-112">Type: **Variant**</span></span>

<span data-ttu-id="821dd-113">Retourne la valeur des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="821dd-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="821dd-114">Le type de retour dépend des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="821dd-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="821dd-115">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="821dd-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="821dd-116">VB</span><span class="sxs-lookup"><span data-stu-id="821dd-116">VB</span></span>

<span data-ttu-id="821dd-117">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="821dd-117">Type: **Variant**</span></span>

<span data-ttu-id="821dd-118">Retourne la valeur des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="821dd-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="821dd-119">Le type de retour dépend des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="821dd-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="821dd-120">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="821dd-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="821dd-121">Notes </span><span class="sxs-lookup"><span data-stu-id="821dd-121">Remarks</span></span>

<span data-ttu-id="821dd-122">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. GetSystemInformation**](./shell-getsysteminformation.md) .</span><span class="sxs-lookup"><span data-stu-id="821dd-122">This method is implemented and accessed through the [**Shell.GetSystemInformation**](./shell-getsysteminformation.md) method.</span></span>

<span data-ttu-id="821dd-123">Cette méthode peut être utilisée pour demander de nombreuses valeurs d’informations système.</span><span class="sxs-lookup"><span data-stu-id="821dd-123">This method can be used to request many system information values.</span></span> <span data-ttu-id="821dd-124">Le tableau suivant indique la valeur *sName* utilisée pour demander les informations et le type associé de la valeur retournée.</span><span class="sxs-lookup"><span data-stu-id="821dd-124">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="821dd-125">*sName*</span><span class="sxs-lookup"><span data-stu-id="821dd-125">*sName*</span></span>

<span data-ttu-id="821dd-126">Type de retour</span><span class="sxs-lookup"><span data-stu-id="821dd-126">Return type</span></span>

<span data-ttu-id="821dd-127">Description</span><span class="sxs-lookup"><span data-stu-id="821dd-127">Description</span></span>

<span data-ttu-id="821dd-128">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="821dd-128">DirectoryServiceAvailable</span></span>

<span data-ttu-id="821dd-129">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="821dd-129">**Boolean**</span></span>

<span data-ttu-id="821dd-130">Affectez la valeur **true** si le service d’annuaire est disponible ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="821dd-130">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="821dd-131">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="821dd-131">DoubleClickTime</span></span>

<span data-ttu-id="821dd-132">**Integer**</span><span class="sxs-lookup"><span data-stu-id="821dd-132">**Integer**</span></span>

<span data-ttu-id="821dd-133">Durée du double-clic, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="821dd-133">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="821dd-134">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="821dd-134">ProcessorLevel</span></span>

<span data-ttu-id="821dd-135">**Integer**</span><span class="sxs-lookup"><span data-stu-id="821dd-135">**Integer**</span></span>

<span data-ttu-id="821dd-136">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="821dd-136">**Windows Vista and later**.</span></span> <span data-ttu-id="821dd-137">Niveau du processeur.</span><span class="sxs-lookup"><span data-stu-id="821dd-137">The processor level.</span></span> <span data-ttu-id="821dd-138">Retourne 3, 4 ou 5 pour les processeurs de niveau x386, x486 et Pentium, respectivement.</span><span class="sxs-lookup"><span data-stu-id="821dd-138">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="821dd-139">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="821dd-139">ProcessorSpeed</span></span>

<span data-ttu-id="821dd-140">**Integer**</span><span class="sxs-lookup"><span data-stu-id="821dd-140">**Integer**</span></span>

<span data-ttu-id="821dd-141">Vitesse du processeur, en mégahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="821dd-141">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="821dd-142">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="821dd-142">ProcessorArchitecture</span></span>

<span data-ttu-id="821dd-143">**Integer**</span><span class="sxs-lookup"><span data-stu-id="821dd-143">**Integer**</span></span>

<span data-ttu-id="821dd-144">Architecture du processeur.</span><span class="sxs-lookup"><span data-stu-id="821dd-144">The processor architecture.</span></span> <span data-ttu-id="821dd-145">Pour plus d’informations, consultez la description du membre **wProcessorArchitecture** de la structure des [**\_ informations système**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="821dd-145">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="821dd-146">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="821dd-146">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="821dd-147">**Integer**</span><span class="sxs-lookup"><span data-stu-id="821dd-147">**Integer**</span></span>

<span data-ttu-id="821dd-148">Quantité de mémoire physique installée, en octets.</span><span class="sxs-lookup"><span data-stu-id="821dd-148">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="821dd-149">Les éléments suivants sont valides uniquement sur Windows XP.</span><span class="sxs-lookup"><span data-stu-id="821dd-149">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="821dd-150">Fichiers ISO \_ professionnel</span><span class="sxs-lookup"><span data-stu-id="821dd-150">IsOS\_Professional</span></span>

<span data-ttu-id="821dd-151">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="821dd-151">**Boolean**</span></span>

<span data-ttu-id="821dd-152">Définir sur **true** si le système d’exploitation est Windows XP Professionnel Edition ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="821dd-152">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="821dd-153">Fichiers ISO \_ personnel</span><span class="sxs-lookup"><span data-stu-id="821dd-153">IsOS\_Personal</span></span>

<span data-ttu-id="821dd-154">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="821dd-154">**Boolean**</span></span>

<span data-ttu-id="821dd-155">Définir sur **true** si le système d’exploitation est Windows XP Édition personnelle ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="821dd-155">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="821dd-156">Les éléments suivants sont valides uniquement sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="821dd-156">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="821dd-157">Fichiers ISO \_ MEMBRE_DOMAINE</span><span class="sxs-lookup"><span data-stu-id="821dd-157">IsOS\_DomainMember</span></span>

<span data-ttu-id="821dd-158">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="821dd-158">**Boolean**</span></span>

<span data-ttu-id="821dd-159">Défini sur **true** si l’ordinateur est membre d’un domaine ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="821dd-159">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="821dd-160">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="821dd-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="821dd-161">Exemples</span><span class="sxs-lookup"><span data-stu-id="821dd-161">Examples</span></span>

<span data-ttu-id="821dd-162">Les exemples suivants illustrent l’utilisation de **GetSystemInformation** pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="821dd-162">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="821dd-163">Langage</span><span class="sxs-lookup"><span data-stu-id="821dd-163">JScript:</span></span>


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



<span data-ttu-id="821dd-164">VBScript</span><span class="sxs-lookup"><span data-stu-id="821dd-164">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="821dd-165">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="821dd-165">Requirements</span></span>



| <span data-ttu-id="821dd-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="821dd-166">Requirement</span></span> | <span data-ttu-id="821dd-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="821dd-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="821dd-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="821dd-168">Minimum supported client</span></span><br/> | <span data-ttu-id="821dd-169">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="821dd-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="821dd-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="821dd-170">Minimum supported server</span></span><br/> | <span data-ttu-id="821dd-171">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="821dd-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="821dd-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="821dd-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="821dd-173"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="821dd-173"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="821dd-174">MIDL</span><span class="sxs-lookup"><span data-stu-id="821dd-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="821dd-175"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="821dd-175"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="821dd-176">DLL</span><span class="sxs-lookup"><span data-stu-id="821dd-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="821dd-177"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="821dd-177"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
