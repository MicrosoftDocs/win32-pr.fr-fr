---
description: Shell. GetSystemInformation, méthode-récupère les informations système.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Shell. GetSystemInformation, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b9e021e767309007cfee2cfc78268fb7d7cea042
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104277"
---
# <a name="shellgetsysteminformation-method"></a><span data-ttu-id="47ac4-103">Shell. GetSystemInformation, méthode</span><span class="sxs-lookup"><span data-stu-id="47ac4-103">Shell.GetSystemInformation method</span></span>

<span data-ttu-id="47ac4-104">Récupère des informations système.</span><span class="sxs-lookup"><span data-stu-id="47ac4-104">Retrieves system information.</span></span>

## <a name="syntax"></a><span data-ttu-id="47ac4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47ac4-105">Syntax</span></span>


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="47ac4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47ac4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47ac4-107">*sName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47ac4-107">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47ac4-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="47ac4-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="47ac4-109">**Chaîne** qui spécifie les informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="47ac4-109">A **String** that specifies the system information that is being requested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47ac4-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="47ac4-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="47ac4-111">JScript</span><span class="sxs-lookup"><span data-stu-id="47ac4-111">JScript</span></span>

<span data-ttu-id="47ac4-112">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="47ac4-112">Type: **Variant**</span></span>

<span data-ttu-id="47ac4-113">Retourne la valeur des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="47ac4-113">Returns the value of the requested system information.</span></span> <span data-ttu-id="47ac4-114">Le type de retour dépend des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="47ac4-114">The return type depends on which system information is requested.</span></span> <span data-ttu-id="47ac4-115">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="47ac4-115">See the Remarks section for details.</span></span>

### <a name="vb"></a><span data-ttu-id="47ac4-116">VB</span><span class="sxs-lookup"><span data-stu-id="47ac4-116">VB</span></span>

<span data-ttu-id="47ac4-117">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="47ac4-117">Type: **Variant**</span></span>

<span data-ttu-id="47ac4-118">Retourne la valeur des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="47ac4-118">Returns the value of the requested system information.</span></span> <span data-ttu-id="47ac4-119">Le type de retour dépend des informations système demandées.</span><span class="sxs-lookup"><span data-stu-id="47ac4-119">The return type depends on which system information is requested.</span></span> <span data-ttu-id="47ac4-120">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="47ac4-120">See the Remarks section for details.</span></span>

## <a name="remarks"></a><span data-ttu-id="47ac4-121">Notes </span><span class="sxs-lookup"><span data-stu-id="47ac4-121">Remarks</span></span>

<span data-ttu-id="47ac4-122">Cette méthode peut être utilisée pour demander de nombreuses valeurs d’informations système.</span><span class="sxs-lookup"><span data-stu-id="47ac4-122">This method can be used to request many system information values.</span></span> <span data-ttu-id="47ac4-123">Le tableau suivant indique la valeur *sName* utilisée pour demander les informations et le type associé de la valeur retournée.</span><span class="sxs-lookup"><span data-stu-id="47ac4-123">The following table gives the *sName* value that is used to request the information and the associated type of the returned value.</span></span>



<span data-ttu-id="47ac4-124">*sName*</span><span class="sxs-lookup"><span data-stu-id="47ac4-124">*sName*</span></span>

<span data-ttu-id="47ac4-125">Type de retour</span><span class="sxs-lookup"><span data-stu-id="47ac4-125">Return type</span></span>

<span data-ttu-id="47ac4-126">Description</span><span class="sxs-lookup"><span data-stu-id="47ac4-126">Description</span></span>

<span data-ttu-id="47ac4-127">DirectoryServiceAvailable</span><span class="sxs-lookup"><span data-stu-id="47ac4-127">DirectoryServiceAvailable</span></span>

<span data-ttu-id="47ac4-128">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="47ac4-128">**Boolean**</span></span>

<span data-ttu-id="47ac4-129">Affectez la valeur **true** si le service d’annuaire est disponible ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="47ac4-129">Set to **true** if the directory service is available; otherwise, **false**.</span></span>

<span data-ttu-id="47ac4-130">DoubleClickTime</span><span class="sxs-lookup"><span data-stu-id="47ac4-130">DoubleClickTime</span></span>

<span data-ttu-id="47ac4-131">**Integer**</span><span class="sxs-lookup"><span data-stu-id="47ac4-131">**Integer**</span></span>

<span data-ttu-id="47ac4-132">Durée du double-clic, en millisecondes.</span><span class="sxs-lookup"><span data-stu-id="47ac4-132">The double-click time, in milliseconds.</span></span>

<span data-ttu-id="47ac4-133">ProcessorLevel</span><span class="sxs-lookup"><span data-stu-id="47ac4-133">ProcessorLevel</span></span>

<span data-ttu-id="47ac4-134">**Integer**</span><span class="sxs-lookup"><span data-stu-id="47ac4-134">**Integer**</span></span>

<span data-ttu-id="47ac4-135">**Windows Vista et versions ultérieures**.</span><span class="sxs-lookup"><span data-stu-id="47ac4-135">**Windows Vista and later**.</span></span> <span data-ttu-id="47ac4-136">Niveau du processeur.</span><span class="sxs-lookup"><span data-stu-id="47ac4-136">The processor level.</span></span> <span data-ttu-id="47ac4-137">Retourne 3, 4 ou 5 pour les processeurs de niveau x386, x486 et Pentium, respectivement.</span><span class="sxs-lookup"><span data-stu-id="47ac4-137">Returns 3, 4, or 5, for x386, x486, and Pentium-level processors, respectively.</span></span>

