---
description: Indique si la confirmation d’un utilisateur physiquement présent est requise pour une opération de présence physique donnée.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Win32_Tpm :: GetPhysicalPresenceConfirmationStatus, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952370"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a><span data-ttu-id="de64f-103">Win32 \_ TPM :: GetPhysicalPresenceConfirmationStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="de64f-103">Win32\_Tpm::GetPhysicalPresenceConfirmationStatus method</span></span>

<span data-ttu-id="de64f-104">Indique si la confirmation d’un utilisateur physiquement présent est requise pour une opération de présence physique donnée.</span><span class="sxs-lookup"><span data-stu-id="de64f-104">Indicates if confirmation from a physically present user is required for a given physical presence operation.</span></span>

<span data-ttu-id="de64f-105">Cette méthode est accessible uniquement par les administrateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="de64f-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="de64f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de64f-106">Syntax</span></span>


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="de64f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de64f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de64f-108">*Opération* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="de64f-108">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de64f-109">Valeur entière qui spécifie l’opération TPM demandée qui requiert une présence physique.</span><span class="sxs-lookup"><span data-stu-id="de64f-109">An integer value that specifies the requested TPM operation that requires physical presence.</span></span> <span data-ttu-id="de64f-110">Les commandes spécifiques au fournisseur sont également prises en charge.</span><span class="sxs-lookup"><span data-stu-id="de64f-110">Vendor specific commands are supported as well.</span></span>

<span data-ttu-id="de64f-111">Le paramètre d' *opération* peut comprendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="de64f-111">The *Operation* parameter may consist of the following values.</span></span>



