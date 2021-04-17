---
title: Classe Win32_TSSessionSetting
description: Définit des paramètres de configuration pour la \_ classe de terminal Win32, tels que les limites de temps, les actions de déconnexion et de reconnexion.
ms.assetid: e115f370-270c-404f-b6c6-7781c1ff376f
ms.tgt_platform: multiple
keywords:
- Win32_TSSessionSetting de la classe Services Bureau à distance
- Win32_TSSessionSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSSessionSetting
- Win32_TSSessionSetting.Caption
- Win32_TSSessionSetting.Description
- Win32_TSSessionSetting.InstallDate
- Win32_TSSessionSetting.Name
- Win32_TSSessionSetting.Status
- Win32_TSSessionSetting.TerminalName
- Win32_TSSessionSetting.ActiveSessionLimit
- Win32_TSSessionSetting.BrokenConnectionAction
- Win32_TSSessionSetting.BrokenConnectionPolicy
- Win32_TSSessionSetting.DisconnectedSessionLimit
- Win32_TSSessionSetting.IdleSessionLimit
- Win32_TSSessionSetting.PolicySourceActiveSessionLimit
- Win32_TSSessionSetting.PolicySourceBrokenConnectionAction
- Win32_TSSessionSetting.PolicySourceDisconnectedSessionLimit
- Win32_TSSessionSetting.PolicySourceIdleSessionLimit
- Win32_TSSessionSetting.PolicySourceReconnectionPolicy
- Win32_TSSessionSetting.ReconnectionPolicy
- Win32_TSSessionSetting.TimeLimitPolicy
- Win32_TSSessionSetting.EnableTimeoutWarning
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e780cdedee0fe447499bed5013dadc2ba9b448b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509374"
---
# <a name="win32_tssessionsetting-class"></a><span data-ttu-id="446e4-105">\_Classe TSSessionSetting Win32</span><span class="sxs-lookup"><span data-stu-id="446e4-105">Win32\_TSSessionSetting class</span></span>

<span data-ttu-id="446e4-106">La classe WMI **Win32 \_ TSSessionSetting** définit des paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , tels que les limites de temps, les actions de déconnexion et de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="446e4-106">The **Win32\_TSSessionSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

