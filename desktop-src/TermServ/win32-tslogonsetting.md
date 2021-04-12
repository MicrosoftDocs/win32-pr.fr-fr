---
title: Classe Win32_TSLogonSetting
description: Définit des paramètres de configuration pour la \_ classe de terminal Win32 relative à l’ouverture de session client.
ms.assetid: a2ccb419-da1a-44d1-8a7a-4d0266fc1be8
ms.tgt_platform: multiple
keywords:
- Win32_TSLogonSetting de la classe Services Bureau à distance
- Win32_TSLogonSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting
- Win32_TSLogonSetting.Caption
- Win32_TSLogonSetting.Description
- Win32_TSLogonSetting.InstallDate
- Win32_TSLogonSetting.Name
- Win32_TSLogonSetting.Status
- Win32_TSLogonSetting.TerminalName
- Win32_TSLogonSetting.ClientLogonInfoPolicy
- Win32_TSLogonSetting.Domain
- Win32_TSLogonSetting.Password
- Win32_TSLogonSetting.PolicySourceDomain
- Win32_TSLogonSetting.PolicySourcePromptForPassword
- Win32_TSLogonSetting.PolicySourceUserName
- Win32_TSLogonSetting.PromptForPassword
- Win32_TSLogonSetting.UserName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e656f3913bb7320253dc9dbca6710f37e0cbdded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384956"
---
# <a name="win32_tslogonsetting-class"></a><span data-ttu-id="96fad-105">\_Classe TSLogonSetting Win32</span><span class="sxs-lookup"><span data-stu-id="96fad-105">Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="96fad-106">La classe WMI **Win32 \_ TSLogonSetting** définit des paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) relative à l’ouverture de session client.</span><span class="sxs-lookup"><span data-stu-id="96fad-106">The **Win32\_TSLogonSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

<span data-ttu-id="96fad-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="96fad-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="96fad-108">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="96fad-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="96fad-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96fad-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSLOGONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSLogonSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientLogonInfoPolicy;
  string   Domain;
  string   Password;
  uint32   PolicySourceDomain;
  uint32   PolicySourcePromptForPassword;
  uint32   PolicySourceUserName;
  uint32   PromptForPassword;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="96fad-110">Membres</span><span class="sxs-lookup"><span data-stu-id="96fad-110">Members</span></span>

<span data-ttu-id="96fad-111">La classe **Win32 \_ TSLogonSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="96fad-111">The **Win32\_TSLogonSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="96fad-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="96fad-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="96fad-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="96fad-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="96fad-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="96fad-114">Methods</span></span>

<span data-ttu-id="96fad-115">La classe **Win32 \_ TSLogonSetting** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="96fad-115">The **Win32\_TSLogonSetting** class has these methods.</span></span>



| <span data-ttu-id="96fad-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="96fad-116">Method</span></span>                                                                    | <span data-ttu-id="96fad-117">Description</span><span class="sxs-lookup"><span data-stu-id="96fad-117">Description</span></span>                                                                    |
|:--------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="96fad-118">**ExplicitLogon**</span><span class="sxs-lookup"><span data-stu-id="96fad-118">**ExplicitLogon**</span></span>](win32-tslogonsetting-explicitlogon.md)               | <span data-ttu-id="96fad-119">Définit les informations d’identification du nom d’utilisateur, du mot de passe et de l’authentification de domaine.</span><span class="sxs-lookup"><span data-stu-id="96fad-119">Sets the UserName, Password, and Domain authentication credentials.</span></span><br/> |
| [<span data-ttu-id="96fad-120">**SetPromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="96fad-120">**SetPromptForPassword**</span></span>](win32-tslogonsetting-setpromptforpassword.md) | <span data-ttu-id="96fad-121">Définit la propriété **PromptForPassword** .</span><span class="sxs-lookup"><span data-stu-id="96fad-121">Sets the **PromptForPassword** property.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="96fad-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="96fad-122">Properties</span></span>

<span data-ttu-id="96fad-123">La classe **Win32 \_ TSLogonSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="96fad-123">The **Win32\_TSLogonSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96fad-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="96fad-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="96fad-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96fad-127">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="96fad-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="96fad-128">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="96fad-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="96fad-129">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="96fad-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="96fad-130">**ClientLogonInfoPolicy**</span><span class="sxs-lookup"><span data-stu-id="96fad-130">**ClientLogonInfoPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-131">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96fad-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-132">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="96fad-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="96fad-133">La stratégie utilisée par le serveur pour déterminer les paramètres de connexion.</span><span class="sxs-lookup"><span data-stu-id="96fad-133">The policy the server uses to determine connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="96fad-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)</span><span class="sxs-lookup"><span data-stu-id="96fad-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="96fad-135">Les paramètres de connexion utilisateur individuels sont activés.</span><span class="sxs-lookup"><span data-stu-id="96fad-135">Individual user connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="96fad-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serveur-override** (1)</span><span class="sxs-lookup"><span data-stu-id="96fad-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="96fad-137">Les paramètres de connexion utilisateur individuels sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="96fad-137">Individual user connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="96fad-138">**Description**</span><span class="sxs-lookup"><span data-stu-id="96fad-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-139">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="96fad-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96fad-141">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="96fad-141">Description of the object.</span></span>

