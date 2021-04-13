---
title: Classe Win32_TSDeploymentSettings
description: Définit les paramètres par défaut utilisés par la Gestionnaire RemoteApp lors de la création de fichiers protocole RDP (Remote Desktop Protocol) (RDP).
ms.assetid: b3eeef86-e6cb-40ea-99f8-200c5993f31e
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentSettings de la classe Services Bureau à distance
- Win32_TSDeploymentSettings de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSDeploymentSettings
- Win32_TSDeploymentSettings.Caption
- Win32_TSDeploymentSettings.Description
- Win32_TSDeploymentSettings.InstallDate
- Win32_TSDeploymentSettings.Name
- Win32_TSDeploymentSettings.Status
- Win32_TSDeploymentSettings.Port
- Win32_TSDeploymentSettings.FarmName
- Win32_TSDeploymentSettings.GatewayUsage
- Win32_TSDeploymentSettings.GatewayName
- Win32_TSDeploymentSettings.GatewayAuthMode
- Win32_TSDeploymentSettings.GatewayUseCachedCreds
- Win32_TSDeploymentSettings.RequireServerAuth
- Win32_TSDeploymentSettings.ColorBitDepth
- Win32_TSDeploymentSettings.AllowFontSmoothing
- Win32_TSDeploymentSettings.UseMultimon
- Win32_TSDeploymentSettings.RedirectionOptions
- Win32_TSDeploymentSettings.HasCertificate
- Win32_TSDeploymentSettings.CertificateHash
- Win32_TSDeploymentSettings.CertificateIssuedTo
- Win32_TSDeploymentSettings.CertificateIssuedBy
- Win32_TSDeploymentSettings.CertificateExpiresOn
- Win32_TSDeploymentSettings.CustomRDPSettings
- Win32_TSDeploymentSettings.DeploymentRDPSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f254363968099ab73c5f3f14f1f15ab8554f62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465091"
---
# <a name="win32_tsdeploymentsettings-class"></a><span data-ttu-id="e0f7f-105">\_Classe TSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="e0f7f-105">Win32\_TSDeploymentSettings class</span></span>

