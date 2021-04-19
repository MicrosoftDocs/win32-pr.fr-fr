---
description: Représente le Module de plateforme sécurisée (TPM) (TPM), une puce de sécurité matérielle qui fournit une racine de confiance pour un système informatique.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530894"
---
# <a name="win32_tpm-class"></a><span data-ttu-id="d854c-103">\_Classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="d854c-103">Win32\_Tpm class</span></span>

<span data-ttu-id="d854c-104">La **classe \_ TPM Win32** représente le module de plateforme sécurisée (TPM) (TPM), une puce de sécurité matérielle qui fournit une racine de confiance pour un système informatique.</span><span class="sxs-lookup"><span data-stu-id="d854c-104">The **Win32\_Tpm** class represents the Trusted Platform Module (TPM), a hardware security chip that provides a root of trust for a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="d854c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d854c-105">Syntax</span></span>

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a><span data-ttu-id="d854c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d854c-106">Members</span></span>

<span data-ttu-id="d854c-107">La **classe \_ TPM Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d854c-107">The **Win32\_Tpm** class has these types of members:</span></span>

-   [<span data-ttu-id="d854c-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d854c-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="d854c-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d854c-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d854c-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d854c-110">Methods</span></span>

<span data-ttu-id="d854c-111">La **classe \_ TPM Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="d854c-111">The **Win32\_Tpm** class has these methods.</span></span>



| <span data-ttu-id="d854c-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="d854c-112">Method</span></span>                                                                                   | <span data-ttu-id="d854c-113">Description</span><span class="sxs-lookup"><span data-stu-id="d854c-113">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d854c-114">**AddBlockedCommand**</span><span class="sxs-lookup"><span data-stu-id="d854c-114">**AddBlockedCommand**</span></span>](addblockedcommand-win32-tpm.md)                                 | <span data-ttu-id="d854c-115">Ajoute une commande TPM à la liste locale des commandes bloquées sur Windows.</span><span class="sxs-lookup"><span data-stu-id="d854c-115">Adds a TPM command to the local list of commands blocked on Windows.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="d854c-116">**ChangeOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="d854c-116">**ChangeOwnerAuth**</span></span>](changeownerauth-win32-tpm.md)                                     | <span data-ttu-id="d854c-117">Modifie la valeur d’autorisation du propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-117">Changes the TPM owner authorization value.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="d854c-118">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="d854c-118">**Clear**</span></span>](clear-win32-tpm.md)                                                         | <span data-ttu-id="d854c-119">Réinitialise le module de plateforme sécurisée à son état d’usine par défaut.</span><span class="sxs-lookup"><span data-stu-id="d854c-119">Resets the TPM to its factory-default state.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="d854c-120">**ConvertToOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="d854c-120">**ConvertToOwnerAuth**</span></span>](converttoownerauth-win32-tpm.md)                               | <span data-ttu-id="d854c-121">Convertit une phrase secrète fournie par l’utilisateur en une valeur d’autorisation de propriétaire de 20 octets qui peut être utilisée pour interagir avec le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-121">Converts a user-provided passphrase to a 20-byte owner authorization value that can be used to interact with the TPM.</span></span><br/>                                                            |
| [<span data-ttu-id="d854c-122">**CreateEndorsementKeyPair**</span><span class="sxs-lookup"><span data-stu-id="d854c-122">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)                   | <span data-ttu-id="d854c-123">Crée une paire de clés de type EK 2048 bits sur le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-123">Creates a 2048-bit endorsement key pair on the TPM.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="d854c-124">**Désactiver**</span><span class="sxs-lookup"><span data-stu-id="d854c-124">**Disable**</span></span>](disable-win32-tpm.md)                                                     | <span data-ttu-id="d854c-125">Autorise le propriétaire du module de plateforme sécurisée à désactiver le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-125">Allows the TPM owner to disable the TPM.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="d854c-126">**Activer**</span><span class="sxs-lookup"><span data-stu-id="d854c-126">**Enable**</span></span>](enable-win32-tpm.md)                                                       | <span data-ttu-id="d854c-127">Autorise le propriétaire du module de plateforme sécurisée à activer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-127">Allows the TPM owner to enable the TPM.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="d854c-128">**GetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="d854c-128">**GetPhysicalPresenceRequest**</span></span>](getphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="d854c-129">Obtient et retourne l’opération de présence physique TPM en attente.</span><span class="sxs-lookup"><span data-stu-id="d854c-129">Gets and returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="d854c-130">Utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) pour demander une opération.</span><span class="sxs-lookup"><span data-stu-id="d854c-130">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span><br/> |
| [<span data-ttu-id="d854c-131">**GetPhysicalPresenceResponse**</span><span class="sxs-lookup"><span data-stu-id="d854c-131">**GetPhysicalPresenceResponse**</span></span>](getphysicalpresenceresponse-win32-tpm.md)             | <span data-ttu-id="d854c-132">Obtient et retourne les résultats d’une opération de présence physique TPM effectuée.</span><span class="sxs-lookup"><span data-stu-id="d854c-132">Gets and returns the results from a TPM physical presence operation that was performed.</span></span><br/>                                                                                          |
| [<span data-ttu-id="d854c-133">**GetPhysicalPresenceTransition**</span><span class="sxs-lookup"><span data-stu-id="d854c-133">**GetPhysicalPresenceTransition**</span></span>](getphysicalpresencetransition-win32-tpm.md)         | <span data-ttu-id="d854c-134">Indique l’action de l’utilisateur nécessaire pour effectuer une opération de présence physique TPM.</span><span class="sxs-lookup"><span data-stu-id="d854c-134">Indicates the user action that is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                           |
| [<span data-ttu-id="d854c-135">**IsActivated**</span><span class="sxs-lookup"><span data-stu-id="d854c-135">**IsActivated**</span></span>](isactivated-win32-tpm.md)                                             | <span data-ttu-id="d854c-136">Indique si le module de plateforme sécurisée est activé.</span><span class="sxs-lookup"><span data-stu-id="d854c-136">Indicates whether the TPM is activated.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="d854c-137">**IsCommandBlocked**</span><span class="sxs-lookup"><span data-stu-id="d854c-137">**IsCommandBlocked**</span></span>](iscommandblocked-win32-tpm.md)                                   | <span data-ttu-id="d854c-138">Indique si la commande TPM peut s’exécuter sur ce système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d854c-138">Indicates whether the TPM command can run on this operating system.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="d854c-139">**IsCommandPresent**</span><span class="sxs-lookup"><span data-stu-id="d854c-139">**IsCommandPresent**</span></span>](iscommandpresent-win32-tpm.md)                                   | <span data-ttu-id="d854c-140">Indique si une commande de module de plateforme sécurisée est prise en charge par cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d854c-140">Indicates whether a TPM command is supported by this computer.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="d854c-141">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="d854c-141">**IsEnabled**</span></span>](isenabled-win32-tpm.md)                                                 | <span data-ttu-id="d854c-142">Indique si le module de plateforme sécurisée est activé.</span><span class="sxs-lookup"><span data-stu-id="d854c-142">Indicates whether the TPM is enabled.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="d854c-143">**IsEndorsementKeyPairPresent**</span><span class="sxs-lookup"><span data-stu-id="d854c-143">**IsEndorsementKeyPairPresent**</span></span>](isendorsementkeypairpresent-win32-tpm.md)             | <span data-ttu-id="d854c-144">Indique si le module de plateforme sécurisée a une paire de clés de type EK.</span><span class="sxs-lookup"><span data-stu-id="d854c-144">Indicates whether the TPM has an endorsement key pair.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="d854c-145">**IsOwned**</span><span class="sxs-lookup"><span data-stu-id="d854c-145">**IsOwned**</span></span>](isowned-win32-tpm.md)                                                     | <span data-ttu-id="d854c-146">Indique si le module de plateforme sécurisée a un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="d854c-146">Indicates whether the TPM has an owner.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="d854c-147">**IsOwnerClearDisabled**</span><span class="sxs-lookup"><span data-stu-id="d854c-147">**IsOwnerClearDisabled**</span></span>](isownercleardisabled-win32-tpm.md)                           | <span data-ttu-id="d854c-148">Indique si le propriétaire du module de plateforme sécurisée peut effacer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-148">Indicates whether the TPM owner can clear the TPM.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="d854c-149">**IsOwnershipAllowed**</span><span class="sxs-lookup"><span data-stu-id="d854c-149">**IsOwnershipAllowed**</span></span>](isownershipallowed-win32-tpm.md)                               | <span data-ttu-id="d854c-150">Indique si un propriétaire de module de plateforme sécurisée peut être installé.</span><span class="sxs-lookup"><span data-stu-id="d854c-150">Indicates whether a TPM owner can be installed.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="d854c-151">**IsPhysicalClearDisabled**</span><span class="sxs-lookup"><span data-stu-id="d854c-151">**IsPhysicalClearDisabled**</span></span>](isphysicalcleardisabled-win32-tpm.md)                     | <span data-ttu-id="d854c-152">Indique si une opération de présence physique TPM peut effacer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-152">Indicates whether a TPM physical presence operation can clear the TPM.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="d854c-153">**IsPhysicalPresenceHardwareEnabled**</span><span class="sxs-lookup"><span data-stu-id="d854c-153">**IsPhysicalPresenceHardwareEnabled**</span></span>](isphysicalpresencehardwareenabled-win32-tpm.md) | <span data-ttu-id="d854c-154">Indique si cet ordinateur prend en charge un chemin d’accès matériel dédié pour signaler la présence physique.</span><span class="sxs-lookup"><span data-stu-id="d854c-154">Indicates whether this computer supports a dedicated hardware path to signal physical presence.</span></span><br/>                                                                                  |
| [<span data-ttu-id="d854c-155">**IsSrkAuthCompatible**</span><span class="sxs-lookup"><span data-stu-id="d854c-155">**IsSrkAuthCompatible**</span></span>](issrkauthcompatible-win32-tpm.md)                             | <span data-ttu-id="d854c-156">Indique si l’autorisation de clé racine de stockage (SRK) est compatible avec Windows.</span><span class="sxs-lookup"><span data-stu-id="d854c-156">Indicates whether the Storage Root Key (SRK) authorization is compatible with Windows.</span></span><br/>                                                                                           |
| [<span data-ttu-id="d854c-157">**RemoveBlockedCommand**</span><span class="sxs-lookup"><span data-stu-id="d854c-157">**RemoveBlockedCommand**</span></span>](removeblockedcommand-win32-tpm.md)                           | <span data-ttu-id="d854c-158">Supprime une commande TPM de la liste locale des commandes bloquées par Windows.</span><span class="sxs-lookup"><span data-stu-id="d854c-158">Removes a TPM command from the local list of commands blocked by Windows.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="d854c-159">**ResetAuthLockOut**</span><span class="sxs-lookup"><span data-stu-id="d854c-159">**ResetAuthLockOut**</span></span>](resetauthlockout-win32-tpm.md)                                   | <span data-ttu-id="d854c-160">Réinitialise le délai d’attente ou tout autre mécanisme que les fabricants de module de plateforme sécurisée implémentent pour se protéger contre les attaques par dictionnaire sur le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-160">Resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on the TPM.</span></span><br/>                                                 |
| [<span data-ttu-id="d854c-161">**ResetSrkAuth**</span><span class="sxs-lookup"><span data-stu-id="d854c-161">**ResetSrkAuth**</span></span>](resetsrkauth-win32-tpm.md)                                           | <span data-ttu-id="d854c-162">Réinitialise la valeur d’autorisation de la clé de racine de stockage (SRK) pour qu’elle soit compatible avec Windows.</span><span class="sxs-lookup"><span data-stu-id="d854c-162">Resets the Storage Root Key (SRK) authorization value to be compatible with Windows.</span></span><br/>                                                                                             |
| [<span data-ttu-id="d854c-163">**SelfTest**</span><span class="sxs-lookup"><span data-stu-id="d854c-163">**SelfTest**</span></span>](selftest-win32-tpm.md)                                                   | <span data-ttu-id="d854c-164">Effectue un test automatique du module de plateforme sécurisée et retourne le résultat.</span><span class="sxs-lookup"><span data-stu-id="d854c-164">Performs a self-test of the TPM and returns the result.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="d854c-165">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="d854c-165">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="d854c-166">Demande l’exécution d’une opération de présence physique TPM.</span><span class="sxs-lookup"><span data-stu-id="d854c-166">Requests a TPM physical presence operation to run.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="d854c-167">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="d854c-167">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)                                         | <span data-ttu-id="d854c-168">Installe un propriétaire pour le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-168">Installs an owner for the TPM.</span></span><br/>                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="d854c-169">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d854c-169">Properties</span></span>

