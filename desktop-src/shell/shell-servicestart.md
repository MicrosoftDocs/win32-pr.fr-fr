---
description: Démarre un service nommé.
ms.assetid: 72214E80-38A2-4a57-B555-942902BAFC3D
title: Shell. ServiceStart, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8cd3b910306fc995d15e9731823614717450ef55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865261"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="1e501-103">Shell. ServiceStart, méthode</span><span class="sxs-lookup"><span data-stu-id="1e501-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="1e501-104">Démarre un service nommé.</span><span class="sxs-lookup"><span data-stu-id="1e501-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e501-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e501-105">Syntax</span></span>


```JScript
retVal = Shell.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

Shell.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="1e501-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e501-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e501-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e501-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e501-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="1e501-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="1e501-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="1e501-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="1e501-110">*vPersistent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1e501-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e501-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="1e501-111">Type: **Variant**</span></span>

<span data-ttu-id="1e501-112">Affectez la valeur **true** pour que le service démarre automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="1e501-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="1e501-113">Affectez la valeur **false** pour que la configuration du service reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="1e501-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e501-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e501-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1e501-115">JScript</span><span class="sxs-lookup"><span data-stu-id="1e501-115">JScript</span></span>

<span data-ttu-id="1e501-116">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="1e501-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="1e501-117">Retourne _ *true*\* en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="1e501-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="1e501-118">VB</span><span class="sxs-lookup"><span data-stu-id="1e501-118">VB</span></span>

<span data-ttu-id="1e501-119">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="1e501-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="1e501-120">Retourne _ *true*\* en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="1e501-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e501-121">Notes</span><span class="sxs-lookup"><span data-stu-id="1e501-121">Remarks</span></span>

<span data-ttu-id="1e501-122">La méthode retourne la **valeur false** si le service a déjà été démarré.</span><span class="sxs-lookup"><span data-stu-id="1e501-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="1e501-123">Avant d’appeler cette méthode, vous pouvez appeler [**Shell. IsServiceRunning**](./shell-isservicerunning.md) pour déterminer l’état du service.</span><span class="sxs-lookup"><span data-stu-id="1e501-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="1e501-124">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1e501-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="1e501-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="1e501-125">Examples</span></span>

<span data-ttu-id="1e501-126">Les exemples suivants illustrent l’utilisation de **ServiceStart** pour démarrer le service Messenger.</span><span class="sxs-lookup"><span data-stu-id="1e501-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="1e501-127">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="1e501-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="1e501-128">Langage</span><span class="sxs-lookup"><span data-stu-id="1e501-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="1e501-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="1e501-129">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnServiceStartVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ServiceStart("Messenger", true)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="1e501-130">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1e501-130">Requirements</span></span>



| <span data-ttu-id="1e501-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e501-131">Requirement</span></span> | <span data-ttu-id="1e501-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e501-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e501-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e501-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1e501-134">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e501-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e501-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e501-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1e501-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1e501-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1e501-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e501-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e501-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e501-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1e501-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="1e501-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e501-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e501-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1e501-141">DLL</span><span class="sxs-lookup"><span data-stu-id="1e501-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e501-142"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1e501-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
