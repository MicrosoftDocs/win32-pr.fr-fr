---
description: Si le Module de plateforme sécurisée (TPM) (TPM) est disponible, cette méthode sécurise la clé de chiffrement du volume.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Méthode ProtectKeyWithTPM de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0369e44d96a4f1dcacf33dbf1b1da6ad6d37eed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537046"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ec12e-103">Méthode ProtectKeyWithTPM de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="ec12e-103">ProtectKeyWithTPM method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ec12e-104">La méthode **ProtectKeyWithTPM** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sécurise la clé de chiffrement du volume à l’aide du matériel de sécurité module de plateforme sécurisée (TPM) (TPM) sur l’ordinateur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ec12e-104">The **ProtectKeyWithTPM** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available.</span></span>

<span data-ttu-id="ec12e-105">Un protecteur de clé de type « TPM » est créé pour le volume, s’il n’en existe pas déjà un.</span><span class="sxs-lookup"><span data-stu-id="ec12e-105">A key protector of type "TPM" is created for the volume, if one does not already exist.</span></span>

<span data-ttu-id="ec12e-106">Cette méthode s’applique uniquement au volume qui contient le système d’exploitation en cours d’exécution et si un protecteur de clé n’existe pas déjà sur le volume.</span><span class="sxs-lookup"><span data-stu-id="ec12e-106">This method is only applicable for the volume that contains the currently running operating system, and if a key protector does not already exist on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec12e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec12e-107">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="ec12e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec12e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec12e-109">*FriendlyName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ec12e-109">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec12e-110">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ec12e-110">Type: **string**</span></span>

<span data-ttu-id="ec12e-111">Chaîne qui spécifie un identificateur de chaîne assigné par l’utilisateur pour ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="ec12e-111">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="ec12e-112">Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ec12e-112">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="ec12e-113">*PlatformValidationProfile* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="ec12e-113">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ec12e-114">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="ec12e-114">Type: **uint8\[\]**</span></span>

