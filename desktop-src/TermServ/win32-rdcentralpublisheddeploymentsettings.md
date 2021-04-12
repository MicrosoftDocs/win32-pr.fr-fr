---
title: Classe Win32_RDCentralPublishedDeploymentSettings
description: Contient les paramètres de déploiement utilisés pour générer des fichiers RDP pour les ressources publiées à partir d’une batterie de serveurs.
ms.assetid: 6d1be0b2-e070-4c60-8068-b59ba121bf9f
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedDeploymentSettings de la classe Services Bureau à distance
- Win32_RDCentralPublishedDeploymentSettings de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedDeploymentSettings
- Win32_RDCentralPublishedDeploymentSettings.Caption
- Win32_RDCentralPublishedDeploymentSettings.Description
- Win32_RDCentralPublishedDeploymentSettings.InstallDate
- Win32_RDCentralPublishedDeploymentSettings.Name
- Win32_RDCentralPublishedDeploymentSettings.Status
- Win32_RDCentralPublishedDeploymentSettings.PublishingFarm
- Win32_RDCentralPublishedDeploymentSettings.Port
- Win32_RDCentralPublishedDeploymentSettings.FarmName
- Win32_RDCentralPublishedDeploymentSettings.GatewayUsage
- Win32_RDCentralPublishedDeploymentSettings.GatewayName
- Win32_RDCentralPublishedDeploymentSettings.GatewayAuthMode
- Win32_RDCentralPublishedDeploymentSettings.GatewayUseCachedCreds
- Win32_RDCentralPublishedDeploymentSettings.ColorBitDepth
- Win32_RDCentralPublishedDeploymentSettings.AllowFontSmoothing
- Win32_RDCentralPublishedDeploymentSettings.UseMultimon
- Win32_RDCentralPublishedDeploymentSettings.RedirectionOptions
- Win32_RDCentralPublishedDeploymentSettings.HasCertificate
- Win32_RDCentralPublishedDeploymentSettings.CertificateHash
- Win32_RDCentralPublishedDeploymentSettings.CustomRDPSettings
- Win32_RDCentralPublishedDeploymentSettings.DeploymentRDPSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4dd1b118f2fabf22f10e47c0b8467b0ddf6388
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385163"
---
# <a name="win32_rdcentralpublisheddeploymentsettings-class"></a><span data-ttu-id="5fc6c-105">\_Classe RDCentralPublishedDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="5fc6c-105">Win32\_RDCentralPublishedDeploymentSettings class</span></span>

<span data-ttu-id="5fc6c-106">Contient les paramètres de déploiement utilisés pour générer des fichiers RDP pour les ressources publiées à partir d’une batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-106">Contains the deployment settings used to generate RDP files for resources published from a farm.</span></span>

<span data-ttu-id="5fc6c-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc6c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fc6c-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="5fc6c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5fc6c-109">Members</span></span>

<span data-ttu-id="5fc6c-110">La classe **Win32 \_ RDCentralPublishedDeploymentSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5fc6c-110">The **Win32\_RDCentralPublishedDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="5fc6c-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5fc6c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fc6c-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5fc6c-112">Properties</span></span>

<span data-ttu-id="5fc6c-113">La classe **Win32 \_ RDCentralPublishedDeploymentSettings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-113">The **Win32\_RDCentralPublishedDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5fc6c-114">**AllowFontSmoothing**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-115">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-117">**true** pour autoriser le lissage des polices ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-117">**true** to allow font smoothing; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fc6c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-122">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="5fc6c-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5fc6c-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-124">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-124">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-125">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-127">Certificat utilisé pour signer les fichiers RDP ; nécessairement uniquement si *HasCertificate* a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-127">The certificate used to sign the RDP files; necessarily only if *HasCertificate* is true.</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-128">**ColorBitDepth**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-128">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-129">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-130">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-131">Contient la profondeur de bit de couleur :</span><span class="sxs-lookup"><span data-stu-id="5fc6c-131">Contains the color bit depth:</span></span>

<dt>

<span id="4"></span>

<span data-ttu-id="5fc6c-132">**4** ()</span><span class="sxs-lookup"><span data-stu-id="5fc6c-132">**4** ()</span></span>


</dt> <dd></dd> <dt>

<span id="8"></span>

<span data-ttu-id="5fc6c-133">**8** ()</span><span class="sxs-lookup"><span data-stu-id="5fc6c-133">**8** ()</span></span>


</dt> <dd></dd> <dt>

<span id="15"></span>