<span data-ttu-id="d854c-170">La **classe \_ TPM Win32** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d854c-170">The **Win32\_Tpm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d854c-171">**IsActivated \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="d854c-171">**IsActivated\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d854c-172">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d854c-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d854c-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d854c-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d854c-174">Indique si le module de plateforme sécurisée est activé.</span><span class="sxs-lookup"><span data-stu-id="d854c-174">Indicates whether the TPM is activated.</span></span>

<span data-ttu-id="d854c-175">**true** si l’appareil est activé (autrement dit, si **isActivated \_ InitialValue** a la valeur true); sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d854c-175">**true** if the device is activated (that is, if **IsActivated\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="d854c-176">Cette valeur est stockée lorsque la classe est instanciée.</span><span class="sxs-lookup"><span data-stu-id="d854c-176">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="d854c-177">Il est possible que le module de plateforme sécurisée change d’État entre l’instanciation et lorsque vous vérifiez cette valeur.</span><span class="sxs-lookup"><span data-stu-id="d854c-177">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="d854c-178">Pour vérifier si le module de plateforme sécurisée est activé en temps réel, utilisez la méthode [**isActivated**](isactivated-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="d854c-178">To check whether the TPM is activated in real time, use the [**IsActivated**](isactivated-win32-tpm.md) method.</span></span>

