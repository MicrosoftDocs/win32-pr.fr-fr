---
description: Représente les paramètres pour les services Terminal Server des ordinateurs virtuels sur un ordinateur hôte.
ms.assetid: 1f8d0718-09da-4231-95eb-cc63b6f324dd
title: Classe Msvm_TerminalServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalServiceSettingData
- Msvm_TerminalServiceSettingData.InstanceID
- Msvm_TerminalServiceSettingData.Caption
- Msvm_TerminalServiceSettingData.Description
- Msvm_TerminalServiceSettingData.ElementName
- Msvm_TerminalServiceSettingData.ListenerPort
- Msvm_TerminalServiceSettingData.DisableSelfSignedCertificateGeneration
- Msvm_TerminalServiceSettingData.AuthCertificateHash
- Msvm_TerminalServiceSettingData.TrustedIssuerCertificateHashes
- Msvm_TerminalServiceSettingData.AllowedHashAlgorithms
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27d98971c847eab5042823e8a1524051a15fd679
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753557"
---
# <a name="msvm_terminalservicesettingdata-class"></a><span data-ttu-id="dee3f-103">MSVM \_ TerminalServiceSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="dee3f-103">Msvm\_TerminalServiceSettingData class</span></span>

<span data-ttu-id="dee3f-104">Représente les paramètres pour les services Terminal Server des ordinateurs virtuels sur un ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="dee3f-104">Represents the settings for the virtual computer terminal services on a host.</span></span> <span data-ttu-id="dee3f-105">Les propriétés de cette classe ne peuvent pas être modifiées directement.</span><span class="sxs-lookup"><span data-stu-id="dee3f-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="dee3f-106">Le client doit appeler la méthode [**MSVM \_ TerminalService. ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) pour modifier l’une de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="dee3f-106">The client must call the [**Msvm\_TerminalService.ModifyServiceSettings**](modifyservicesettings-msvm-terminalservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="dee3f-107">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="dee3f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dee3f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dee3f-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption = "Hyper-V Terminal Service Settings";
  string  Description = "Settings for the Hyper-V Terminal Service";
  string  ElementName = "Hyper-V Terminal Service Settings";
  uint32  ListenerPort;
  boolean DisableSelfSignedCertificateGeneration;
  uint8   AuthCertificateHash[];
  string  TrustedIssuerCertificateHashes[];
  string  AllowedHashAlgorithms[];
};
```

## <a name="members"></a><span data-ttu-id="dee3f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="dee3f-109">Members</span></span>

<span data-ttu-id="dee3f-110">La classe **MSVM \_ TerminalServiceSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="dee3f-110">The **Msvm\_TerminalServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="dee3f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dee3f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dee3f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dee3f-112">Properties</span></span>

<span data-ttu-id="dee3f-113">La classe **MSVM \_ TerminalServiceSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="dee3f-113">The **Msvm\_TerminalServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dee3f-114">**AllowedHashAlgorithms**</span><span class="sxs-lookup"><span data-stu-id="dee3f-114">**AllowedHashAlgorithms**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee3f-115">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="dee3f-115">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dee3f-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dee3f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee3f-117">Liste des algorithmes de hachage acceptés pour vérifier la signature des jetons d’authentification fédérée.</span><span class="sxs-lookup"><span data-stu-id="dee3f-117">The list of hash algorithms accepted for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="dee3f-118">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="dee3f-118">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="dee3f-119">**AuthCertificateHash**</span><span class="sxs-lookup"><span data-stu-id="dee3f-119">**AuthCertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee3f-120">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="dee3f-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dee3f-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dee3f-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee3f-122">Hachage du certificat à utiliser pour l’authentification distante.</span><span class="sxs-lookup"><span data-stu-id="dee3f-122">The hash of the certificate to use for remote authentication.</span></span>

</dd> <dt>

<span data-ttu-id="dee3f-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="dee3f-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee3f-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dee3f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee3f-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dee3f-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee3f-126">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dee3f-126">A short description of the object.</span></span> <span data-ttu-id="dee3f-127">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dee3f-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dee3f-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="dee3f-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee3f-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dee3f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee3f-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dee3f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee3f-131">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="dee3f-131">A description of the object.</span></span> <span data-ttu-id="dee3f-132">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dee3f-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dee3f-133">**DisableSelfSignedCertificateGeneration**</span><span class="sxs-lookup"><span data-stu-id="dee3f-133">**DisableSelfSignedCertificateGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee3f-134">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="dee3f-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="dee3f-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dee3f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee3f-136">Désactive la génération de certificats auto-signés.</span><span class="sxs-lookup"><span data-stu-id="dee3f-136">Disables self-signed certificate generation.</span></span>

</dd> <dt>

<span data-ttu-id="dee3f-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="dee3f-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee3f-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dee3f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee3f-139">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dee3f-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee3f-140">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dee3f-140">A display name for the object.</span></span> <span data-ttu-id="dee3f-141">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dee3f-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dee3f-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dee3f-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee3f-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="dee3f-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dee3f-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dee3f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dee3f-145">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="dee3f-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="dee3f-146">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="dee3f-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="dee3f-147">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="dee3f-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="dee3f-148">**ListenerPort**</span><span class="sxs-lookup"><span data-stu-id="dee3f-148">**ListenerPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee3f-149">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dee3f-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="dee3f-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dee3f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee3f-151">Port réseau sur lequel la connexion de session à distance initiale sera établie.</span><span class="sxs-lookup"><span data-stu-id="dee3f-151">The network port on which the initial remote session connection will be made.</span></span>

</dd> <dt>

<span data-ttu-id="dee3f-152">**TrustedIssuerCertificateHashes**</span><span class="sxs-lookup"><span data-stu-id="dee3f-152">**TrustedIssuerCertificateHashes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dee3f-153">Type de données : tableau de **chaînes**</span><span class="sxs-lookup"><span data-stu-id="dee3f-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dee3f-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="dee3f-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dee3f-155">Liste des hachages de certificat de l’émetteur approuvé pour vérifier la signature des jetons d’authentification fédérés.</span><span class="sxs-lookup"><span data-stu-id="dee3f-155">The list of trusted issuer certificate hashes for verifying the signature of federated authentication tokens.</span></span>

<span data-ttu-id="dee3f-156">**Windows 8.1 :** Cette valeur n’est pas prise en charge tant que Windows 8.1 et Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="dee3f-156">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dee3f-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dee3f-157">Requirements</span></span>



| <span data-ttu-id="dee3f-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dee3f-158">Requirement</span></span> | <span data-ttu-id="dee3f-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="dee3f-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dee3f-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dee3f-160">Minimum supported client</span></span><br/> | <span data-ttu-id="dee3f-161">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dee3f-161">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="dee3f-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dee3f-162">Minimum supported server</span></span><br/> | <span data-ttu-id="dee3f-163">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dee3f-163">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dee3f-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dee3f-164">Namespace</span></span><br/>                | <span data-ttu-id="dee3f-165">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="dee3f-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="dee3f-166">MOF</span><span class="sxs-lookup"><span data-stu-id="dee3f-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dee3f-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dee3f-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dee3f-168">DLL</span><span class="sxs-lookup"><span data-stu-id="dee3f-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dee3f-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dee3f-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

