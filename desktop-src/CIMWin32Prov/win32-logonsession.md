---
description: Décrit la session de connexion ou les sessions associées à un utilisateur connecté à un système d’ordinateur exécutant Windows.
ms.assetid: d09a115b-95a3-47c7-a04d-c810d044ccc8
ms.tgt_platform: multiple
title: Classe Win32_LogonSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSession
- Win32_LogonSession.Caption
- Win32_LogonSession.Description
- Win32_LogonSession.InstallDate
- Win32_LogonSession.Name
- Win32_LogonSession.Status
- Win32_LogonSession.StartTime
- Win32_LogonSession.AuthenticationPackage
- Win32_LogonSession.LogonId
- Win32_LogonSession.LogonType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 78e14bbd41c2fd8bb0c10a7bfeeda0dc9d426b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747981"
---
# <a name="win32_logonsession-class"></a><span data-ttu-id="4484f-103">\_Classe LogonSession Win32</span><span class="sxs-lookup"><span data-stu-id="4484f-103">Win32\_LogonSession class</span></span>

<span data-ttu-id="4484f-104">La classe WMI **Win32 \_ LogonSession** (consultez [récupération d’une classe WMI](/windows/desktop/wmisdk/retrieving-a-class)) décrit la session de connexion ou les sessions associées à un utilisateur connecté à un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="4484f-104">The **Win32\_LogonSession** WMI class (see [Retrieving a WMI class](/windows/desktop/wmisdk/retrieving-a-class)) describes the logon session or sessions associated with a user logged on to a computer system running Windows.</span></span>

