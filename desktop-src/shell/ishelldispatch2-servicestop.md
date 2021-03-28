---
description: Arrête un service nommé.
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
ms.openlocfilehash: 6a4a76c1f53309c14875eeaf6f3f4c0839a511bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972382"
---
# <a name="ishelldispatch2servicestop-method"></a><span data-ttu-id="e4eab-103">Méthode IShellDispatch2. ServiceStop</span><span class="sxs-lookup"><span data-stu-id="e4eab-103">IShellDispatch2.ServiceStop method</span></span>

<span data-ttu-id="e4eab-104">Arrête un service nommé.</span><span class="sxs-lookup"><span data-stu-id="e4eab-104">Stops a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4eab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4eab-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="e4eab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4eab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4eab-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4eab-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4eab-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="e4eab-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="e4eab-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="e4eab-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="e4eab-110">*vPersistent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4eab-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4eab-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="e4eab-111">Type: **Variant**</span></span>

<span data-ttu-id="e4eab-112">Affectez la valeur **true** pour que le service soit démarré par le gestionnaire de contrôle des services lors de l’appel de [**ServiceStart**](ishelldispatch2-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="e4eab-112">Set to **true** to have the service started by the service control manager when [**ServiceStart**](ishelldispatch2-servicestart.md) is called.</span></span> <span data-ttu-id="e4eab-113">Pour que la configuration du service reste inchangée, affectez à *vPersistent* la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="e4eab-113">To leave the service configuration unchanged, set *vPersistent* to **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4eab-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4eab-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="e4eab-115">JScript</span><span class="sxs-lookup"><span data-stu-id="e4eab-115">JScript</span></span>

<span data-ttu-id="e4eab-116">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="e4eab-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="e4eab-117">Retourne _ *true*\* en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e4eab-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="e4eab-118">VB</span><span class="sxs-lookup"><span data-stu-id="e4eab-118">VB</span></span>

<span data-ttu-id="e4eab-119">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="e4eab-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="e4eab-120">Retourne _ *true*\* en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e4eab-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4eab-121">Notes</span><span class="sxs-lookup"><span data-stu-id="e4eab-121">Remarks</span></span>

<span data-ttu-id="e4eab-122">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ServiceStop**](./shell-servicestop.md) .</span><span class="sxs-lookup"><span data-stu-id="e4eab-122">This method is implemented and accessed through the [**Shell.ServiceStop**](./shell-servicestop.md) method.</span></span>

<span data-ttu-id="e4eab-123">La méthode retourne la **valeur false** si le service a déjà été arrêté.</span><span class="sxs-lookup"><span data-stu-id="e4eab-123">The method returns **false** if the service has already been stopped.</span></span> <span data-ttu-id="e4eab-124">Avant d’appeler cette méthode, vous pouvez appeler [**Shell. IsServiceRunning**](./shell-isservicerunning.md) pour déterminer l’état du service.</span><span class="sxs-lookup"><span data-stu-id="e4eab-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="e4eab-125">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e4eab-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="e4eab-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="e4eab-126">Examples</span></span>

<span data-ttu-id="e4eab-127">Les exemples suivants illustrent l’utilisation de **ServiceStop** pour arrêter le service Messenger.</span><span class="sxs-lookup"><span data-stu-id="e4eab-127">The following examples show the use of **ServiceStop** to stop the Messenger service.</span></span> <span data-ttu-id="e4eab-128">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="e4eab-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="e4eab-129">Langage</span><span class="sxs-lookup"><span data-stu-id="e4eab-129">JScript:</span></span>


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



<span data-ttu-id="e4eab-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="e4eab-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="e4eab-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e4eab-131">Requirements</span></span>



| <span data-ttu-id="e4eab-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4eab-132">Requirement</span></span> | <span data-ttu-id="e4eab-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4eab-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4eab-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4eab-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e4eab-135">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4eab-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e4eab-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4eab-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e4eab-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4eab-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e4eab-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4eab-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4eab-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4eab-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="e4eab-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="e4eab-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4eab-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4eab-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="e4eab-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e4eab-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4eab-143"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e4eab-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