<span data-ttu-id="ec12e-115">Tableau d’entiers qui spécifie la façon dont le matériel de sécurité du Module de plateforme sécurisée (TPM) (TPM) de l’ordinateur sécurise la clé de chiffrement du volume de disque.</span><span class="sxs-lookup"><span data-stu-id="ec12e-115">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="ec12e-116">Un profil de validation de plateforme se compose d’un ensemble d’index de registre de configuration de plateforme (PCR) compris entre 0 et 23 inclus.</span><span class="sxs-lookup"><span data-stu-id="ec12e-116">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="ec12e-117">Les valeurs de répétition dans le paramètre sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="ec12e-117">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="ec12e-118">Chaque index PCR est associé à des services qui s’exécutent au démarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ec12e-118">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="ec12e-119">Chaque fois que l’ordinateur démarre, le module de plateforme sécurisée vérifie que les services que vous avez spécifiés dans le profil de validation de plateforme n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="ec12e-119">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="ec12e-120">Si l’un de ces services change alors que la protection Chiffrement de lecteur BitLocker (BDE) est toujours activée, le module de plateforme sécurisée ne libère pas la clé de chiffrement pour déverrouiller le volume de disque et l’ordinateur passe en mode de récupération.</span><span class="sxs-lookup"><span data-stu-id="ec12e-120">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="ec12e-121">Si ce paramètre est spécifié alors que le paramètre de stratégie de groupe correspondant a été activé, il doit correspondre au paramètre stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="ec12e-121">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="ec12e-122">Si ce paramètre n’est pas spécifié, la valeur par défaut 0, 2, 4, 5, 8, 9, 10 et 11 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="ec12e-122">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="ec12e-123">Le profil de validation de plateforme par défaut protège la clé de chiffrement contre les modifications apportées à la racine principale de l’approbation de mesure (CRTM). le BIOS et les extensions de plateforme (PCR 0), le code d’option ROM (PCR 2), le code d’enregistrement de démarrage principal (PCR 4), la table de partition MBR (Master Boot Record) (PCR 5), le secteur de démarrage NTFS (PCR 8), le code de démarrage NTFS (PCR 9), le gestionnaire de démarrage (PCR 10) et le Chiffrement de lecteur BitLocker Access Control (PCR 11).</span><span class="sxs-lookup"><span data-stu-id="ec12e-123">The default platform validation profile secures the encryption key against changes to the Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions (PCR 0), Option ROM Code (PCR 2), the Master Boot Record (MBR) Code (PCR 4), the Master Boot Record (MBR) Partition Table (PCR 5), the NTFS Boot Sector (PCR 8), the NTFS Boot Code (PCR 9), the Boot Manager (PCR 10), and the BitLocker Drive Encryption Access Control (PCR 11).</span></span> <span data-ttu-id="ec12e-124">Pour la sécurité de votre ordinateur, nous vous recommandons le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="ec12e-124">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="ec12e-125">Les ordinateurs basés sur Unified Extensible Firmware Interface (UEFI) n’utilisent pas la PCR 5 par défaut.</span><span class="sxs-lookup"><span data-stu-id="ec12e-125">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span> <span data-ttu-id="ec12e-126">Pour bénéficier d’une protection supplémentaire contre les changements de configuration de démarrage précoces, utilisez un profil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="ec12e-126">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="ec12e-127">La modification du profil par défaut affecte la sécurité et la facilité de gestion de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ec12e-127">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="ec12e-128">La sensibilité de BitLocker aux modifications de la plateforme (malveillantes ou autorisées) est augmentée ou réduite en fonction de l’inclusion ou de l’exclusion, respectivement, du PCR.</span><span class="sxs-lookup"><span data-stu-id="ec12e-128">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="ec12e-129">Pour que la protection BitLocker soit activée, le profil de validation de plateforme doit inclure PCR 11.</span><span class="sxs-lookup"><span data-stu-id="ec12e-129">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="ec12e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec12e-130">Value</span></span>                                                                         | <span data-ttu-id="ec12e-131">Signification</span><span class="sxs-lookup"><span data-stu-id="ec12e-131">Meaning</span></span>                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec12e-132"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-132"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="ec12e-133">Racine principale de l’approbation des extensions de mesure (CRTM), du BIOS et de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="ec12e-133">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions.</span></span><br/> |
| <dl> <span data-ttu-id="ec12e-134"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-134"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="ec12e-135">Configuration et données de la plateforme et de la carte mère</span><span class="sxs-lookup"><span data-stu-id="ec12e-135">Platform and Motherboard Configuration and Data</span></span><br/>                          |
| <dl> <span data-ttu-id="ec12e-136"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-136"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="ec12e-137">Code option ROM</span><span class="sxs-lookup"><span data-stu-id="ec12e-137">Option ROM Code</span></span><br/>                                                          |
| <dl> <span data-ttu-id="ec12e-138"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-138"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="ec12e-139">Configuration et données de la ROM optionnelle</span><span class="sxs-lookup"><span data-stu-id="ec12e-139">Option ROM Configuration and Data</span></span><br/>                                        |
| <dl> <span data-ttu-id="ec12e-140"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-140"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="ec12e-141">Code d’enregistrement de démarrage principal (MBR)</span><span class="sxs-lookup"><span data-stu-id="ec12e-141">Master Boot Record (MBR) Code</span></span><br/>                                            |
| <dl> <span data-ttu-id="ec12e-142"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-142"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="ec12e-143">Table de partition d’enregistrement de démarrage principal (MBR)</span><span class="sxs-lookup"><span data-stu-id="ec12e-143">Master Boot Record (MBR) Partition Table</span></span><br/>                                 |
| <dl> <span data-ttu-id="ec12e-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-144"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="ec12e-145">Événements de transition d’État et de mise en éveil</span><span class="sxs-lookup"><span data-stu-id="ec12e-145">State Transition and Wake Events</span></span><br/>                                         |
| <dl> <span data-ttu-id="ec12e-146"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-146"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="ec12e-147">Ordinateur Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="ec12e-147">Computer Manufacturer-Specific</span></span><br/>                                           |
| <dl> <span data-ttu-id="ec12e-148"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-148"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="ec12e-149">Secteur de démarrage NTFS</span><span class="sxs-lookup"><span data-stu-id="ec12e-149">NTFS Boot Sector</span></span><br/>                                                         |
| <dl> <span data-ttu-id="ec12e-150"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-150"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="ec12e-151">Code de démarrage NTFS</span><span class="sxs-lookup"><span data-stu-id="ec12e-151">NTFS Boot Code</span></span><br/>                                                           |
| <dl> <span data-ttu-id="ec12e-152"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-152"><dt>10</dt></span></span> </dl> | <span data-ttu-id="ec12e-153">Gestionnaire de démarrage</span><span class="sxs-lookup"><span data-stu-id="ec12e-153">Boot Manager</span></span><br/>                                                             |
| <dl> <span data-ttu-id="ec12e-154"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-154"><dt>11</dt></span></span> </dl> | <span data-ttu-id="ec12e-155">Chiffrement de lecteur BitLocker Access Control</span><span class="sxs-lookup"><span data-stu-id="ec12e-155">BitLocker Drive Encryption Access Control</span></span><br/>                                |
| <dl> <span data-ttu-id="ec12e-156"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-156"><dt>12</dt></span></span> </dl> | <span data-ttu-id="ec12e-157">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="ec12e-157">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="ec12e-158"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-158"><dt>13</dt></span></span> </dl> | <span data-ttu-id="ec12e-159">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="ec12e-159">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="ec12e-160"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-160"><dt>14</dt></span></span> </dl> | <span data-ttu-id="ec12e-161">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="ec12e-161">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="ec12e-162"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-162"><dt>15</dt></span></span> </dl> | <span data-ttu-id="ec12e-163">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="ec12e-163">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="ec12e-164"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-164"><dt>16</dt></span></span> </dl> | <span data-ttu-id="ec12e-165">Utilisé pour le débogage</span><span class="sxs-lookup"><span data-stu-id="ec12e-165">Used for debugging</span></span><br/>                                                       |
| <dl> <span data-ttu-id="ec12e-166"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-166"><dt>17</dt></span></span> </dl> | <span data-ttu-id="ec12e-167">CRTM dynamique</span><span class="sxs-lookup"><span data-stu-id="ec12e-167">Dynamic CRTM</span></span><br/>                                                             |
| <dl> <span data-ttu-id="ec12e-168"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-168"><dt>18</dt></span></span> </dl> | <span data-ttu-id="ec12e-169">Plateforme définie</span><span class="sxs-lookup"><span data-stu-id="ec12e-169">Platform defined</span></span><br/>                                                         |
| <dl> <span data-ttu-id="ec12e-170"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-170"><dt>19</dt></span></span> </dl> | <span data-ttu-id="ec12e-171">Utilisé par le système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="ec12e-171">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="ec12e-172"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-172"><dt>20</dt></span></span> </dl> | <span data-ttu-id="ec12e-173">Utilisé par le système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="ec12e-173">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="ec12e-174"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-174"><dt>21</dt></span></span> </dl> | <span data-ttu-id="ec12e-175">Utilisé par le système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="ec12e-175">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="ec12e-176"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-176"><dt>22</dt></span></span> </dl> | <span data-ttu-id="ec12e-177">Utilisé par le système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="ec12e-177">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="ec12e-178"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-178"><dt>23</dt></span></span> </dl> | <span data-ttu-id="ec12e-179">Prise en charge des applications</span><span class="sxs-lookup"><span data-stu-id="ec12e-179">Application support</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="ec12e-180">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ec12e-180">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec12e-181">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ec12e-181">Type: **string**</span></span>

