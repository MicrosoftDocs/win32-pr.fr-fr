---
title: Classe Win32_TSGeneralSetting
description: Représente les paramètres généraux du terminal, tels que le niveau de chiffrement et le protocole de transport.
ms.assetid: a31d68c0-e446-4d78-85e0-5173e7870255
ms.tgt_platform: multiple
keywords:
- Win32_TSGeneralSetting de la classe Services Bureau à distance
- Win32_TSGeneralSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting
- Win32_TSGeneralSetting.Caption
- Win32_TSGeneralSetting.Description
- Win32_TSGeneralSetting.InstallDate
- Win32_TSGeneralSetting.Name
- Win32_TSGeneralSetting.Status
- Win32_TSGeneralSetting.TerminalName
- Win32_TSGeneralSetting.CertificateName
- Win32_TSGeneralSetting.Certificates
- Win32_TSGeneralSetting.Comment
- Win32_TSGeneralSetting.MinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceMinEncryptionLevel
- Win32_TSGeneralSetting.PolicySourceSecurityLayer
- Win32_TSGeneralSetting.PolicySourceUserAuthenticationRequired
- Win32_TSGeneralSetting.SecurityLayer
- Win32_TSGeneralSetting.SSLCertificateSHA1Hash
- Win32_TSGeneralSetting.SSLCertificateSHA1HashType
- Win32_TSGeneralSetting.TerminalProtocol
- Win32_TSGeneralSetting.Transport
- Win32_TSGeneralSetting.UserAuthenticationRequired
- Win32_TSGeneralSetting.WindowsAuthentication
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172f18bbddd364d74dfcfb00e7e665628267af36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741773"
---
# <a name="win32_tsgeneralsetting-class"></a><span data-ttu-id="20aaf-105">\_Classe TSGeneralSetting Win32</span><span class="sxs-lookup"><span data-stu-id="20aaf-105">Win32\_TSGeneralSetting class</span></span>

<span data-ttu-id="20aaf-106">La classe WMI **\_ TSGeneralSetting** WMI représente les paramètres généraux du terminal, tels que le niveau de chiffrement et le protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="20aaf-106">The **Win32\_TSGeneralSetting** WMI class represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

