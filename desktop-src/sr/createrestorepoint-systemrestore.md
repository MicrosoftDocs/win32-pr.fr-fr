---
title: Méthode CreateRestorePoint de la classe SystemRestore
description: Crée un point de restauration.
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- Restauration du système de méthode CreateRestorePoint
- Restauration du système de méthode CreateRestorePoint, classe SystemRestore
- Restauration du système de la classe SystemRestore, méthode CreateRestorePoint
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465594"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a><span data-ttu-id="34d33-106">Méthode CreateRestorePoint de la classe SystemRestore</span><span class="sxs-lookup"><span data-stu-id="34d33-106">CreateRestorePoint method of the SystemRestore class</span></span>

<span data-ttu-id="34d33-107">Crée un point de restauration.</span><span class="sxs-lookup"><span data-stu-id="34d33-107">Creates a restore point.</span></span>

<span data-ttu-id="34d33-108">Cette méthode est l’équivalent scriptable de la fonction [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) .</span><span class="sxs-lookup"><span data-stu-id="34d33-108">This method is the scriptable equivalent of the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d33-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34d33-109">Syntax</span></span>


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a><span data-ttu-id="34d33-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34d33-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34d33-111">*Description* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34d33-111">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34d33-112">Description à afficher pour permettre à l’utilisateur d’identifier facilement un point de restauration.</span><span class="sxs-lookup"><span data-stu-id="34d33-112">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="34d33-113">La longueur maximale d’une chaîne ANSI est la valeur \_ desc max.</span><span class="sxs-lookup"><span data-stu-id="34d33-113">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="34d33-114">La longueur maximale d’une chaîne Unicode est le nombre maximal de \_ desc \_ W.</span><span class="sxs-lookup"><span data-stu-id="34d33-114">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="34d33-115">Pour plus d’informations, consultez [texte de description du point de restauration](restore-point-description-text.md).</span><span class="sxs-lookup"><span data-stu-id="34d33-115">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="34d33-116">*RestorePointType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34d33-116">*RestorePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34d33-117">Type de point de restauration.</span><span class="sxs-lookup"><span data-stu-id="34d33-117">The type of restore point.</span></span> <span data-ttu-id="34d33-118">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="34d33-118">This member can be one of the following values.</span></span>



| <span data-ttu-id="34d33-119">Type de point de restauration</span><span class="sxs-lookup"><span data-stu-id="34d33-119">Restore point type</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="34d33-120">Signification</span><span class="sxs-lookup"><span data-stu-id="34d33-120">Meaning</span></span>                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="34d33-121"><dt>**Application \_ INSTALLER**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="34d33-121"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="34d33-122">Une application a été installée.</span><span class="sxs-lookup"><span data-stu-id="34d33-122">An application has been installed.</span></span><br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="34d33-123"><dt>**Application \_ Désinstaller**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="34d33-123"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="34d33-124">Une application a été désinstallée.</span><span class="sxs-lookup"><span data-stu-id="34d33-124">An application has been uninstalled.</span></span><br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="34d33-125"><dt>**Appareil mobile \_ \_Installation du pilote**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="34d33-125"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="34d33-126">Un pilote de périphérique a été installé.</span><span class="sxs-lookup"><span data-stu-id="34d33-126">A device driver has been installed.</span></span><br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="34d33-127"><dt>**Modifier \_ PARAMÈTRES**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="34d33-127"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="34d33-128">Des fonctionnalités ont été ajoutées ou supprimées pour une application.</span><span class="sxs-lookup"><span data-stu-id="34d33-128">An application has had features added or removed.</span></span><br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="34d33-129"><dt>**Annulé \_ OPÉRATION**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="34d33-129"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="34d33-130">Une application doit supprimer le point de restauration créé.</span><span class="sxs-lookup"><span data-stu-id="34d33-130">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="34d33-131">Par exemple, une application utilise cet indicateur lorsqu’un utilisateur annule une installation.</span><span class="sxs-lookup"><span data-stu-id="34d33-131">For example, an application would use this flag when a user cancels an installation.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="34d33-132">*EventType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="34d33-132">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34d33-133">Type de l'événement.</span><span class="sxs-lookup"><span data-stu-id="34d33-133">The type of event.</span></span> <span data-ttu-id="34d33-134">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="34d33-134">This member can be one of the following values.</span></span>



| <span data-ttu-id="34d33-135">Type d'événement</span><span class="sxs-lookup"><span data-stu-id="34d33-135">Event type</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="34d33-136">Signification</span><span class="sxs-lookup"><span data-stu-id="34d33-136">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="34d33-137"><dt>**Commencer \_ \_ \_ Modification système imbriquée**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="34d33-137"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="34d33-138">Une modification du système a commencé.</span><span class="sxs-lookup"><span data-stu-id="34d33-138">A system change has begun.</span></span> <span data-ttu-id="34d33-139">Un appel imbriqué suivant ne crée pas de nouveau point de restauration.</span><span class="sxs-lookup"><span data-stu-id="34d33-139">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="34d33-140">Les appels suivants doivent utiliser la fin du \_ \_ \_ changement de système imbriqué, pas la modification du système de fin \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="34d33-140">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="34d33-141"><dt>**Commencer \_ \_Modification système**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="34d33-141"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="34d33-142">Une modification du système a commencé.</span><span class="sxs-lookup"><span data-stu-id="34d33-142">A system change has begun.</span></span> <br/> <span data-ttu-id="34d33-143">Un appel suivant doit utiliser la \_ modification du système \_ de fin, et non une \_ modification du système imbriquée \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="34d33-143">A subsequent call must use END\_SYSTEM\_CHANGE, not END\_NESTED\_SYSTEM\_CHANGE.</span></span><br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="34d33-144"><dt>**Fin \_ \_ \_ Modification système imbriquée**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="34d33-144"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="34d33-145">Une modification du système s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="34d33-145">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="34d33-146"><dt>**Fin \_ \_Modification système**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="34d33-146"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="34d33-147">Une modification du système s’est terminée.</span><span class="sxs-lookup"><span data-stu-id="34d33-147">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34d33-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34d33-148">Return value</span></span>

