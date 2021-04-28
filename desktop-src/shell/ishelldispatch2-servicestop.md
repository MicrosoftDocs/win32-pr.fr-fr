---
description: 'Méthode IShellDispatch2. ServiceStop : arrête un service nommé.'
ms.assetid: f4cd0e2c-4ecc-4e9f-a0b5-d2a8a739f0e2
title: Méthode IShellDispatch2. ServiceStop (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStop
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 651138eb687cfd83406bc6e1a7fcf520ff001171
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117027"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="be72a-103">Méthode IShellDispatch2. ServiceStop</span><span class="sxs-lookup"><span data-stu-id="be72a-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="be72a-104">Arrête un service nommé.</span><span class="sxs-lookup"><span data-stu-id="be72a-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="be72a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be72a-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStop(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStop( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="be72a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="be72a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be72a-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be72a-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be72a-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="be72a-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="be72a-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="be72a-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="be72a-110">*vPersistent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="be72a-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="be72a-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="be72a-111">Type: **Variant**</span></span>

<span data-ttu-id="be72a-112">Affectez la valeur **true** pour que le service soit démarré par le gestionnaire de contrôle des services lors de l’appel de [**ServiceStart**](ishelldispatch2-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="be72a-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="be72a-113">Pour que la configuration du service reste inchangée, affectez à *vPersistent* la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="be72a-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be72a-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="be72a-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="be72a-115">JScript</span><span class="sxs-lookup"><span data-stu-id="be72a-115">JScript</span></span>

<span data-ttu-id="be72a-116">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="be72a-116">Type: **Variant\***</span></span>

<span data-ttu-id="be72a-117">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="be72a-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="be72a-118">VB</span><span class="sxs-lookup"><span data-stu-id="be72a-118">VB</span></span>

<span data-ttu-id="be72a-119">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="be72a-119">Type: **Variant\***</span></span>

<span data-ttu-id="be72a-120">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="be72a-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="be72a-121">Notes </span><span class="sxs-lookup"><span data-stu-id="be72a-121">Remarks</span></span>

<span data-ttu-id="be72a-122">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ServiceStop**](./shell-servicestop.md) .</span><span class="sxs-lookup"><span data-stu-id="be72a-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="be72a-123">La méthode retourne la **valeur false** si le service a déjà été arrêté.</span><span class="sxs-lookup"><span data-stu-id="be72a-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="be72a-124">Avant d’appeler cette méthode, vous pouvez appeler [**Shell. IsServiceRunning**](./shell-isservicerunning.md) pour déterminer l’état du service.</span><span class="sxs-lookup"><span data-stu-id="be72a-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="be72a-125">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="be72a-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="be72a-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="be72a-126">Examples</span></span>

<span data-ttu-id="be72a-127">Les exemples suivants illustrent l’utilisation de **ServiceStop** pour arrêter le service Messenger.</span><span class="sxs-lookup"><span data-stu-id="be72a-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="be72a-128">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="be72a-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="be72a-129">Langage</span><span class="sxs-lookup"><span data-stu-id="be72a-129">JScript:</span></span>


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



<span data-ttu-id="be72a-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="be72a-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="be72a-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be72a-131">Requirements</span></span>



| <span data-ttu-id="be72a-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be72a-132">Requirement</span></span> | <span data-ttu-id="be72a-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="be72a-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be72a-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be72a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="be72a-135">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be72a-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be72a-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="be72a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="be72a-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="be72a-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="be72a-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="be72a-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="be72a-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="be72a-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="be72a-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="be72a-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="be72a-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="be72a-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="be72a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="be72a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be72a-143"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="be72a-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