<span data-ttu-id="96fad-142">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="96fad-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="96fad-143">**Domaine**</span><span class="sxs-lookup"><span data-stu-id="96fad-143">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-144">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="96fad-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-145">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96fad-146">Informations d’identification d’authentification de connexion au domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96fad-146">The user's domain logon authentication credential.</span></span> <span data-ttu-id="96fad-147">Il s’agit du domaine dans lequel réside l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96fad-147">This is the domain in which the user's computer resides.</span></span> <span data-ttu-id="96fad-148">Cette propriété ne peut pas dépasser 17 caractères.</span><span class="sxs-lookup"><span data-stu-id="96fad-148">This property cannot be longer than 17 characters.</span></span>

</dd> <dt>

<span data-ttu-id="96fad-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="96fad-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-150">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="96fad-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-151">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96fad-152">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="96fad-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="96fad-153">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="96fad-153">The date the object was installed.</span></span> <span data-ttu-id="96fad-154">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="96fad-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="96fad-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="96fad-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="96fad-156">**Nom**</span><span class="sxs-lookup"><span data-stu-id="96fad-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="96fad-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96fad-159">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="96fad-159">The name of the object.</span></span>

<span data-ttu-id="96fad-160">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="96fad-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="96fad-161">**Mot de passe**</span><span class="sxs-lookup"><span data-stu-id="96fad-161">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="96fad-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96fad-164">Informations d’identification d’authentification par mot de passe de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96fad-164">The user's password logon authentication credential.</span></span> <span data-ttu-id="96fad-165">Cette propriété ne peut pas comporter plus de 14 caractères.</span><span class="sxs-lookup"><span data-stu-id="96fad-165">This property cannot be longer than 14 characters.</span></span> <span data-ttu-id="96fad-166">Il est recommandé de définir le niveau de sécurité sur la confidentialité des paquets (wbemAuthenticationLevelPktPrivacy = 6) si vous interrogez cette propriété.</span><span class="sxs-lookup"><span data-stu-id="96fad-166">It is recommended that you set the security level to packet privacy (wbemAuthenticationLevelPktPrivacy = 6) if you query this property.</span></span> <span data-ttu-id="96fad-167">Cela est dû au fait que le mot de passe n’est pas chiffré sur le réseau sans ce niveau de sécurité.</span><span class="sxs-lookup"><span data-stu-id="96fad-167">This is because the password is not encrypted on the wire without this level of security.</span></span> <span data-ttu-id="96fad-168">Pour plus d’informations sur la définition des niveaux de sécurité, consultez Définition de la sécurité des processus de l' [application cliente](/windows/desktop/WmiSdk/setting-client-application-process-security) dans la documentation du SDK WMI.</span><span class="sxs-lookup"><span data-stu-id="96fad-168">For more information about setting security levels, see [Setting Client Application Process Security](/windows/desktop/WmiSdk/setting-client-application-process-security) in the WMI SDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="96fad-169">**PolicySourceDomain**</span><span class="sxs-lookup"><span data-stu-id="96fad-169">**PolicySourceDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-170">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96fad-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96fad-172">Indique si la propriété de **domaine** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="96fad-172">Indicates whether the **Domain** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="96fad-173">0</span><span class="sxs-lookup"><span data-stu-id="96fad-173">0</span></span>
</dt> <dd>

<span data-ttu-id="96fad-174">Serveur</span><span class="sxs-lookup"><span data-stu-id="96fad-174">Server</span></span>

</dd> <dt>

<span data-ttu-id="96fad-175">1</span><span class="sxs-lookup"><span data-stu-id="96fad-175">1</span></span>
</dt> <dd>

<span data-ttu-id="96fad-176">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="96fad-176">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="96fad-177">2</span><span class="sxs-lookup"><span data-stu-id="96fad-177">2</span></span>
</dt> <dd>

<span data-ttu-id="96fad-178">Default</span><span class="sxs-lookup"><span data-stu-id="96fad-178">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="96fad-179">**PolicySourcePromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="96fad-179">**PolicySourcePromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-180">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96fad-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96fad-182">Indique si la propriété **PromptForPassword** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="96fad-182">Indicates whether the **PromptForPassword** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="96fad-183">0</span><span class="sxs-lookup"><span data-stu-id="96fad-183">0</span></span>
</dt> <dd>

<span data-ttu-id="96fad-184">Serveur</span><span class="sxs-lookup"><span data-stu-id="96fad-184">Server</span></span>

</dd> <dt>

<span data-ttu-id="96fad-185">1</span><span class="sxs-lookup"><span data-stu-id="96fad-185">1</span></span>
</dt> <dd>

<span data-ttu-id="96fad-186">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="96fad-186">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="96fad-187">2</span><span class="sxs-lookup"><span data-stu-id="96fad-187">2</span></span>
</dt> <dd>

