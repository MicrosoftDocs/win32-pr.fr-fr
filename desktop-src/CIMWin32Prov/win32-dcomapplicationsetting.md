---
description: Le \_ DCOMApplicationSetting Win32&\# 8194 ; La classe WMI représente les paramètres d’une application DCOM.
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519231"
---
# <a name="win32_dcomapplicationsetting-class"></a><span data-ttu-id="5a59c-103">\_Classe DCOMApplicationSetting Win32</span><span class="sxs-lookup"><span data-stu-id="5a59c-103">Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="5a59c-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ DCOMApplicationSetting** représente les paramètres d’une application DCOM.</span><span class="sxs-lookup"><span data-stu-id="5a59c-104">The **Win32\_DCOMApplicationSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a DCOM application.</span></span> <span data-ttu-id="5a59c-105">Il contient les options de configuration DCOM associées à la clé **AppID** dans le registre.</span><span class="sxs-lookup"><span data-stu-id="5a59c-105">It contains DCOM configuration options associated with the **AppID** key in the registry.</span></span> <span data-ttu-id="5a59c-106">Ces options sont valides sur les composants regroupés logiquement sous la classe d’application donnée.</span><span class="sxs-lookup"><span data-stu-id="5a59c-106">These options are valid on the components logically grouped under the given application class.</span></span>

<span data-ttu-id="5a59c-107">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="5a59c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5a59c-108">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="5a59c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a59c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a59c-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a><span data-ttu-id="5a59c-110">Membres</span><span class="sxs-lookup"><span data-stu-id="5a59c-110">Members</span></span>

<span data-ttu-id="5a59c-111">La classe **Win32 \_ DCOMApplicationSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5a59c-111">The **Win32\_DCOMApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="5a59c-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a59c-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a59c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a59c-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a59c-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5a59c-114">Methods</span></span>

<span data-ttu-id="5a59c-115">La classe **Win32 \_ DCOMApplicationSetting** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5a59c-115">The **Win32\_DCOMApplicationSetting** class has these methods.</span></span>



