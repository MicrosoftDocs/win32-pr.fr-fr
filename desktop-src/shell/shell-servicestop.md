---
description: Shell. ServiceStop, méthode-arrête un service nommé.
ms.assetid: AC22C91E-BBC6-4a2e-8D39-F9D7C0AC0947
title: Shell. ServiceStop, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5307fabe79ab9e634ca1e2815c0b90d59b13b1f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104157"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="e4435-103">Shell. ServiceStop, méthode</span><span class="sxs-lookup"><span data-stu-id="e4435-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="e4435-104">Arrête un service nommé.</span><span class="sxs-lookup"><span data-stu-id="e4435-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4435-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4435-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="e4435-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4435-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4435-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4435-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4435-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="e4435-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="e4435-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="e4435-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="e4435-110">*vPersistent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4435-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4435-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="e4435-111">Type: **Variant**</span></span>

<span data-ttu-id="e4435-112">Affectez la valeur **true** pour que le service soit démarré par le gestionnaire de contrôle des services lors de l’appel de [**ServiceStart**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="e4435-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="e4435-113">Pour que la configuration du service reste inchangée, affectez à *vPersistent* la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="e4435-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4435-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e4435-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e4435-115">JScript</span><span class="sxs-lookup"><span data-stu-id="e4435-115">JScript</span></span>

<span data-ttu-id="e4435-116">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="e4435-116">Type: **Variant\***</span></span>

<span data-ttu-id="e4435-117">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e4435-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="e4435-118">VB</span><span class="sxs-lookup"><span data-stu-id="e4435-118">VB</span></span>

<span data-ttu-id="e4435-119">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="e4435-119">Type: **Variant\***</span></span>

<span data-ttu-id="e4435-120">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e4435-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4435-121">Notes </span><span class="sxs-lookup"><span data-stu-id="e4435-121">Remarks</span></span>

<span data-ttu-id="e4435-122">La méthode retourne la **valeur false** si le service a déjà été arrêté.</span><span class="sxs-lookup"><span data-stu-id="e4435-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="e4435-123">Avant d’appeler cette méthode, vous pouvez appeler [**Shell. IsServiceRunning**](./shell-isservicerunning.md) pour déterminer l’état du service.</span><span class="sxs-lookup"><span data-stu-id="e4435-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="e4435-124">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e4435-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="e4435-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="e4435-125">Examples</span></span>

<span data-ttu-id="e4435-126">Les exemples suivants illustrent l’utilisation de **ServiceStop** pour arrêter le service Messenger.</span><span class="sxs-lookup"><span data-stu-id="e4435-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="e4435-127">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="e4435-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="e4435-128">Langage</span><span class="sxs-lookup"><span data-stu-id="e4435-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStop("Messenger", true);
    }
</script>
```



<span data-ttu-id="e4435-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="e4435-129">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStopVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStop("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="e4435-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4435-130">Requirements</span></span>



| <span data-ttu-id="e4435-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4435-131">Requirement</span></span> | <span data-ttu-id="e4435-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4435-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4435-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4435-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e4435-134">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4435-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4435-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4435-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e4435-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4435-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e4435-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4435-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4435-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4435-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e4435-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="e4435-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4435-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4435-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e4435-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e4435-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4435-142"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e4435-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