<span data-ttu-id="d854c-179">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d854c-179">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="d854c-180">**IsEnabled \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="d854c-180">**IsEnabled\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d854c-181">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d854c-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d854c-182">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d854c-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d854c-183">Indique si le module de plateforme sécurisée est activé.</span><span class="sxs-lookup"><span data-stu-id="d854c-183">Indicates whether the TPM is enabled.</span></span>

<span data-ttu-id="d854c-184">**true** si l’appareil est activé (autrement dit, si **IsEnabled \_ InitialValue** a la valeur true); sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d854c-184">**true** if the device is enabled (that is, if **IsEnabled\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="d854c-185">Cette valeur est stockée lorsque la classe est instanciée.</span><span class="sxs-lookup"><span data-stu-id="d854c-185">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="d854c-186">Il est possible que le module de plateforme sécurisée change d’État entre l’instanciation et lorsque vous vérifiez cette valeur.</span><span class="sxs-lookup"><span data-stu-id="d854c-186">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="d854c-187">Pour vérifier si le module de plateforme sécurisée est activé en temps réel, utilisez la méthode [**IsEnabled**](isenabled-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="d854c-187">To check whether the TPM is enabled in real time, use the [**IsEnabled**](isenabled-win32-tpm.md) method.</span></span>

<span data-ttu-id="d854c-188">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d854c-188">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="d854c-189">**IsOwned \_ InitialValue**</span><span class="sxs-lookup"><span data-stu-id="d854c-189">**IsOwned\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d854c-190">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="d854c-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d854c-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d854c-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d854c-192">Indique si le module de plateforme sécurisée a un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="d854c-192">Indicates whether the TPM has an owner.</span></span>