| <span data-ttu-id="5a59c-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="5a59c-116">Method</span></span>                                                                                                                        | <span data-ttu-id="5a59c-117">Description</span><span class="sxs-lookup"><span data-stu-id="5a59c-117">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a59c-118">**GetAccessSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5a59c-118">**GetAccessSecurityDescriptor**</span></span>](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="5a59c-119">Obtient le descripteur de sécurité qui contrôle les personnes autorisées à accéder à une application DCOM.</span><span class="sxs-lookup"><span data-stu-id="5a59c-119">Gets the security descriptor that controls who is allowed to access a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="5a59c-120">**GetConfigurationSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5a59c-120">**GetConfigurationSecurityDescriptor**</span></span>](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="5a59c-121">Obtient le descripteur de sécurité qui contrôle les personnes autorisées à configurer une application DCOM.</span><span class="sxs-lookup"><span data-stu-id="5a59c-121">Gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="5a59c-122">**GetLaunchSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5a59c-122">**GetLaunchSecurityDescriptor**</span></span>](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | <span data-ttu-id="5a59c-123">Obtient le descripteur de sécurité qui contrôle les personnes autorisées à lancer une application DCOM.</span><span class="sxs-lookup"><span data-stu-id="5a59c-123">Gets the security descriptor that controls who is allowed to launch a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="5a59c-124">**SetAccessSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5a59c-124">**SetAccessSecurityDescriptor**</span></span>](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="5a59c-125">Met à jour le descripteur de sécurité d’accès de l’application DCOM avec un nouveau descripteur de sécurité défini par une instance de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="5a59c-125">Updates the access security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |
| [<span data-ttu-id="5a59c-126">**SetConfigurationSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5a59c-126">**SetConfigurationSecurityDescriptor**</span></span>](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="5a59c-127">Met à jour le descripteur de sécurité de configuration de l’application DCOM avec un nouveau descripteur de sécurité défini par une instance de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="5a59c-127">Updates the configuration security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/> |
| [<span data-ttu-id="5a59c-128">**SetLaunchSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="5a59c-128">**SetLaunchSecurityDescriptor**</span></span>](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="5a59c-129">Met à jour le descripteur de sécurité de lancement de l’application DCOM avec un nouveau descripteur de sécurité défini par une instance de la classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="5a59c-129">Updates the launch security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="5a59c-130">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5a59c-130">Properties</span></span>

<span data-ttu-id="5a59c-131">La classe **Win32 \_ DCOMApplicationSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5a59c-131">The **Win32\_DCOMApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a59c-132">**AppID**</span><span class="sxs-lookup"><span data-stu-id="5a59c-132">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a59c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a59c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-135">Qualificateurs : [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« Win32Registry \| HKEY \_ local \_ machine \\ \\ Software \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ default \] »)</span><span class="sxs-lookup"><span data-stu-id="5a59c-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-136">Identificateur global unique (GUID) de cette application DCOM.</span><span class="sxs-lookup"><span data-stu-id="5a59c-136">Globally unique identifier (GUID) for this DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="5a59c-137">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="5a59c-137">**AuthenticationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5a59c-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5a59c-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-140">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ AuthenticationLevel \] ")</span><span class="sxs-lookup"><span data-stu-id="5a59c-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[AuthenticationLevel\]")</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-141">Niveau minimal d’authentification du client requis par ce serveur COM.</span><span class="sxs-lookup"><span data-stu-id="5a59c-141">Minimum client authentication level required by this COM server.</span></span> <span data-ttu-id="5a59c-142">Si la **valeur est null**, les valeurs par défaut sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="5a59c-142">If **NULL**, the default values are used.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="5a59c-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Aucun** (1)</span><span class="sxs-lookup"><span data-stu-id="5a59c-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5a59c-144">Aucun (aucune authentification n’est effectuée)</span><span class="sxs-lookup"><span data-stu-id="5a59c-144">None (no authentication is performed)</span></span>

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span data-ttu-id="5a59c-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connexion** (2)</span><span class="sxs-lookup"><span data-stu-id="5a59c-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connect** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5a59c-146">Se connecter (l’authentification est effectuée uniquement lorsque le client établit une relation avec l’application)</span><span class="sxs-lookup"><span data-stu-id="5a59c-146">Connect (authentication is performed only when the client establishes a relationship with the application)</span></span>

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span data-ttu-id="5a59c-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Appel** (3)</span><span class="sxs-lookup"><span data-stu-id="5a59c-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Call** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5a59c-148">Appel (l’authentification est effectuée uniquement au début de chaque appel lorsque l’application reçoit la demande)</span><span class="sxs-lookup"><span data-stu-id="5a59c-148">Call (authentication is performed only at the beginning of each call when the application receives the request)</span></span>

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span data-ttu-id="5a59c-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Paquet** (4)</span><span class="sxs-lookup"><span data-stu-id="5a59c-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Packet** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5a59c-150">Paquet (l’authentification est effectuée sur toutes les données reçues du client)</span><span class="sxs-lookup"><span data-stu-id="5a59c-150">Packet (authentication is performed on all of the data received from the client)</span></span>

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span data-ttu-id="5a59c-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span><span class="sxs-lookup"><span data-stu-id="5a59c-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5a59c-152">PacketIntegrity (toutes les données transférées entre le client et l’application sont authentifiées et vérifiées)</span><span class="sxs-lookup"><span data-stu-id="5a59c-152">PacketIntegrity (all of the data transferred between the client and the application is authenticated and verified)</span></span>

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span data-ttu-id="5a59c-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span><span class="sxs-lookup"><span data-stu-id="5a59c-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5a59c-154">PacketPrivacy (les propriétés des autres niveaux d’authentification sont utilisées et toutes les données sont chiffrées)</span><span class="sxs-lookup"><span data-stu-id="5a59c-154">PacketPrivacy (the properties of the other authentication levels are used and all of the data is encrypted)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5a59c-155">**Caption**</span><span class="sxs-lookup"><span data-stu-id="5a59c-155">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a59c-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a59c-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-158">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5a59c-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-159">Courte description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="5a59c-159">Short textual description of the current object.</span></span>

<span data-ttu-id="5a59c-160">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="5a59c-160">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a59c-161">**CustomSurrogate**</span><span class="sxs-lookup"><span data-stu-id="5a59c-161">**CustomSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a59c-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a59c-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-164">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")</span><span class="sxs-lookup"><span data-stu-id="5a59c-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-165">Nom du substitut personnalisé dans lequel l’application DCOM in-process est activée.</span><span class="sxs-lookup"><span data-stu-id="5a59c-165">Name of the custom surrogate in which the in-process DCOM application is activated.</span></span> <span data-ttu-id="5a59c-166">Si cette valeur est **null** et que la clé **UseSurrogate** est **true**, le système fournit un processus de substitution.</span><span class="sxs-lookup"><span data-stu-id="5a59c-166">If this value is **NULL** and the **UseSurrogate** key is **TRUE**, then the system provides a surrogate process.</span></span>

</dd> <dt>

<span data-ttu-id="5a59c-167">**Description**</span><span class="sxs-lookup"><span data-stu-id="5a59c-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-168">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a59c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-169">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a59c-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-170">Description textuelle de l’objet actuel.</span><span class="sxs-lookup"><span data-stu-id="5a59c-170">Textual description of the current object.</span></span>

<span data-ttu-id="5a59c-171">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="5a59c-171">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a59c-172">**EnableAtStorageActivation**</span><span class="sxs-lookup"><span data-stu-id="5a59c-172">**EnableAtStorageActivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-173">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5a59c-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a59c-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-175">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ ActivateAtStorage \] ")</span><span class="sxs-lookup"><span data-stu-id="5a59c-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ActivateAtStorage\]")</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-176">L’application DCOM récupère l’état enregistré de l’application ou commence à l’État dans lequel l’application est initialisée pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="5a59c-176">DCOM application retrieves the saved state of the application or begins from the state in which the application is first initialized.</span></span>

</dd> <dt>

