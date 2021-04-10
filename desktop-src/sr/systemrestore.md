---
title: SystemRestore, classe
description: Fournit des méthodes pour désactiver et activer la surveillance, répertorier les points de restauration disponibles et initialiser une restauration sur le système local.
ms.assetid: 87216a56-6d40-44ea-a1ab-d43590b639a4
keywords:
- Restauration du système de la classe SystemRestore
- Restauration du système de la classe SystemRestore, Description
topic_type:
- apiref
api_name:
- SystemRestore
- SystemRestore.Description
- SystemRestore.RestorePointType
- SystemRestore.EventType
- SystemRestore.SequenceNumber
- SystemRestore.CreationTime
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64d2b609a7a49a9b319c15745600aa54193350e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032983"
---
# <a name="systemrestore-class"></a><span data-ttu-id="226ec-105">SystemRestore, classe</span><span class="sxs-lookup"><span data-stu-id="226ec-105">SystemRestore class</span></span>

<span data-ttu-id="226ec-106">Fournit des méthodes pour désactiver et activer la surveillance, répertorier les points de restauration disponibles et initialiser une restauration sur le système local.</span><span class="sxs-lookup"><span data-stu-id="226ec-106">Provides methods for disabling and enabling monitoring, listing available restore points, and initiating a restore on the local system.</span></span>

## <a name="syntax"></a><span data-ttu-id="226ec-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="226ec-107">Syntax</span></span>

``` syntax
class SystemRestore
{
  String Description;
  uint32 RestorePointType;
  uint32 EventType;
  uint32 SequenceNumber;
  String CreationTime;
};
```

## <a name="members"></a><span data-ttu-id="226ec-108">Membres</span><span class="sxs-lookup"><span data-stu-id="226ec-108">Members</span></span>

<span data-ttu-id="226ec-109">La classe **SystemRestore** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="226ec-109">The **SystemRestore** class has these types of members:</span></span>

-   [<span data-ttu-id="226ec-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="226ec-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="226ec-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="226ec-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="226ec-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="226ec-112">Methods</span></span>

<span data-ttu-id="226ec-113">La classe **SystemRestore** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="226ec-113">The **SystemRestore** class has these methods.</span></span>



| <span data-ttu-id="226ec-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="226ec-114">Method</span></span>                                                             | <span data-ttu-id="226ec-115">Description</span><span class="sxs-lookup"><span data-stu-id="226ec-115">Description</span></span>                                                 |
|:-------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="226ec-116">**CreateRestorePoint**</span><span class="sxs-lookup"><span data-stu-id="226ec-116">**CreateRestorePoint**</span></span>](createrestorepoint-systemrestore.md)     | <span data-ttu-id="226ec-117">Crée un point de restauration.</span><span class="sxs-lookup"><span data-stu-id="226ec-117">Creates a restore point.</span></span><br/>                         |
| [<span data-ttu-id="226ec-118">**Désactiver**</span><span class="sxs-lookup"><span data-stu-id="226ec-118">**Disable**</span></span>](disable-systemrestore.md)                           | <span data-ttu-id="226ec-119">Désactive la surveillance sur un lecteur particulier.</span><span class="sxs-lookup"><span data-stu-id="226ec-119">Disables monitoring on a particular drive.</span></span><br/>       |
| [<span data-ttu-id="226ec-120">**Activer**</span><span class="sxs-lookup"><span data-stu-id="226ec-120">**Enable**</span></span>](enable-systemrestore.md)                             | <span data-ttu-id="226ec-121">Active la surveillance sur un lecteur particulier.</span><span class="sxs-lookup"><span data-stu-id="226ec-121">Enables monitoring on a particular drive.</span></span><br/>        |
| [<span data-ttu-id="226ec-122">**GetLastRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="226ec-122">**GetLastRestoreStatus**</span></span>](getlastrestorestatus-systemrestore.md) | <span data-ttu-id="226ec-123">Récupère l’état de la dernière restauration du système.</span><span class="sxs-lookup"><span data-stu-id="226ec-123">Retrieves the status of the last system restore.</span></span><br/> |
| [<span data-ttu-id="226ec-124">**Restaurer**</span><span class="sxs-lookup"><span data-stu-id="226ec-124">**Restore**</span></span>](restore-systemrestore.md)                           | <span data-ttu-id="226ec-125">Lance une restauration du système.</span><span class="sxs-lookup"><span data-stu-id="226ec-125">Initiates a system restore.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="226ec-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="226ec-126">Properties</span></span>

