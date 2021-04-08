---
description: Si le Module de plateforme sécurisée (TPM) (TPM) est disponible, cette méthode sécurise la clé de chiffrement du volume améliorée par un numéro d’identification personnel spécifié par l’utilisateur.
ms.assetid: 8c4c434a-dd60-491a-a983-b3fa78c91c0d
title: Méthode ProtectKeyWithTPMAndPIN de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e5a0a7a253723bec84df7a86fa94ab182bd192dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862278"
---
# <a name="protectkeywithtpmandpin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="22080-103">Méthode ProtectKeyWithTPMAndPIN de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="22080-103">ProtectKeyWithTPMAndPIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="22080-104">La méthode **ProtectKeyWithTPMAndPIN** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sécurise la clé de chiffrement du volume à l’aide du matériel de sécurité module de plateforme sécurisée (TPM) (TPM) de l’ordinateur, s’il est disponible, amélioré par un code confidentiel (pin) spécifié par l’utilisateur, qui doit être fourni à l’ordinateur au démarrage.</span><span class="sxs-lookup"><span data-stu-id="22080-104">The **ProtectKeyWithTPMAndPIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by a user-specified personal identification number (PIN) that must be provided to the computer at startup.</span></span>

<span data-ttu-id="22080-105">La validation par le module de plateforme sécurisée et l’entrée de la chaîne d’identification personnelle sont nécessaires pour accéder à la clé de chiffrement du volume et déverrouiller le contenu du volume.</span><span class="sxs-lookup"><span data-stu-id="22080-105">Both validation by the TPM and input of the personal identification string are necessary to access the volume's encryption key and unlock volume contents.</span></span>

<span data-ttu-id="22080-106">Cette méthode s’applique uniquement au volume qui contient le système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22080-106">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="22080-107">Un protecteur de clé de type « TPM et PIN » est créé pour le volume, s’il n’en existe pas déjà un.</span><span class="sxs-lookup"><span data-stu-id="22080-107">A key protector of type "TPM And PIN" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="22080-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="22080-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndPIN(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in]           string PIN,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="22080-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="22080-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22080-110">*FriendlyName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="22080-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22080-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22080-111">Type: **string**</span></span>

<span data-ttu-id="22080-112">Identificateur de chaîne affecté à l’utilisateur pour ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="22080-112">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="22080-113">Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.</span><span class="sxs-lookup"><span data-stu-id="22080-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="22080-114">*PlatformValidationProfile* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="22080-114">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="22080-115">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="22080-115">Type: **uint8\[\]**</span></span>

