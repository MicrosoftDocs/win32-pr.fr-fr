---
description: Représente les paramètres pour le service de réplication sur un hôte de récupération. Les propriétés de cette classe ne peuvent pas être modifiées directement. Le client doit appeler la \_ méthode MSVM ReplicationService. ModifyServiceSettings pour modifier l’une de ces propriétés.
ms.assetid: a0c0b45a-3578-412a-910e-cd4b3ff0e262
title: Classe Msvm_ReplicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationServiceSettingData
- Msvm_ReplicationServiceSettingData.InstanceID
- Msvm_ReplicationServiceSettingData.Caption
- Msvm_ReplicationServiceSettingData.Description
- Msvm_ReplicationServiceSettingData.ElementName
- Msvm_ReplicationServiceSettingData.RecoveryServerEnabled
- Msvm_ReplicationServiceSettingData.AllowedAuthenticationType
- Msvm_ReplicationServiceSettingData.CertificateThumbPrint
- Msvm_ReplicationServiceSettingData.HttpsPort
- Msvm_ReplicationServiceSettingData.HttpPort
- Msvm_ReplicationServiceSettingData.MonitoringStartTime
- Msvm_ReplicationServiceSettingData.MonitoringInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e2886529ab74fed52ec0c6077bfa3d9222fca55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866121"
---
# <a name="msvm_replicationservicesettingdata-class"></a><span data-ttu-id="4bfa1-105">MSVM \_ ReplicationServiceSettingData, classe</span><span class="sxs-lookup"><span data-stu-id="4bfa1-105">Msvm\_ReplicationServiceSettingData class</span></span>

