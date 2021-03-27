---
description: Retourne une valeur qui indique si un service particulier est en cours d’exécution.
ms.assetid: FDC41C2D-7462-458f-BBE6-D97260C26B6C
title: Shell. IsServiceRunning, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.IsServiceRunning
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3a65be4955c6f49e8e6baa49cd9dedb82fc5cc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865262"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="4dc31-103">Shell. IsServiceRunning, méthode</span><span class="sxs-lookup"><span data-stu-id="4dc31-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="4dc31-104">Retourne une valeur qui indique si un service particulier est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="4dc31-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dc31-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4dc31-105">Syntax</span></span>


```JScript
retVal = Shell.IsServiceRunning(
  sServiceName
)
```


```VB

Shell.IsServiceRunning( _
  ByVal sServiceName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="4dc31-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4dc31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4dc31-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4dc31-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4dc31-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="4dc31-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="4dc31-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="4dc31-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4dc31-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4dc31-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="4dc31-111">JScript</span><span class="sxs-lookup"><span data-stu-id="4dc31-111">JScript</span></span>

<span data-ttu-id="4dc31-112">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="4dc31-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="4dc31-113">Retourne _ *true*\* si le service spécifié par *sServiceName* est en cours d’exécution ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="4dc31-113">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="4dc31-114">VB</span><span class="sxs-lookup"><span data-stu-id="4dc31-114">VB</span></span>

<span data-ttu-id="4dc31-115">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="4dc31-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="4dc31-116">Retourne _ *true*\* si le service spécifié par *sServiceName* est en cours d’exécution ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="4dc31-116">Returns _ *true*\* if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dc31-117">Notes</span><span class="sxs-lookup"><span data-stu-id="4dc31-117">Remarks</span></span>

<span data-ttu-id="4dc31-118">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4dc31-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="4dc31-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="4dc31-119">Examples</span></span>

<span data-ttu-id="4dc31-120">Les exemples suivants illustrent l’utilisation de **IsServiceRunning** pour déterminer si le service themes est en cours d’exécution pour une application.</span><span class="sxs-lookup"><span data-stu-id="4dc31-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="4dc31-121">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="4dc31-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="4dc31-122">Langage</span><span class="sxs-lookup"><span data-stu-id="4dc31-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="4dc31-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="4dc31-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="4dc31-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4dc31-124">Requirements</span></span>



| <span data-ttu-id="4dc31-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4dc31-125">Requirement</span></span> | <span data-ttu-id="4dc31-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4dc31-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dc31-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4dc31-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4dc31-128">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4dc31-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4dc31-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4dc31-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4dc31-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4dc31-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4dc31-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="4dc31-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dc31-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dc31-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="4dc31-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="4dc31-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4dc31-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4dc31-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="4dc31-135">DLL</span><span class="sxs-lookup"><span data-stu-id="4dc31-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dc31-136"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="4dc31-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