<span data-ttu-id="22080-116">Tableau d’entiers qui spécifie la façon dont le matériel de sécurité du Module de plateforme sécurisée (TPM) (TPM) de l’ordinateur sécurise la clé de chiffrement du volume de disque.</span><span class="sxs-lookup"><span data-stu-id="22080-116">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="22080-117">Un profil de validation de plateforme se compose d’un ensemble d’index de registre de configuration de plateforme (PCR) compris entre 0 et 23 inclus.</span><span class="sxs-lookup"><span data-stu-id="22080-117">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="22080-118">Les valeurs de répétition dans le paramètre sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="22080-118">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="22080-119">Chaque index PCR est associé à des services qui s’exécutent au démarrage du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="22080-119">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="22080-120">Chaque fois que l’ordinateur démarre, le module de plateforme sécurisée vérifie que les services que vous avez spécifiés dans le profil de validation de plateforme n’ont pas changé.</span><span class="sxs-lookup"><span data-stu-id="22080-120">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="22080-121">Si l’un de ces services change alors que la protection Chiffrement de lecteur BitLocker (BDE) est toujours activée, le module de plateforme sécurisée ne libère pas la clé de chiffrement pour déverrouiller le volume de disque, et l’ordinateur passe en mode de récupération.</span><span class="sxs-lookup"><span data-stu-id="22080-121">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="22080-122">Si ce paramètre est spécifié alors que le paramètre de stratégie de groupe correspondant a été activé, il doit correspondre au paramètre stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="22080-122">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="22080-123">Si ce paramètre n’est pas spécifié, la valeur par défaut 0, 2, 4, 5, 8, 9, 10 et 11 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="22080-123">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="22080-124">Le profil de validation de plateforme par défaut protège la clé de chiffrement contre les modifications apportées aux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="22080-124">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="22080-125">Racine principale de l’approbation de mesure (CRTM)</span><span class="sxs-lookup"><span data-stu-id="22080-125">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="22080-126">BIOS</span><span class="sxs-lookup"><span data-stu-id="22080-126">BIOS</span></span>
-   <span data-ttu-id="22080-127">Extensions de plateforme (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="22080-127">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="22080-128">Code option ROM (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="22080-128">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="22080-129">Code d’enregistrement de démarrage principal (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="22080-129">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="22080-130">Table de partition d’enregistrement de démarrage principal (DDL) (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="22080-130">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="22080-131">Secteur de démarrage NTFS (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="22080-131">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="22080-132">Bloc de démarrage NTFS (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="22080-132">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="22080-133">Gestionnaire de démarrage (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="22080-133">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="22080-134">Access Control BitLocker (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="22080-134">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="22080-135">Pour la sécurité de votre ordinateur, nous vous recommandons le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="22080-135">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="22080-136">Pour bénéficier d’une protection supplémentaire contre les changements de configuration de démarrage précoces, utilisez un profil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="22080-136">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="22080-137">Les ordinateurs basés sur Unified Extensible Firmware Interface (UEFI) n’utilisent pas la PCR 5 par défaut.</span><span class="sxs-lookup"><span data-stu-id="22080-137">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="22080-138">La modification du profil par défaut affecte la sécurité et la facilité de gestion de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="22080-138">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="22080-139">La sensibilité de BitLocker aux modifications de la plateforme (malveillantes ou autorisées) est augmentée ou réduite en fonction de l’inclusion ou de l’exclusion, respectivement, du PCR.</span><span class="sxs-lookup"><span data-stu-id="22080-139">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="22080-140">Pour que la protection BitLocker soit activée, le profil de validation de plateforme doit inclure PCR 11.</span><span class="sxs-lookup"><span data-stu-id="22080-140">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="22080-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="22080-141">Value</span></span>                                                                         | <span data-ttu-id="22080-142">Signification</span><span class="sxs-lookup"><span data-stu-id="22080-142">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22080-143"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="22080-143"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="22080-144">Racine principale de l’approbation de la mesure (CRTM), du BIOS et des extensions de plateforme</span><span class="sxs-lookup"><span data-stu-id="22080-144">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="22080-145"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="22080-145"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="22080-146">Configuration et données de la plateforme et de la carte mère</span><span class="sxs-lookup"><span data-stu-id="22080-146">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="22080-147"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="22080-147"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="22080-148">Code option ROM</span><span class="sxs-lookup"><span data-stu-id="22080-148">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="22080-149"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="22080-149"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="22080-150">Configuration et données de la ROM optionnelle</span><span class="sxs-lookup"><span data-stu-id="22080-150">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="22080-151"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="22080-151"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="22080-152">Code d’enregistrement de démarrage principal (MBR)</span><span class="sxs-lookup"><span data-stu-id="22080-152">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="22080-153"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="22080-153"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="22080-154">Table de partition d’enregistrement de démarrage principal (MBR)</span><span class="sxs-lookup"><span data-stu-id="22080-154">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="22080-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="22080-155"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="22080-156">Événements de transition d’État et de mise en éveil</span><span class="sxs-lookup"><span data-stu-id="22080-156">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="22080-157"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="22080-157"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="22080-158">Ordinateur Manufacturer-Specific</span><span class="sxs-lookup"><span data-stu-id="22080-158">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="22080-159"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="22080-159"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="22080-160">Secteur de démarrage NTFS</span><span class="sxs-lookup"><span data-stu-id="22080-160">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="22080-161"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="22080-161"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="22080-162">Bloc de démarrage NTFS</span><span class="sxs-lookup"><span data-stu-id="22080-162">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="22080-163"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="22080-163"><dt>10</dt></span></span> </dl> | <span data-ttu-id="22080-164">Gestionnaire de démarrage</span><span class="sxs-lookup"><span data-stu-id="22080-164">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="22080-165"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="22080-165"><dt>11</dt></span></span> </dl> | <span data-ttu-id="22080-166">Access Control BitLocker</span><span class="sxs-lookup"><span data-stu-id="22080-166">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="22080-167"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="22080-167"><dt>12</dt></span></span> </dl> | <span data-ttu-id="22080-168">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="22080-168">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="22080-169"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="22080-169"><dt>13</dt></span></span> </dl> | <span data-ttu-id="22080-170">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="22080-170">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="22080-171"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="22080-171"><dt>14</dt></span></span> </dl> | <span data-ttu-id="22080-172">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="22080-172">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="22080-173"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="22080-173"><dt>15</dt></span></span> </dl> | <span data-ttu-id="22080-174">Défini pour être utilisé par le système d’exploitation statique</span><span class="sxs-lookup"><span data-stu-id="22080-174">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="22080-175"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="22080-175"><dt>16</dt></span></span> </dl> | <span data-ttu-id="22080-176">Utilisé pour le débogage</span><span class="sxs-lookup"><span data-stu-id="22080-176">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="22080-177"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="22080-177"><dt>17</dt></span></span> </dl> | <span data-ttu-id="22080-178">CRTM dynamique</span><span class="sxs-lookup"><span data-stu-id="22080-178">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="22080-179"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="22080-179"><dt>18</dt></span></span> </dl> | <span data-ttu-id="22080-180">Plateforme définie</span><span class="sxs-lookup"><span data-stu-id="22080-180">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="22080-181"><dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="22080-181"><dt>19</dt></span></span> </dl> | <span data-ttu-id="22080-182">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="22080-182">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="22080-183"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="22080-183"><dt>20</dt></span></span> </dl> | <span data-ttu-id="22080-184">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="22080-184">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="22080-185"><dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="22080-185"><dt>21</dt></span></span> </dl> | <span data-ttu-id="22080-186">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="22080-186">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="22080-187"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="22080-187"><dt>22</dt></span></span> </dl> | <span data-ttu-id="22080-188">Utilisé par un système d’exploitation approuvé</span><span class="sxs-lookup"><span data-stu-id="22080-188">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="22080-189"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="22080-189"><dt>23</dt></span></span> </dl> | <span data-ttu-id="22080-190">Prise en charge des applications</span><span class="sxs-lookup"><span data-stu-id="22080-190">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="22080-191">*Code confidentiel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="22080-191">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22080-192">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22080-192">Type: **string**</span></span>

<span data-ttu-id="22080-193">Chaîne d’identification personnelle spécifiée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="22080-193">A user-specified personal identification string.</span></span> <span data-ttu-id="22080-194">Cette chaîne doit être composée d’une séquence de 6 à 20 chiffres ou, si la stratégie de groupe « autoriser les codes confidentiels améliorés pour le démarrage » est activée, de 6 à 20 lettres, des symboles, des espaces ou des nombres.</span><span class="sxs-lookup"><span data-stu-id="22080-194">This string must consist of a sequence of 6 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 6 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> <dt>

<span data-ttu-id="22080-195">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="22080-195">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22080-196">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="22080-196">Type: **string**</span></span>

<span data-ttu-id="22080-197">Identificateur de chaîne unique mis à jour utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="22080-197">The updated unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="22080-198">Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.</span><span class="sxs-lookup"><span data-stu-id="22080-198">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22080-199">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="22080-199">Return value</span></span>

<span data-ttu-id="22080-200">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22080-200">Type: **uint32**</span></span>

<span data-ttu-id="22080-201">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="22080-201">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="22080-202">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="22080-202">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="22080-203">Description</span><span class="sxs-lookup"><span data-stu-id="22080-203">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22080-204"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="22080-204"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="22080-205">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="22080-205">The method was successful.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="22080-206"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="22080-206"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                        | <span data-ttu-id="22080-207">Le paramètre *PlatformValidationProfile* est fourni, mais ses valeurs ne sont pas comprises dans la plage connue, ou il ne correspond pas au paramètre stratégie de groupe actuellement en vigueur.</span><span class="sxs-lookup"><span data-stu-id="22080-207">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="22080-208"><dt>**FVE \_ E \_ amorçable \_ CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="22080-208"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="22080-209">Un CD/DVD de démarrage est détecté sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="22080-209">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="22080-210">Retirez le CD/DVD et redémarrez l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="22080-210">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="22080-211"><dt>**FVE \_ E \_ \_ VOLUME étranger**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="22080-211"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>              | <span data-ttu-id="22080-212">Le module de plateforme sécurisée ne peut pas sécuriser la clé de chiffrement du volume car le volume ne contient pas le système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="22080-212">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                            |
| <dl> <span data-ttu-id="22080-213"><dt>**FVE \_ E \_ \_ \_ caractères pin non valides**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="22080-213"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="22080-214">Le paramètre *NewPIN* contient des caractères qui ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="22080-214">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="22080-215">Lorsque l’stratégie de groupe « autoriser les codes confidentiels améliorés au démarrage » est désactivée, seuls les nombres sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="22080-215">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>          |
| <dl> <span data-ttu-id="22080-216"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="22080-216"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="22080-217">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="22080-217">The volume is locked.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="22080-218"><dt>**FVE \_ \_Longueur de \_ \_ code confidentiel \_ non valide pour la stratégie E**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="22080-218"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="22080-219">Le paramètre *NewPIN* fourni comporte plus de 20 caractères, moins de 6 caractères, ou une valeur inférieure à la longueur minimale spécifiée par stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="22080-219">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 6 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>            |
| <dl> <span data-ttu-id="22080-220"><dt>**FVE \_ Le \_ protecteur E \_ existe**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="22080-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="22080-221">Un protecteur de clé de ce type existe déjà.</span><span class="sxs-lookup"><span data-stu-id="22080-221">A key protector of this type already exists.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="22080-222"><dt>**Tbs \_ \_Service E \_ non \_ exécuté**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="22080-222"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="22080-223">Aucun module de plateforme sécurisée compatible n’a été trouvé sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="22080-223">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="22080-224">Considérations relatives à la sécurité</span><span class="sxs-lookup"><span data-stu-id="22080-224">Security Considerations</span></span>

<span data-ttu-id="22080-225">Pour la sécurité de votre ordinateur, nous vous recommandons le profil par défaut.</span><span class="sxs-lookup"><span data-stu-id="22080-225">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="22080-226">Pour bénéficier d’une protection supplémentaire contre les modifications du code de démarrage anticipé, utilisez un profil de PCR 0, 2, 4, 5, 8, 9, 10 et 11.</span><span class="sxs-lookup"><span data-stu-id="22080-226">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="22080-227">Pour bénéficier d’une protection supplémentaire contre les changements de configuration de démarrage précoces, utilisez un profil de PCR 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="22080-227">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="22080-228">La modification du profil par défaut affecte la sécurité ou l’utilisation de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="22080-228">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="22080-229">Notes</span><span class="sxs-lookup"><span data-stu-id="22080-229">Remarks</span></span>

<span data-ttu-id="22080-230">Au plus un protecteur de clé de type « TPM et PIN » peut exister pour un volume à tout moment.</span><span class="sxs-lookup"><span data-stu-id="22080-230">At most one key protector of type "TPM And PIN" can exist for a volume at any time.</span></span> <span data-ttu-id="22080-231">Si vous souhaitez modifier le nom complet ou le profil de validation de plateforme utilisé par un protecteur de clé « TPM et PIN » existant, vous devez d’abord supprimer le protecteur de clé existant, puis appeler **ProtectKeyWithTPMAndPIN** pour en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="22080-231">If you want to change the display name or the platform validation profile used by an existing "TPM And PIN" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndPIN** to create a new one.</span></span>

<span data-ttu-id="22080-232">Des protecteurs de clé supplémentaires doivent être spécifiés pour déverrouiller le volume dans les scénarios de récupération où l’accès à la clé de chiffrement du volume ne peut pas être obtenu. par exemple, lorsque le module de plateforme sécurisée ne peut pas être validé avec le profil de validation de plateforme ou que le code confidentiel est perdu.</span><span class="sxs-lookup"><span data-stu-id="22080-232">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when the PIN is lost.</span></span>

<span data-ttu-id="22080-233">Utilisez [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) ou [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) pour créer un ou plusieurs protecteurs de clé pour la récupération d’un volume autrement verrouillé.</span><span class="sxs-lookup"><span data-stu-id="22080-233">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="22080-234">Bien qu’il soit possible d’avoir à la fois un protecteur de clé du type « TPM » et un autre du type « TPM et PIN », la présence du type de protecteur de clé « TPM » nie les effets des autres protecteurs de clés basés sur le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="22080-234">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And PIN", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="22080-235">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="22080-235">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="22080-236">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="22080-236">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="22080-237">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="22080-237">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="22080-238">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="22080-238">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22080-239">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="22080-239">Requirements</span></span>



| <span data-ttu-id="22080-240">Condition requise</span><span class="sxs-lookup"><span data-stu-id="22080-240">Requirement</span></span> | <span data-ttu-id="22080-241">Valeur</span><span class="sxs-lookup"><span data-stu-id="22080-241">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22080-242">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22080-242">Minimum supported client</span></span><br/> | <span data-ttu-id="22080-243">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22080-243">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="22080-244">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="22080-244">Minimum supported server</span></span><br/> | <span data-ttu-id="22080-245">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="22080-245">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22080-246">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="22080-246">Namespace</span></span><br/>                | <span data-ttu-id="22080-247">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="22080-247">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="22080-248">MOF</span><span class="sxs-lookup"><span data-stu-id="22080-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22080-249"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22080-249"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22080-250">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="22080-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22080-251">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="22080-251">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="22080-252">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="22080-252">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
