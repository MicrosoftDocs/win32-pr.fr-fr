---
description: Récupère le profil de validation de plateforme pour un protecteur de clé donné du type approprié.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Méthode GetKeyProtectorPlatformValidationProfile de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526204"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="6b769-103">Méthode GetKeyProtectorPlatformValidationProfile de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="6b769-103">GetKeyProtectorPlatformValidationProfile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="6b769-104">La méthode **GetKeyProtectorPlatformValidationProfile** récupère le profil de validation de plateforme pour un protecteur de clé donné du type approprié.</span><span class="sxs-lookup"><span data-stu-id="6b769-104">The **GetKeyProtectorPlatformValidationProfile** method retrieves the platform validation profile for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="6b769-105">L’identificateur de protecteur de clé doit faire référence à un protecteur de clé de type « TPM », « TPM et PIN », « TPM et PIN et clé de démarrage », ou « TPM et clé de démarrage ».</span><span class="sxs-lookup"><span data-stu-id="6b769-105">The key protector identifier must refer to a key protector of type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="6b769-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b769-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a><span data-ttu-id="6b769-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b769-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b769-108">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b769-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b769-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="6b769-109">Type: **string**</span></span>

<span data-ttu-id="6b769-110">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="6b769-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="6b769-111">*PlatformValidationProfile* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b769-111">*PlatformValidationProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b769-112">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="6b769-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="6b769-113">Tableau d’entiers qui spécifie la façon dont le matériel de sécurité Module de plateforme sécurisée (TPM) (TPM) de l’ordinateur sécurise la clé de chiffrement du volume de disque.</span><span class="sxs-lookup"><span data-stu-id="6b769-113">An array of integers that specifies how the Trusted Platform Module (TPM) Security Hardware of the computer secures the encryption key of the disk volume.</span></span>



