---
description: Détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.
ms.assetid: cbb54ae9-02e6-4243-a782-e9f125c21c0d
title: Méthode IShellDispatch2. CanStartStopService (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.CanStartStopService
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 92655c2c561284f00204826e1848a75f00f4a04d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527328"
---
# <a name="ishelldispatch2canstartstopservice-method"></a><span data-ttu-id="3bf95-103">Méthode IShellDispatch2. CanStartStopService</span><span class="sxs-lookup"><span data-stu-id="3bf95-103">IShellDispatch2.CanStartStopService method</span></span>

<span data-ttu-id="3bf95-104">Détermine si l’utilisateur actuel peut démarrer et arrêter le service nommé.</span><span class="sxs-lookup"><span data-stu-id="3bf95-104">Determines if the current user can start and stop the named service.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bf95-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3bf95-105">Syntax</span></span>


```JScript
retVal = IShellDispatch2.CanStartStopService(
  sServiceName
)
```


```VB

IShellDispatch2.CanStartStopService( _
  ByVal sServiceName As String _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="3bf95-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3bf95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bf95-107">*sServiceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3bf95-107">*sServiceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bf95-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3bf95-108">Type: **String**</span></span>

<span data-ttu-id="3bf95-109">**Chaîne** qui contient le nom du service.</span><span class="sxs-lookup"><span data-stu-id="3bf95-109">A **String** that contains the name of the service.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bf95-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3bf95-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="3bf95-111">JScript</span><span class="sxs-lookup"><span data-stu-id="3bf95-111">JScript</span></span>

<span data-ttu-id="3bf95-112">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="3bf95-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="3bf95-113">Retourne _ *true*\* si l’utilisateur peut démarrer et arrêter le service ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="3bf95-113">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

### <a name="vb"></a><span data-ttu-id="3bf95-114">VB</span><span class="sxs-lookup"><span data-stu-id="3bf95-114">VB</span></span>

<span data-ttu-id="3bf95-115">Type : \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="3bf95-115">Type: \**Variant\** _</span></span>

<span data-ttu-id="3bf95-116">Retourne _ *true*\* si l’utilisateur peut démarrer et arrêter le service ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="3bf95-116">Returns _ *true*\* if the user can start and stop the service; otherwise, **false**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bf95-117">Notes</span><span class="sxs-lookup"><span data-stu-id="3bf95-117">Remarks</span></span>

<span data-ttu-id="3bf95-118">Cette méthode est implémentée et accessible par le biais de la méthode [**Shell. CanStartStopService**](./shell-canstartstopservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3bf95-118">This method is implemented and accessed through the [**Shell.CanStartStopService**](./shell-canstartstopservice.md) method.</span></span>

<span data-ttu-id="3bf95-119">Cette méthode n’est pas disponible actuellement dans Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3bf95-119">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="3bf95-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="3bf95-120">Examples</span></span>

<span data-ttu-id="3bf95-121">Les exemples suivants illustrent l’utilisation de **CanStartStopService** pour JScript et VBScript.</span><span class="sxs-lookup"><span data-stu-id="3bf95-121">The following examples show the usage of **CanStartStopService** for JScript and VBScript.</span></span>

<span data-ttu-id="3bf95-122">Langage</span><span class="sxs-lookup"><span data-stu-id="3bf95-122">JScript:</span></span>


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



<span data-ttu-id="3bf95-123">VBScript</span><span class="sxs-lookup"><span data-stu-id="3bf95-123">VBScript:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="3bf95-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3bf95-124">Requirements</span></span>



| <span data-ttu-id="3bf95-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3bf95-125">Requirement</span></span> | <span data-ttu-id="3bf95-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3bf95-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf95-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bf95-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3bf95-128">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3bf95-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3bf95-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3bf95-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3bf95-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3bf95-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3bf95-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3bf95-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3bf95-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bf95-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="3bf95-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="3bf95-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3bf95-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3bf95-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="3bf95-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3bf95-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bf95-136"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="3bf95-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