<span data-ttu-id="34d33-149">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="34d33-149">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="34d33-150">Sinon, la méthode retourne l’un des codes d’erreur COM définis dans WinError. h.</span><span class="sxs-lookup"><span data-stu-id="34d33-150">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="34d33-151">Notes</span><span class="sxs-lookup"><span data-stu-id="34d33-151">Remarks</span></span>

<span data-ttu-id="34d33-152">\* \* Windows 8 : \* \*</span><span class="sxs-lookup"><span data-stu-id="34d33-152">\*\*Windows 8:  \*\*</span></span>

<span data-ttu-id="34d33-153">Une nouvelle clé de registre permet aux développeurs d’applications de modifier la fréquence de création du point de restauration.</span><span class="sxs-lookup"><span data-stu-id="34d33-153">A new registry key enables application developers to change the frequency of restore-point creation.</span></span>

<span data-ttu-id="34d33-154">Les applications doivent créer cette clé pour l’utiliser, car elle n’est pas préexistante dans le système.</span><span class="sxs-lookup"><span data-stu-id="34d33-154">Applications should create this key to use it because it will not preexist in the system.</span></span> <span data-ttu-id="34d33-155">Les éléments suivants s’appliquent par défaut si la clé n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="34d33-155">The following will apply by default if the key does not exist.</span></span> <span data-ttu-id="34d33-156">Si une application appelle la méthode **CreateRestorePoint** pour créer un point de restauration, Windows ignore la création de ce nouveau point de restauration si des points de restauration ont été créés au cours des dernières 24 heures.</span><span class="sxs-lookup"><span data-stu-id="34d33-156">If an application calls the **CreateRestorePoint** method to create a restore point, Windows skips creating this new restore point if any restore points have been created in the last 24 hours.</span></span> <span data-ttu-id="34d33-157">La méthode **CreateRestorePoint** retourne **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="34d33-157">The **CreateRestorePoint** method returns **S\_OK**.</span></span>

<span data-ttu-id="34d33-158">Les développeurs peuvent écrire des applications qui créent la valeur **DWORD** **SystemRestorePointCreationFrequency** sous la clé de Registre **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore**.</span><span class="sxs-lookup"><span data-stu-id="34d33-158">Developers can write applications that create the **DWORD** value **SystemRestorePointCreationFrequency** under the registry key **HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\SystemRestore**.</span></span> <span data-ttu-id="34d33-159">La valeur de cette clé de Registre peut modifier la fréquence de création du point de restauration.</span><span class="sxs-lookup"><span data-stu-id="34d33-159">The value of this registry key can change the frequency of restore point creation.</span></span> <span data-ttu-id="34d33-160">La valeur de cette clé de Registre peut modifier la fréquence de création du point de restauration.</span><span class="sxs-lookup"><span data-stu-id="34d33-160">The value of this registry key can change the frequency of restore point creation.</span></span>

<span data-ttu-id="34d33-161">Si l’application appelle **CreateRestorePoint** pour créer un point de restauration et que la valeur de la clé de Registre est 0, la restauration du système n’ignore pas la création du nouveau point de restauration.</span><span class="sxs-lookup"><span data-stu-id="34d33-161">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is 0, system restore does not skip creating the new restore point.</span></span>

<span data-ttu-id="34d33-162">Si l’application appelle **CreateRestorePoint** pour créer un point de restauration et que la valeur de la clé de Registre est l’entier N, la restauration du système ignore la création d’un nouveau point de restauration si des points de restauration ont été créés au cours des N minutes précédentes.</span><span class="sxs-lookup"><span data-stu-id="34d33-162">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is the integer N, system restore skips creating a new restore point if any restore points were created in the previous N minutes.</span></span>

## <a name="examples"></a><span data-ttu-id="34d33-163">Exemples</span><span class="sxs-lookup"><span data-stu-id="34d33-163">Examples</span></span>


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="34d33-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34d33-164">Requirements</span></span>



| <span data-ttu-id="34d33-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34d33-165">Requirement</span></span> | <span data-ttu-id="34d33-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="34d33-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="34d33-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34d33-167">Minimum supported client</span></span><br/> | <span data-ttu-id="34d33-168">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34d33-168">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="34d33-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34d33-169">Minimum supported server</span></span><br/> | <span data-ttu-id="34d33-170">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="34d33-170">None supported</span></span><br/>                                                         |
| <span data-ttu-id="34d33-171">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="34d33-171">Namespace</span></span><br/>                | <span data-ttu-id="34d33-172">Racine \\ par défaut</span><span class="sxs-lookup"><span data-stu-id="34d33-172">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="34d33-173">MOF</span><span class="sxs-lookup"><span data-stu-id="34d33-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34d33-174"><dt>SR. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34d33-174"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34d33-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34d33-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d33-176">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="34d33-176">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





