---
title: Activer la méthode de la classe SystemRestore
description: Active la surveillance sur un lecteur particulier.
ms.assetid: f3140f6d-d190-46a4-8587-c2e928ac8ecf
keywords:
- Activer la restauration du système de méthode
- Activer la restauration du système de la méthode, classe SystemRestore
- Restauration du système de la classe SystemRestore, activer la méthode
topic_type:
- apiref
api_name:
- SystemRestore.Enable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090aa01b4028a7146ea1d7f271ba4390f43ca260
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510144"
---
# <a name="enable-method-of-the-systemrestore-class"></a><span data-ttu-id="06601-106">Activer la méthode de la classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="06601-106">Enable method of the SystemRestore class</span></span>

<span data-ttu-id="06601-107">Active la surveillance sur un lecteur particulier.</span><span class="sxs-lookup"><span data-stu-id="06601-107">Enables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="06601-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06601-108">Syntax</span></span>


```mof
uint32 Enable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="06601-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06601-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06601-110">*Lecteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="06601-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06601-111">Lecteur à activer.</span><span class="sxs-lookup"><span data-stu-id="06601-111">The drive to be enabled.</span></span> <span data-ttu-id="06601-112">La chaîne de lecteur doit se présenter sous la forme « C : \\ ».</span><span class="sxs-lookup"><span data-stu-id="06601-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="06601-113">Si ce paramètre est le lecteur système ou une chaîne vide (""), tous les lecteurs sont analysés.</span><span class="sxs-lookup"><span data-stu-id="06601-113">If this parameter is the system drive or an empty string (""), all drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06601-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06601-114">Return value</span></span>

<span data-ttu-id="06601-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="06601-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="06601-116">Sinon, la méthode retourne l’un des codes d’erreur COM définis dans WinError. h.</span><span class="sxs-lookup"><span data-stu-id="06601-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="06601-117">Notes</span><span class="sxs-lookup"><span data-stu-id="06601-117">Remarks</span></span>

<span data-ttu-id="06601-118">La méthode **Enable** n’attend pas l’activation complète de l’analyse avant son retour, car cela peut prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="06601-118">The **Enable** method does not wait for monitoring to be enabled completely before it returns, because this could take a while.</span></span> <span data-ttu-id="06601-119">Au lieu de cela, elle est retournée immédiatement après le démarrage du service de restauration du système et du pilote de filtre.</span><span class="sxs-lookup"><span data-stu-id="06601-119">Instead, it returns immediately after starting the System Restore service and filter driver.</span></span>

<span data-ttu-id="06601-120">Pour activer la restauration du système sur un lecteur non-système, vous devez d’abord activer la restauration du système sur le lecteur système.</span><span class="sxs-lookup"><span data-stu-id="06601-120">To enable System Restore on a non-system drive, you must first enable System Restore on the system drive.</span></span>

<span data-ttu-id="06601-121">Cette méthode échoue en mode sans échec.</span><span class="sxs-lookup"><span data-stu-id="06601-121">This method fails in safe mode.</span></span>

## <a name="examples"></a><span data-ttu-id="06601-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="06601-122">Examples</span></span>


```VB
'Enable Method of the SystemRestore Class
'Enables monitoring on a particular drive.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else 
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
If (obj.Enable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="06601-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06601-123">Requirements</span></span>



| <span data-ttu-id="06601-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06601-124">Requirement</span></span> | <span data-ttu-id="06601-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="06601-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="06601-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06601-126">Minimum supported client</span></span><br/> | <span data-ttu-id="06601-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="06601-127">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="06601-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06601-128">Minimum supported server</span></span><br/> | <span data-ttu-id="06601-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="06601-129">None supported</span></span><br/>                                                         |
| <span data-ttu-id="06601-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="06601-130">Namespace</span></span><br/>                | <span data-ttu-id="06601-131">Racine \\ par défaut</span><span class="sxs-lookup"><span data-stu-id="06601-131">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="06601-132">MOF</span><span class="sxs-lookup"><span data-stu-id="06601-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06601-133"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06601-133"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06601-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06601-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06601-135">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="06601-135">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





