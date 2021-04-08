---
title: Méthode Restore de la classe SystemRestore
description: Lance une restauration du système.
ms.assetid: ca4aa97b-fa59-407d-b127-951d46932c33
keywords:
- Restaurer la méthode restauration du système
- Restore, méthode restauration du système, classe SystemRestore
- Restauration du système de la classe SystemRestore, méthode Restore
topic_type:
- apiref
api_name:
- SystemRestore.Restore
api_location:
- Root\\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b7747b710801718d9b169c8999c51dd30cefde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740309"
---
# <a name="restore-method-of-the-systemrestore-class"></a><span data-ttu-id="e7f40-106">Méthode Restore de la classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="e7f40-106">Restore method of the SystemRestore class</span></span>

<span data-ttu-id="e7f40-107">Lance une restauration du système.</span><span class="sxs-lookup"><span data-stu-id="e7f40-107">Initiates a system restore.</span></span> <span data-ttu-id="e7f40-108">L’appelant doit forcer un redémarrage du système.</span><span class="sxs-lookup"><span data-stu-id="e7f40-108">The caller must force a system reboot.</span></span> <span data-ttu-id="e7f40-109">La restauration réelle se produit lors du redémarrage.</span><span class="sxs-lookup"><span data-stu-id="e7f40-109">The actual restoration occurs during the reboot.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f40-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7f40-110">Syntax</span></span>


```mof
uint32 Restore(
  [in] uint32 SequenceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="e7f40-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7f40-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f40-112"> N \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f40-112">*SequenceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f40-113">Numéro de séquence du point de restauration.</span><span class="sxs-lookup"><span data-stu-id="e7f40-113">The sequence number of the restore point.</span></span> <span data-ttu-id="e7f40-114">Pour déterminer le numéro de séquence d’un point de restauration spécifique, énumérez tous les points de restauration sur le système.</span><span class="sxs-lookup"><span data-stu-id="e7f40-114">To determine the sequence number for a specific restore point, enumerate all restore points on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f40-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7f40-115">Return value</span></span>

<span data-ttu-id="e7f40-116">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7f40-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e7f40-117">Sinon, la méthode retourne l’un des codes d’erreur COM définis dans WinError. h.</span><span class="sxs-lookup"><span data-stu-id="e7f40-117">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="examples"></a><span data-ttu-id="e7f40-118">Exemples</span><span class="sxs-lookup"><span data-stu-id="e7f40-118">Examples</span></span>


```VB
'Restore Method of the SystemRestore Class
'Initiates a system restore. The caller must 
'force a system reboot. The actual restoration 
'occurs during the reboot.
Set Args = wscript.Arguments
RpNum = Args.item(0)
Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")
if obj.Restore(RpNum) <> 0 Then
    wscript.Echo "Restore failed"
End If
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
for each OpSys in OpSysSet
    OpSys.Reboot()
next
```



## <a name="requirements"></a><span data-ttu-id="e7f40-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7f40-119">Requirements</span></span>



| <span data-ttu-id="e7f40-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7f40-120">Requirement</span></span> | <span data-ttu-id="e7f40-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7f40-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e7f40-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f40-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7f40-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7f40-123">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e7f40-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f40-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7f40-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7f40-125">None supported</span></span><br/>                                                         |
| <span data-ttu-id="e7f40-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e7f40-126">Namespace</span></span><br/>                | <span data-ttu-id="e7f40-127">Racine \\ \\ par défaut</span><span class="sxs-lookup"><span data-stu-id="e7f40-127">Root\\\\Default</span></span><br/>                                                        |
| <span data-ttu-id="e7f40-128">MOF</span><span class="sxs-lookup"><span data-stu-id="e7f40-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7f40-129"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7f40-129"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7f40-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f40-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f40-131">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="e7f40-131">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





