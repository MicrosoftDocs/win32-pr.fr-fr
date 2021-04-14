---
title: SystemRestoreConfig, classe
description: Fournit des propriétés pour contrôler la fréquence de création de points de restauration planifiée et la quantité d’espace disque consommée sur chaque lecteur.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Restauration du système de la classe SystemRestoreConfig
- Restauration du système de la classe SystemRestoreConfig, Description
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384844"
---
# <a name="systemrestoreconfig-class"></a><span data-ttu-id="6c441-105">SystemRestoreConfig, classe</span><span class="sxs-lookup"><span data-stu-id="6c441-105">SystemRestoreConfig class</span></span>

<span data-ttu-id="6c441-106">Fournit des propriétés pour contrôler la fréquence de création de points de restauration planifiée et la quantité d’espace disque consommée sur chaque lecteur.</span><span class="sxs-lookup"><span data-stu-id="6c441-106">Provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed on each drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c441-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c441-107">Syntax</span></span>

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a><span data-ttu-id="6c441-108">Membres</span><span class="sxs-lookup"><span data-stu-id="6c441-108">Members</span></span>

<span data-ttu-id="6c441-109">La classe **SystemRestoreConfig** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6c441-109">The **SystemRestoreConfig** class has these types of members:</span></span>

-   [<span data-ttu-id="6c441-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6c441-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c441-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6c441-111">Properties</span></span>

<span data-ttu-id="6c441-112">La classe **SystemRestoreConfig** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6c441-112">The **SystemRestoreConfig** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c441-113">**DiskPercent**</span><span class="sxs-lookup"><span data-stu-id="6c441-113">**DiskPercent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c441-114">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c441-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c441-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c441-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c441-116">Quantité maximale d’espace disque sur chaque lecteur qui peut être utilisée par la restauration du système.</span><span class="sxs-lookup"><span data-stu-id="6c441-116">The maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="6c441-117">Cette valeur est spécifiée sous la forme d’un pourcentage de l’espace disque total.</span><span class="sxs-lookup"><span data-stu-id="6c441-117">This value is specified as a percentage of the total drive space.</span></span> <span data-ttu-id="6c441-118">La valeur par défaut est 12 pour cent.</span><span class="sxs-lookup"><span data-stu-id="6c441-118">The default value is 12 percent.</span></span>

<span data-ttu-id="6c441-119">**Windows Vista :** Reçoit une valeur de la Service VSS (VSS).</span><span class="sxs-lookup"><span data-stu-id="6c441-119">**Windows Vista:** Receives a value from the Volume Shadow Copy Service (VSS).</span></span> <span data-ttu-id="6c441-120">Il s’agit de la quantité maximale d’espace disque sur chaque lecteur qui peut être utilisée par la restauration du système.</span><span class="sxs-lookup"><span data-stu-id="6c441-120">This this is the maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="6c441-121">La valeur par défaut est 15% de l’espace disque total ou 30 pour cent de l’espace libre disponible, la valeur la plus petite étant retenue.</span><span class="sxs-lookup"><span data-stu-id="6c441-121">The default value is 15 percent of the total drive space or 30 percent of the available free space, whichever is smaller.</span></span>

</dd> <dt>

<span data-ttu-id="6c441-122">**RPGlobalInterval**</span><span class="sxs-lookup"><span data-stu-id="6c441-122">**RPGlobalInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c441-123">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c441-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c441-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c441-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c441-125">Intervalle de temps absolu auquel les points de contrôle système planifiés sont créés, en secondes.</span><span class="sxs-lookup"><span data-stu-id="6c441-125">The absolute time interval at which scheduled system checkpoints are created, in seconds.</span></span> <span data-ttu-id="6c441-126">La valeur par défaut est 86 400 (24 heures).</span><span class="sxs-lookup"><span data-stu-id="6c441-126">The default value is 86,400 (24 hours).</span></span>

<span data-ttu-id="6c441-127">**Windows Vista :** Reçoit une valeur du planificateur de tâches pour la restauration du système.</span><span class="sxs-lookup"><span data-stu-id="6c441-127">**Windows Vista:** Receives a value from the task scheduler for System Restore.</span></span> <span data-ttu-id="6c441-128">Zéro si la tâche est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6c441-128">Zero if the task is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="6c441-129">**RPLifeInterval**</span><span class="sxs-lookup"><span data-stu-id="6c441-129">**RPLifeInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c441-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c441-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c441-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c441-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c441-132">Intervalle de temps pendant lequel les points de restauration sont conservés, en secondes.</span><span class="sxs-lookup"><span data-stu-id="6c441-132">The time interval for which restore points are preserved, in seconds.</span></span> <span data-ttu-id="6c441-133">Lorsqu’un point de restauration devient antérieur à cet intervalle spécifié, il est supprimé.</span><span class="sxs-lookup"><span data-stu-id="6c441-133">When a restore point becomes older than this specified interval, it is deleted.</span></span> <span data-ttu-id="6c441-134">La limite d’âge par défaut est de 90 jours.</span><span class="sxs-lookup"><span data-stu-id="6c441-134">The default age limit is 90 days.</span></span>

<span data-ttu-id="6c441-135">**Windows Vista :** Reçoit la valeur **UINTMAX**.</span><span class="sxs-lookup"><span data-stu-id="6c441-135">**Windows Vista:** Receives a value of **UINTMAX**.</span></span>

</dd> <dt>

<span data-ttu-id="6c441-136">**RPSessionInterval**</span><span class="sxs-lookup"><span data-stu-id="6c441-136">**RPSessionInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c441-137">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6c441-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6c441-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="6c441-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c441-139">Intervalle de temps pendant lequel les points de contrôle du système planifiés sont créés au cours de la session, en secondes.</span><span class="sxs-lookup"><span data-stu-id="6c441-139">The time interval at which scheduled system checkpoints are created during the session, in seconds.</span></span> <span data-ttu-id="6c441-140">La valeur par défaut est zéro, ce qui indique que la fonctionnalité est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6c441-140">The default value is zero, indicating that the feature is turned off.</span></span>

<span data-ttu-id="6c441-141">**Windows Vista :** Reçoit zéro si la restauration du système est désactivée.</span><span class="sxs-lookup"><span data-stu-id="6c441-141">**Windows Vista:** Receives zero if System Restore is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="6c441-142">Exemples</span><span class="sxs-lookup"><span data-stu-id="6c441-142">Examples</span></span>

<span data-ttu-id="6c441-143">L’exemple de code suivant n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6c441-143">The following sample code is not supported.</span></span> <span data-ttu-id="6c441-144">Utilisez l’outil de ligne de commande Vssadmin.exe pour modifier la taille de l’espace réservé pour le lecteur.</span><span class="sxs-lookup"><span data-stu-id="6c441-144">Use the command-line tool Vssadmin.exe to change the size of reserved drive space.</span></span>

<span data-ttu-id="6c441-145">**Windows XP :** Cet exemple est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="6c441-145">**Windows XP:** This sample is supported.</span></span>


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a><span data-ttu-id="6c441-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c441-146">Requirements</span></span>



| <span data-ttu-id="6c441-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c441-147">Requirement</span></span> | <span data-ttu-id="6c441-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c441-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6c441-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c441-149">Minimum supported client</span></span><br/> | <span data-ttu-id="6c441-150">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c441-150">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6c441-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c441-151">Minimum supported server</span></span><br/> | <span data-ttu-id="6c441-152">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c441-152">None supported</span></span><br/>                                                         |
| <span data-ttu-id="6c441-153">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6c441-153">Namespace</span></span><br/>                | <span data-ttu-id="6c441-154">Racine \\ par défaut</span><span class="sxs-lookup"><span data-stu-id="6c441-154">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="6c441-155">MOF</span><span class="sxs-lookup"><span data-stu-id="6c441-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c441-156"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c441-156"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c441-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c441-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c441-158">Points de restauration</span><span class="sxs-lookup"><span data-stu-id="6c441-158">Restore Points</span></span>](restore-points.md)
</dt> <dt>

[<span data-ttu-id="6c441-159">Windows Management Instrumentation</span><span class="sxs-lookup"><span data-stu-id="6c441-159">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