<span data-ttu-id="96fad-188">Default</span><span class="sxs-lookup"><span data-stu-id="96fad-188">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="96fad-189">**PolicySourceUserName**</span><span class="sxs-lookup"><span data-stu-id="96fad-189">**PolicySourceUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-190">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96fad-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-191">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96fad-192">Indique si la propriété de **nom d’utilisateur** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="96fad-192">Indicates whether the **UserName** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="96fad-193">0</span><span class="sxs-lookup"><span data-stu-id="96fad-193">0</span></span>
</dt> <dd>

<span data-ttu-id="96fad-194">Serveur</span><span class="sxs-lookup"><span data-stu-id="96fad-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="96fad-195">1</span><span class="sxs-lookup"><span data-stu-id="96fad-195">1</span></span>
</dt> <dd>

<span data-ttu-id="96fad-196">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="96fad-196">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="96fad-197">2</span><span class="sxs-lookup"><span data-stu-id="96fad-197">2</span></span>
</dt> <dd>

<span data-ttu-id="96fad-198">Default</span><span class="sxs-lookup"><span data-stu-id="96fad-198">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="96fad-199">**PromptForPassword**</span><span class="sxs-lookup"><span data-stu-id="96fad-199">**PromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-200">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="96fad-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-201">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96fad-202">Spécifie si l’utilisateur est toujours invité à entrer un mot de passe lors de la connexion au serveur.</span><span class="sxs-lookup"><span data-stu-id="96fad-202">Specifies whether the user is always prompted for a password while logging into the server.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="96fad-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="96fad-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="96fad-204">L’utilisateur n’est pas invité à entrer un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="96fad-204">The user is not prompted for a password.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="96fad-205"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="96fad-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="96fad-206">L'utilisateur est invité à entrer un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="96fad-206">The user is prompted for a password.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="96fad-207">**État**</span><span class="sxs-lookup"><span data-stu-id="96fad-207">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-208">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="96fad-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-209">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96fad-210">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="96fad-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="96fad-211">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="96fad-211">Current status of the object.</span></span> <span data-ttu-id="96fad-212">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="96fad-212">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="96fad-213">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="96fad-213">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="96fad-214">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="96fad-214">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="96fad-215">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="96fad-215">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="96fad-216">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="96fad-216">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="96fad-217">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="96fad-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="96fad-218">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="96fad-218">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96fad-219">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="96fad-219">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96fad-220">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="96fad-220">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96fad-221">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="96fad-221">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96fad-222">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="96fad-222">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96fad-223">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="96fad-223">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96fad-224">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="96fad-224">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="96fad-225">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="96fad-225">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="96fad-226">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="96fad-226">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="96fad-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96fad-229">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="96fad-229">The name of the terminal.</span></span>

<span data-ttu-id="96fad-230">Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="96fad-230">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="96fad-231">**UserName**</span><span class="sxs-lookup"><span data-stu-id="96fad-231">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96fad-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="96fad-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96fad-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="96fad-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="96fad-234">Informations d’identification d’authentification par nom d’utilisateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96fad-234">The user's user name logon authentication credential.</span></span> <span data-ttu-id="96fad-235">Cette propriété ne peut pas comporter plus de 20 caractères.</span><span class="sxs-lookup"><span data-stu-id="96fad-235">This property cannot be longer than 20 characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96fad-236">Notes</span><span class="sxs-lookup"><span data-stu-id="96fad-236">Remarks</span></span>

<span data-ttu-id="96fad-237">Sachez que les winstations associés à la session de console ne peuvent pas accéder aux méthodes et aux propriétés de cette classe.</span><span class="sxs-lookup"><span data-stu-id="96fad-237">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="96fad-238">Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété TerminalName, les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="96fad-238">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="96fad-239">Ce code d’erreur est retourné si une station Windows tente d’appeler des méthodes de cet objet pour ajouter ou modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="96fad-239">This error code is returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="96fad-240">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="96fad-240">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="96fad-241">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="96fad-241">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="96fad-242">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="96fad-242">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="96fad-243">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="96fad-243">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="96fad-244">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="96fad-244">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="96fad-245">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="96fad-245">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="96fad-246">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="96fad-246">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="96fad-247">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="96fad-247">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="96fad-248">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="96fad-248">Requirements</span></span>



| <span data-ttu-id="96fad-249">Condition requise</span><span class="sxs-lookup"><span data-stu-id="96fad-249">Requirement</span></span> | <span data-ttu-id="96fad-250">Valeur</span><span class="sxs-lookup"><span data-stu-id="96fad-250">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96fad-251">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96fad-251">Minimum supported client</span></span><br/> | <span data-ttu-id="96fad-252">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="96fad-252">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="96fad-253">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="96fad-253">Minimum supported server</span></span><br/> | <span data-ttu-id="96fad-254">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="96fad-254">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="96fad-255">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="96fad-255">Namespace</span></span><br/>                | <span data-ttu-id="96fad-256">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="96fad-256">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="96fad-257">MOF</span><span class="sxs-lookup"><span data-stu-id="96fad-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96fad-258"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96fad-258"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="96fad-259">DLL</span><span class="sxs-lookup"><span data-stu-id="96fad-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96fad-260"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96fad-260"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96fad-261">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96fad-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96fad-262">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="96fad-262">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="96fad-263">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="96fad-263">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