<span data-ttu-id="47ac4-138">ProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="47ac4-138">ProcessorSpeed</span></span>

<span data-ttu-id="47ac4-139">**Integer**</span><span class="sxs-lookup"><span data-stu-id="47ac4-139">**Integer**</span></span>

<span data-ttu-id="47ac4-140">Vitesse du processeur, en mégahertz (MHz).</span><span class="sxs-lookup"><span data-stu-id="47ac4-140">The processor speed, in megahertz (MHz).</span></span>

<span data-ttu-id="47ac4-141">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="47ac4-141">ProcessorArchitecture</span></span>

<span data-ttu-id="47ac4-142">**Integer**</span><span class="sxs-lookup"><span data-stu-id="47ac4-142">**Integer**</span></span>

<span data-ttu-id="47ac4-143">Architecture du processeur.</span><span class="sxs-lookup"><span data-stu-id="47ac4-143">The processor architecture.</span></span> <span data-ttu-id="47ac4-144">Pour plus d’informations, consultez la description du membre **wProcessorArchitecture** de la structure des [**\_ informations système**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="47ac4-144">For details, see the discussion of the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span>

<span data-ttu-id="47ac4-145">PhysicalMemoryInstalled</span><span class="sxs-lookup"><span data-stu-id="47ac4-145">PhysicalMemoryInstalled</span></span>

<span data-ttu-id="47ac4-146">**Integer**</span><span class="sxs-lookup"><span data-stu-id="47ac4-146">**Integer**</span></span>

<span data-ttu-id="47ac4-147">Quantité de mémoire physique installée, en octets.</span><span class="sxs-lookup"><span data-stu-id="47ac4-147">The amount of physical memory installed, in bytes.</span></span>

<span data-ttu-id="47ac4-148">Les éléments suivants sont valides uniquement sur Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47ac4-148">The following are valid only on Windows XP.</span></span>

<span data-ttu-id="47ac4-149">Fichiers ISO \_ professionnel</span><span class="sxs-lookup"><span data-stu-id="47ac4-149">IsOS\_Professional</span></span>

<span data-ttu-id="47ac4-150">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="47ac4-150">**Boolean**</span></span>

<span data-ttu-id="47ac4-151">Définir sur **true** si le système d’exploitation est Windows XP Professionnel Edition ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="47ac4-151">Set to **true** if the operating system is Windows XP Professional Edition; otherwise, **false**.</span></span>

<span data-ttu-id="47ac4-152">Fichiers ISO \_ personnel</span><span class="sxs-lookup"><span data-stu-id="47ac4-152">IsOS\_Personal</span></span>

<span data-ttu-id="47ac4-153">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="47ac4-153">**Boolean**</span></span>

<span data-ttu-id="47ac4-154">Définir sur **true** si le système d’exploitation est Windows XP Édition personnelle ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="47ac4-154">Set to **true** if the operating system is Windows XP Home Edition; otherwise, **false**.</span></span>

<span data-ttu-id="47ac4-155">Les éléments suivants sont valides uniquement sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="47ac4-155">The following is valid only on Windows XP and later.</span></span>

<span data-ttu-id="47ac4-156">Fichiers ISO \_ MEMBRE_DOMAINE</span><span class="sxs-lookup"><span data-stu-id="47ac4-156">IsOS\_DomainMember</span></span>

<span data-ttu-id="47ac4-157">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="47ac4-157">**Boolean**</span></span>

<span data-ttu-id="47ac4-158">Défini sur **true** si l’ordinateur est membre d’un domaine ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="47ac4-158">Set to **true** if the computer is a member of a domain; otherwise, **false**.</span></span>



 

<span data-ttu-id="47ac4-159">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="47ac4-159">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="47ac4-160">Exemples</span><span class="sxs-lookup"><span data-stu-id="47ac4-160">Examples</span></span>

<span data-ttu-id="47ac4-161">Les exemples suivants illustrent l’utilisation de **GetSystemInformation** pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="47ac4-161">The following examples show the use of **GetSystemInformation** for JScript and VBScript.</span></span>

<span data-ttu-id="47ac4-162">Langage</span><span class="sxs-lookup"><span data-stu-id="47ac4-162">JScript:</span></span>


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



<span data-ttu-id="47ac4-163">VBScript</span><span class="sxs-lookup"><span data-stu-id="47ac4-163">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="47ac4-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47ac4-164">Requirements</span></span>



| <span data-ttu-id="47ac4-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47ac4-165">Requirement</span></span> | <span data-ttu-id="47ac4-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="47ac4-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47ac4-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47ac4-167">Minimum supported client</span></span><br/> | <span data-ttu-id="47ac4-168">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47ac4-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="47ac4-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47ac4-169">Minimum supported server</span></span><br/> | <span data-ttu-id="47ac4-170">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47ac4-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="47ac4-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="47ac4-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="47ac4-172"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="47ac4-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="47ac4-173">MIDL</span><span class="sxs-lookup"><span data-stu-id="47ac4-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="47ac4-174"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="47ac4-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="47ac4-175">DLL</span><span class="sxs-lookup"><span data-stu-id="47ac4-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47ac4-176"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="47ac4-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