<span data-ttu-id="d854c-193">**true** si l’appareil a un propriétaire (autrement dit, si **IsOwned \_ InitialValue** a la valeur true); sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d854c-193">**true** if the device has an owner (that is, if **IsOwned\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="d854c-194">Cette valeur est stockée lorsque la classe est instanciée.</span><span class="sxs-lookup"><span data-stu-id="d854c-194">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="d854c-195">Il est possible que le module de plateforme sécurisée change d’État entre l’instanciation et lorsque vous vérifiez cette valeur.</span><span class="sxs-lookup"><span data-stu-id="d854c-195">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="d854c-196">Pour vérifier si le module de plateforme sécurisée est détenu en temps réel, utilisez la méthode [**IsOwned**](isowned-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="d854c-196">To check whether the TPM is owned in real time, use the [**IsOwned**](isowned-win32-tpm.md) method.</span></span>

<span data-ttu-id="d854c-197">**Windows Server 2008 et Windows Vista :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="d854c-197">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="d854c-198">**ManufacturerId**</span><span class="sxs-lookup"><span data-stu-id="d854c-198">**ManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d854c-199">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d854c-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d854c-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d854c-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d854c-201">Informations d’identification qui renomment de façon unique le fabricant du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-201">The identifying information that uniquely names the TPM manufacturer.</span></span>