<span data-ttu-id="5fc6c-134">**15** ()</span><span class="sxs-lookup"><span data-stu-id="5fc6c-134">**15** ()</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="5fc6c-135">**16** ()</span><span class="sxs-lookup"><span data-stu-id="5fc6c-135">**16** ()</span></span>


</dt> <dd></dd> <dt>

<span id="24"></span>

<span data-ttu-id="5fc6c-136">**24** ()</span><span class="sxs-lookup"><span data-stu-id="5fc6c-136">**24** ()</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="5fc6c-137">**32** ()</span><span class="sxs-lookup"><span data-stu-id="5fc6c-137">**32** ()</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5fc6c-138">**CustomRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-138">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-140">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-140">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-141">Contient le contenu du fichier RDP correspondant aux paramètres RDP personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-141">Contains the contents of the RDP file corresponding to the custom RDP settings.</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-142">**DeploymentRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-142">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-143">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-144">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-144">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-145">Contient le contenu du fichier RDP correspondant aux paramètres de déploiement.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-145">Contains the contents of the RDP file corresponding to the deployment settings.</span></span> <span data-ttu-id="5fc6c-146">Si ce paramètre est défini, le système utilise ce fichier RDP et ignore les autres paramètres RDP de cet appel.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-146">If this parameter is set, the system will use this RDP file, and ignore the other RDP settings in this call.</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-147">**Description**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-147">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-148">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fc6c-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-150">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-150">Description of the object.</span></span>

<span data-ttu-id="5fc6c-151">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5fc6c-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-152">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-152">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-154">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-155">Nom de la batterie de serveurs.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-155">The name of the farm.</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-156">**GatewayAuthMode**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-156">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-157">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-158">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-159">Contient le mode d’authentification de la passerelle :</span><span class="sxs-lookup"><span data-stu-id="5fc6c-159">Contains the gateway authentication mode:</span></span>

<dt>

<span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>

<span data-ttu-id="5fc6c-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Mot de passe (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-160"><span id="Password_0_"></span><span id="password_0_"></span><span id="PASSWORD_0_"></span>**Password(0)** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>

<span data-ttu-id="5fc6c-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Carte à puce (1)** (1)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-161"><span id="Smartcard_1_"></span><span id="smartcard_1_"></span><span id="SMARTCARD_1_"></span>**Smartcard(1)** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>

<span data-ttu-id="5fc6c-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Autoriser l’utilisateur à choisir (4)** (4)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-162"><span id="Allow_User_to_Choose_4_"></span><span id="allow_user_to_choose_4_"></span><span id="ALLOW_USER_TO_CHOOSE_4_"></span>**Allow User to Choose(4)** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5fc6c-163">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-163">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-165">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-166">Le nom de la passerelle.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-166">The name of the gateway.</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-167">**GatewayUsage**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-167">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-168">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-169">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-170">Décrit l’utilisation de la passerelle :</span><span class="sxs-lookup"><span data-stu-id="5fc6c-170">Describes how the gateway is used:</span></span>

<dt>

<span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>

<span data-ttu-id="5fc6c-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**Nogateway** (0)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-171"><span id="NoGateway"></span><span id="nogateway"></span><span id="NOGATEWAY"></span>**NoGateway** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5fc6c-172">Aucune passerelle.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-172">No gateway.</span></span>

</dd> <dt>

<span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>

<span data-ttu-id="5fc6c-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-173"><span id="UseGatewayBypassLocal"></span><span id="usegatewaybypasslocal"></span><span id="USEGATEWAYBYPASSLOCAL"></span>**UseGatewayBypassLocal** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5fc6c-174">Utilisez la passerelle Pass-the-local.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-174">Use gateway pass by local.</span></span>

</dd> <dt>

<span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>

<span data-ttu-id="5fc6c-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-175"><span id="UseGateway"></span><span id="usegateway"></span><span id="USEGATEWAY"></span>**UseGateway** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5fc6c-176">Utilisez la passerelle.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-176">Use gateway.</span></span>

</dd> <dt>

<span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>

<span data-ttu-id="5fc6c-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-177"><span id="DetectGateway"></span><span id="detectgateway"></span><span id="DETECTGATEWAY"></span>**DetectGateway** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5fc6c-178">Détectez la passerelle.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-178">Detect gateway.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5fc6c-179">**GatewayUseCachedCreds**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-179">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-180">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-181">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-182">**true** pour utiliser les mêmes informations d’identification utilisateur pour la passerelle TS et le serveur TS dans la mesure du possible ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-182">**true** to use the same user credentials for TS gateway and TS server when possible; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-183">**HasCertificate**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-183">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-184">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-185">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-185">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-186">**true** pour utiliser un certificat pour signer les fichiers RDP ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-186">**true** to use a certificate to sign the RDP files; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-187">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-187">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-188">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-188">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fc6c-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-190">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="5fc6c-190">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-191">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-191">The date the object was installed.</span></span> <span data-ttu-id="5fc6c-192">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-192">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="5fc6c-193">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5fc6c-193">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-194">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-194">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-195">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-196">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fc6c-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-197">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-197">The name of the object.</span></span>