<span data-ttu-id="20aaf-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="20aaf-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="20aaf-108">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="20aaf-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="20aaf-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20aaf-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSGENERALSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSGeneralSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   CertificateName;
  uint8    Certificates[];
  string   Comment;
  uint32   MinEncryptionLevel;
  uint32   PolicySourceMinEncryptionLevel;
  uint32   PolicySourceSecurityLayer;
  uint32   PolicySourceUserAuthenticationRequired;
  uint32   SecurityLayer;
  string   SSLCertificateSHA1Hash;
  uint32   SSLCertificateSHA1HashType;
  string   TerminalProtocol;
  string   Transport;
  uint32   UserAuthenticationRequired;
  uint32   WindowsAuthentication;
};
```

## <a name="members"></a><span data-ttu-id="20aaf-110">Membres</span><span class="sxs-lookup"><span data-stu-id="20aaf-110">Members</span></span>

<span data-ttu-id="20aaf-111">La classe **Win32 \_ TSGeneralSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="20aaf-111">The **Win32\_TSGeneralSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="20aaf-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="20aaf-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="20aaf-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20aaf-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="20aaf-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="20aaf-114">Methods</span></span>

<span data-ttu-id="20aaf-115">La classe **Win32 \_ TSGeneralSetting** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="20aaf-115">The **Win32\_TSGeneralSetting** class has these methods.</span></span>



| <span data-ttu-id="20aaf-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="20aaf-116">Method</span></span>                                                                                        | <span data-ttu-id="20aaf-117">Description</span><span class="sxs-lookup"><span data-stu-id="20aaf-117">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20aaf-118">**SetEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="20aaf-118">**SetEncryptionLevel**</span></span>](win32-tsgeneralsetting-setencryptionlevel.md)                       | <span data-ttu-id="20aaf-119">Définit le niveau de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="20aaf-119">Sets the encryption level.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="20aaf-120">**SetSecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="20aaf-120">**SetSecurityLayer**</span></span>](win32-tsgeneralsetting-setsecuritylayer.md)                           | <span data-ttu-id="20aaf-121">Définit la couche de sécurité sur l’une des « couches de sécurité RDP » (0), « Negotiate » (1) ou « SSL » (2).</span><span class="sxs-lookup"><span data-stu-id="20aaf-121">Sets the security layer to one of "RDP Security Layer" (0), "Negotiate" (1), or "SSL" (2).</span></span><br/>                                                                   |
| [<span data-ttu-id="20aaf-122">**SetUserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="20aaf-122">**SetUserAuthenticationRequired**</span></span>](setuserauthenticationrequired-win32-tsgeneralsetting.md) | <span data-ttu-id="20aaf-123">Active ou désactive l’exigence selon laquelle les utilisateurs doivent être authentifiés au moment de la connexion en définissant la valeur de la propriété **UserAuthenticationRequired** .</span><span class="sxs-lookup"><span data-stu-id="20aaf-123">Enables or disables the requirement that users must be authenticated at connection time by setting the value of the **UserAuthenticationRequired** property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="20aaf-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="20aaf-124">Properties</span></span>

<span data-ttu-id="20aaf-125">La classe **Win32 \_ TSGeneralSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="20aaf-125">The **Win32\_TSGeneralSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20aaf-126">**Caption**</span><span class="sxs-lookup"><span data-stu-id="20aaf-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-127">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20aaf-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-128">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-129">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="20aaf-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-130">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="20aaf-130">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="20aaf-131">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20aaf-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-132">**CertificateName**</span><span class="sxs-lookup"><span data-stu-id="20aaf-132">**CertificateName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20aaf-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-135">Nom d’affichage du nom d’objet du certificat personnel de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="20aaf-135">Display name for the local computer personal certificate subject name.</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-136">**Certificates**</span><span class="sxs-lookup"><span data-stu-id="20aaf-136">**Certificates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-137">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="20aaf-137">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-139">Contient un magasin de certificats sérialisés qui contient tous les certificats du magasin de **comptes My User** sur l’ordinateur qui sont des certificats de serveur valides pour une utilisation avec SSL (Secure Sockets Layer).</span><span class="sxs-lookup"><span data-stu-id="20aaf-139">Contains a serialized certificate store that contains all of the certificates from the **My user account** store on the computer that are valid server certificates for use with secure sockets layer (SSL).</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-140">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="20aaf-140">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-141">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20aaf-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-142">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="20aaf-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-143">Nom descriptif de la combinaison couche de session et protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="20aaf-143">Descriptive name of the combination of session layer and transport protocol.</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-144">**Description**</span><span class="sxs-lookup"><span data-stu-id="20aaf-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20aaf-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-147">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="20aaf-147">Description of the object.</span></span>

<span data-ttu-id="20aaf-148">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20aaf-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="20aaf-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-150">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="20aaf-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-152">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="20aaf-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-153">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="20aaf-153">The date the object was installed.</span></span> <span data-ttu-id="20aaf-154">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="20aaf-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="20aaf-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20aaf-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-156">**MinEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="20aaf-156">**MinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20aaf-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-159">Qualificateurs : **faible** («seules les données envoyées du client au serveur sont protégées par un chiffrement basé sur la puissance de clé standard du serveur.</span><span class="sxs-lookup"><span data-stu-id="20aaf-159">Qualifiers: **Low** ("Only data sent from client to server is protected by encryption based on server's standard key strength.</span></span> <span data-ttu-id="20aaf-160">Les données envoyées du serveur au client ne sont pas protégées.»), **moyenne** (« toutes les données envoyées entre le serveur et le client sont protégées par un chiffrement basé sur la puissance de clé standard du serveur »), **élevé** (« toutes les données envoyées entre le serveur et le client sont protégées par le niveau de clé maximal de onserver basé sur le chiffrement. »)</span><span class="sxs-lookup"><span data-stu-id="20aaf-160">Data sent from Server to client is not protected."), **Medium** ("All data sent between Server and client is protected by encryption based on server's standard key strength."), **High** ("All data sent between Server and client is protected by encryption based onserver's maximum key strength.")</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-161">Niveau de chiffrement minimal.</span><span class="sxs-lookup"><span data-stu-id="20aaf-161">The minimum encryption level.</span></span>

<dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="20aaf-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Faible** (1)</span><span class="sxs-lookup"><span data-stu-id="20aaf-162"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (1)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-163">Niveau de chiffrement faible.</span><span class="sxs-lookup"><span data-stu-id="20aaf-163">Low level of encryption.</span></span> <span data-ttu-id="20aaf-164">Seules les données envoyées du client au serveur sont chiffrées à l’aide du chiffrement 56 bits.</span><span class="sxs-lookup"><span data-stu-id="20aaf-164">Only data sent from the client to the server is encrypted using 56-bit encryption.</span></span> <span data-ttu-id="20aaf-165">Sachez que les données envoyées du serveur au client ne sont pas chiffrées.</span><span class="sxs-lookup"><span data-stu-id="20aaf-165">Be aware that data sent from the server to the client is not encrypted.</span></span>

</dd> <dt>

<span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>

<span data-ttu-id="20aaf-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Compatible moyenne/client** (2)</span><span class="sxs-lookup"><span data-stu-id="20aaf-166"><span id="Medium___Client_Compatible"></span><span id="medium___client_compatible"></span><span id="MEDIUM___CLIENT_COMPATIBLE"></span>**Medium / Client Compatible** (2)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-167">Niveau de chiffrement compatible avec le client.</span><span class="sxs-lookup"><span data-stu-id="20aaf-167">Client compatible level of encryption.</span></span> <span data-ttu-id="20aaf-168">Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées au niveau de clé maximal pris en charge par le client.</span><span class="sxs-lookup"><span data-stu-id="20aaf-168">All data sent from client to server and from server to client is encrypted at the maximum key strength supported by the client.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="20aaf-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Élevé** (3)</span><span class="sxs-lookup"><span data-stu-id="20aaf-169"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (3)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-170">Niveau élevé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="20aaf-170">High level of encryption.</span></span> <span data-ttu-id="20aaf-171">Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées à l’aide d’un chiffrement 128 bits puissant.</span><span class="sxs-lookup"><span data-stu-id="20aaf-171">All data sent from client to server and from server to client is encrypted using strong 128-bit encryption.</span></span> <span data-ttu-id="20aaf-172">Les clients qui ne prennent pas en charge ce niveau de chiffrement ne peuvent pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="20aaf-172">Clients that do not support this level of encryption cannot connect.</span></span>

</dd> <dt>

<span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>

<span data-ttu-id="20aaf-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**Compatible FIPS** (4)</span><span class="sxs-lookup"><span data-stu-id="20aaf-173"><span id="FIPS_Compliant"></span><span id="fips_compliant"></span><span id="FIPS_COMPLIANT"></span>**FIPS Compliant** (4)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-174">Chiffrement compatible FIPS.</span><span class="sxs-lookup"><span data-stu-id="20aaf-174">FIPS compliant encryption.</span></span> <span data-ttu-id="20aaf-175">Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées et déchiffrées avec les algorithmes de chiffrement normes FIPS (Federal Information Processing Standard) (FIPS) à l’aide des modules de chiffrement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="20aaf-175">All data sent from client to server and from server to client is encrypted and decrypted with the Federal Information Processing Standard (FIPS) encryption algorithms using the Microsoft cryptographic modules.</span></span> <span data-ttu-id="20aaf-176">FIPS est une norme intitulée « exigences de sécurité pour les modules cryptographiques ».</span><span class="sxs-lookup"><span data-stu-id="20aaf-176">FIPS is a standard entitled "Security Requirements for Cryptographic Modules".</span></span> <span data-ttu-id="20aaf-177">FIPS 140-1 (1994) et FIPS 140-2 (2001) décrivent les exigences gouvernementales pour les modules de chiffrement matériels et logiciels utilisés au sein du gouvernement des États-Unis.</span><span class="sxs-lookup"><span data-stu-id="20aaf-177">FIPS 140-1 (1994) and FIPS 140-2 (2001) describe government requirements for hardware and software cryptographic modules used within the U.S. government.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20aaf-178">**Nom**</span><span class="sxs-lookup"><span data-stu-id="20aaf-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20aaf-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-181">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="20aaf-181">The name of the object.</span></span>

<span data-ttu-id="20aaf-182">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20aaf-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-183">**PolicySourceMinEncryptionLevel**</span><span class="sxs-lookup"><span data-stu-id="20aaf-183">**PolicySourceMinEncryptionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-184">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20aaf-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-186">Indique si la propriété **MinEncryptionLevel** est configurée par le serveur, par la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="20aaf-186">Indicates whether the **MinEncryptionLevel** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="20aaf-187">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="20aaf-187">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-188">Serveur</span><span class="sxs-lookup"><span data-stu-id="20aaf-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-189">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="20aaf-189">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-190">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="20aaf-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-191">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="20aaf-191">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-192">Default</span><span class="sxs-lookup"><span data-stu-id="20aaf-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20aaf-193">**PolicySourceSecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="20aaf-193">**PolicySourceSecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-194">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20aaf-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-196">Indique si la propriété **securitylayer** est configurée par le serveur, par la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="20aaf-196">Indicates whether the **SecurityLayer** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="20aaf-197">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="20aaf-197">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-198">Serveur</span><span class="sxs-lookup"><span data-stu-id="20aaf-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-199">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="20aaf-199">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-200">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="20aaf-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-201">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="20aaf-201">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-202">Default</span><span class="sxs-lookup"><span data-stu-id="20aaf-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20aaf-203">**PolicySourceUserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="20aaf-203">**PolicySourceUserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-204">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20aaf-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-206">Indique si la propriété **UserAuthenticationRequired** est configurée par le serveur, par la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="20aaf-206">Indicates whether the **UserAuthenticationRequired** property is configured by the server, by group policy, or by default.</span></span>

<dt>

<span data-ttu-id="20aaf-207">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="20aaf-207">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-208">Serveur</span><span class="sxs-lookup"><span data-stu-id="20aaf-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-209">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="20aaf-209">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-210">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="20aaf-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-211">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="20aaf-211">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-212">Default</span><span class="sxs-lookup"><span data-stu-id="20aaf-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20aaf-213">**SecurityLayer**</span><span class="sxs-lookup"><span data-stu-id="20aaf-213">**SecurityLayer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-214">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20aaf-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-216">Qualificateurs : **RDPSecurityLayer** (« couche de sécurité RDP : communication entre le serverand le client utilise le chiffrement RDP natif. »), **Negotiate** («la couche la plus sécurisée prise en charge par le client sera utilisée. S’il est pris en charge, TLS 1,0 sera utilisé.»), **SSL** («SSL (TLS 1,0) sera utilisé pour l’authentification du serveur et forencrypting toutes les données transférées entre le serveur et le client. Ce paramètre requiert que le serveur dispose d’un certificat compatible SSL.»), **NEWTBD** (« une nouvelle couche de sécurité dans LONGHORN ».)</span><span class="sxs-lookup"><span data-stu-id="20aaf-216">Qualifiers: **RDPSecurityLayer** ("RDP Security Layer: Communication between the serverand the client will use native RDP encryption."), **Negotiate** ("The most secure layer that is supported by the client will be used.If supported, TLS 1.0 will be used."), **SSL** ("SSL (TLS 1.0) will be used for server authentication as well as forencrypting all data transferred between the server and the client.This setting requires the server to have an SSL compatible certificate."), **NEWTBD** ("A NEW SECURITY LAYER in LONGHORN.")</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-217">Spécifie la couche de sécurité utilisée entre le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="20aaf-217">Specifies the security layer used between the client and server.</span></span>

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span data-ttu-id="20aaf-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Couche de sécurité RDP** (1)</span><span class="sxs-lookup"><span data-stu-id="20aaf-218"><span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**RDP Security Layer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-219">La communication entre le serveur et le client utilise le chiffrement RDP natif.</span><span class="sxs-lookup"><span data-stu-id="20aaf-219">Communication between the server and the client uses native RDP encryption.</span></span>

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="20aaf-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Négocier** (2)</span><span class="sxs-lookup"><span data-stu-id="20aaf-220"><span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (2)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-221">La couche la plus sécurisée prise en charge par le client est utilisée.</span><span class="sxs-lookup"><span data-stu-id="20aaf-221">The most secure layer that is supported by the client is used.</span></span> <span data-ttu-id="20aaf-222">S’il est pris en charge, SSL (TLS 1,0) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="20aaf-222">If supported, SSL (TLS 1.0) is used.</span></span>

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span data-ttu-id="20aaf-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span><span class="sxs-lookup"><span data-stu-id="20aaf-223"><span id="SSL"></span><span id="ssl"></span>**SSL** (3)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-224">SSL (TLS 1,0) est utilisé pour l’authentification du serveur et pour le chiffrement de toutes les données transférées entre le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="20aaf-224">SSL (TLS 1.0) is used for server authentication and for encrypting all data transferred between the server and the client.</span></span> <span data-ttu-id="20aaf-225">Ce paramètre requiert que le serveur dispose d’un certificat compatible SSL.</span><span class="sxs-lookup"><span data-stu-id="20aaf-225">This setting requires the server to have an SSL-compatible certificate.</span></span> <span data-ttu-id="20aaf-226">Ce paramètre n’est pas compatible avec une valeur **MinEncryptionLevel** de 1.</span><span class="sxs-lookup"><span data-stu-id="20aaf-226">This setting is not compatible with a **MinEncryptionLevel** value of 1.</span></span>

</dd> <dt>

<span id="NEWTBD"></span><span id="newtbd"></span>

<span data-ttu-id="20aaf-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span><span class="sxs-lookup"><span data-stu-id="20aaf-227"><span id="NEWTBD"></span><span id="newtbd"></span>**NEWTBD** (4)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-228">Nouvelle couche de sécurité.</span><span class="sxs-lookup"><span data-stu-id="20aaf-228">A new security layer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20aaf-229">**SSLCertificateSHA1Hash**</span><span class="sxs-lookup"><span data-stu-id="20aaf-229">**SSLCertificateSHA1Hash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-230">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20aaf-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-231">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="20aaf-231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-232">Spécifie le hachage SHA1 au format hexadécimal du certificat SSL à utiliser par le serveur cible.</span><span class="sxs-lookup"><span data-stu-id="20aaf-232">Specifies the SHA1 hash in hexadecimal format of the SSL certificate for the target server to use.</span></span>

<span data-ttu-id="20aaf-233">L’empreinte numérique d’un certificat peut être trouvée à l’aide du composant logiciel enfichable Certificats de la console MMC sous l’onglet Détails de la page Propriétés du certificat.</span><span class="sxs-lookup"><span data-stu-id="20aaf-233">The thumbprint of a certificate may be found using the Certificates MMC snap-in on the Details tab of the certificate properties page.</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-234">**SSLCertificateSHA1HashType**</span><span class="sxs-lookup"><span data-stu-id="20aaf-234">**SSLCertificateSHA1HashType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-235">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20aaf-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-236">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-237">Indique l’état de la propriété **SSLCertificateSHA1Hash** .</span><span class="sxs-lookup"><span data-stu-id="20aaf-237">Indicates the state of the **SSLCertificateSHA1Hash** property.</span></span>

<dt>

<span data-ttu-id="20aaf-238">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="20aaf-238">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-239">Non valide</span><span class="sxs-lookup"><span data-stu-id="20aaf-239">Not valid</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-240">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="20aaf-240">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-241">Auto-signé par défaut</span><span class="sxs-lookup"><span data-stu-id="20aaf-241">Default self-signed</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-242">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="20aaf-242">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-243">Stratégie de groupe par défaut appliquée</span><span class="sxs-lookup"><span data-stu-id="20aaf-243">Default group policy enforced</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-244">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="20aaf-244">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="20aaf-245">Custom</span><span class="sxs-lookup"><span data-stu-id="20aaf-245">Custom</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20aaf-246">**État**</span><span class="sxs-lookup"><span data-stu-id="20aaf-246">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-247">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20aaf-247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-249">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="20aaf-249">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-250">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="20aaf-250">Current status of the object.</span></span> <span data-ttu-id="20aaf-251">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="20aaf-251">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="20aaf-252">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="20aaf-252">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="20aaf-253">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="20aaf-253">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="20aaf-254">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="20aaf-254">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="20aaf-255">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="20aaf-255">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="20aaf-256">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="20aaf-256">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="20aaf-257">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="20aaf-257">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20aaf-258">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="20aaf-258">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20aaf-259">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="20aaf-259">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20aaf-260">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="20aaf-260">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20aaf-261">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="20aaf-261">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20aaf-262">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="20aaf-262">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20aaf-263">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="20aaf-263">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="20aaf-264">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="20aaf-264">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="20aaf-265">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="20aaf-265">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-266">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20aaf-266">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-267">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-267">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-268">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="20aaf-268">The name of the terminal.</span></span>

<span data-ttu-id="20aaf-269">Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="20aaf-269">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-270">**TerminalProtocol**</span><span class="sxs-lookup"><span data-stu-id="20aaf-270">**TerminalProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-271">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20aaf-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-272">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-273">Nom du protocole de couche session ; par exemple, Microsoft RDP 5,0.</span><span class="sxs-lookup"><span data-stu-id="20aaf-273">The name of the session layer protocol; for example, Microsoft RDP 5.0.</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-274">**Transport**</span><span class="sxs-lookup"><span data-stu-id="20aaf-274">**Transport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-275">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="20aaf-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-276">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-277">Type de transport utilisé dans la connexion ; par exemple, TCP, NetBIOS ou IPX/SPX.</span><span class="sxs-lookup"><span data-stu-id="20aaf-277">The type of transport used in the connection; for example, TCP, NetBIOS, or IPX/SPX.</span></span>

</dd> <dt>

<span data-ttu-id="20aaf-278">**UserAuthenticationRequired**</span><span class="sxs-lookup"><span data-stu-id="20aaf-278">**UserAuthenticationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-279">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20aaf-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="20aaf-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-281">Spécifie le type d’authentification utilisateur utilisé pour les connexions à distance.</span><span class="sxs-lookup"><span data-stu-id="20aaf-281">Specifies the type of user authentication used for remote connections.</span></span> <span data-ttu-id="20aaf-282">Si la valeur est 1, ce qui signifie qu’elle est activée, **UserAuthenticationRequired** nécessite l’authentification de l’utilisateur au moment de la connexion pour augmenter la protection du serveur contre les attaques réseau.</span><span class="sxs-lookup"><span data-stu-id="20aaf-282">If set to 1, which means enabled, **UserAuthenticationRequired** requires user authentication at connection time to increase server protection against network attacks.</span></span> <span data-ttu-id="20aaf-283">Seuls les clients [protocole RDP (Remote Desktop Protocol)](remote-desktop-protocol.md) (RDP) qui prennent en charge le protocole rdp version 6,0 ou une version ultérieure sont en mesure de se connecter.</span><span class="sxs-lookup"><span data-stu-id="20aaf-283">Only [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) clients that support RDP version 6.0 or higher are able to connect.</span></span> <span data-ttu-id="20aaf-284">Pour éviter les interruptions pour les utilisateurs distants, il est recommandé de déployer les clients RDP qui prennent en charge la version de protocole appropriée avant d’activer la propriété.</span><span class="sxs-lookup"><span data-stu-id="20aaf-284">To avoid disruptions for remote users, it is recommended that you deploy RDP clients supporting the appropriate protocol version before you enable the property.</span></span>

<span data-ttu-id="20aaf-285">Utilisez la méthode [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) pour activer ou désactiver cette propriété.</span><span class="sxs-lookup"><span data-stu-id="20aaf-285">Use the [**SetUserAuthenticationRequired**](setuserauthenticationrequired-win32-tsgeneralsetting.md) method to enable or disable this property.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="20aaf-286"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="20aaf-286"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-287">L’authentification de l’utilisateur au niveau de la connexion est désactivée.</span><span class="sxs-lookup"><span data-stu-id="20aaf-287">User authentication at connection is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="20aaf-288"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="20aaf-288"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-289">L’authentification utilisateur à la connexion est activée.</span><span class="sxs-lookup"><span data-stu-id="20aaf-289">User authentication at connection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="20aaf-290">**WindowsAuthentication**</span><span class="sxs-lookup"><span data-stu-id="20aaf-290">**WindowsAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20aaf-291">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20aaf-291">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="20aaf-292">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="20aaf-292">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="20aaf-293">Spécifie si la connexion est définie par défaut sur le processus d’authentification Windows standard ou sur un autre package d’authentification qui a été installé sur le système.</span><span class="sxs-lookup"><span data-stu-id="20aaf-293">Specifies whether the connection defaults to the standard Windows authentication process or to another authentication package that has been installed on the system.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="20aaf-294"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="20aaf-294"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-295">N’utilise pas par défaut le processus d’authentification Windows standard.</span><span class="sxs-lookup"><span data-stu-id="20aaf-295">Does not default to the standard Windows authentication process.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="20aaf-296"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="20aaf-296"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="20aaf-297">La valeur par défaut est le processus d’authentification Windows standard.</span><span class="sxs-lookup"><span data-stu-id="20aaf-297">Defaults to the standard Windows authentication process.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20aaf-298">Notes</span><span class="sxs-lookup"><span data-stu-id="20aaf-298">Remarks</span></span>

<span data-ttu-id="20aaf-299">Sachez que les stations Windows qui ne sont pas associées à la session de console ne peuvent pas accéder aux méthodes et aux propriétés de cette classe.</span><span class="sxs-lookup"><span data-stu-id="20aaf-299">Be aware that window stations not associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="20aaf-300">Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété TerminalName, les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="20aaf-300">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="20aaf-301">Ce code d’erreur est également renvoyé si une station Windows tente d’appeler des méthodes de cet objet dans le but d’ajouter ou de modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="20aaf-301">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="20aaf-302">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="20aaf-302">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="20aaf-303">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="20aaf-303">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="20aaf-304">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="20aaf-304">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="20aaf-305">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="20aaf-305">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="20aaf-306">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="20aaf-306">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="20aaf-307">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="20aaf-307">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="20aaf-308">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="20aaf-308">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="20aaf-309">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="20aaf-309">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="20aaf-310">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20aaf-310">Requirements</span></span>



| <span data-ttu-id="20aaf-311">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20aaf-311">Requirement</span></span> | <span data-ttu-id="20aaf-312">Valeur</span><span class="sxs-lookup"><span data-stu-id="20aaf-312">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="20aaf-313">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20aaf-313">Minimum supported client</span></span><br/> | <span data-ttu-id="20aaf-314">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20aaf-314">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="20aaf-315">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20aaf-315">Minimum supported server</span></span><br/> | <span data-ttu-id="20aaf-316">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20aaf-316">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="20aaf-317">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="20aaf-317">Namespace</span></span><br/>                | <span data-ttu-id="20aaf-318">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="20aaf-318">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="20aaf-319">MOF</span><span class="sxs-lookup"><span data-stu-id="20aaf-319">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20aaf-320"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20aaf-320"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="20aaf-321">DLL</span><span class="sxs-lookup"><span data-stu-id="20aaf-321">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20aaf-322"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20aaf-322"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20aaf-323">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20aaf-323">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20aaf-324">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="20aaf-324">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