<span data-ttu-id="446e4-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="446e4-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="446e4-108">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="446e4-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="446e4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="446e4-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSSessionSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ActiveSessionLimit;
  uint32   BrokenConnectionAction;
  uint32   BrokenConnectionPolicy;
  uint32   DisconnectedSessionLimit;
  uint32   IdleSessionLimit;
  uint32   PolicySourceActiveSessionLimit;
  uint32   PolicySourceBrokenConnectionAction;
  uint32   PolicySourceDisconnectedSessionLimit;
  uint32   PolicySourceIdleSessionLimit;
  uint32   PolicySourceReconnectionPolicy;
  uint32   ReconnectionPolicy;
  uint32   TimeLimitPolicy;
  uint32   EnableTimeoutWarning;
};
```

## <a name="members"></a><span data-ttu-id="446e4-110">Membres</span><span class="sxs-lookup"><span data-stu-id="446e4-110">Members</span></span>

<span data-ttu-id="446e4-111">La classe **Win32 \_ TSSessionSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="446e4-111">The **Win32\_TSSessionSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="446e4-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="446e4-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="446e4-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="446e4-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="446e4-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="446e4-114">Methods</span></span>

<span data-ttu-id="446e4-115">La classe **Win32 \_ TSSessionSetting** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="446e4-115">The **Win32\_TSSessionSetting** class has these methods.</span></span>



| <span data-ttu-id="446e4-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="446e4-116">Method</span></span>                                                              | <span data-ttu-id="446e4-117">Description</span><span class="sxs-lookup"><span data-stu-id="446e4-117">Description</span></span>                                                              |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="446e4-118">**BrokenConnection**</span><span class="sxs-lookup"><span data-stu-id="446e4-118">**BrokenConnection**</span></span>](win32-tssessionsetting-brokenconnection.md) | <span data-ttu-id="446e4-119">Définit les propriétés de connexion rompues incluses dans cette classe.</span><span class="sxs-lookup"><span data-stu-id="446e4-119">Sets the broken connection properties included in this class.</span></span><br/> |
| [<span data-ttu-id="446e4-120">**TimeLimit**</span><span class="sxs-lookup"><span data-stu-id="446e4-120">**TimeLimit**</span></span>](win32-tssessionsetting-timelimit.md)               | <span data-ttu-id="446e4-121">Définit les propriétés de limite de temps incluses dans cette classe.</span><span class="sxs-lookup"><span data-stu-id="446e4-121">Sets the time-limit properties included in this class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="446e4-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="446e4-122">Properties</span></span>

<span data-ttu-id="446e4-123">La classe **Win32 \_ TSSessionSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="446e4-123">The **Win32\_TSSessionSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="446e4-124">**ActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="446e4-124">**ActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-125">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-127">Durée maximale, en millisecondes, allouée à une session active.</span><span class="sxs-lookup"><span data-stu-id="446e4-127">The maximum amount of time, in milliseconds, allocated to an active session.</span></span> <span data-ttu-id="446e4-128">La valeur 0 spécifie une durée infinie.</span><span class="sxs-lookup"><span data-stu-id="446e4-128">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="446e4-129">**BrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="446e4-129">**BrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-130">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-132">Action que le serveur effectue sur la session lorsqu’une connexion a été interrompue en raison d’une perte de réseau ou de délais.</span><span class="sxs-lookup"><span data-stu-id="446e4-132">The action the server takes on the session when a connection has been broken due to network loss or exceeded time-limits.</span></span>

<dt>

<span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>

<span data-ttu-id="446e4-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Déconnecter** (0)</span><span class="sxs-lookup"><span data-stu-id="446e4-133"><span id="Disconnect"></span><span id="disconnect"></span><span id="DISCONNECT"></span>**Disconnect** (0)</span></span>


</dt> <dd>

<span data-ttu-id="446e4-134">L’utilisateur est déconnecté de la session.</span><span class="sxs-lookup"><span data-stu-id="446e4-134">The user is disconnected from the session.</span></span>

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span data-ttu-id="446e4-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span><span class="sxs-lookup"><span data-stu-id="446e4-135"><span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**Terminate** (1)</span></span>


</dt> <dd>

<span data-ttu-id="446e4-136">La session est définitivement supprimée du serveur.</span><span class="sxs-lookup"><span data-stu-id="446e4-136">The session is permanently deleted from the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="446e4-137">**BrokenConnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="446e4-137">**BrokenConnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-138">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="446e4-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="446e4-140">La stratégie utilisée par le serveur pour déterminer quand arrêter une connexion en raison d’une perte de réseau ou de délais.</span><span class="sxs-lookup"><span data-stu-id="446e4-140">The policy the server uses to determine when to break a connection because of network loss or exceeded time-limits.</span></span>

<dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="446e4-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serveur-override** (1)</span><span class="sxs-lookup"><span data-stu-id="446e4-141"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="446e4-142">Les paramètres de stratégie de déconnexion de l’utilisateur sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="446e4-142">The user's disconnection policy settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="446e4-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)</span><span class="sxs-lookup"><span data-stu-id="446e4-143"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="446e4-144">Les paramètres de stratégie de déconnexion de l’utilisateur sont activés.</span><span class="sxs-lookup"><span data-stu-id="446e4-144">The user's disconnection policy settings are in effect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="446e4-145">**Caption**</span><span class="sxs-lookup"><span data-stu-id="446e4-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-146">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="446e4-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446e4-148">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="446e4-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="446e4-149">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="446e4-149">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="446e4-150">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="446e4-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="446e4-151">**Description**</span><span class="sxs-lookup"><span data-stu-id="446e4-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-152">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="446e4-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-154">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="446e4-154">Description of the object.</span></span>

<span data-ttu-id="446e4-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="446e4-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="446e4-156">**DisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="446e4-156">**DisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-159">Intervalle de temps, en millisecondes, après lequel une session déconnectée est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="446e4-159">The time interval, in milliseconds, after which a disconnected session is terminated.</span></span> <span data-ttu-id="446e4-160">La valeur 0 spécifie une durée infinie.</span><span class="sxs-lookup"><span data-stu-id="446e4-160">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="446e4-161">**EnableTimeoutWarning**</span><span class="sxs-lookup"><span data-stu-id="446e4-161">**EnableTimeoutWarning**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-163">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="446e4-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="446e4-164">Active l’avertissement d’expiration du délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="446e4-164">Enables the timeout warning.</span></span>

<span data-ttu-id="446e4-165">**Windows 7, Windows server 2008 R2, Windows Vista et Windows server 2008 :** Cette propriété n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="446e4-165">**Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="446e4-166">**IdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="446e4-166">**IdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-167">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-167">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-168">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-169">Intervalle de temps, en millisecondes, après lequel une session inactive est terminée.</span><span class="sxs-lookup"><span data-stu-id="446e4-169">The time interval, in milliseconds, after which an idle session is terminated.</span></span> <span data-ttu-id="446e4-170">La valeur 0 spécifie une durée infinie.</span><span class="sxs-lookup"><span data-stu-id="446e4-170">A value of 0 specifies an infinite amount of time.</span></span>

</dd> <dt>

<span data-ttu-id="446e4-171">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="446e4-171">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-172">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="446e4-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446e4-174">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="446e4-174">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="446e4-175">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="446e4-175">The date the object was installed.</span></span> <span data-ttu-id="446e4-176">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="446e4-176">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="446e4-177">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="446e4-177">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="446e4-178">**Nom**</span><span class="sxs-lookup"><span data-stu-id="446e4-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="446e4-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-181">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="446e4-181">The name of the object.</span></span>

<span data-ttu-id="446e4-182">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="446e4-182">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="446e4-183">**PolicySourceActiveSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="446e4-183">**PolicySourceActiveSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-184">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-185">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-186">Indique si la propriété **ActiveSessionLimit** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="446e4-186">Indicates whether the **ActiveSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="446e4-187">0</span><span class="sxs-lookup"><span data-stu-id="446e4-187">0</span></span>
</dt> <dd>

<span data-ttu-id="446e4-188">Serveur</span><span class="sxs-lookup"><span data-stu-id="446e4-188">Server</span></span>

</dd> <dt>

<span data-ttu-id="446e4-189">1</span><span class="sxs-lookup"><span data-stu-id="446e4-189">1</span></span>
</dt> <dd>

<span data-ttu-id="446e4-190">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="446e4-190">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="446e4-191">2</span><span class="sxs-lookup"><span data-stu-id="446e4-191">2</span></span>
</dt> <dd>

<span data-ttu-id="446e4-192">Default</span><span class="sxs-lookup"><span data-stu-id="446e4-192">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="446e4-193">**PolicySourceBrokenConnectionAction**</span><span class="sxs-lookup"><span data-stu-id="446e4-193">**PolicySourceBrokenConnectionAction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-194">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-194">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-195">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-196">Indique si la propriété **BrokenConnectionAction** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="446e4-196">Indicates whether the **BrokenConnectionAction** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="446e4-197">0</span><span class="sxs-lookup"><span data-stu-id="446e4-197">0</span></span>
</dt> <dd>

<span data-ttu-id="446e4-198">Serveur</span><span class="sxs-lookup"><span data-stu-id="446e4-198">Server</span></span>

</dd> <dt>

<span data-ttu-id="446e4-199">1</span><span class="sxs-lookup"><span data-stu-id="446e4-199">1</span></span>
</dt> <dd>

<span data-ttu-id="446e4-200">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="446e4-200">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="446e4-201">2</span><span class="sxs-lookup"><span data-stu-id="446e4-201">2</span></span>
</dt> <dd>

<span data-ttu-id="446e4-202">Default</span><span class="sxs-lookup"><span data-stu-id="446e4-202">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="446e4-203">**PolicySourceDisconnectedSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="446e4-203">**PolicySourceDisconnectedSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-204">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-205">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-205">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-206">Indique si la propriété **DisconnectedSessionLimit** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="446e4-206">Indicates whether the **DisconnectedSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="446e4-207">0</span><span class="sxs-lookup"><span data-stu-id="446e4-207">0</span></span>
</dt> <dd>

<span data-ttu-id="446e4-208">Serveur</span><span class="sxs-lookup"><span data-stu-id="446e4-208">Server</span></span>

</dd> <dt>

<span data-ttu-id="446e4-209">1</span><span class="sxs-lookup"><span data-stu-id="446e4-209">1</span></span>
</dt> <dd>

<span data-ttu-id="446e4-210">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="446e4-210">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="446e4-211">2</span><span class="sxs-lookup"><span data-stu-id="446e4-211">2</span></span>
</dt> <dd>

<span data-ttu-id="446e4-212">Default</span><span class="sxs-lookup"><span data-stu-id="446e4-212">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="446e4-213">**PolicySourceIdleSessionLimit**</span><span class="sxs-lookup"><span data-stu-id="446e4-213">**PolicySourceIdleSessionLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-214">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-215">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-215">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-216">Indique si la propriété **IdleSessionLimit** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="446e4-216">Indicates whether the **IdleSessionLimit** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="446e4-217">0</span><span class="sxs-lookup"><span data-stu-id="446e4-217">0</span></span>
</dt> <dd>

<span data-ttu-id="446e4-218">Serveur</span><span class="sxs-lookup"><span data-stu-id="446e4-218">Server</span></span>

</dd> <dt>

<span data-ttu-id="446e4-219">1</span><span class="sxs-lookup"><span data-stu-id="446e4-219">1</span></span>
</dt> <dd>

<span data-ttu-id="446e4-220">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="446e4-220">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="446e4-221">2</span><span class="sxs-lookup"><span data-stu-id="446e4-221">2</span></span>
</dt> <dd>

<span data-ttu-id="446e4-222">Default</span><span class="sxs-lookup"><span data-stu-id="446e4-222">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="446e4-223">**PolicySourceReconnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="446e4-223">**PolicySourceReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-224">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-225">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-226">Indique si la propriété **ReconnectPolicy** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="446e4-226">Indicates whether the **ReconnectPolicy** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="446e4-227">0</span><span class="sxs-lookup"><span data-stu-id="446e4-227">0</span></span>
</dt> <dd>

<span data-ttu-id="446e4-228">Serveur</span><span class="sxs-lookup"><span data-stu-id="446e4-228">Server</span></span>

</dd> <dt>

<span data-ttu-id="446e4-229">1</span><span class="sxs-lookup"><span data-stu-id="446e4-229">1</span></span>
</dt> <dd>

<span data-ttu-id="446e4-230">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="446e4-230">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="446e4-231">2</span><span class="sxs-lookup"><span data-stu-id="446e4-231">2</span></span>
</dt> <dd>

<span data-ttu-id="446e4-232">Default</span><span class="sxs-lookup"><span data-stu-id="446e4-232">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="446e4-233">**ReconnectionPolicy**</span><span class="sxs-lookup"><span data-stu-id="446e4-233">**ReconnectionPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-234">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-235">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="446e4-235">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="446e4-236">Spécifie si un utilisateur doit utiliser le client précédent pour se reconnecter à une session déconnectée.</span><span class="sxs-lookup"><span data-stu-id="446e4-236">Specifies whether a user must use the previous client to reconnect to a disconnected session.</span></span>

<dt>

<span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>

<span data-ttu-id="446e4-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**N’importe quel client** (0)</span><span class="sxs-lookup"><span data-stu-id="446e4-237"><span id="Any_Client"></span><span id="any_client"></span><span id="ANY_CLIENT"></span>**Any Client** (0)</span></span>


</dt> <dd>

<span data-ttu-id="446e4-238">N’importe quel client sera utilisé pour se reconnecter.</span><span class="sxs-lookup"><span data-stu-id="446e4-238">Any client will be used to reconnect.</span></span>

</dd> <dt>

<span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>

<span data-ttu-id="446e4-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Client précédent** (1)</span><span class="sxs-lookup"><span data-stu-id="446e4-239"><span id="Previous_Client"></span><span id="previous_client"></span><span id="PREVIOUS_CLIENT"></span>**Previous Client** (1)</span></span>


</dt> <dd>

<span data-ttu-id="446e4-240">Le client précédent utilisé dans une connexion sera utilisé pour se reconnecter.</span><span class="sxs-lookup"><span data-stu-id="446e4-240">The previous client used in a connection will be used to reconnect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="446e4-241">**État**</span><span class="sxs-lookup"><span data-stu-id="446e4-241">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="446e4-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="446e4-244">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="446e4-244">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="446e4-245">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="446e4-245">Current status of the object.</span></span> <span data-ttu-id="446e4-246">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="446e4-246">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="446e4-247">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="446e4-247">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="446e4-248">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="446e4-248">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="446e4-249">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="446e4-249">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="446e4-250">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="446e4-250">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="446e4-251">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="446e4-251">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="446e4-252">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="446e4-252">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="446e4-253">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="446e4-253">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="446e4-254">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="446e4-254">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="446e4-255">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="446e4-255">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="446e4-256">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="446e4-256">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="446e4-257">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="446e4-257">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="446e4-258">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="446e4-258">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="446e4-259">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="446e4-259">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="446e4-260">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="446e4-260">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="446e4-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="446e4-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="446e4-263">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="446e4-263">The name of the terminal.</span></span>

<span data-ttu-id="446e4-264">Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="446e4-264">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="446e4-265">**TimeLimitPolicy**</span><span class="sxs-lookup"><span data-stu-id="446e4-265">**TimeLimitPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="446e4-266">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="446e4-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="446e4-267">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="446e4-267">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="446e4-268">La stratégie utilisée par le serveur pour déterminer les limites de temps pour les sessions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="446e4-268">The policy the server uses to determine time-limits for user sessions.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="446e4-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)</span><span class="sxs-lookup"><span data-stu-id="446e4-269"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="446e4-270">Les paramètres de stratégie de limites horaires de l’utilisateur sont activés.</span><span class="sxs-lookup"><span data-stu-id="446e4-270">The user's time-limits policy settings are in effect.</span></span>

</dd> <dt>

<span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>

<span data-ttu-id="446e4-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Remplacement de serveur** (1)</span><span class="sxs-lookup"><span data-stu-id="446e4-271"><span id="Server_Override"></span><span id="server_override"></span><span id="SERVER_OVERRIDE"></span>**Server Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="446e4-272">Les paramètres de stratégie de limites horaires de l’utilisateur sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="446e4-272">The user's time-limits policy settings are overridden by the server.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="446e4-273">Notes</span><span class="sxs-lookup"><span data-stu-id="446e4-273">Remarks</span></span>

<span data-ttu-id="446e4-274">Sachez que les winstations associés à la session de console ne peuvent pas accéder aux méthodes et aux propriétés de cette classe.</span><span class="sxs-lookup"><span data-stu-id="446e4-274">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="446e4-275">Si vous tentez de le faire en spécifiant « console » comme valeur de la propriété TerminalName, les méthodes de cet objet retournent **WBEM \_ E \_ non \_ pris en charge**.</span><span class="sxs-lookup"><span data-stu-id="446e4-275">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object will return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="446e4-276">Ce code d’erreur est également renvoyé si une station Windows tente d’appeler des méthodes de cet objet dans le but d’ajouter ou de modifier les propriétés de sécurité des comptes LocalSystem, LocalService ou NetworkService.</span><span class="sxs-lookup"><span data-stu-id="446e4-276">This error code will also be returned if a window station attempts to call methods of this object for the purpose of adding or modifying the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="446e4-277">Pour se connecter à l’espace de noms « root \\ cimv2 \\ licences TS », le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="446e4-277">To connect to the "root\\CIMV2\\TerminalServices" namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="446e4-278">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="446e4-278">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="446e4-279">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="446e4-279">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="446e4-280">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="446e4-280">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="446e4-281">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="446e4-281">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="446e4-282">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="446e4-282">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="446e4-283">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="446e4-283">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="446e4-284">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="446e4-284">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="446e4-285">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="446e4-285">Requirements</span></span>



| <span data-ttu-id="446e4-286">Condition requise</span><span class="sxs-lookup"><span data-stu-id="446e4-286">Requirement</span></span> | <span data-ttu-id="446e4-287">Valeur</span><span class="sxs-lookup"><span data-stu-id="446e4-287">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="446e4-288">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="446e4-288">Minimum supported client</span></span><br/> | <span data-ttu-id="446e4-289">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="446e4-289">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="446e4-290">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="446e4-290">Minimum supported server</span></span><br/> | <span data-ttu-id="446e4-291">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="446e4-291">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="446e4-292">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="446e4-292">Namespace</span></span><br/>                | <span data-ttu-id="446e4-293">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="446e4-293">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="446e4-294">MOF</span><span class="sxs-lookup"><span data-stu-id="446e4-294">MOF</span></span><br/>                      | <dl> <span data-ttu-id="446e4-295"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="446e4-295"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="446e4-296">DLL</span><span class="sxs-lookup"><span data-stu-id="446e4-296">DLL</span></span><br/>                      | <dl> <span data-ttu-id="446e4-297"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="446e4-297"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="446e4-298">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="446e4-298">See also</span></span>

<dl> <dt>

[<span data-ttu-id="446e4-299">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="446e4-299">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dt>

[<span data-ttu-id="446e4-300">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="446e4-300">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