<span data-ttu-id="ec12e-182">Chaîne qui identifie de façon unique le protecteur créé et qui peut être utilisée pour gérer le protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="ec12e-182">A string that uniquely identifies the created protector and which can be used to manage the key protector.</span></span>

<span data-ttu-id="ec12e-183">Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.</span><span class="sxs-lookup"><span data-stu-id="ec12e-183">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec12e-184">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec12e-184">Return value</span></span>

<span data-ttu-id="ec12e-185">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec12e-185">Type: **uint32**</span></span>

<span data-ttu-id="ec12e-186">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="ec12e-186">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ec12e-187">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ec12e-187">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="ec12e-188">Description</span><span class="sxs-lookup"><span data-stu-id="ec12e-188">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec12e-189"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-189"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="ec12e-190">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="ec12e-190">The method was successful.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="ec12e-191"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-191"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="ec12e-192">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="ec12e-192">The volume is locked.</span></span><br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="ec12e-193"><dt>**Tbs \_ \_Service E \_ non \_ exécuté**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-193"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="ec12e-194">Aucun module de plateforme sécurisée compatible n’a été trouvé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ec12e-194">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="ec12e-195"><dt>**FVE \_ E \_ \_ VOLUME étranger**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-195"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="ec12e-196">Le module de plateforme sécurisée ne peut pas sécuriser la clé de chiffrement du volume car le volume ne contient pas le système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ec12e-196">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                           |
| <dl> <span data-ttu-id="ec12e-197"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-197"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="ec12e-198">Le paramètre *PlatformValidationProfile* est fourni, mais ses valeurs ne sont pas comprises dans la plage connue, ou il ne correspond pas au paramètre stratégie de groupe actuellement en vigueur.</span><span class="sxs-lookup"><span data-stu-id="ec12e-198">The *PlatformValidationProfile* parameter is provided but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="ec12e-199"><dt>**FVE \_ Le \_ protecteur E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-199"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="ec12e-200">Un protecteur de clé de ce type existe déjà.</span><span class="sxs-lookup"><span data-stu-id="ec12e-200">A key protector of this type already exists.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="ec12e-201">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="ec12e-201">Security Considerations</span></span>