<span data-ttu-id="4bfa1-106">Représente les paramètres pour le service de réplication sur un hôte de récupération.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-106">Represents the settings for the replication service on a recovery host.</span></span> <span data-ttu-id="4bfa1-107">Les propriétés de cette classe ne peuvent pas être modifiées directement.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="4bfa1-108">Le client doit appeler la méthode [**MSVM \_ ReplicationService. ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) pour modifier l’une de ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-108">The client must call the [**Msvm\_ReplicationService.ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="4bfa1-109">La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bfa1-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bfa1-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Replication Service Settings";
  string   Description = "Virtual Machine Replication Service Settings Data";
  string   ElementName = "Replication Service Settings";
  boolean  RecoveryServerEnabled = False;
  uint16   AllowedAuthenticationType = 0;
  string   CertificateThumbPrint;
  uint16   HttpsPort = 443;
  uint16   HttpPort = 80;
  datetime MonitoringStartTime;
  uint32   MonitoringInterval = 43200;
};
```

## <a name="members"></a><span data-ttu-id="4bfa1-111">Membres</span><span class="sxs-lookup"><span data-stu-id="4bfa1-111">Members</span></span>

<span data-ttu-id="4bfa1-112">La classe **MSVM \_ ReplicationServiceSettingData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4bfa1-112">The **Msvm\_ReplicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4bfa1-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4bfa1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4bfa1-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4bfa1-114">Properties</span></span>

<span data-ttu-id="4bfa1-115">La classe **MSVM \_ ReplicationServiceSettingData** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-115">The **Msvm\_ReplicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4bfa1-116">**AllowedAuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-116">**AllowedAuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-117">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-119">Définir les modes d’authentification autorisés pour la connexion au serveur hôte de récupération.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-119">Define authentication modes allowed for connecting to recovery host server.</span></span>

<dt>

<span data-ttu-id="4bfa1-120">0</span><span class="sxs-lookup"><span data-stu-id="4bfa1-120">0</span></span>
</dt> <dd>

<span data-ttu-id="4bfa1-121">Non défini.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-121">Not defined.</span></span>

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="4bfa1-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Authentification Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="4bfa1-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4bfa1-123">Authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-123">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="4bfa1-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Authentification basée sur les certificats** (2)</span><span class="sxs-lookup"><span data-stu-id="4bfa1-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4bfa1-125">Authentification basée sur les certificats.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-125">Certificate based authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="4bfa1-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Authentification basée sur les certificats et authentification Kerberos** (3)</span><span class="sxs-lookup"><span data-stu-id="4bfa1-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Certificate based authentication and kerberos authentication** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4bfa1-127">L’authentification basée sur les certificats et l’authentification intégrée.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-127">Both certificate based authentication and integrated authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4bfa1-128">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-131">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-131">A short description of the object.</span></span> <span data-ttu-id="4bfa1-132">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du service de réplication ».</span><span class="sxs-lookup"><span data-stu-id="4bfa1-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="4bfa1-133">**Empreinte**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-133">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-136">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="4bfa1-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-137">Empreinte de certificat à utiliser lorsque **AuthenticationType** est l’authentification basée sur les certificats.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-137">Certificate thumbprint to use when **AuthenticationType** is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="4bfa1-138">**Description**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-141">Description de l'objet .</span><span class="sxs-lookup"><span data-stu-id="4bfa1-141">A description of the object.</span></span> <span data-ttu-id="4bfa1-142">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « données des paramètres de réplication de l’ordinateur virtuel ».</span><span class="sxs-lookup"><span data-stu-id="4bfa1-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="4bfa1-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-146">Nom complet de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-146">A display name for the object.</span></span> <span data-ttu-id="4bfa1-147">Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)et est toujours définie sur « paramètres du service de réplication ».</span><span class="sxs-lookup"><span data-stu-id="4bfa1-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="4bfa1-148">**HttpPort**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-148">**HttpPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-149">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-151">Numéro de port du serveur de récupération à utiliser lors de l’acceptation d’une connexion non sécurisée pour la réplication.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-151">Recovery server port number to use when accepting a nonsecure connection for replication.</span></span> <span data-ttu-id="4bfa1-152">La valeur par défaut est 80.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-152">The default value is 80.</span></span>

</dd> <dt>

<span data-ttu-id="4bfa1-153">**HttpsPort**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-153">**HttpsPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-154">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-155">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-156">Numéro de port du serveur de récupération à utiliser lors de l’acceptation d’une connexion sécurisée pour la réplication.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-156">Recovery server port number to use when accepting secure connection for replication.</span></span> <span data-ttu-id="4bfa1-157">La valeur par défaut est 443.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-157">The default value is 443.</span></span>

</dd> <dt>

<span data-ttu-id="4bfa1-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-161">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-162">Identifie de façon unique une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4bfa1-163">Cette propriété est héritée de la [**\_ SettingData CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4bfa1-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4bfa1-164">**MonitoringInterval**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-164">**MonitoringInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-167">Intervalle, en secondes, auquel les statistiques de réplication doivent être réinitialisées.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-167">The interval, in seconds, at which replication statistics should be reset.</span></span> <span data-ttu-id="4bfa1-168">L’intervalle par défaut est de 12 heures (43200 secondes).</span><span class="sxs-lookup"><span data-stu-id="4bfa1-168">The default interval is 12 hours (43200 seconds).</span></span> <span data-ttu-id="4bfa1-169">La valeur minimale valide est de 60 minutes (3600 secondes) et la valeur maximale valide est de 7 jours (604800 secondes).</span><span class="sxs-lookup"><span data-stu-id="4bfa1-169">The minimum valid value is 60 minutes (3600 seconds), and the maximum valid value is 7 days (604800 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="4bfa1-170">**MonitoringStartTime**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-170">**MonitoringStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-171">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-173">Heure de début de la surveillance de la réplication, en UTC.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-173">The start time for replication monitoring, in UTC.</span></span> <span data-ttu-id="4bfa1-174">La valeur par défaut est 9:00 A.M., heure locale, représentée au format UTC.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-174">The default value is 9:00 A.M., local time, represented in UTC.</span></span> <span data-ttu-id="4bfa1-175">Les éléments date de l’objet **DateTime** doivent être nuls.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-175">The date elements of the **datetime** object must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4bfa1-176">**RecoveryServerEnabled**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-176">**RecoveryServerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bfa1-177">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4bfa1-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bfa1-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bfa1-179">Spécifie si l’hôte Hyper-V est activé en tant que serveur de récupération.</span><span class="sxs-lookup"><span data-stu-id="4bfa1-179">Specifies whether the Hyper-V host is enabled as a recovery server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4bfa1-180">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bfa1-180">Requirements</span></span>



| <span data-ttu-id="4bfa1-181">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bfa1-181">Requirement</span></span> | <span data-ttu-id="4bfa1-182">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bfa1-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfa1-183">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bfa1-183">Minimum supported client</span></span><br/> | <span data-ttu-id="4bfa1-184">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bfa1-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4bfa1-185">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bfa1-185">Minimum supported server</span></span><br/> | <span data-ttu-id="4bfa1-186">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4bfa1-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4bfa1-187">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4bfa1-187">Namespace</span></span><br/>                | <span data-ttu-id="4bfa1-188">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="4bfa1-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4bfa1-189">MOF</span><span class="sxs-lookup"><span data-stu-id="4bfa1-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bfa1-190"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa1-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bfa1-191">DLL</span><span class="sxs-lookup"><span data-stu-id="4bfa1-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bfa1-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4bfa1-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4bfa1-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bfa1-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfa1-194">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-194">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="4bfa1-195">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="4bfa1-195">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