| <span data-ttu-id="de64f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="de64f-112">Value</span></span>                                                                                                                               | <span data-ttu-id="de64f-113">Signification</span><span class="sxs-lookup"><span data-stu-id="de64f-113">Meaning</span></span>                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="de64f-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-114"><dt>1</dt></span></span> </dl>                                                        | <span data-ttu-id="de64f-115">Activer</span><span class="sxs-lookup"><span data-stu-id="de64f-115">Enable</span></span><br/>                                        |
| <dl> <span data-ttu-id="de64f-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-116"><dt>2</dt></span></span> </dl>                                                        | <span data-ttu-id="de64f-117">Désactiver</span><span class="sxs-lookup"><span data-stu-id="de64f-117">Disable</span></span><br/>                                       |
| <dl> <span data-ttu-id="de64f-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-118"><dt>3</dt></span></span> </dl>                                                        | <span data-ttu-id="de64f-119">Activer</span><span class="sxs-lookup"><span data-stu-id="de64f-119">Activate</span></span><br/>                                      |
| <dl> <span data-ttu-id="de64f-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-120"><dt>4</dt></span></span> </dl>                                                        | <span data-ttu-id="de64f-121">Désactivation</span><span class="sxs-lookup"><span data-stu-id="de64f-121">Deactivate</span></span><br/>                                    |
| <dl> <span data-ttu-id="de64f-122"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-122"><dt>5</dt></span></span> </dl>                                                        | <span data-ttu-id="de64f-123">Effacer</span><span class="sxs-lookup"><span data-stu-id="de64f-123">Clear</span></span><br/>                                         |
| <dl> <span data-ttu-id="de64f-124"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-124"><dt>6</dt></span></span> </dl>                                                        | <span data-ttu-id="de64f-125">Activer + activer</span><span class="sxs-lookup"><span data-stu-id="de64f-125">Enable + Activate</span></span><br/>                             |
| <dl> <span data-ttu-id="de64f-126"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-126"><dt>7</dt></span></span> </dl>                                                        | <span data-ttu-id="de64f-127">Désactiver + désactiver</span><span class="sxs-lookup"><span data-stu-id="de64f-127">Deactivate + Disable</span></span><br/>                          |
| <dl> <span data-ttu-id="de64f-128"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-128"><dt>8</dt></span></span> </dl>                                                        | <span data-ttu-id="de64f-129">SetOwnerInstall \_ true</span><span class="sxs-lookup"><span data-stu-id="de64f-129">SetOwnerInstall\_True</span></span><br/>                         |
| <dl> <span data-ttu-id="de64f-130"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-130"><dt>9</dt></span></span> </dl>                                                        | <span data-ttu-id="de64f-131">SetOwnerInstall \_ false</span><span class="sxs-lookup"><span data-stu-id="de64f-131">SetOwnerInstall\_False</span></span><br/>                        |
| <dl> <span data-ttu-id="de64f-132"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-132"><dt>10</dt></span></span> </dl>                                                       | <span data-ttu-id="de64f-133">Enable + Activate + SetOwnerInstall \_ true</span><span class="sxs-lookup"><span data-stu-id="de64f-133">Enable + Activate + SetOwnerInstall\_True</span></span><br/>     |
| <dl> <span data-ttu-id="de64f-134"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-134"><dt>11</dt></span></span> </dl>                                                       | <span data-ttu-id="de64f-135">SetOwnerInstall \_ false + Deactivate + Disable</span><span class="sxs-lookup"><span data-stu-id="de64f-135">SetOwnerInstall\_False + Deactivate + Disable</span></span><br/> |
| <dl> <span data-ttu-id="de64f-136"><dt></dt><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-136"><dt></dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="de64f-137">PresenceunownedFieldUpgrade physique différé</span><span class="sxs-lookup"><span data-stu-id="de64f-137">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> |
| <dl> <span data-ttu-id="de64f-138"><dt></dt><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-138"><dt></dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="de64f-139">Clear + activer + activer</span><span class="sxs-lookup"><span data-stu-id="de64f-139">Clear + Enable + Activate</span></span><br/>                     |
| <dl> <span data-ttu-id="de64f-140"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-140"><dt>15</dt></span></span> </dl>                                                       | <span data-ttu-id="de64f-141">SetNoPPIProvision \_ false</span><span class="sxs-lookup"><span data-stu-id="de64f-141">SetNoPPIProvision\_False</span></span><br/>                      |
| <dl> <span data-ttu-id="de64f-142"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-142"><dt>16</dt></span></span> </dl>                                                       | <span data-ttu-id="de64f-143">SetNoPPIProvision \_ true</span><span class="sxs-lookup"><span data-stu-id="de64f-143">SetNoPPIProvision\_True</span></span><br/>                       |
| <dl> <span data-ttu-id="de64f-144"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-144"><dt>17</dt></span></span> </dl>                                                       | <span data-ttu-id="de64f-145">SetNoPPIClear \_ false</span><span class="sxs-lookup"><span data-stu-id="de64f-145">SetNoPPIClear\_False</span></span><br/>                          |
| <dl> <span data-ttu-id="de64f-146"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-146"><dt>18</dt></span></span> </dl>                                                       | <span data-ttu-id="de64f-147">SetNoPPIClear \_ true</span><span class="sxs-lookup"><span data-stu-id="de64f-147">SetNoPPIClear\_True</span></span><br/>                           |
| <dl> <span data-ttu-id="de64f-148"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-148"><dt>19</dt></span></span> </dl>                                                       | <span data-ttu-id="de64f-149">SetNoPPIMaintenance \_ false</span><span class="sxs-lookup"><span data-stu-id="de64f-149">SetNoPPIMaintenance\_False</span></span><br/>                    |
| <dl> <span data-ttu-id="de64f-150"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-150"><dt>20</dt></span></span> </dl>                                                       | <span data-ttu-id="de64f-151">SetNoPPIMaintenance \_ true</span><span class="sxs-lookup"><span data-stu-id="de64f-151">SetNoPPIMaintenance\_True</span></span><br/>                     |
| <dl> <span data-ttu-id="de64f-152"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-152"><dt>21</dt></span></span> </dl>                                                       | <span data-ttu-id="de64f-153">Activer + activer + effacer</span><span class="sxs-lookup"><span data-stu-id="de64f-153">Enable + Activate + Clear</span></span><br/>                     |
| <dl> <span data-ttu-id="de64f-154"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-154"><dt>22</dt></span></span> </dl>                                                       | <span data-ttu-id="de64f-155">Activer + activer + effacer + activer + activer</span><span class="sxs-lookup"><span data-stu-id="de64f-155">Enable + Activate + Clear + Enable + Activate</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="de64f-156">*ConfirmationStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="de64f-156">*ConfirmationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="de64f-157">Retourne l’état de confirmation de la commande de présence physique.</span><span class="sxs-lookup"><span data-stu-id="de64f-157">Returns the confirmation status for physical presence command.</span></span>

