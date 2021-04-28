---
description: Shell. IsServiceRunning, méthode-retourne une valeur qui indique si un service particulier est en cours d’exécution.
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
ms.openlocfilehash: 01af900bb7930ec7b6dde0b0700c83f211733dc3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083717"
---
# <a name="shellisservicerunning-method"></a><span data-ttu-id="32746-103">Shell. IsServiceRunning, méthode</span><span class="sxs-lookup"><span data-stu-id="32746-103">Shell.IsServiceRunning method</span></span>

<span data-ttu-id="32746-104">Retourne une valeur qui indique si un service particulier est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="32746-104">Returns a value that indicates whether a particular service is running.</span></span>

## <a name="syntax"></a><span data-ttu-id="32746-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32746-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="32746-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32746-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32746-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="32746-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32746-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="32746-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="32746-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="32746-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32746-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="32746-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="32746-111">JScript</span><span class="sxs-lookup"><span data-stu-id="32746-111">JScript</span></span>

<span data-ttu-id="32746-112">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="32746-112">Type: **Variant\***</span></span>

<span data-ttu-id="32746-113">Retourne la **valeur true** si le service spécifié par *sServiceName* est en cours d’exécution ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="32746-113">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="32746-114">VB</span><span class="sxs-lookup"><span data-stu-id="32746-114">VB</span></span>

<span data-ttu-id="32746-115">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="32746-115">Type: **Variant\***</span></span>

<span data-ttu-id="32746-116">Retourne la **valeur true** si le service spécifié par *sServiceName* est en cours d’exécution ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="32746-116">Returns **true** if the service specified by *sServiceName* is running; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="32746-117">Notes </span><span class="sxs-lookup"><span data-stu-id="32746-117">Remarks</span></span>

<span data-ttu-id="32746-118">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="32746-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="32746-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="32746-119">Examples</span></span>

<span data-ttu-id="32746-120">Les exemples suivants illustrent l’utilisation de **IsServiceRunning** pour déterminer si le service themes est en cours d’exécution pour une application.</span><span class="sxs-lookup"><span data-stu-id="32746-120">The following examples show the use of **IsServiceRunning** to determine whether the Themes service is running for an application.</span></span> <span data-ttu-id="32746-121">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="32746-121">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="32746-122">Langage</span><span class="sxs-lookup"><span data-stu-id="32746-122">JScript:</span></span>


```JScript
function fnIsServiceRunningJ()
{
    var objShell = new ActiveXObject("shell.application");
    var bReturn;

    bReturn = objShell.IsServiceRunning("Themes");
}
```



<span data-ttu-id="32746-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="32746-123">VBScript:</span></span>


```VB
function fnIsServiceRunningVB()
    dim objShell
    dim bReturn

    set objShell = CreateObject("shell.application")

    bReturn = objShell.IsServiceRunning("Themes")

    set objShell = nothing
end function
```



## <a name="requirements"></a><span data-ttu-id="32746-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32746-124">Requirements</span></span>



| <span data-ttu-id="32746-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32746-125">Requirement</span></span> | <span data-ttu-id="32746-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="32746-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32746-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32746-127">Minimum supported client</span></span><br/> | <span data-ttu-id="32746-128">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32746-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32746-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32746-129">Minimum supported server</span></span><br/> | <span data-ttu-id="32746-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32746-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="32746-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="32746-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="32746-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="32746-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="32746-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="32746-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32746-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32746-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="32746-135">DLL</span><span class="sxs-lookup"><span data-stu-id="32746-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32746-136"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="32746-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