<span data-ttu-id="d854c-202">Lorsque les données ne sont pas disponibles, la valeur zéro est retournée.</span><span class="sxs-lookup"><span data-stu-id="d854c-202">When the data is unavailable, zero is returned.</span></span>

<span data-ttu-id="d854c-203">Cette valeur entière peut être convertie en valeur de chaîne en interprétant chaque octet comme un caractère ASCII.</span><span class="sxs-lookup"><span data-stu-id="d854c-203">This integer value can be translated to a string value by interpreting each byte as an ASCII character.</span></span> <span data-ttu-id="d854c-204">Par exemple, une valeur entière de 1414548736 peut être divisée en ces 4 octets : 0x54, 0x50, 0x4D et 0x00.</span><span class="sxs-lookup"><span data-stu-id="d854c-204">For example, an integer value of 1414548736 can be divided into these 4 bytes: 0x54, 0x50, 0x4D, and 0x00.</span></span> <span data-ttu-id="d854c-205">En supposant que la chaîne est interprétée de gauche à droite, cette valeur entière est convertie en valeur de chaîne « TPM ».</span><span class="sxs-lookup"><span data-stu-id="d854c-205">Assuming the string is interpreted from left to right, this integer value translated to a string value of "TPM".</span></span>

</dd> <dt>

<span data-ttu-id="d854c-206">**ManufacturerVersion**</span><span class="sxs-lookup"><span data-stu-id="d854c-206">**ManufacturerVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d854c-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d854c-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d854c-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d854c-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d854c-209">Version du module de plateforme sécurisée (TPM), telle que spécifiée par le fabricant.</span><span class="sxs-lookup"><span data-stu-id="d854c-209">The version of the TPM, as specified by the manufacturer.</span></span>

<span data-ttu-id="d854c-210">Lorsque les données ne sont pas disponibles, « non pris en charge » est retourné.</span><span class="sxs-lookup"><span data-stu-id="d854c-210">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="d854c-211">**ManufacturerVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="d854c-211">**ManufacturerVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d854c-212">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d854c-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d854c-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d854c-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d854c-214">Autres informations de version spécifiques au fabricant pour le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="d854c-214">Other manufacturer-specific version information for the TPM.</span></span>

