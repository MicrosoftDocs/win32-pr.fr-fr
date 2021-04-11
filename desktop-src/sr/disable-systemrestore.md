---
title: Désactivation de la méthode de la classe SystemRestore
description: Désactive la surveillance sur un lecteur particulier.
ms.assetid: 2ad37dd4-7d80-4697-9dbb-abb329a34ff7
keywords:
- Désactiver la restauration du système de méthode
- Désactiver la restauration du système de la méthode, classe SystemRestore
- Restauration du système de la classe SystemRestore, désactivation de la méthode
topic_type:
- apiref
api_name:
- SystemRestore.Disable
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19556833684aeab0cc126eff7aff0a258335c8e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104062"
---
# <a name="disable-method-of-the-systemrestore-class"></a><span data-ttu-id="37b88-106">Désactivation de la méthode de la classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="37b88-106">Disable method of the SystemRestore class</span></span>

<span data-ttu-id="37b88-107">Désactive la surveillance sur un lecteur particulier.</span><span class="sxs-lookup"><span data-stu-id="37b88-107">Disables monitoring on a particular drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="37b88-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37b88-108">Syntax</span></span>


```mof
uint32 Disable(
  [in] String Drive
);
```



## <a name="parameters"></a><span data-ttu-id="37b88-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37b88-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37b88-110">*Lecteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37b88-110">*Drive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37b88-111">Lecteur à désactiver.</span><span class="sxs-lookup"><span data-stu-id="37b88-111">The drive to be disabled.</span></span> <span data-ttu-id="37b88-112">La chaîne de lecteur doit se présenter sous la forme « C : \\ ».</span><span class="sxs-lookup"><span data-stu-id="37b88-112">The drive string should be of the form "C:\\".</span></span> <span data-ttu-id="37b88-113">Si ce paramètre est le lecteur système ou une chaîne vide (""), aucun lecteur n’est analysé.</span><span class="sxs-lookup"><span data-stu-id="37b88-113">If this parameter is the system drive or an empty string (""), no drives are monitored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37b88-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="37b88-114">Return value</span></span>

<span data-ttu-id="37b88-115">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="37b88-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="37b88-116">Sinon, la méthode retourne l’un des codes d’erreur COM définis dans WinError. h.</span><span class="sxs-lookup"><span data-stu-id="37b88-116">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="37b88-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="37b88-117">Examples</span></span>


```VB
'Disable Method of the SystemRestore Class
'Disables monitoring on a particular drive.
Set Args = wscript.Arguments
If Args.Count() > 0 Then
    Drive = Args.item(0)
Else
    Drive = ""
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.Disable(Drive)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="37b88-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37b88-118">Requirements</span></span>



| <span data-ttu-id="37b88-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37b88-119">Requirement</span></span> | <span data-ttu-id="37b88-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="37b88-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="37b88-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37b88-121">Minimum supported client</span></span><br/> | <span data-ttu-id="37b88-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37b88-122">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="37b88-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37b88-123">Minimum supported server</span></span><br/> | <span data-ttu-id="37b88-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="37b88-124">None supported</span></span><br/>                                                         |
| <span data-ttu-id="37b88-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37b88-125">Namespace</span></span><br/>                | <span data-ttu-id="37b88-126">Racine \\ par défaut</span><span class="sxs-lookup"><span data-stu-id="37b88-126">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="37b88-127">MOF</span><span class="sxs-lookup"><span data-stu-id="37b88-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37b88-128"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37b88-128"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37b88-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37b88-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37b88-130">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="37b88-130">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





