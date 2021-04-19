---
description: Si le Module de plateforme sécurisée (TPM) (TPM) est disponible, cette méthode sécurise la clé de chiffrement du volume améliorée par une clé externe.
ms.assetid: 58bc2de7-645f-4049-949c-975062f8c8ce
title: Méthode ProtectKeyWithTPMAndStartupKey de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 06ab2b9474b3564a567374490d9aeb70448338be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106539054"
---
# <a name="protectkeywithtpmandstartupkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="61cba-103">Méthode ProtectKeyWithTPMAndStartupKey de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="61cba-103">ProtectKeyWithTPMAndStartupKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="61cba-104">La méthode **ProtectKeyWithTPMAndStartupKey** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sécurise la clé de chiffrement du volume à l’aide du matériel de sécurité module de plateforme sécurisée (TPM) (TPM) de l’ordinateur, s’il est disponible, amélioré par une clé externe qui doit être présentée à l’ordinateur au démarrage.</span><span class="sxs-lookup"><span data-stu-id="61cba-104">The **ProtectKeyWithTPMAndStartupKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by an external key that must be presented to the computer at startup.</span></span>

<span data-ttu-id="61cba-105">La validation par le module de plateforme sécurisée et l’entrée d’un périphérique de mémoire USB qui contient la clé externe sont nécessaires pour accéder à la clé de chiffrement du volume et déverrouiller le contenu du volume.</span><span class="sxs-lookup"><span data-stu-id="61cba-105">Both validation by the TPM and input of a USB memory device that contains the external key are necessary to access the volume's encryption key and unlock the volume contents.</span></span> <span data-ttu-id="61cba-106">Utilisez la méthode [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) pour enregistrer cette clé externe dans un fichier sur un périphérique de mémoire USB en vue de son utilisation en tant que clé de démarrage.</span><span class="sxs-lookup"><span data-stu-id="61cba-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file on a USB memory device for usage as a startup key.</span></span>

<span data-ttu-id="61cba-107">Cette méthode s’applique uniquement au volume qui contient le système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="61cba-107">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="61cba-108">Un protecteur de clé de type « TPM et clé de démarrage » est créé pour le volume, s’il n’en existe pas déjà un.</span><span class="sxs-lookup"><span data-stu-id="61cba-108">A key protector of type "TPM And Startup Key" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="61cba-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61cba-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="61cba-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61cba-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61cba-111">*FriendlyName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="61cba-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61cba-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="61cba-112">Type: **string**</span></span>

<span data-ttu-id="61cba-113">Identificateur de chaîne affecté à l’utilisateur pour ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="61cba-113">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="61cba-114">Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.</span><span class="sxs-lookup"><span data-stu-id="61cba-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="61cba-115">*PlatformValidationProfile* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="61cba-115">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61cba-116">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="61cba-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="61cba-117">Tableau d’entiers qui spécifie la façon dont le matériel de sécurité du Module de plateforme sécurisée (TPM) (TPM) de l’ordinateur sécurise la clé de chiffrement du volume de disque.</span><span class="sxs-lookup"><span data-stu-id="61cba-117">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the encryption key of the disk volume.</span></span>

