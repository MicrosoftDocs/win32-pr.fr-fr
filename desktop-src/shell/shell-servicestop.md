---
description: Arrête un service nommé.
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
ms.openlocfilehash: 31388078fe1c0e15c2e54efc86f0ff76bcfb7ed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203438"
---
# <a name="shellservicestop-method"></a><span data-ttu-id="fe949-103">Shell. ServiceStop, méthode</span><span class="sxs-lookup"><span data-stu-id="fe949-103">Shell.ServiceStop method</span></span>

<span data-ttu-id="fe949-104">Arrête un service nommé.</span><span class="sxs-lookup"><span data-stu-id="fe949-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe949-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe949-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="fe949-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe949-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe949-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe949-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe949-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="fe949-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="fe949-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="fe949-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="fe949-110">*vPersistent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fe949-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe949-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="fe949-111">Type: **Variant**</span></span>

<span data-ttu-id="fe949-112">Affectez la valeur **true** pour que le service soit démarré par le gestionnaire de contrôle des services lors de l’appel de [**ServiceStart**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="fe949-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](./shell-servicestart.md) is called.</span></span> <span data-ttu-id="fe949-113">Pour que la configuration du service reste inchangée, affectez à *vPersistent* la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="fe949-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe949-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe949-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="fe949-115">JScript</span><span class="sxs-lookup"><span data-stu-id="fe949-115">JScript</span></span>

<span data-ttu-id="fe949-116">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="fe949-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="fe949-117">Retourne _ *true*\* en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="fe949-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="fe949-118">VB</span><span class="sxs-lookup"><span data-stu-id="fe949-118">VB</span></span>

<span data-ttu-id="fe949-119">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="fe949-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="fe949-120">Retourne _ *true*\* en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="fe949-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe949-121">Notes</span><span class="sxs-lookup"><span data-stu-id="fe949-121">Remarks</span></span>

<span data-ttu-id="fe949-122">La méthode retourne la **valeur false** si le service a déjà été arrêté.</span><span class="sxs-lookup"><span data-stu-id="fe949-122">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="fe949-123">Avant d’appeler cette méthode, vous pouvez appeler [**Shell. IsServiceRunning**](./shell-isservicerunning.md) pour déterminer l’état du service.</span><span class="sxs-lookup"><span data-stu-id="fe949-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="fe949-124">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="fe949-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="fe949-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="fe949-125">Examples</span></span>

<span data-ttu-id="fe949-126">Les exemples suivants illustrent l’utilisation de **ServiceStop** pour arrêter le service Messenger.</span><span class="sxs-lookup"><span data-stu-id="fe949-126">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="fe949-127">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="fe949-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="fe949-128">Langage</span><span class="sxs-lookup"><span data-stu-id="fe949-128">JScript:</span></span>


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



<span data-ttu-id="fe949-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="fe949-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="fe949-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fe949-130">Requirements</span></span>



| <span data-ttu-id="fe949-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe949-131">Requirement</span></span> | <span data-ttu-id="fe949-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe949-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe949-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe949-133">Minimum supported client</span></span><br/> | <span data-ttu-id="fe949-134">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe949-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe949-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fe949-135">Minimum supported server</span></span><br/> | <span data-ttu-id="fe949-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fe949-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fe949-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="fe949-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe949-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe949-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fe949-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="fe949-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fe949-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fe949-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fe949-141">DLL</span><span class="sxs-lookup"><span data-stu-id="fe949-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe949-142"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="fe949-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