<span data-ttu-id="5a59c-177">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="5a59c-177">**LocalService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a59c-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-179">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a59c-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-180">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")</span><span class="sxs-lookup"><span data-stu-id="5a59c-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[LocalService\]")</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-181">Nom des services fournis par l’application DCOM.</span><span class="sxs-lookup"><span data-stu-id="5a59c-181">Name for the services provided by the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="5a59c-182">**RemoteServerName**</span><span class="sxs-lookup"><span data-stu-id="5a59c-182">**RemoteServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-183">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a59c-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-184">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5a59c-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-185">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ RemoteServerName \] ")</span><span class="sxs-lookup"><span data-stu-id="5a59c-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RemoteServerName\]")</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-186">Nom du serveur distant sur lequel l’application est activée.</span><span class="sxs-lookup"><span data-stu-id="5a59c-186">Name of the remote server where the application is activated.</span></span>

</dd> <dt>

<span data-ttu-id="5a59c-187">**RunAsUser**</span><span class="sxs-lookup"><span data-stu-id="5a59c-187">**RunAsUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-188">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a59c-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a59c-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-190">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ runas \] ")</span><span class="sxs-lookup"><span data-stu-id="5a59c-190">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RunAs\]")</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-191">Compte d’utilisateur spécifique sous lequel l’application doit être exécutée lors de l’activation.</span><span class="sxs-lookup"><span data-stu-id="5a59c-191">Specific user account under which the application is to be run on activation.</span></span>

</dd> <dt>

<span data-ttu-id="5a59c-192">**ServiceParameters**</span><span class="sxs-lookup"><span data-stu-id="5a59c-192">**ServiceParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-193">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a59c-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a59c-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-195">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ ServiceParameters \] ")</span><span class="sxs-lookup"><span data-stu-id="5a59c-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ServiceParameters\]")</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-196">Paramètres de ligne de commande passés à l’application DCOM.</span><span class="sxs-lookup"><span data-stu-id="5a59c-196">Command-line parameters passed to the DCOM application.</span></span> <span data-ttu-id="5a59c-197">Cela est valide uniquement si l’application est écrite en tant que service Windows.</span><span class="sxs-lookup"><span data-stu-id="5a59c-197">This is valid only if the application is written as a Windows-based service.</span></span>

</dd> <dt>

<span data-ttu-id="5a59c-198">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="5a59c-198">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5a59c-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5a59c-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-201">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5a59c-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-202">Identificateur par lequel l’objet actuel est connu.</span><span class="sxs-lookup"><span data-stu-id="5a59c-202">Identifier by which the current object is known.</span></span>

<span data-ttu-id="5a59c-203">Cette propriété est héritée [**du \_ paramètre CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="5a59c-203">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="5a59c-204">**UseSurrogate**</span><span class="sxs-lookup"><span data-stu-id="5a59c-204">**UseSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a59c-205">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="5a59c-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-206">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5a59c-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5a59c-207">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HKEY \_ local \_ machine machine \\ \\ \\ \\ classes \\ \\ AppID \\ \\ {GUID} \[ DllSurrogate \] ")</span><span class="sxs-lookup"><span data-stu-id="5a59c-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="5a59c-208">L’application DCOM peut être activée en tant que serveur hors processus à l’aide d’un fichier exécutable de substitution.</span><span class="sxs-lookup"><span data-stu-id="5a59c-208">DCOM application can be activated as an out-of-process server by use of a surrogate executable file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a59c-209">Notes</span><span class="sxs-lookup"><span data-stu-id="5a59c-209">Remarks</span></span>

<span data-ttu-id="5a59c-210">La classe **Win32 \_ DCOMApplicationSetting** est dérivée de la [**\_ comdéfinition Win32**](win32-comsetting.md).</span><span class="sxs-lookup"><span data-stu-id="5a59c-210">The **Win32\_DCOMApplicationSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a59c-211">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a59c-211">Requirements</span></span>



| <span data-ttu-id="5a59c-212">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a59c-212">Requirement</span></span> | <span data-ttu-id="5a59c-213">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a59c-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a59c-214">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a59c-214">Minimum supported client</span></span><br/> | <span data-ttu-id="5a59c-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a59c-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a59c-216">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5a59c-216">Minimum supported server</span></span><br/> | <span data-ttu-id="5a59c-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a59c-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a59c-218">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5a59c-218">Namespace</span></span><br/>                | <span data-ttu-id="5a59c-219">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="5a59c-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5a59c-220">MOF</span><span class="sxs-lookup"><span data-stu-id="5a59c-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a59c-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a59c-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a59c-222">DLL</span><span class="sxs-lookup"><span data-stu-id="5a59c-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a59c-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a59c-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a59c-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a59c-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a59c-225">**Configuration de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="5a59c-225">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="5a59c-226">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5a59c-226">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5a59c-227">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="5a59c-227">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="5a59c-228">Objets descripteurs de sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="5a59c-228">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="5a59c-229">Modification de la sécurité d’accès sur les objets sécurisables</span><span class="sxs-lookup"><span data-stu-id="5a59c-229">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

