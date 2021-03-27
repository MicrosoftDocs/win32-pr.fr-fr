---
description: Démarre un service nommé.
ms.assetid: 3af57cdc-f449-433d-a9e1-119038045e4c
title: Méthode IShellDispatch2. ServiceStart (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ServiceStart
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 508b4f1c05625acdaed2b5a235ee697cceb544c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972386"
---
# <a name="ishelldispatch2servicestart-method"></a><span data-ttu-id="b650c-103">Méthode IShellDispatch2. ServiceStart</span><span class="sxs-lookup"><span data-stu-id="b650c-103">IShellDispatch2.ServiceStart method</span></span>

<span data-ttu-id="b650c-104">Démarre un service nommé.</span><span class="sxs-lookup"><span data-stu-id="b650c-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="b650c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b650c-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.ServiceStart(
  sServiceName,
  vPersistent
)
```


```VB

IShellDispatch2.ServiceStart( _
  ByVal sServiceName As BSTR, _
  ByVal vPersistent As Variant _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="b650c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b650c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b650c-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b650c-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b650c-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="b650c-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="b650c-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="b650c-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="b650c-110">*vPersistent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b650c-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b650c-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="b650c-111">Type: **Variant**</span></span>

<span data-ttu-id="b650c-112">Affectez la valeur **true** pour que le service démarre automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="b650c-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="b650c-113">Affectez la valeur **false** pour que la configuration du service reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="b650c-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b650c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b650c-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b650c-115">JScript</span><span class="sxs-lookup"><span data-stu-id="b650c-115">JScript</span></span>

<span data-ttu-id="b650c-116">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="b650c-116">Type: \**Variant\** _</span></span>

<span data-ttu-id="b650c-117">Retourne _ *true*\* en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="b650c-117">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="b650c-118">VB</span><span class="sxs-lookup"><span data-stu-id="b650c-118">VB</span></span>

<span data-ttu-id="b650c-119">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="b650c-119">Type: \**Variant\** _</span></span>

<span data-ttu-id="b650c-120">Retourne _ *true*\* en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="b650c-120">Returns _ *true*\* if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b650c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="b650c-121">Remarks</span></span>

<span data-ttu-id="b650c-122">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. ServiceStart**](./shell-servicestart.md) .</span><span class="sxs-lookup"><span data-stu-id="b650c-122">This method is implemented and accessed through the [**Shell.ServiceStart**](./shell-servicestart.md) method.</span></span>

<span data-ttu-id="b650c-123">La méthode retourne la **valeur false** si le service a déjà été démarré.</span><span class="sxs-lookup"><span data-stu-id="b650c-123">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="b650c-124">Avant d’appeler cette méthode, vous pouvez appeler [**Shell. IsServiceRunning**](./shell-isservicerunning.md) pour déterminer l’état du service.</span><span class="sxs-lookup"><span data-stu-id="b650c-124">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="b650c-125">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b650c-125">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="b650c-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="b650c-126">Examples</span></span>

<span data-ttu-id="b650c-127">Les exemples suivants illustrent l’utilisation de **ServiceStart** pour démarrer le service Messenger.</span><span class="sxs-lookup"><span data-stu-id="b650c-127">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="b650c-128">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="b650c-128">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="b650c-129">Langage</span><span class="sxs-lookup"><span data-stu-id="b650c-129">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
</script>
```



<span data-ttu-id="b650c-130">VBScript</span><span class="sxs-lookup"><span data-stu-id="b650c-130">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="b650c-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b650c-131">Requirements</span></span>



| <span data-ttu-id="b650c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b650c-132">Requirement</span></span> | <span data-ttu-id="b650c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b650c-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b650c-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b650c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b650c-135">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b650c-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b650c-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b650c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b650c-137">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b650c-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b650c-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="b650c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="b650c-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b650c-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b650c-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="b650c-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b650c-141"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b650c-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b650c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="b650c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b650c-143"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b650c-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
