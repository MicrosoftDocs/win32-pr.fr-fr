---
description: Méthode Shell. ServiceStart-démarre un service nommé.
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
ms.openlocfilehash: 9c88b1980d215ad088a4a24362f17147b5d6e432
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083747"
---
# <a name="shellservicestart-method"></a><span data-ttu-id="960d4-103">Shell. ServiceStart, méthode</span><span class="sxs-lookup"><span data-stu-id="960d4-103">Shell.ServiceStart method</span></span>

<span data-ttu-id="960d4-104">Démarre un service nommé.</span><span class="sxs-lookup"><span data-stu-id="960d4-104">Starts a named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="960d4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="960d4-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="960d4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="960d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="960d4-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="960d4-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="960d4-108">Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="960d4-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="960d4-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="960d4-109">A **String** that contains the name of the service.</span></span>

</dd> <dt>

<span data-ttu-id="960d4-110">*vPersistent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="960d4-110">*vPersistent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="960d4-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="960d4-111">Type: **Variant**</span></span>

<span data-ttu-id="960d4-112">Affectez la valeur **true** pour que le service démarre automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="960d4-112">Set to **true** to have the service started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="960d4-113">Affectez la valeur **false** pour que la configuration du service reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="960d4-113">Set to **false** to leave the service configuration unchanged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="960d4-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="960d4-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="960d4-115">JScript</span><span class="sxs-lookup"><span data-stu-id="960d4-115">JScript</span></span>

<span data-ttu-id="960d4-116">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="960d4-116">Type: **Variant\***</span></span>

<span data-ttu-id="960d4-117">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="960d4-117">Returns **true** if successful; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="960d4-118">VB</span><span class="sxs-lookup"><span data-stu-id="960d4-118">VB</span></span>

<span data-ttu-id="960d4-119">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="960d4-119">Type: **Variant\***</span></span>

<span data-ttu-id="960d4-120">Retourne la **valeur true** en cas de réussite ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="960d4-120">Returns **true** if successful; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="960d4-121">Notes </span><span class="sxs-lookup"><span data-stu-id="960d4-121">Remarks</span></span>

<span data-ttu-id="960d4-122">La méthode retourne la **valeur false** si le service a déjà été démarré.</span><span class="sxs-lookup"><span data-stu-id="960d4-122">The method returns **false** if the service has already been started.</span></span> <span data-ttu-id="960d4-123">Avant d’appeler cette méthode, vous pouvez appeler [**Shell. IsServiceRunning**](./shell-isservicerunning.md) pour déterminer l’état du service.</span><span class="sxs-lookup"><span data-stu-id="960d4-123">Before calling this method, you can call [**Shell.IsServiceRunning**](./shell-isservicerunning.md) to ascertain the status of the service.</span></span>

<span data-ttu-id="960d4-124">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="960d4-124">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="960d4-125">Exemples</span><span class="sxs-lookup"><span data-stu-id="960d4-125">Examples</span></span>

<span data-ttu-id="960d4-126">Les exemples suivants illustrent l’utilisation de **ServiceStart** pour démarrer le service Messenger.</span><span class="sxs-lookup"><span data-stu-id="960d4-126">The following examples show the use of **ServiceStart** to start the Messenger service.</span></span> <span data-ttu-id="960d4-127">L’utilisation est indiquée pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="960d4-127">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="960d4-128">Langage</span><span class="sxs-lookup"><span data-stu-id="960d4-128">JScript:</span></span>


```JScript
<script language="JScript">
    function fnServiceStartJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ServiceStart("Messenger", true);
    }
```



<span data-ttu-id="960d4-129">VBScript</span><span class="sxs-lookup"><span data-stu-id="960d4-129">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="960d4-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="960d4-130">Requirements</span></span>



| <span data-ttu-id="960d4-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="960d4-131">Requirement</span></span> | <span data-ttu-id="960d4-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="960d4-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="960d4-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="960d4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="960d4-134">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="960d4-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="960d4-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="960d4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="960d4-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="960d4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="960d4-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="960d4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="960d4-138"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="960d4-138"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="960d4-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="960d4-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="960d4-140"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="960d4-140"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="960d4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="960d4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="960d4-142"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="960d4-142"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