| <span data-ttu-id="6b769-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b769-114">Value</span></span>                                                                         | <span data-ttu-id="6b769-115">Signification</span><span class="sxs-lookup"><span data-stu-id="6b769-115">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b769-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-116"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="6b769-117">Racine principale de l’approbation de la mesure (CRTM), du BIOS et des extensions de plateforme</span><span class="sxs-lookup"><span data-stu-id="6b769-117">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="6b769-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-118"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="6b769-119">Configuration et données de la plateforme et de la carte mère</span><span class="sxs-lookup"><span data-stu-id="6b769-119">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="6b769-120"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-120"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="6b769-121">Code option ROM</span><span class="sxs-lookup"><span data-stu-id="6b769-121">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="6b769-122"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-122"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="6b769-123">Configuration et données de la ROM optionnelle</span><span class="sxs-lookup"><span data-stu-id="6b769-123">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="6b769-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-124"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="6b769-125">Code d’enregistrement de démarrage principal (MBR)</span><span class="sxs-lookup"><span data-stu-id="6b769-125">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="6b769-126"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-126"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="6b769-127">Table de partition d’enregistrement de démarrage principal (MBR)</span><span class="sxs-lookup"><span data-stu-id="6b769-127">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="6b769-128"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-128"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="6b769-129">Événements de transition d’État et de mise en éveil</span><span class="sxs-lookup"><span data-stu-id="6b769-129">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="6b769-130"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-130"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="6b769-131">Ordinateur Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="6b769-131">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="6b769-132"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-132"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="6b769-133">Secteur de démarrage NTFS</span><span class="sxs-lookup"><span data-stu-id="6b769-133">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6b769-134"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-134"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="6b769-135">Bloc de démarrage NTFS</span><span class="sxs-lookup"><span data-stu-id="6b769-135">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="6b769-136"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-136"><dt>10</dt></span></span> </dl> | <span data-ttu-id="6b769-137">Gestionnaire de démarrage</span><span class="sxs-lookup"><span data-stu-id="6b769-137">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="6b769-138"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-138"><dt>11</dt></span></span> </dl> | <span data-ttu-id="6b769-139">Access Control BitLocker</span><span class="sxs-lookup"><span data-stu-id="6b769-139">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="6b769-140"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-140"><dt>12</dt></span></span> </dl> | <span data-ttu-id="6b769-141">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="6b769-141">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="6b769-142"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-142"><dt>13</dt></span></span> </dl> | <span data-ttu-id="6b769-143">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="6b769-143">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="6b769-144"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-144"><dt>14</dt></span></span> </dl> | <span data-ttu-id="6b769-145">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="6b769-145">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="6b769-146"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-146"><dt>15</dt></span></span> </dl> | <span data-ttu-id="6b769-147">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="6b769-147">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="6b769-148"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-148"><dt>16</dt></span></span> </dl> | <span data-ttu-id="6b769-149">Utilisé pour le débogage</span><span class="sxs-lookup"><span data-stu-id="6b769-149">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="6b769-150"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-150"><dt>17</dt></span></span> </dl> | <span data-ttu-id="6b769-151">CRTM dynamique</span><span class="sxs-lookup"><span data-stu-id="6b769-151">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="6b769-152"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-152"><dt>18</dt></span></span> </dl> | <span data-ttu-id="6b769-153">Plateforme définie</span><span class="sxs-lookup"><span data-stu-id="6b769-153">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="6b769-154"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-154"><dt>19</dt></span></span> </dl> | <span data-ttu-id="6b769-155">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="6b769-155">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="6b769-156"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-156"><dt>20</dt></span></span> </dl> | <span data-ttu-id="6b769-157">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="6b769-157">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="6b769-158"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-158"><dt>21</dt></span></span> </dl> | <span data-ttu-id="6b769-159">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="6b769-159">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="6b769-160"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-160"><dt>22</dt></span></span> </dl> | <span data-ttu-id="6b769-161">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="6b769-161">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="6b769-162"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-162"><dt>23</dt></span></span> </dl> | <span data-ttu-id="6b769-163">Prise en charge des applications</span><span class="sxs-lookup"><span data-stu-id="6b769-163">Application support</span></span><br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b769-164">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b769-164">Return value</span></span>

<span data-ttu-id="6b769-165">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6b769-165">Type: **uint32**</span></span>

<span data-ttu-id="6b769-166">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="6b769-166">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="6b769-167">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6b769-167">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="6b769-168">Description</span><span class="sxs-lookup"><span data-stu-id="6b769-168">Description</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6b769-169"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-169"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="6b769-170">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="6b769-170">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="6b769-171"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-171"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="6b769-172">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé de type « TPM », « TPM et pin », « TPM et pin et clé de démarrage », ou « TPM et clé de démarrage ».</span><span class="sxs-lookup"><span data-stu-id="6b769-172">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="6b769-173"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-173"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="6b769-174">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="6b769-174">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="6b769-175">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="6b769-175">Add a key protector to enable BitLocker.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="6b769-176">Notes</span><span class="sxs-lookup"><span data-stu-id="6b769-176">Remarks</span></span>

<span data-ttu-id="6b769-177">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="6b769-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6b769-178">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="6b769-178">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="6b769-179">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="6b769-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6b769-180">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="6b769-180">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b769-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b769-181">Requirements</span></span>



| <span data-ttu-id="6b769-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b769-182">Requirement</span></span> | <span data-ttu-id="6b769-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b769-183">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b769-184">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b769-184">Minimum supported client</span></span><br/> | <span data-ttu-id="6b769-185">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b769-185">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6b769-186">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b769-186">Minimum supported server</span></span><br/> | <span data-ttu-id="6b769-187">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b769-187">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b769-188">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6b769-188">Namespace</span></span><br/>                | <span data-ttu-id="6b769-189">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="6b769-189">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="6b769-190">MOF</span><span class="sxs-lookup"><span data-stu-id="6b769-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b769-191"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b769-191"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b769-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b769-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b769-193">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="6b769-193">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