<span data-ttu-id="d854c-215">Lorsque les données ne sont pas disponibles, « non pris en charge » est retourné.</span><span class="sxs-lookup"><span data-stu-id="d854c-215">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="d854c-216">**PhysicalPresenceVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="d854c-216">**PhysicalPresenceVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d854c-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d854c-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d854c-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d854c-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d854c-219">La version de l’interface de présence physique, un mécanisme de communication utilisé pour exécuter des opérations d’appareil qui nécessitent une présence physique, que l’ordinateur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="d854c-219">The version of the Physical Presence Interface, a communication mechanism used to run device operations that require physical presence, that the computer supports.</span></span>

<span data-ttu-id="d854c-220">Cette interface doit être disponible pour exécuter des opérations de présence physique TPM.</span><span class="sxs-lookup"><span data-stu-id="d854c-220">This interface must be available to run TPM physical presence operations.</span></span> <span data-ttu-id="d854c-221">Les **méthodes \_ TPM Win32** [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)et [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) exposent les fonctionnalités de l’interface de présence physique.</span><span class="sxs-lookup"><span data-stu-id="d854c-221">The **Win32\_Tpm** methods [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md), and [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) expose the capabilities of the Physical Presence Interface.</span></span>

<span data-ttu-id="d854c-222">Lorsque les données ne sont pas disponibles, « non pris en charge » est retourné.</span><span class="sxs-lookup"><span data-stu-id="d854c-222">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="d854c-223">**SpecVersion**</span><span class="sxs-lookup"><span data-stu-id="d854c-223">**SpecVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d854c-224">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="d854c-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d854c-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d854c-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d854c-226">Version de la spécification du Trusted Computing Group (TCG) que le module de plateforme sécurisée prend en charge.</span><span class="sxs-lookup"><span data-stu-id="d854c-226">The version of the Trusted Computing Group (TCG) specification that the TPM supports.</span></span> <span data-ttu-id="d854c-227">Cette valeur comprend la version principale et secondaire de la spécification TCG, le niveau de révision de la spécification et le niveau de révision de l’errata.</span><span class="sxs-lookup"><span data-stu-id="d854c-227">This value includes the major and minor TCG specification version, the specification revision level, and the errata revision level.</span></span> <span data-ttu-id="d854c-228">Toutes les valeurs sont au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="d854c-228">All values are in hexadecimal.</span></span> <span data-ttu-id="d854c-229">Par exemple, les informations de version « 1,2, 2, 0 » indiquent que l’appareil a été implémenté à la spécification TCG version 1,2, version de révision 2 et sans errata.</span><span class="sxs-lookup"><span data-stu-id="d854c-229">For example, a version information of "1.2, 2, 0" indicates that the device was implemented to TCG specification version 1.2, revision level 2, and with no errata.</span></span>

<span data-ttu-id="d854c-230">Lorsque les données ne sont pas disponibles, « non pris en charge » est retourné.</span><span class="sxs-lookup"><span data-stu-id="d854c-230">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d854c-231">Notes</span><span class="sxs-lookup"><span data-stu-id="d854c-231">Remarks</span></span>

<span data-ttu-id="d854c-232">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d854c-232">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d854c-233">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d854c-233">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d854c-234">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d854c-234">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d854c-235">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d854c-235">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d854c-236">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d854c-236">Requirements</span></span>



| <span data-ttu-id="d854c-237">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d854c-237">Requirement</span></span> | <span data-ttu-id="d854c-238">Valeur</span><span class="sxs-lookup"><span data-stu-id="d854c-238">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d854c-239">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d854c-239">Minimum supported client</span></span><br/> | <span data-ttu-id="d854c-240">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d854c-240">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d854c-241">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d854c-241">Minimum supported server</span></span><br/> | <span data-ttu-id="d854c-242">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d854c-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d854c-243">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d854c-243">Namespace</span></span><br/>                | <span data-ttu-id="d854c-244">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="d854c-244">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="d854c-245">MOF</span><span class="sxs-lookup"><span data-stu-id="d854c-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d854c-246"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="d854c-246"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="d854c-247">DLL</span><span class="sxs-lookup"><span data-stu-id="d854c-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d854c-248"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="d854c-248"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



 

 
