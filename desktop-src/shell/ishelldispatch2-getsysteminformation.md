---
description: Récupère des informations système.
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
ms.openlocfilehash: 624c7383d458f20a13f0e2249ec302181fc4a7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863138"
---
# <a name="ishelldispatch2getsysteminformation-method"></a><span data-ttu-id="8845b-103">Méthode IShellDispatch2. GetSystemInformation</span><span class="sxs-lookup"><span data-stu-id="8845b-103">IShellDispatch2.GetSystemInformation method</span></span>

<span data-ttu-id="8845b-104">Récupère des informations système.</span><span class="sxs-lookup"><span data-stu-id="8845b-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="8845b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8845b-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="8845b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8845b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8845b-107">*sName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8845b-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8845b-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="8845b-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="8845b-109">**Chaîne** qui spécifie les informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="8845b-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8845b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8845b-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="8845b-111">JScript</span><span class="sxs-lookup"><span data-stu-id="8845b-111">JScript</span></span>

<span data-ttu-id="8845b-112">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="8845b-112">Type: **Variant**</span></span>

<span data-ttu-id="8845b-113">Retourne la valeur des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="8845b-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="8845b-114">Le type de retour dépend des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="8845b-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="8845b-115">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="8845b-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="8845b-116">VB</span><span class="sxs-lookup"><span data-stu-id="8845b-116">VB</span></span>

<span data-ttu-id="8845b-117">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="8845b-117">Type: **Variant**</span></span>

<span data-ttu-id="8845b-118">Retourne la valeur des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="8845b-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="8845b-119">Le type de retour dépend des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="8845b-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="8845b-120">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="8845b-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="8845b-121">Notes</span><span class="sxs-lookup"><span data-stu-id="8845b-121">Remarks</span></span>

<span data-ttu-id="8845b-122">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. GetSystemInformation**](./shell-getsysteminformation.md) .</span><span class="sxs-lookup"><span data-stu-id="8845b-122">This method is implemented and accessed through the [**Shell.GetSystemInformation**](./shell-getsysteminformation.md) method.</span></span>

<span data-ttu-id="8845b-123">Cette méthode peut être utilisée pour demander de nombreuses valeurs d’informations système.</span><span class="sxs-lookup"><span data-stu-id="8845b-123">This method can be used to request many system information values.</span></span> <span data-ttu-id="8845b-124">Le tableau suivant indique la valeur *sName* utilisée pour demander les informations et le type associé de la valeur retournée.</span><span class="sxs-lookup"><span data-stu-id="8845b-124">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="8845b-125">*sName*</span><span class="sxs-lookup"><span data-stu-id="8845b-125">*sName*</span></span>

<span data-ttu-id="8845b-126">Type de retour</span><span class="sxs-lookup"><span data-stu-id="8845b-126">Return type</span></span>

<span data-ttu-id="8845b-127">Description</span><span class="sxs-lookup"><span data-stu-id="8845b-127">Description</span></span>

<span data-ttu-id="8845b-128">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="8845b-128">DirectoryServiceAvailable</span></span>

<span data-ttu-id="8845b-129">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="8845b-129">**Boolean**</span></span>

<span data-ttu-id="8845b-130">Affectez la valeur **true** si le service d’annuaire est disponible ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="8845b-130">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="8845b-131">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="8845b-131">DoubleClickTime</span></span>

<span data-ttu-id="8845b-132">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8845b-132">**Integer**</span></span>

<span data-ttu-id="8845b-133">Durée du double-clic, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="8845b-133">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="8845b-134">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="8845b-134">ProcessorLevel</span></span>

<span data-ttu-id="8845b-135">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8845b-135">**Integer**</span></span>

<span data-ttu-id="8845b-136">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="8845b-136">**Windows Vista and later**.</span></span> <span data-ttu-id="8845b-137">Niveau du processeur.</span><span class="sxs-lookup"><span data-stu-id="8845b-137">The processor level.</span></span> <span data-ttu-id="8845b-138">Retourne 3, 4 ou 5 pour les processeurs de niveau x386, x486 et Pentium, respectivement.</span><span class="sxs-lookup"><span data-stu-id="8845b-138">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="8845b-139">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="8845b-139">ProcessorSpeed</span></span>