<span data-ttu-id="226ec-127">La classe **SystemRestore** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="226ec-127">The **SystemRestore** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="226ec-128">**CreationTime**</span><span class="sxs-lookup"><span data-stu-id="226ec-128">**CreationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="226ec-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="226ec-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="226ec-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="226ec-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="226ec-131">Heure à laquelle le changement d’État s’est produit.</span><span class="sxs-lookup"><span data-stu-id="226ec-131">The time at which the state change occurred.</span></span>

</dd> <dt>

<span data-ttu-id="226ec-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="226ec-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="226ec-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="226ec-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="226ec-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="226ec-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="226ec-135">Description à afficher pour permettre à l’utilisateur d’identifier facilement un point de restauration.</span><span class="sxs-lookup"><span data-stu-id="226ec-135">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="226ec-136">La longueur maximale d’une chaîne ANSI est la valeur \_ desc max.</span><span class="sxs-lookup"><span data-stu-id="226ec-136">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="226ec-137">La longueur maximale d’une chaîne Unicode est le nombre maximal de \_ desc \_ W.</span><span class="sxs-lookup"><span data-stu-id="226ec-137">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="226ec-138">Pour plus d’informations, consultez [texte de description du point de restauration](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="226ec-138">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="226ec-139">**EventType**</span><span class="sxs-lookup"><span data-stu-id="226ec-139">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="226ec-140">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="226ec-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="226ec-141">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="226ec-141">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="226ec-142">Type de l'événement.</span><span class="sxs-lookup"><span data-stu-id="226ec-142">The type of event.</span></span> <span data-ttu-id="226ec-143">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="226ec-143">This member can be one of the following values.</span></span>



| <span data-ttu-id="226ec-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="226ec-144">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="226ec-145">Signification</span><span class="sxs-lookup"><span data-stu-id="226ec-145">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="226ec-146"><dt>**Commencer \_ \_ \_ Modification système imbriquée**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="226ec-146"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="226ec-147">Une modification du système a commencé.</span><span class="sxs-lookup"><span data-stu-id="226ec-147">A system change has begun.</span></span> <span data-ttu-id="226ec-148">Un appel imbriqué suivant ne crée pas de nouveau point de restauration.</span><span class="sxs-lookup"><span data-stu-id="226ec-148">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="226ec-149">Les appels suivants doivent utiliser la fin du \_ \_ \_ changement de système imbriqué, pas la modification du système de fin \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="226ec-149">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="226ec-150"><dt>**Commencer \_ \_Modification système**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="226ec-150"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="226ec-151">Une modification du système a commencé.</span><span class="sxs-lookup"><span data-stu-id="226ec-151">A system change has begun.</span></span><br/>                                                                                                                                                           |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="226ec-152"><dt>**Fin \_ \_ \_ Modification système imbriquée**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="226ec-152"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="226ec-153">Une modification du système s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="226ec-153">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="226ec-154"><dt>**Fin \_ \_Modification système**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="226ec-154"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="226ec-155">Une modification du système s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="226ec-155">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="226ec-156">**RestorePointType**</span><span class="sxs-lookup"><span data-stu-id="226ec-156">**RestorePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="226ec-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="226ec-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="226ec-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="226ec-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="226ec-159">Type de point de restauration.</span><span class="sxs-lookup"><span data-stu-id="226ec-159">The type of restore point.</span></span> <span data-ttu-id="226ec-160">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="226ec-160">This member can be one of the following values.</span></span>



| <span data-ttu-id="226ec-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="226ec-161">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="226ec-162">Signification</span><span class="sxs-lookup"><span data-stu-id="226ec-162">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="226ec-163"><dt>**Application \_ INSTALLER**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="226ec-163"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="226ec-164">Une application a été installée.</span><span class="sxs-lookup"><span data-stu-id="226ec-164">An application has been installed.</span></span><br/>                                                                                                                 |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="226ec-165"><dt>**Application \_ Désinstaller**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="226ec-165"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="226ec-166">Une application a été désinstallée.</span><span class="sxs-lookup"><span data-stu-id="226ec-166">An application has been uninstalled.</span></span><br/>                                                                                                               |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="226ec-167"><dt>**Annulé \_ OPÉRATION**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="226ec-167"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="226ec-168">Une application doit supprimer le point de restauration créé.</span><span class="sxs-lookup"><span data-stu-id="226ec-168">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="226ec-169">Par exemple, une application utilise cet indicateur lorsqu’un utilisateur annule une installation.</span><span class="sxs-lookup"><span data-stu-id="226ec-169">For example, an application would use this flag when a user cancels an installation.</span></span> <br/> |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="226ec-170"><dt>**Appareil mobile \_ \_Installation du pilote**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="226ec-170"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="226ec-171">Un pilote de périphérique a été installé.</span><span class="sxs-lookup"><span data-stu-id="226ec-171">A device driver has been installed.</span></span><br/>                                                                                                                |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="226ec-172"><dt>**Modifier \_ PARAMÈTRES**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="226ec-172"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="226ec-173">Des fonctionnalités ont été ajoutées ou supprimées pour une application.</span><span class="sxs-lookup"><span data-stu-id="226ec-173">An application has had features added or removed.</span></span><br/>                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="226ec-174">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="226ec-174">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="226ec-175">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="226ec-175">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="226ec-176">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="226ec-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="226ec-177">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="226ec-177">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="226ec-178">Numéro de séquence du point de restauration.</span><span class="sxs-lookup"><span data-stu-id="226ec-178">The sequence number of the restore point.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="226ec-179">Notes</span><span class="sxs-lookup"><span data-stu-id="226ec-179">Remarks</span></span>

<span data-ttu-id="226ec-180">Vous pouvez obtenir une liste de points de restauration à l’aide de la méthode [**SWbemServices. InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) pour récupérer une collection d’objets **SystemRestore** .</span><span class="sxs-lookup"><span data-stu-id="226ec-180">You can obtain a list of restore points by using the [**SWbemServices.InstancesOf**](/windows/desktop/WmiSdk/swbemservices-instancesof) method to retrieve a collection of **SystemRestore** objects.</span></span> <span data-ttu-id="226ec-181">Vous pouvez utiliser les propriétés de la classe pour identifier le point de restauration.</span><span class="sxs-lookup"><span data-stu-id="226ec-181">You can use the class properties to identify the restore point.</span></span>

## <a name="examples"></a><span data-ttu-id="226ec-182">Exemples</span><span class="sxs-lookup"><span data-stu-id="226ec-182">Examples</span></span>

<span data-ttu-id="226ec-183">L’exemple de script suivant énumère les points de restauration actuels.</span><span class="sxs-lookup"><span data-stu-id="226ec-183">The following sample script enumerates the current restore points.</span></span>


```VB
'SystemRestore Class
'Provides methods for disabling and enabling monitoring, 
'listing available restore points, and initiating a 
'restore on the local system.

Set RPSet = GetObject("winmgmts:root/default").InstancesOf ("SystemRestore")
for each RP in RPSet
    wscript.Echo "Dir: RP" & RP.SequenceNumber & ", Name: " & RP.Description & ", Type: ", RP.RestorePointType & ", Time: " & RP.CreationTime
next
```



## <a name="requirements"></a><span data-ttu-id="226ec-184">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="226ec-184">Requirements</span></span>



| <span data-ttu-id="226ec-185">Condition requise</span><span class="sxs-lookup"><span data-stu-id="226ec-185">Requirement</span></span> | <span data-ttu-id="226ec-186">Valeur</span><span class="sxs-lookup"><span data-stu-id="226ec-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="226ec-187">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="226ec-187">Minimum supported client</span></span><br/> | <span data-ttu-id="226ec-188">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="226ec-188">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="226ec-189">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="226ec-189">Minimum supported server</span></span><br/> | <span data-ttu-id="226ec-190">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="226ec-190">None supported</span></span><br/>                                                         |
| <span data-ttu-id="226ec-191">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="226ec-191">Namespace</span></span><br/>                | <span data-ttu-id="226ec-192">Racine \\ par défaut</span><span class="sxs-lookup"><span data-stu-id="226ec-192">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="226ec-193">MOF</span><span class="sxs-lookup"><span data-stu-id="226ec-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="226ec-194"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="226ec-194"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="226ec-195">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="226ec-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="226ec-196">Windows Management Instrumentation</span><span class="sxs-lookup"><span data-stu-id="226ec-196">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