<span data-ttu-id="ec12e-202">Pour la sécurité de votre ordinateur, nous vous recommandons le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="ec12e-202">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="ec12e-203">Pour bénéficier d’une protection supplémentaire contre les changements de configuration de démarrage précoces, utilisez un profil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="ec12e-203">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="ec12e-204">La modification du profil par défaut affecte la sécurité ou l’utilisation de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ec12e-204">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec12e-205">Notes</span><span class="sxs-lookup"><span data-stu-id="ec12e-205">Remarks</span></span>

<span data-ttu-id="ec12e-206">Au plus un protecteur de clé de type « TPM » peut exister pour un volume à tout moment.</span><span class="sxs-lookup"><span data-stu-id="ec12e-206">At most one key protector of type "TPM" can exist for a volume at any time.</span></span> <span data-ttu-id="ec12e-207">Si vous souhaitez modifier le nom complet ou le profil de validation de plateforme utilisé par un protecteur de clé « TPM » existant, vous devez d’abord supprimer le protecteur de clé existant, puis appeler **ProtectKeyWithTPM** pour en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="ec12e-207">If you want to change the display name or the platform validation profile used by an existing "TPM" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPM** to create a new one.</span></span>

<span data-ttu-id="ec12e-208">Pour les index PCR de 0 à 5, les mesures actuelles dans les registres sont utilisées pour protéger la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="ec12e-208">For PCR indices 0 through 5, the current measurements in the registers are used to protect the encryption key.</span></span> <span data-ttu-id="ec12e-209">Pour les valeurs PCR de 8 à 11, les mesures utilisées sont celles attendues au cours du prochain cycle de démarrage.</span><span class="sxs-lookup"><span data-stu-id="ec12e-209">For PCR values 8 through 11, the measurements used are the ones expected to exist on the next start cycle.</span></span>

<span data-ttu-id="ec12e-210">Des protecteurs de clé supplémentaires doivent être spécifiés pour déverrouiller le volume dans les scénarios de récupération où l’accès à la clé de chiffrement du volume ne peut pas être obtenu. par exemple, lorsque le module de plateforme sécurisée ne peut pas être validé avec le profil de validation de plateforme.</span><span class="sxs-lookup"><span data-stu-id="ec12e-210">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile.</span></span> <span data-ttu-id="ec12e-211">Utilisez [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) ou [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) pour créer un ou plusieurs protecteurs de clé pour la récupération d’un volume autrement verrouillé.</span><span class="sxs-lookup"><span data-stu-id="ec12e-211">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="ec12e-212">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="ec12e-212">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ec12e-213">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="ec12e-213">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ec12e-214">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="ec12e-214">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ec12e-215">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ec12e-215">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec12e-216">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec12e-216">Requirements</span></span>



| <span data-ttu-id="ec12e-217">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec12e-217">Requirement</span></span> | <span data-ttu-id="ec12e-218">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec12e-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec12e-219">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec12e-219">Minimum supported client</span></span><br/> | <span data-ttu-id="ec12e-220">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec12e-220">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ec12e-221">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec12e-221">Minimum supported server</span></span><br/> | <span data-ttu-id="ec12e-222">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ec12e-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec12e-223">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ec12e-223">Namespace</span></span><br/>                | <span data-ttu-id="ec12e-224">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ec12e-224">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ec12e-225">MOF</span><span class="sxs-lookup"><span data-stu-id="ec12e-225">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec12e-226"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-226"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec12e-227">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec12e-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec12e-228">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="ec12e-228">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="ec12e-229">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="ec12e-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