<span data-ttu-id="61cba-118">Un profil de validation de plateforme se compose d’un ensemble d’index de registre de configuration de plateforme (PCR) compris entre 0 et 23 inclus.</span><span class="sxs-lookup"><span data-stu-id="61cba-118">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="61cba-119">Les valeurs de répétition dans le paramètre sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="61cba-119">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="61cba-120">Chaque index PCR est associé à des services qui s’exécutent au démarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="61cba-120">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="61cba-121">Chaque fois que l’ordinateur démarre, le module de plateforme sécurisée vérifie que les services que vous avez spécifiés dans le profil de validation de plateforme n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="61cba-121">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="61cba-122">Si l’un de ces services change alors que la protection Chiffrement de lecteur BitLocker (BDE) est toujours activée, le module de plateforme sécurisée ne libère pas la clé de chiffrement pour déverrouiller le volume de disque, et l’ordinateur passe en mode de récupération.</span><span class="sxs-lookup"><span data-stu-id="61cba-122">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="61cba-123">Si ce paramètre est spécifié alors que le paramètre de stratégie de groupe correspondant a été activé, il doit correspondre au paramètre stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="61cba-123">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="61cba-124">Si ce paramètre n’est pas spécifié, la valeur par défaut 0, 2, 4, 5, 8, 9, 10 et 11 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="61cba-124">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="61cba-125">Le profil de validation de plateforme par défaut protège la clé de chiffrement contre les modifications apportées aux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="61cba-125">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="61cba-126">Racine principale de l’approbation de mesure (CRTM)</span><span class="sxs-lookup"><span data-stu-id="61cba-126">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="61cba-127">BIOS</span><span class="sxs-lookup"><span data-stu-id="61cba-127">BIOS</span></span>
-   <span data-ttu-id="61cba-128">Extensions de plateforme (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="61cba-128">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="61cba-129">Code option ROM (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="61cba-129">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="61cba-130">Code d’enregistrement de démarrage principal (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="61cba-130">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="61cba-131">Table de partition d’enregistrement de démarrage principal (DDL) (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="61cba-131">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="61cba-132">Secteur de démarrage NTFS (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="61cba-132">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="61cba-133">Bloc de démarrage NTFS (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="61cba-133">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="61cba-134">Gestionnaire de démarrage (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="61cba-134">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="61cba-135">Access Control BitLocker (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="61cba-135">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="61cba-136">Pour la sécurité de votre ordinateur, nous vous recommandons le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="61cba-136">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="61cba-137">Pour bénéficier d’une protection supplémentaire contre les changements de configuration de démarrage précoces, utilisez un profil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="61cba-137">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="61cba-138">Les ordinateurs basés sur Unified Extensible Firmware Interface (UEFI) n’utilisent pas la PCR 5 par défaut.</span><span class="sxs-lookup"><span data-stu-id="61cba-138">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="61cba-139">La modification du profil par défaut affecte la sécurité et la facilité de gestion de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61cba-139">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="61cba-140">La sensibilité de BitLocker aux modifications de la plateforme (malveillantes ou autorisées) est augmentée ou réduite en fonction de l’inclusion ou de l’exclusion, respectivement, du PCR.</span><span class="sxs-lookup"><span data-stu-id="61cba-140">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="61cba-141">Pour que la protection BitLocker soit activée, le profil de validation de plateforme doit inclure PCR 11.</span><span class="sxs-lookup"><span data-stu-id="61cba-141">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="61cba-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="61cba-142">Value</span></span>                                                                         | <span data-ttu-id="61cba-143">Signification</span><span class="sxs-lookup"><span data-stu-id="61cba-143">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61cba-144"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-144"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="61cba-145">Racine principale de l’approbation de la mesure (CRTM), du BIOS et des extensions de plateforme</span><span class="sxs-lookup"><span data-stu-id="61cba-145">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="61cba-146"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-146"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="61cba-147">Configuration et données de la plateforme et de la carte mère</span><span class="sxs-lookup"><span data-stu-id="61cba-147">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="61cba-148"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-148"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="61cba-149">Code option ROM</span><span class="sxs-lookup"><span data-stu-id="61cba-149">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="61cba-150"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-150"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="61cba-151">Configuration et données de la ROM optionnelle</span><span class="sxs-lookup"><span data-stu-id="61cba-151">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="61cba-152"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-152"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="61cba-153">Code d’enregistrement de démarrage principal (MBR)</span><span class="sxs-lookup"><span data-stu-id="61cba-153">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="61cba-154"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-154"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="61cba-155">Table de partition d’enregistrement de démarrage principal (MBR)</span><span class="sxs-lookup"><span data-stu-id="61cba-155">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="61cba-156"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-156"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="61cba-157">Événements de transition d’État et de mise en éveil</span><span class="sxs-lookup"><span data-stu-id="61cba-157">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="61cba-158"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-158"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="61cba-159">Ordinateur Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="61cba-159">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="61cba-160"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-160"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="61cba-161">Secteur de démarrage NTFS</span><span class="sxs-lookup"><span data-stu-id="61cba-161">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="61cba-162"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-162"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="61cba-163">Bloc de démarrage NTFS</span><span class="sxs-lookup"><span data-stu-id="61cba-163">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="61cba-164"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-164"><dt>10</dt></span></span> </dl> | <span data-ttu-id="61cba-165">Gestionnaire de démarrage</span><span class="sxs-lookup"><span data-stu-id="61cba-165">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="61cba-166"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-166"><dt>11</dt></span></span> </dl> | <span data-ttu-id="61cba-167">Access Control BitLocker</span><span class="sxs-lookup"><span data-stu-id="61cba-167">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="61cba-168"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-168"><dt>12</dt></span></span> </dl> | <span data-ttu-id="61cba-169">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="61cba-169">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="61cba-170"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-170"><dt>13</dt></span></span> </dl> | <span data-ttu-id="61cba-171">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="61cba-171">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="61cba-172"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-172"><dt>14</dt></span></span> </dl> | <span data-ttu-id="61cba-173">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="61cba-173">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="61cba-174"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-174"><dt>15</dt></span></span> </dl> | <span data-ttu-id="61cba-175">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="61cba-175">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="61cba-176"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-176"><dt>16</dt></span></span> </dl> | <span data-ttu-id="61cba-177">Utilisé pour le débogage</span><span class="sxs-lookup"><span data-stu-id="61cba-177">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="61cba-178"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-178"><dt>17</dt></span></span> </dl> | <span data-ttu-id="61cba-179">CRTM dynamique</span><span class="sxs-lookup"><span data-stu-id="61cba-179">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="61cba-180"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-180"><dt>18</dt></span></span> </dl> | <span data-ttu-id="61cba-181">Plateforme définie</span><span class="sxs-lookup"><span data-stu-id="61cba-181">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="61cba-182"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-182"><dt>19</dt></span></span> </dl> | <span data-ttu-id="61cba-183">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="61cba-183">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="61cba-184"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-184"><dt>20</dt></span></span> </dl> | <span data-ttu-id="61cba-185">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="61cba-185">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="61cba-186"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-186"><dt>21</dt></span></span> </dl> | <span data-ttu-id="61cba-187">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="61cba-187">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="61cba-188"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-188"><dt>22</dt></span></span> </dl> | <span data-ttu-id="61cba-189">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="61cba-189">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="61cba-190"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-190"><dt>23</dt></span></span> </dl> | <span data-ttu-id="61cba-191">Prise en charge des applications</span><span class="sxs-lookup"><span data-stu-id="61cba-191">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="61cba-192">*ExternalKey* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="61cba-192">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="61cba-193">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="61cba-193">Type: **uint8\[\]**</span></span>

<span data-ttu-id="61cba-194">Tableau d’octets qui spécifie la clé externe 256 bits utilisée pour déverrouiller le volume au démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61cba-194">An array of bytes that specifies the 256-bit external key used to unlock the volume when the computer starts.</span></span>

<span data-ttu-id="61cba-195">Si aucune clé externe n’est spécifiée, une clé est générée de façon aléatoire.</span><span class="sxs-lookup"><span data-stu-id="61cba-195">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="61cba-196">Utilisez la méthode [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) pour obtenir la clé générée de façon aléatoire.</span><span class="sxs-lookup"><span data-stu-id="61cba-196">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="61cba-197">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="61cba-197">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61cba-198">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="61cba-198">Type: **string**</span></span>

<span data-ttu-id="61cba-199">Chaîne qui est l’identificateur unique associé au protecteur de clé créé qui peut être utilisé pour gérer le protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="61cba-199">A string that is the unique identifier associated with the created key protector that can be used to manage the key protector.</span></span>

<span data-ttu-id="61cba-200">Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.</span><span class="sxs-lookup"><span data-stu-id="61cba-200">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61cba-201">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61cba-201">Return value</span></span>

<span data-ttu-id="61cba-202">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61cba-202">Type: **uint32**</span></span>

<span data-ttu-id="61cba-203">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="61cba-203">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="61cba-204">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="61cba-204">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="61cba-205">Description</span><span class="sxs-lookup"><span data-stu-id="61cba-205">Description</span></span>                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61cba-206"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-206"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="61cba-207">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="61cba-207">The method was successful.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="61cba-208"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-208"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="61cba-209">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="61cba-209">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="61cba-210"><dt>**Tbs \_ \_Service E \_ non \_ exécuté**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-210"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="61cba-211">Aucun module de plateforme sécurisée compatible n’a été trouvé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61cba-211">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="61cba-212"><dt>**FVE \_ E \_ \_ VOLUME étranger**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-212"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="61cba-213">Le module de plateforme sécurisée ne peut pas sécuriser la clé de chiffrement du volume car le volume ne contient pas le système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="61cba-213">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                                                                                                               |
| <dl> <span data-ttu-id="61cba-214"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-214"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="61cba-215">Le paramètre *PlatformValidationProfile* est fourni, mais ses valeurs ne sont pas comprises dans la plage connue, ou il ne correspond pas au paramètre stratégie de groupe actuellement en vigueur.</span><span class="sxs-lookup"><span data-stu-id="61cba-215">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> <span data-ttu-id="61cba-216">Le paramètre *ExternalKey* est fourni, mais n’est pas un tableau de taille 32.</span><span class="sxs-lookup"><span data-stu-id="61cba-216">The *ExternalKey* parameter is provided but is not an array of size 32.</span></span><br/> |
| <dl> <span data-ttu-id="61cba-217"><dt>**FVE \_ E \_ amorçable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-217"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>       | <span data-ttu-id="61cba-218">Un CD/DVD de démarrage est détecté sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61cba-218">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="61cba-219">Retirez le CD/DVD et redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61cba-219">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="61cba-220"><dt>**FVE \_ Le \_ protecteur E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>     | <span data-ttu-id="61cba-221">Un protecteur de clé de ce type existe déjà.</span><span class="sxs-lookup"><span data-stu-id="61cba-221">A key protector of this type already exists.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="security-considerations"></a><span data-ttu-id="61cba-222">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="61cba-222">Security Considerations</span></span>

<span data-ttu-id="61cba-223">Pour la sécurité de votre ordinateur, nous vous recommandons le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="61cba-223">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="61cba-224">Pour bénéficier d’une protection supplémentaire contre les modifications du code de démarrage anticipé, utilisez un profil de PCR 0, 2, 4, 5, 8, 9, 10 et 11.</span><span class="sxs-lookup"><span data-stu-id="61cba-224">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="61cba-225">Pour bénéficier d’une protection supplémentaire contre les changements de configuration de démarrage précoces, utilisez un profil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="61cba-225">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="61cba-226">La modification du profil par défaut affecte la sécurité ou l’utilisation de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="61cba-226">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="61cba-227">Notes</span><span class="sxs-lookup"><span data-stu-id="61cba-227">Remarks</span></span>

<span data-ttu-id="61cba-228">Au plus un protecteur de clé de type « TPM et clé de démarrage » peut exister pour un volume à tout moment.</span><span class="sxs-lookup"><span data-stu-id="61cba-228">At most one key protector of type "TPM And Startup Key" can exist for a volume at any time.</span></span> <span data-ttu-id="61cba-229">Si vous souhaitez modifier le nom complet ou le profil de validation de plateforme utilisé par un protecteur de clé « TPM plus clé de démarrage » existant, vous devez d’abord supprimer le protecteur de clé existant, puis appeler **ProtectKeyWithTPMAndStartupKey** pour en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="61cba-229">If you want to change the display name or the platform validation profile used by an existing "TPM plus Startup Key" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndStartupKey** to create a new one.</span></span> <span data-ttu-id="61cba-230">Des protecteurs de clé supplémentaires doivent être spécifiés pour déverrouiller le volume dans les scénarios de récupération où l’accès à la clé de chiffrement du volume ne peut pas être obtenu. par exemple, lorsque le module de plateforme sécurisée ne peut pas être validé avec le profil de validation de plateforme ou lorsque la mémoire USB qui contient la clé externe est perdue.</span><span class="sxs-lookup"><span data-stu-id="61cba-230">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when USB memory that contains the external key is lost.</span></span>

<span data-ttu-id="61cba-231">Utilisez [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) ou [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) pour créer un ou plusieurs protecteurs de clé pour la récupération d’un volume autrement verrouillé.</span><span class="sxs-lookup"><span data-stu-id="61cba-231">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="61cba-232">Bien qu’il soit possible d’avoir à la fois un protecteur de clé du type « TPM » et un autre du type « TPM et clé de démarrage », la présence du type de protecteur de clé « TPM » nie les effets des autres protecteurs de clés basés sur le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="61cba-232">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And Startup Key", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="61cba-233">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="61cba-233">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="61cba-234">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="61cba-234">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="61cba-235">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="61cba-235">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="61cba-236">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="61cba-236">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61cba-237">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61cba-237">Requirements</span></span>



| <span data-ttu-id="61cba-238">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61cba-238">Requirement</span></span> | <span data-ttu-id="61cba-239">Valeur</span><span class="sxs-lookup"><span data-stu-id="61cba-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61cba-240">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61cba-240">Minimum supported client</span></span><br/> | <span data-ttu-id="61cba-241">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61cba-241">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="61cba-242">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61cba-242">Minimum supported server</span></span><br/> | <span data-ttu-id="61cba-243">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61cba-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="61cba-244">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="61cba-244">Namespace</span></span><br/>                | <span data-ttu-id="61cba-245">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="61cba-245">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="61cba-246">MOF</span><span class="sxs-lookup"><span data-stu-id="61cba-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="61cba-247"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="61cba-247"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61cba-248">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61cba-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61cba-249">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="61cba-249">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="61cba-250">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="61cba-250">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