<span data-ttu-id="de64f-158">Le paramètre *ConfirmationStatus* peut contenir les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="de64f-158">The *ConfirmationStatus* parameter may consist of the following values.</span></span>



| <span data-ttu-id="de64f-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="de64f-159">Value</span></span>                                                                        | <span data-ttu-id="de64f-160">Signification</span><span class="sxs-lookup"><span data-stu-id="de64f-160">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="de64f-161"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-161"><dt>0</dt></span></span> </dl> | <span data-ttu-id="de64f-162">Non implémenté</span><span class="sxs-lookup"><span data-stu-id="de64f-162">Not implemented</span></span><br/>                                             |
| <dl> <span data-ttu-id="de64f-163"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-163"><dt>1</dt></span></span> </dl> | <span data-ttu-id="de64f-164">BIOS uniquement.</span><span class="sxs-lookup"><span data-stu-id="de64f-164">BIOS only.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="de64f-165"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-165"><dt>2</dt></span></span> </dl> | <span data-ttu-id="de64f-166">Bloqué pour le système d’exploitation par la configuration du BIOS.</span><span class="sxs-lookup"><span data-stu-id="de64f-166">Blocked for the operating system by the BIOS configuration.</span></span><br/> |
| <dl> <span data-ttu-id="de64f-167"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-167"><dt>3</dt></span></span> </dl> | <span data-ttu-id="de64f-168">Utilisateur autorisé et physiquement présent requis.</span><span class="sxs-lookup"><span data-stu-id="de64f-168">Allowed and physically present user required.</span></span><br/>               |
| <dl> <span data-ttu-id="de64f-169"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-169"><dt>4</dt></span></span> </dl> | <span data-ttu-id="de64f-170">Utilisateur autorisé et physiquement présent non requis</span><span class="sxs-lookup"><span data-stu-id="de64f-170">Allowed and physically present user not required</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de64f-171">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="de64f-171">Return value</span></span>

<span data-ttu-id="de64f-172">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="de64f-172">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="de64f-173">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="de64f-173">Common return codes are listed below.</span></span>



| <span data-ttu-id="de64f-174">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="de64f-174">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="de64f-175">Description</span><span class="sxs-lookup"><span data-stu-id="de64f-175">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="de64f-176"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-176"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="de64f-177">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="de64f-177">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de64f-178">Notes</span><span class="sxs-lookup"><span data-stu-id="de64f-178">Remarks</span></span>

<span data-ttu-id="de64f-179">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="de64f-179">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="de64f-180">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="de64f-180">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="de64f-181">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="de64f-181">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="de64f-182">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="de64f-182">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de64f-183">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="de64f-183">Requirements</span></span>



| <span data-ttu-id="de64f-184">Condition requise</span><span class="sxs-lookup"><span data-stu-id="de64f-184">Requirement</span></span> | <span data-ttu-id="de64f-185">Valeur</span><span class="sxs-lookup"><span data-stu-id="de64f-185">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="de64f-186">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de64f-186">Minimum supported client</span></span><br/> | <span data-ttu-id="de64f-187">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de64f-187">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="de64f-188">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="de64f-188">Minimum supported server</span></span><br/> | <span data-ttu-id="de64f-189">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="de64f-189">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="de64f-190">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="de64f-190">Namespace</span></span><br/>                | <span data-ttu-id="de64f-191">\\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="de64f-191">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="de64f-192">MOF</span><span class="sxs-lookup"><span data-stu-id="de64f-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de64f-193"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-193"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="de64f-194">DLL</span><span class="sxs-lookup"><span data-stu-id="de64f-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de64f-195"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="de64f-195"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de64f-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de64f-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de64f-197">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="de64f-197">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
