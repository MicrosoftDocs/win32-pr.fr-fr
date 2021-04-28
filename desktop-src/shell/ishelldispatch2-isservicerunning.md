---
description: IShellDispatch2. IsServiceRunning, méthode-retourne une valeur qui indique si un service particulier est en cours d’exécution.
ms.assetid: 91f3fba1-7aa5-423a-bc37-49db230c79db
title: Méthode IShellDispatch2. IsServiceRunning (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e8ad792f1669a8ebcfa411c58b34da214ccf69a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117087"
---
# <a name="ishelldispatch2isservicerunning-method"></a><span data-ttu-id="2476f-103">Méthode IShellDispatch2. IsServiceRunning</span><span class="sxs-lookup"><span data-stu-id="2476f-103">IShellDispatch2.IsServiceRunning method</span></span>

<span data-ttu-id="2476f-104">Retourne une valeur qui indique si un service particulier est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2476f-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="2476f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2476f-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.IsServiceRunning(
  sServiceName
)
```


```VB

IShellDispatch2.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="2476f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2476f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2476f-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2476f-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2476f-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="2476f-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="2476f-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="2476f-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2476f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2476f-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="2476f-111">JScript</span><span class="sxs-lookup"><span data-stu-id="2476f-111">JScript</span></span>

<span data-ttu-id="2476f-112">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="2476f-112">Type: **Variant\***</span></span>

<span data-ttu-id="2476f-113">Retourne la **valeur true** si le service spécifié par *sServiceName* est en cours d’exécution ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="2476f-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="2476f-114">VB</span><span class="sxs-lookup"><span data-stu-id="2476f-114">VB</span></span>

<span data-ttu-id="2476f-115">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="2476f-115">Type: **Variant\***</span></span>

<span data-ttu-id="2476f-116">Retourne la **valeur true** si le service spécifié par *sServiceName* est en cours d’exécution ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="2476f-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2476f-117">Notes </span><span class="sxs-lookup"><span data-stu-id="2476f-117">Remarks</span></span>

<span data-ttu-id="2476f-118">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. IsServiceRunning**](./shell-isservicerunning.md) .</span><span class="sxs-lookup"><span data-stu-id="2476f-118">This method is implemented and accessed through the [**Shell.IsServiceRunning**](./shell-isservicerunning.md) method.</span></span>

<span data-ttu-id="2476f-119">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2476f-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="2476f-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="2476f-120">Examples</span></span>

<span data-ttu-id="2476f-121">Les exemples suivants illustrent l’utilisation de **IsServiceRunning** pour déterminer si le service themes est en cours d’exécution pour une application.</span><span class="sxs-lookup"><span data-stu-id="2476f-121">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="2476f-122">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="2476f-122">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="2476f-123">Langage</span><span class="sxs-lookup"><span data-stu-id="2476f-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsServiceRunningJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
    
        bReturn = objShell.IsServiceRunning("Themes");
    }
</script>
```



<span data-ttu-id="2476f-124">VBScript</span><span class="sxs-lookup"><span data-stu-id="2476f-124">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsServiceRunningVB()
        dim objShell
        dim bReturn
    
        set objShell = CreateObject("shell.application")
    
        bReturn = objShell.IsServiceRunning("Themes")
    
        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="2476f-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2476f-125">Requirements</span></span>



| <span data-ttu-id="2476f-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2476f-126">Requirement</span></span> | <span data-ttu-id="2476f-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2476f-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2476f-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2476f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2476f-129">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2476f-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2476f-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2476f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2476f-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2476f-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2476f-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="2476f-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2476f-133"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2476f-133"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2476f-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="2476f-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2476f-135"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2476f-135"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2476f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2476f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2476f-137"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="2476f-137"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
