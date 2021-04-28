---
description: 'Shell. CanStartStopService, méthode : détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.'
ms.assetid: 1428F529-61F6-4113-A553-2C0D617FD859
title: Shell. CanStartStopService, méthode (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 29561519b95329093ef1f7bfc64023fd1ac4533d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083687"
---
# <a name="shellcanstartstopservice-method"></a><span data-ttu-id="57257-103">Shell. CanStartStopService, méthode</span><span class="sxs-lookup"><span data-stu-id="57257-103">Shell.CanStartStopService method</span></span>

<span data-ttu-id="57257-104">Détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.</span><span class="sxs-lookup"><span data-stu-id="57257-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="57257-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57257-105">Syntax</span></span>


```JScript
retVal = Shell.CanStartStopService(
  sServiceName
)
```


```VB

Shell.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="57257-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57257-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57257-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="57257-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57257-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="57257-108">Type: **String**</span></span>

<span data-ttu-id="57257-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="57257-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57257-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57257-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="57257-111">JScript</span><span class="sxs-lookup"><span data-stu-id="57257-111">JScript</span></span>

<span data-ttu-id="57257-112">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="57257-112">Type: **Variant\***</span></span>

<span data-ttu-id="57257-113">Retourne la **valeur true** si l’utilisateur peut démarrer et arrêter le service ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="57257-113">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="57257-114">VB</span><span class="sxs-lookup"><span data-stu-id="57257-114">VB</span></span>

<span data-ttu-id="57257-115">Type : **variante \***</span><span class="sxs-lookup"><span data-stu-id="57257-115">Type: **Variant\***</span></span>

<span data-ttu-id="57257-116">Retourne la **valeur true** si l’utilisateur peut démarrer et arrêter le service ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="57257-116">Returns **true** if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="57257-117">Notes </span><span class="sxs-lookup"><span data-stu-id="57257-117">Remarks</span></span>

<span data-ttu-id="57257-118">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="57257-118">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="57257-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="57257-119">Examples</span></span>

<span data-ttu-id="57257-120">Les exemples suivants illustrent l’utilisation de **CanStartStopService** pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="57257-120">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="57257-121">Langage</span><span class="sxs-lookup"><span data-stu-id="57257-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCanStartStopServiceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;

        bReturn = objShell.CanStartStopService("service name");
    }
</script>
```



<span data-ttu-id="57257-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="57257-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCanStartStopServiceVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.CanStartStopService("service name")

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="57257-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57257-123">Requirements</span></span>



| <span data-ttu-id="57257-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57257-124">Requirement</span></span> | <span data-ttu-id="57257-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="57257-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57257-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57257-126">Minimum supported client</span></span><br/> | <span data-ttu-id="57257-127">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57257-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="57257-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="57257-128">Minimum supported server</span></span><br/> | <span data-ttu-id="57257-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="57257-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="57257-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="57257-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="57257-131"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="57257-131"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="57257-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="57257-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="57257-133"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="57257-133"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="57257-134">DLL</span><span class="sxs-lookup"><span data-stu-id="57257-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57257-135"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="57257-135"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