<span data-ttu-id="e0f7f-106">Définit les paramètres par défaut utilisés par la Gestionnaire RemoteApp lors de la création de fichiers protocole RDP (Remote Desktop Protocol) (RDP).</span><span class="sxs-lookup"><span data-stu-id="e0f7f-106">Defines the default settings that the RemoteApp Manager uses when creating Remote Desktop Protocol (RDP) files.</span></span> <span data-ttu-id="e0f7f-107">Ces paramètres n’affectent pas les applications ou les ordinateurs de bureau publiés.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-107">These settings do not affect any published applications or desktops.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f7f-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0f7f-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentSettings : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Port;
  string   FarmName;
  sint32   GatewayUsage;
  string   GatewayName;
  sint32   GatewayAuthMode;
  boolean  GatewayUseCachedCreds;
  boolean  RequireServerAuth;
  sint32   ColorBitDepth;
  boolean  AllowFontSmoothing;
  boolean  UseMultimon;
  sint32   RedirectionOptions;
  boolean  HasCertificate;
  uint8    CertificateHash[];
  string   CertificateIssuedTo;
  string   CertificateIssuedBy;
  string   CertificateExpiresOn;
  string   CustomRDPSettings;
  string   DeploymentRDPSettings;
};
```

## <a name="members"></a><span data-ttu-id="e0f7f-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e0f7f-109">Members</span></span>

<span data-ttu-id="e0f7f-110">La classe **Win32 \_ TSDeploymentSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e0f7f-110">The **Win32\_TSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="e0f7f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0f7f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0f7f-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e0f7f-112">Properties</span></span>

<span data-ttu-id="e0f7f-113">La classe **Win32 \_ TSDeploymentSettings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-113">The **Win32\_TSDeploymentSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0f7f-114">**AllowFontSmoothing**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-114">**AllowFontSmoothing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-115">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-115">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-116">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-117">Indique s’il faut autoriser le lissage des polices.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-117">Indicates whether to allow font smoothing.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-119">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-120">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0f7f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-121">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e0f7f-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-122">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="e0f7f-123">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0f7f-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-124">**CertificateExpiresOn**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-124">**CertificateExpiresOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-126">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-127">Date d’expiration du certificat.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-127">The date that the certificate expires on.</span></span> <span data-ttu-id="e0f7f-128">Cette valeur est stockée sous la forme d’un format [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-128">This value is stored as a 64-bit [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) format.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-129">**CertificateHash**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-129">**CertificateHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-130">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-131">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-131">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-132">Empreinte numérique du certificat utilisé pour signer les fichiers RDP.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-132">The thumbprint of the certificate that is used to sign RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-133">**CertificateIssuedBy**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-133">**CertificateIssuedBy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-134">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-135">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-136">Spécifie à qui le certificat est émis.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-136">Specifies who the certificate is issued by.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-137">**CertificateIssuedTo**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-137">**CertificateIssuedTo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-140">Spécifie à qui le certificat est émis.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-140">Specifies who the certificate is issued to.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-141">**ColorBitDepth**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-141">**ColorBitDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-142">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-143">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-144">Profondeur de bit de couleur de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-144">The color bit depth of the display.</span></span> <span data-ttu-id="e0f7f-145">Les valeurs possibles sont 4, 8, 15, 16, 24 et 32.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-145">Possible values are 4, 8, 15, 16, 24, and 32.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-146">**CustomRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-146">**CustomRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-148">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-148">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-149">Contenu du fichier RDP qui correspond aux paramètres RDP personnalisés dans Gestionnaire RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-149">The contents of the RDP file that correspond to the Custom RDP Settings in RemoteApp Manager.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-150">**DeploymentRDPSettings**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-150">**DeploymentRDPSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-152">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-152">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-153">Contenu du fichier RDP qui correspond aux paramètres de déploiement dans Gestionnaire RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-153">The contents of the RDP file that correspond to the deployment settings in RemoteApp Manager.</span></span> <span data-ttu-id="e0f7f-154">Si cette valeur est définie, les paramètres de déploiement RDP remplacent les paramètres par défaut de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-154">If this value is set, the RDP deployment settings supersede the default settings in this class.</span></span> <span data-ttu-id="e0f7f-155">Par exemple, si vous définissez la propriété **GatewayAuthMode** dans cette classe et que vous définissez la propriété **DeploymentRDPSettings** , la propriété **GatewayAuthMode** de cette classe sera ignorée et la valeur **GatewayAuthMode** de la **DeploymentRDPSettings** sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-155">For example, if you set the **GatewayAuthMode** property in this class, and set the **DeploymentRDPSettings** property, the **GatewayAuthMode** property from this class will be ignored and the **GatewayAuthMode** value from the **DeploymentRDPSettings** will be used.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-156">**Description**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-156">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0f7f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-159">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-159">Description of the object.</span></span>

<span data-ttu-id="e0f7f-160">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0f7f-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-161">**FarmName**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-161">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-164">Nom du serveur hôte de session Bureau à distance ou nom de domaine complet (FQDN) de la batterie de serveurs hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-164">The name of the RD Session Host server, or the fully qualified domain name (FQDN) of the RD Session Host server farm.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-165">**GatewayAuthMode**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-165">**GatewayAuthMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-166">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-166">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-167">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-168">Méthode d’authentification de la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-168">The RD Gateway authentication method.</span></span> <span data-ttu-id="e0f7f-169">Les valeurs suivantes sont possibles.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-169">The following values are possible.</span></span>

<dt>

<span data-ttu-id="e0f7f-170">0</span><span class="sxs-lookup"><span data-stu-id="e0f7f-170">0</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-171">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="e0f7f-171">Password</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-172">1</span><span class="sxs-lookup"><span data-stu-id="e0f7f-172">1</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-173">Carte à puce</span><span class="sxs-lookup"><span data-stu-id="e0f7f-173">Smart card</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-174">4</span><span class="sxs-lookup"><span data-stu-id="e0f7f-174">4</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-175">Autoriser l’utilisateur à effectuer une sélection pendant la connexion.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-175">Allow user to select during connection.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e0f7f-176">**GatewayName**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-176">**GatewayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-178">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-179">Nom du serveur de passerelle Bureau à distance à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-179">The name of the RD Gateway server to use.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-180">**GatewayUsage**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-180">**GatewayUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-181">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-181">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-182">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-183">Indique s’il faut utiliser un serveur de passerelle Bureau à distance pour se connecter au serveur hôte de session Bureau à distance cible à travers un pare-feu.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-183">Indicates whether to use an RD Gateway server to connect to the target RD Session Host server across a firewall.</span></span> <span data-ttu-id="e0f7f-184">Les valeurs suivantes sont possibles.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-184">The following values are possible.</span></span>

<dt>

<span data-ttu-id="e0f7f-185">0</span><span class="sxs-lookup"><span data-stu-id="e0f7f-185">0</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-186">N’utilisez pas de serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-186">Do not use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-187">1</span><span class="sxs-lookup"><span data-stu-id="e0f7f-187">1</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-188">Utilisez un serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-188">Use an RD Gateway server.</span></span> <span data-ttu-id="e0f7f-189">Contournez le serveur de passerelle Bureau à distance pour les adresses locales.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-189">Bypass the RD Gateway server for local addresses.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-190">2</span><span class="sxs-lookup"><span data-stu-id="e0f7f-190">2</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-191">Utilisez un serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-191">Use an RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-192">3</span><span class="sxs-lookup"><span data-stu-id="e0f7f-192">3</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-193">Détecter automatiquement les paramètres du serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-193">Automatically detect RD Gateway server settings.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e0f7f-194">**GatewayUseCachedCreds**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-194">**GatewayUseCachedCreds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-195">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-195">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-196">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-196">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-197">Dans la mesure du possible, utilisez les mêmes informations d’identification de l’utilisateur pour le serveur de passerelle Bureau à distance et le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-197">When possible, use the same user credentials for the RD Gateway server and the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-198">**HasCertificate**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-198">**HasCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-199">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-200">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-200">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-201">Indique s’il faut utiliser un certificat pour signer les fichiers RDP.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-201">Indicates whether to use a certificate to sign the RDP files.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-202">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-202">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-203">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-203">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-204">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0f7f-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-205">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="e0f7f-205">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-206">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-206">The date the object was installed.</span></span> <span data-ttu-id="e0f7f-207">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-207">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e0f7f-208">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0f7f-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-209">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-209">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-210">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-211">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0f7f-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-212">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-212">The name of the object.</span></span>

<span data-ttu-id="e0f7f-213">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0f7f-213">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-214">**Port**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-214">**Port**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-215">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-215">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-216">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-216">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-217">Port RDP à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-217">The RDP port to use.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-218">**RedirectionOptions**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-218">**RedirectionOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-219">Type de données : **sint32**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-220">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-221">Spécifie les options de redirection des appareils et des ressources pour les connexions RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-221">Specifies the device and resource redirection options for RemoteApp connections.</span></span> <span data-ttu-id="e0f7f-222">Les indicateurs pour **RedirectionOptions** peuvent être combinés.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-222">Flags for **RedirectionOptions** can be combined.</span></span> <span data-ttu-id="e0f7f-223">Les valeurs suivantes sont possibles.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-223">The following values are possible.</span></span>

<dt>

<span data-ttu-id="e0f7f-224">0</span><span class="sxs-lookup"><span data-stu-id="e0f7f-224">0</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-225">Aucune redirection de l’appareil ou de la ressource.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-225">No device or resource redirection.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-226">1</span><span class="sxs-lookup"><span data-stu-id="e0f7f-226">1</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-227">Rediriger les lecteurs de disque.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-227">Redirect disk drives.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-228">2</span><span class="sxs-lookup"><span data-stu-id="e0f7f-228">2</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-229">Rediriger les imprimantes.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-229">Redirect printers.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-230">4</span><span class="sxs-lookup"><span data-stu-id="e0f7f-230">4</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-231">Redirigez le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-231">Redirect the Clipboard.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-232">8</span><span class="sxs-lookup"><span data-stu-id="e0f7f-232">8</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-233">Redirigez les appareils Plug-and-Play pris en charge.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-233">Redirect supported Plug and Play devices.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-234">16</span><span class="sxs-lookup"><span data-stu-id="e0f7f-234">16</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-235">Rediriger les cartes à puce.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-235">Redirect smart cards.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-236">32</span><span class="sxs-lookup"><span data-stu-id="e0f7f-236">32</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-237">Rediriger l’audio.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-237">Redirect audio.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-238">64</span><span class="sxs-lookup"><span data-stu-id="e0f7f-238">64</span></span>
</dt> <dd>

<span data-ttu-id="e0f7f-239">Rediriger les ports série.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-239">Redirect serial ports.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e0f7f-240">**RequireServerAuth**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-240">**RequireServerAuth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-241">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-241">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-242">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-242">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-243">Indique s’il faut exiger l’authentification du serveur.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-243">Indicates whether to require server authentication.</span></span>

</dd> <dt>

<span data-ttu-id="e0f7f-244">**État**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-244">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-245">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-246">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e0f7f-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-247">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="e0f7f-247">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-248">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-248">Current status of the object.</span></span> <span data-ttu-id="e0f7f-249">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-249">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="e0f7f-250">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="e0f7f-250">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="e0f7f-251">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="e0f7f-251">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e0f7f-252">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-252">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e0f7f-253">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-253">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e0f7f-254">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0f7f-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="e0f7f-255">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="e0f7f-255">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0f7f-256">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="e0f7f-256">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0f7f-257">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="e0f7f-257">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0f7f-258">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="e0f7f-258">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0f7f-259">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="e0f7f-259">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0f7f-260">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="e0f7f-260">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0f7f-261">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="e0f7f-261">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="e0f7f-262">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="e0f7f-262">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="e0f7f-263">**UseMultimon**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-263">**UseMultimon**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0f7f-264">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="e0f7f-264">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e0f7f-265">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="e0f7f-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e0f7f-266">Indique si plusieurs analyses sont activées pour le bureau.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-266">Indicates if multiple monitors are enabled for the desktop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e0f7f-267">Notes</span><span class="sxs-lookup"><span data-stu-id="e0f7f-267">Remarks</span></span>

<span data-ttu-id="e0f7f-268">Vous devez être membre du groupe administrateurs pour définir des propriétés à l’aide de cette classe.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-268">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="e0f7f-269">Si **RequireServerAuth** a la valeur **true**, tenez compte des points suivants :</span><span class="sxs-lookup"><span data-stu-id="e0f7f-269">If **RequireServerAuth** is set to **TRUE**, consider the following:</span></span>

-   <span data-ttu-id="e0f7f-270">Si le programme RemoteApp est destiné à une utilisation intranet et que tous les ordinateurs clients exécutent Windows Server 2008 ou Windows Vista, vous n’avez pas besoin de configurer le serveur hôte de session Bureau à distance pour utiliser un certificat SSL.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-270">If the RemoteApp program is for intranet use, and all client computers are running either Windows Server 2008 or Windows Vista, you do not have to configure the RD Session Host server to use an SSL certificate.</span></span> <span data-ttu-id="e0f7f-271">Dans ce cas, Authentification au niveau du réseau est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-271">In this case, Network Level Authentication is used.</span></span>
-   <span data-ttu-id="e0f7f-272">Vous devez spécifier le nom de domaine complet du serveur ou de la batterie de serveurs pour la valeur de la propriété **FarmName** .</span><span class="sxs-lookup"><span data-stu-id="e0f7f-272">You must specify the FQDN of the server or farm for the value of the **FarmName** property.</span></span>

<span data-ttu-id="e0f7f-273">Pour se connecter à l’espace de noms « CIMV2 \\ licences TS », le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-273">To connect to the "CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="e0f7f-274">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**, qui peut être défini à l’aide de la fonction com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="e0f7f-274">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="e0f7f-275">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-275">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="e0f7f-276">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-276">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="e0f7f-277">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="e0f7f-277">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e0f7f-278">Ils sont installés sur l’ordinateur lorsque vous ajoutez le rôle associé.</span><span class="sxs-lookup"><span data-stu-id="e0f7f-278">They are installed on the computer when you add the associated role.</span></span> <span data-ttu-id="e0f7f-279">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="e0f7f-279">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f7f-280">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0f7f-280">Requirements</span></span>



| <span data-ttu-id="e0f7f-281">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0f7f-281">Requirement</span></span> | <span data-ttu-id="e0f7f-282">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0f7f-282">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f7f-283">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0f7f-283">Minimum supported client</span></span><br/> | <span data-ttu-id="e0f7f-284">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0f7f-284">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e0f7f-285">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0f7f-285">Minimum supported server</span></span><br/> | <span data-ttu-id="e0f7f-286">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0f7f-286">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0f7f-287">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="e0f7f-287">Namespace</span></span><br/>                | <span data-ttu-id="e0f7f-288">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="e0f7f-288">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e0f7f-289">MOF</span><span class="sxs-lookup"><span data-stu-id="e0f7f-289">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0f7f-290"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0f7f-290"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="e0f7f-291">DLL</span><span class="sxs-lookup"><span data-stu-id="e0f7f-291">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0f7f-292"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0f7f-292"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