<span data-ttu-id="8845b-140">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8845b-140">**Integer**</span></span>

<span data-ttu-id="8845b-141">Vitesse du processeur, en mégahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="8845b-141">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="8845b-142">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="8845b-142">ProcessorArchitecture</span></span>

<span data-ttu-id="8845b-143">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8845b-143">**Integer**</span></span>

<span data-ttu-id="8845b-144">Architecture du processeur.</span><span class="sxs-lookup"><span data-stu-id="8845b-144">The processor architecture.</span></span> <span data-ttu-id="8845b-145">Pour plus d’informations, consultez la description du membre **wProcessorArchitecture** de la structure des [**\_ informations système**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="8845b-145">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="8845b-146">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="8845b-146">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="8845b-147">**Integer**</span><span class="sxs-lookup"><span data-stu-id="8845b-147">**Integer**</span></span>

<span data-ttu-id="8845b-148">Quantité de mémoire physique installée, en octets.</span><span class="sxs-lookup"><span data-stu-id="8845b-148">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="8845b-149">Les éléments suivants sont valides uniquement sur Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8845b-149">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="8845b-150">Fichiers ISO \_ professionnel</span><span class="sxs-lookup"><span data-stu-id="8845b-150">IsOS\_Professional</span></span>

<span data-ttu-id="8845b-151">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="8845b-151">**Boolean**</span></span>

<span data-ttu-id="8845b-152">Définir sur **true** si le système d’exploitation est Windows XP Professionnel Edition ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="8845b-152">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="8845b-153">Fichiers ISO \_ personnel</span><span class="sxs-lookup"><span data-stu-id="8845b-153">IsOS\_Personal</span></span>

<span data-ttu-id="8845b-154">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="8845b-154">**Boolean**</span></span>

<span data-ttu-id="8845b-155">Définir sur **true** si le système d’exploitation est Windows XP Édition personnelle ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="8845b-155">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="8845b-156">Les éléments suivants sont valides uniquement sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="8845b-156">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="8845b-157">Fichiers ISO \_ MEMBRE_DOMAINE</span><span class="sxs-lookup"><span data-stu-id="8845b-157">IsOS\_DomainMember</span></span>

<span data-ttu-id="8845b-158">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="8845b-158">**Boolean**</span></span>

<span data-ttu-id="8845b-159">Défini sur **true** si l’ordinateur est membre d’un domaine ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="8845b-159">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="8845b-160">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8845b-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="8845b-161">Exemples</span><span class="sxs-lookup"><span data-stu-id="8845b-161">Examples</span></span>

<span data-ttu-id="8845b-162">Les exemples suivants illustrent l’utilisation de **GetSystemInformation** pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="8845b-162">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="8845b-163">Langage</span><span class="sxs-lookup"><span data-stu-id="8845b-163">JScript:</span></span>


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



<span data-ttu-id="8845b-164">VBScript</span><span class="sxs-lookup"><span data-stu-id="8845b-164">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8845b-165">Spécifications</span><span class="sxs-lookup"><span data-stu-id="8845b-165">Requirements</span></span>



| <span data-ttu-id="8845b-166">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8845b-166">Requirement</span></span> | <span data-ttu-id="8845b-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="8845b-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8845b-168">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8845b-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8845b-169">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8845b-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8845b-170">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8845b-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8845b-171">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8845b-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8845b-172">En-tête</span><span class="sxs-lookup"><span data-stu-id="8845b-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="8845b-173"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8845b-173"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="8845b-174">MIDL</span><span class="sxs-lookup"><span data-stu-id="8845b-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8845b-175"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8845b-175"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="8845b-176">DLL</span><span class="sxs-lookup"><span data-stu-id="8845b-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8845b-177"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="8845b-177"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