<span data-ttu-id="5fc6c-198">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5fc6c-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-199">**Port**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-199">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-200">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-200">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-201">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-202">Port RDP.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-202">The RDP port.</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-203">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-203">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-204">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-205">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-206">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-207">Alias de la batterie de serveurs qui a publié l’application.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-207">The alias of the farm that published the application.</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-208">**RedirectionOptions**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-208">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-209">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-209">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-210">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-211">Options de redirection :</span><span class="sxs-lookup"><span data-stu-id="5fc6c-211">Redirection Options:</span></span>

<dt>

<span data-ttu-id="5fc6c-212">0</span><span class="sxs-lookup"><span data-stu-id="5fc6c-212">0</span></span>
</dt> <dd>

<span data-ttu-id="5fc6c-213">Aucune</span><span class="sxs-lookup"><span data-stu-id="5fc6c-213">None</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-214">1</span><span class="sxs-lookup"><span data-stu-id="5fc6c-214">1</span></span>
</dt> <dd>

<span data-ttu-id="5fc6c-215">Lecteurs</span><span class="sxs-lookup"><span data-stu-id="5fc6c-215">Drives</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-216">2</span><span class="sxs-lookup"><span data-stu-id="5fc6c-216">2</span></span>
</dt> <dd>

<span data-ttu-id="5fc6c-217">Imprimantes</span><span class="sxs-lookup"><span data-stu-id="5fc6c-217">Printers</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-218">4</span><span class="sxs-lookup"><span data-stu-id="5fc6c-218">4</span></span>
</dt> <dd>

<span data-ttu-id="5fc6c-219">Presse-papiers</span><span class="sxs-lookup"><span data-stu-id="5fc6c-219">Clipboard</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-220">8</span><span class="sxs-lookup"><span data-stu-id="5fc6c-220">8</span></span>
</dt> <dd>

<span data-ttu-id="5fc6c-221">Plug-and-play</span><span class="sxs-lookup"><span data-stu-id="5fc6c-221">Plug and Play</span></span>

</dd> <dt>

<span data-ttu-id="5fc6c-222">16</span><span class="sxs-lookup"><span data-stu-id="5fc6c-222">16</span></span>
</dt> <dd>

<span data-ttu-id="5fc6c-223">Carte à puce</span><span class="sxs-lookup"><span data-stu-id="5fc6c-223">Smart Card</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5fc6c-224">**État**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-224">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-225">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-226">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5fc6c-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-227">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-227">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-228">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-228">Current status of the object.</span></span> <span data-ttu-id="5fc6c-229">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-229">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5fc6c-230">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="5fc6c-230">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5fc6c-231">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="5fc6c-231">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5fc6c-232">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-232">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5fc6c-233">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-233">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5fc6c-234">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5fc6c-234">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="5fc6c-235">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-235">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5fc6c-236">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-236">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5fc6c-237">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-237">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5fc6c-238">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="5fc6c-238">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5fc6c-239">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-239">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5fc6c-240">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-240">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5fc6c-241">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-241">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="5fc6c-242">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="5fc6c-242">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5fc6c-243">**UseMultimon**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-243">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc6c-244">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5fc6c-244">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5fc6c-245">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5fc6c-245">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5fc6c-246">**true** pour activer multi-Monitor pour le bureau (et non rail); Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="5fc6c-246">**true** to enable multi-monitor for desktop (not RAIL); otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fc6c-247">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5fc6c-247">Requirements</span></span>



| <span data-ttu-id="5fc6c-248">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fc6c-248">Requirement</span></span> | <span data-ttu-id="5fc6c-249">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fc6c-249">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc6c-250">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fc6c-250">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc6c-251">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fc6c-251">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5fc6c-252">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fc6c-252">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc6c-253">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5fc6c-253">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="5fc6c-254">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5fc6c-254">Namespace</span></span><br/>                | <span data-ttu-id="5fc6c-255">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="5fc6c-255">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5fc6c-256">MOF</span><span class="sxs-lookup"><span data-stu-id="5fc6c-256">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fc6c-257"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fc6c-257"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="5fc6c-258">DLL</span><span class="sxs-lookup"><span data-stu-id="5fc6c-258">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fc6c-259"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fc6c-259"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