<span data-ttu-id="4484f-105">La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="4484f-105">The following syntax is simplified from Managed Object Format (MOF) code, and includes all of the inherited properties.</span></span> <span data-ttu-id="4484f-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="4484f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4484f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4484f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{9083C21E-7D58-4e0e-BC30-0BC8922AFB8B}"), AMENDMENT]
class Win32_LogonSession : Win32_Session
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
  string   AuthenticationPackage;
  string   LogonId;
  uint32   LogonType;
};
```

## <a name="members"></a><span data-ttu-id="4484f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="4484f-108">Members</span></span>

<span data-ttu-id="4484f-109">La classe **Win32 \_ LogonSession** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4484f-109">The **Win32\_LogonSession** class has these types of members:</span></span>

-   [<span data-ttu-id="4484f-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4484f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4484f-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4484f-111">Properties</span></span>

<span data-ttu-id="4484f-112">La classe **Win32 \_ LogonSession** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4484f-112">The **Win32\_LogonSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4484f-113">**AuthenticationPackage**</span><span class="sxs-lookup"><span data-stu-id="4484f-113">**AuthenticationPackage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4484f-114">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4484f-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4484f-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4484f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4484f-116">Nom du sous-système utilisé pour authentifier la session d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="4484f-116">Name of the subsystem used to authenticate the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="4484f-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4484f-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4484f-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4484f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4484f-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4484f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4484f-120">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="4484f-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="4484f-121">Brève description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4484f-121">A short textual description of the object.</span></span>

<span data-ttu-id="4484f-122">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4484f-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4484f-123">**Description**</span><span class="sxs-lookup"><span data-stu-id="4484f-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4484f-124">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4484f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4484f-125">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4484f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4484f-126">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="4484f-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="4484f-127">Description textuelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4484f-127">A textual description of the object.</span></span>

<span data-ttu-id="4484f-128">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4484f-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4484f-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="4484f-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4484f-130">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4484f-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4484f-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4484f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4484f-132">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="4484f-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="4484f-133">Indique le moment où l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="4484f-133">Indicates when the object was installed.</span></span> <span data-ttu-id="4484f-134">L’absence de valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="4484f-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="4484f-135">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4484f-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4484f-136">**LogonId**</span><span class="sxs-lookup"><span data-stu-id="4484f-136">**LogonId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4484f-137">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4484f-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4484f-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4484f-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4484f-139">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4484f-139">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4484f-140">ID affecté à la session d’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="4484f-140">ID assigned to the logon session.</span></span>

</dd> <dt>

<span data-ttu-id="4484f-141">**LogonType**</span><span class="sxs-lookup"><span data-stu-id="4484f-141">**LogonType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4484f-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4484f-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4484f-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4484f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4484f-144">Valeur numérique qui indique le type de session de connexion.</span><span class="sxs-lookup"><span data-stu-id="4484f-144">Numeric value that indicates the type of logon session.</span></span>

<dt>

<span data-ttu-id="4484f-145">0</span><span class="sxs-lookup"><span data-stu-id="4484f-145">0</span></span>
</dt> <dd>

<span data-ttu-id="4484f-146">Utilisé uniquement par le compte système.</span><span class="sxs-lookup"><span data-stu-id="4484f-146">Used only by the System account.</span></span>

</dd> <dt>

<span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>

<span data-ttu-id="4484f-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interactif** (2)</span><span class="sxs-lookup"><span data-stu-id="4484f-147"><span id="Interactive"></span><span id="interactive"></span><span id="INTERACTIVE"></span>**Interactive** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-148">Destiné aux utilisateurs qui utilisent l’ordinateur de manière interactive, tels qu’un utilisateur connecté par un serveur Terminal Server, un interpréteur de commandes à distance ou un processus similaire.</span><span class="sxs-lookup"><span data-stu-id="4484f-148">Intended for users who are interactively using the machine, such as a user being logged on by a terminal server, remote shell, or similar process.</span></span>

</dd> <dt>

<span id="Network"></span><span id="network"></span><span id="NETWORK"></span>

<span data-ttu-id="4484f-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Réseau** (3)</span><span class="sxs-lookup"><span data-stu-id="4484f-149"><span id="Network"></span><span id="network"></span><span id="NETWORK"></span>**Network** (3)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-150">Destiné aux serveurs à hautes performances pour authentifier les mots de passe en texte clair.</span><span class="sxs-lookup"><span data-stu-id="4484f-150">Intended for high-performance servers to authenticate clear text passwords.</span></span> <span data-ttu-id="4484f-151">LogonUser ne met pas en cache les informations d’identification pour ce type de connexion.</span><span class="sxs-lookup"><span data-stu-id="4484f-151">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>

<span data-ttu-id="4484f-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Lot** (4)</span><span class="sxs-lookup"><span data-stu-id="4484f-152"><span id="Batch"></span><span id="batch"></span><span id="BATCH"></span>**Batch** (4)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-153">Destiné aux serveurs batch, où les processus peuvent être exécutés pour le compte d’un utilisateur sans leur intervention directe ; ou pour les serveurs plus performants qui traitent de nombreuses tentatives d’authentification en texte clair à la fois, telles que les serveurs de messagerie ou les serveurs Web.</span><span class="sxs-lookup"><span data-stu-id="4484f-153">Intended for batch servers, where processes can be executed on behalf of a user without their direct intervention; or for higher performance servers that process many clear-text authentication attempts at a time, such as mail or web servers.</span></span> <span data-ttu-id="4484f-154">LogonUser ne met pas en cache les informations d’identification pour ce type de connexion.</span><span class="sxs-lookup"><span data-stu-id="4484f-154">LogonUser does not cache credentials for this logon type.</span></span>

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4484f-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (5)</span><span class="sxs-lookup"><span data-stu-id="4484f-155"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (5)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-156">Indique une ouverture de session de type service.</span><span class="sxs-lookup"><span data-stu-id="4484f-156">Indicates a service-type logon.</span></span> <span data-ttu-id="4484f-157">Le compte fourni doit avoir le privilège de service activé.</span><span class="sxs-lookup"><span data-stu-id="4484f-157">The account provided must have the service privilege enabled.</span></span>

</dd> <dt>

<span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>

<span data-ttu-id="4484f-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span><span class="sxs-lookup"><span data-stu-id="4484f-158"><span id="Proxy"></span><span id="proxy"></span><span id="PROXY"></span>**Proxy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-159">Indique une ouverture de session de type proxy.</span><span class="sxs-lookup"><span data-stu-id="4484f-159">Indicates a proxy-type logon.</span></span>

</dd> <dt>

<span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>

<span data-ttu-id="4484f-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Déverrouiller** (7)</span><span class="sxs-lookup"><span data-stu-id="4484f-160"><span id="Unlock"></span><span id="unlock"></span><span id="UNLOCK"></span>**Unlock** (7)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-161">Ce type d’ouverture de session est conçu pour la journalisation des DLL GINA sur les utilisateurs qui utilisent l’ordinateur de manière interactive.</span><span class="sxs-lookup"><span data-stu-id="4484f-161">This logon type is intended for GINA DLLs logging on users who are interactively using the machine.</span></span> <span data-ttu-id="4484f-162">Ce type de connexion permet de générer un enregistrement d’audit unique qui indique le moment où la station de travail a été déverrouillée.</span><span class="sxs-lookup"><span data-stu-id="4484f-162">This logon type allows a unique audit record to be generated that shows when the workstation was unlocked.</span></span>

</dd> <dt>

<span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>

<span data-ttu-id="4484f-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span><span class="sxs-lookup"><span data-stu-id="4484f-163"><span id="NetworkCleartext"></span><span id="networkcleartext"></span><span id="NETWORKCLEARTEXT"></span>**NetworkCleartext** (8)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-164">Conserve le nom et le mot de passe dans les packages d’authentification, ce qui permet au serveur d’établir des connexions à d’autres serveurs réseau tout en usurpant l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="4484f-164">Preserves the name and password in the authentication packages, allowing the server to make connections to other network servers while impersonating the client.</span></span> <span data-ttu-id="4484f-165">Cela permet à un serveur d’accepter des informations d’identification en texte clair d’un client, d’appeler LogonUser, de vérifier que l’utilisateur peut accéder au système sur le réseau et de communiquer toujours avec d’autres serveurs.</span><span class="sxs-lookup"><span data-stu-id="4484f-165">This allows a server to accept clear text credentials from a client, call LogonUser, verify that the user can access the system across the network, and still communicate with other servers.</span></span>

</dd> <dt>

<span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>

<span data-ttu-id="4484f-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span><span class="sxs-lookup"><span data-stu-id="4484f-166"><span id="NewCredentials"></span><span id="newcredentials"></span><span id="NEWCREDENTIALS"></span>**NewCredentials** (9)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-167">Permet à l’appelant de cloner son jeton actuel et de spécifier de nouvelles informations d’identification pour les connexions sortantes.</span><span class="sxs-lookup"><span data-stu-id="4484f-167">Allows the caller to clone its current token and specify new credentials for outbound connections.</span></span> <span data-ttu-id="4484f-168">La nouvelle session d’ouverture de session a la même identification locale, mais elle utilise des informations d’identification différentes pour d’autres connexions réseau.</span><span class="sxs-lookup"><span data-stu-id="4484f-168">The new logon session has the same local identify, but uses different credentials for other network connections.</span></span>

</dd> <dt>

<span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>

<span data-ttu-id="4484f-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span><span class="sxs-lookup"><span data-stu-id="4484f-169"><span id="RemoteInteractive"></span><span id="remoteinteractive"></span><span id="REMOTEINTERACTIVE"></span>**RemoteInteractive** (10)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-170">Session des services Terminal Server à la fois à distance et interactive.</span><span class="sxs-lookup"><span data-stu-id="4484f-170">Terminal Services session that is both remote and interactive.</span></span>

</dd> <dt>

<span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>

<span data-ttu-id="4484f-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span><span class="sxs-lookup"><span data-stu-id="4484f-171"><span id="CachedInteractive"></span><span id="cachedinteractive"></span><span id="CACHEDINTERACTIVE"></span>**CachedInteractive** (11)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-172">Essayez les informations d’identification mises en cache sans accéder au réseau.</span><span class="sxs-lookup"><span data-stu-id="4484f-172">Attempt cached credentials without accessing the network.</span></span>

</dd> <dt>

<span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>

<span data-ttu-id="4484f-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span><span class="sxs-lookup"><span data-stu-id="4484f-173"><span id="CachedRemoteInteractive"></span><span id="cachedremoteinteractive"></span><span id="CACHEDREMOTEINTERACTIVE"></span>**CachedRemoteInteractive** (12)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-174">Identique à RemoteInteractive.</span><span class="sxs-lookup"><span data-stu-id="4484f-174">Same as RemoteInteractive.</span></span> <span data-ttu-id="4484f-175">Cela est utilisé pour l’audit interne.</span><span class="sxs-lookup"><span data-stu-id="4484f-175">This is used for internal auditing.</span></span>

</dd> <dt>

<span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>

<span data-ttu-id="4484f-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span><span class="sxs-lookup"><span data-stu-id="4484f-176"><span id="CachedUnlock"></span><span id="cachedunlock"></span><span id="CACHEDUNLOCK"></span>**CachedUnlock** (13)</span></span>


</dt> <dd>

<span data-ttu-id="4484f-177">Ouverture de session de la station de travail.</span><span class="sxs-lookup"><span data-stu-id="4484f-177">Workstation logon.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4484f-178">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4484f-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4484f-179">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4484f-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4484f-180">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4484f-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4484f-181">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="4484f-181">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="4484f-182">Étiquette par laquelle l’objet est connu.</span><span class="sxs-lookup"><span data-stu-id="4484f-182">Label by which the object is known.</span></span> <span data-ttu-id="4484f-183">Lorsqu’elle est sous-classée, cette propriété peut être substituée pour être une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="4484f-183">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="4484f-184">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4484f-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="4484f-185">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="4484f-185">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4484f-186">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4484f-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4484f-187">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4484f-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4484f-188">Heure à laquelle la session a démarré.</span><span class="sxs-lookup"><span data-stu-id="4484f-188">Time at which the session started.</span></span>

<span data-ttu-id="4484f-189">Cette propriété est héritée de la [**\_ session Win32**](win32-session.md).</span><span class="sxs-lookup"><span data-stu-id="4484f-189">This property is inherited from [**Win32\_Session**](win32-session.md).</span></span>

</dd> <dt>

<span data-ttu-id="4484f-190">**État**</span><span class="sxs-lookup"><span data-stu-id="4484f-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4484f-191">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4484f-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4484f-192">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4484f-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4484f-193">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="4484f-193">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="4484f-194">Chaîne qui indique l’état actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4484f-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="4484f-195">L’état opérationnel et non opérationnel peut être défini.</span><span class="sxs-lookup"><span data-stu-id="4484f-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="4484f-196">L’état opérationnel peut inclure « OK », « détérioré » et « échec prédit ».</span><span class="sxs-lookup"><span data-stu-id="4484f-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="4484f-197">« Échec prédit » indique qu’un élément fonctionne correctement, mais prédit un échec (par exemple, un lecteur de disque dur intelligent).</span><span class="sxs-lookup"><span data-stu-id="4484f-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="4484f-198">L’état non opérationnel peut inclure « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="4484f-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="4484f-199">Le « service » peut s’appliquer pendant la mise en miroir de disques, en rechargeant une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="4484f-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="4484f-200">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="4484f-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="4484f-201">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="4484f-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="4484f-202">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4484f-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="4484f-203">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="4484f-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="4484f-204">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="4484f-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="4484f-205">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="4484f-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4484f-206">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="4484f-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="4484f-207">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="4484f-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="4484f-208">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="4484f-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="4484f-209">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="4484f-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="4484f-210">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="4484f-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="4484f-211">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="4484f-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="4484f-212">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="4484f-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="4484f-213">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="4484f-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="4484f-214">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="4484f-214">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="4484f-215"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4484f-215"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="examples"></a><span data-ttu-id="4484f-216">Exemples</span><span class="sxs-lookup"><span data-stu-id="4484f-216">Examples</span></span>

<span data-ttu-id="4484f-217">L’exemple PowerShell [informations de session de connexion de liste](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) retourne des informations sur les sessions de connexion associées à l’utilisateur actuellement connecté à un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4484f-217">The [List Logon Session Information](https://Gallery.TechNet.Microsoft.Com/scriptcenter/64cc7ab5-f1cd-460c-9d37-e6f989444de3) PowerShell sample returns information about logon sessions associated with the user currently logged on to a computer.</span></span>

<span data-ttu-id="4484f-218">L’exemple PowerShell suivant recherche une session à distance ouverte pour un utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="4484f-218">The following PowerShell example checks for remote session open for a specified user.</span></span>


```PowerShell
$user = "<user name>"
$servers = gci servers.txt 

     foreach ($server in $servers){
     $logons = gwmi win32_loggedonuser -computername $server

          foreach ($logon in $logons){
               if ($logon.antecedent -match $user){
               $logonid = $logon.dependent.split("=")[1] 
               $session =gwmi win32_logonsession |? {$_.logonid -match $logonid}
               if ($session.logontype -eq "10"){
               Write-host "You have an active Terminal Server session on server $($server)"
                }
          }
```



## <a name="requirements"></a><span data-ttu-id="4484f-219">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4484f-219">Requirements</span></span>



| <span data-ttu-id="4484f-220">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4484f-220">Requirement</span></span> | <span data-ttu-id="4484f-221">Valeur</span><span class="sxs-lookup"><span data-stu-id="4484f-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4484f-222">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4484f-222">Minimum supported client</span></span><br/> | <span data-ttu-id="4484f-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4484f-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4484f-224">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4484f-224">Minimum supported server</span></span><br/> | <span data-ttu-id="4484f-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4484f-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4484f-226">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4484f-226">Namespace</span></span><br/>                | <span data-ttu-id="4484f-227">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="4484f-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4484f-228">MOF</span><span class="sxs-lookup"><span data-stu-id="4484f-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4484f-229"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4484f-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4484f-230">DLL</span><span class="sxs-lookup"><span data-stu-id="4484f-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4484f-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4484f-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4484f-232">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4484f-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4484f-233">**\_Session Win32**</span><span class="sxs-lookup"><span data-stu-id="4484f-233">**Win32\_Session**</span></span>](win32-session.md)
</dt> <dt>

<span data-ttu-id="4484f-234">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4484f-234">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

