---
title: Classe Win32_TSRemoteControlSetting
description: Définit les paramètres de configuration du contrôle à distance pour la \_ classe de terminal Win32.
ms.assetid: 2e23915e-ee1c-4e53-8d0d-4d3fc2fefce6
ms.tgt_platform: multiple
keywords:
- Win32_TSRemoteControlSetting de la classe Services Bureau à distance
- Win32_TSRemoteControlSetting de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSRemoteControlSetting
- Win32_TSRemoteControlSetting.Caption
- Win32_TSRemoteControlSetting.Description
- Win32_TSRemoteControlSetting.InstallDate
- Win32_TSRemoteControlSetting.Name
- Win32_TSRemoteControlSetting.Status
- Win32_TSRemoteControlSetting.TerminalName
- Win32_TSRemoteControlSetting.LevelOfControl
- Win32_TSRemoteControlSetting.PolicySourceLevelOfControl
- Win32_TSRemoteControlSetting.RemoteControlPolicy
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96e327744ad864e14e1f2580b3b71116e448f36e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465546"
---
# <a name="win32_tsremotecontrolsetting-class"></a><span data-ttu-id="3c2ee-105">\_Classe TSRemoteControlSetting Win32</span><span class="sxs-lookup"><span data-stu-id="3c2ee-105">Win32\_TSRemoteControlSetting class</span></span>

<span data-ttu-id="3c2ee-106">La classe WMI **Win32 \_ TSRemoteControlSetting** définit les paramètres de configuration du contrôle à distance pour la classe de [**\_ Terminal Win32**](win32-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="3c2ee-106">The **Win32\_TSRemoteControlSetting** WMI class defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

<span data-ttu-id="3c2ee-107">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="3c2ee-108">Pour obtenir des informations de référence sur les méthodes, consultez le tableau des méthodes plus loin dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2ee-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c2ee-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSREMOTECONTROLSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSRemoteControlSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   LevelOfControl;
  uint32   PolicySourceLevelOfControl;
  uint32   RemoteControlPolicy;
};
```

## <a name="members"></a><span data-ttu-id="3c2ee-110">Membres</span><span class="sxs-lookup"><span data-stu-id="3c2ee-110">Members</span></span>

<span data-ttu-id="3c2ee-111">La classe **Win32 \_ TSRemoteControlSetting** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3c2ee-111">The **Win32\_TSRemoteControlSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="3c2ee-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3c2ee-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3c2ee-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c2ee-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3c2ee-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3c2ee-114">Methods</span></span>

<span data-ttu-id="3c2ee-115">La classe **Win32 \_ TSRemoteControlSetting** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-115">The **Win32\_TSRemoteControlSetting** class has these methods.</span></span>



| <span data-ttu-id="3c2ee-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="3c2ee-116">Method</span></span>                                                              | <span data-ttu-id="3c2ee-117">Description</span><span class="sxs-lookup"><span data-stu-id="3c2ee-117">Description</span></span>                                                    |
|:--------------------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="3c2ee-118">**RemoteControl**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-118">**RemoteControl**</span></span>](win32-tsremotecontrolsetting-remotecontrol.md) | <span data-ttu-id="3c2ee-119">Définit la propriété **LevelOfControl** de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-119">Sets the **LevelOfControl** property of this class.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3c2ee-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3c2ee-120">Properties</span></span>

<span data-ttu-id="3c2ee-121">La classe **Win32 \_ TSRemoteControlSetting** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-121">The **Win32\_TSRemoteControlSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3c2ee-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2ee-123">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c2ee-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-125">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-125">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3c2ee-126">Brève description (chaîne d’une ligne) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-126">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="3c2ee-127">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3c2ee-127">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c2ee-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2ee-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c2ee-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c2ee-131">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-131">Description of the object.</span></span>

<span data-ttu-id="3c2ee-132">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3c2ee-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c2ee-133">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-133">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2ee-134">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-134">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c2ee-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-136">Qualificateurs : [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="3c2ee-136">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="3c2ee-137">Date à laquelle l’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-137">The date the object was installed.</span></span> <span data-ttu-id="3c2ee-138">L’absence d’une valeur n’indique pas que l’objet n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-138">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="3c2ee-139">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3c2ee-139">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c2ee-140">**LevelOfControl**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-140">**LevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2ee-141">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c2ee-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c2ee-143">Niveau de contrôle de la session, qui spécifie si la session est uniquement affichée par l’utilisateur distant ou affichée et contrôlée par le biais d’un clavier et d’une souris.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-143">Level of control for the session, which specifies whether the session will only be viewed by the remote user, or viewed and controlled through a keyboard and mouse.</span></span> <span data-ttu-id="3c2ee-144">Pour plus d’informations, consultez la section Notes de la méthode [**RemoteControl**](win32-tsremotecontrolsetting-remotecontrol.md) .</span><span class="sxs-lookup"><span data-stu-id="3c2ee-144">For more information, see the Remarks section of the [**RemoteControl**](win32-tsremotecontrolsetting-remotecontrol.md) method.</span></span> <span data-ttu-id="3c2ee-145">Les valeurs suivantes sont admises :</span><span class="sxs-lookup"><span data-stu-id="3c2ee-145">The following values are supported.</span></span>

<dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span data-ttu-id="3c2ee-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Désactiver** (0)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-146"><span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Disable** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3c2ee-147">Le contrôle à distance est désactivé.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-147">Remote control is disabled.</span></span>

</dd> <dt>

<span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>

<span data-ttu-id="3c2ee-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-148"><span id="EnableInputNotify"></span><span id="enableinputnotify"></span><span id="ENABLEINPUTNOTIFY"></span>**EnableInputNotify** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3c2ee-149">L’utilisateur du contrôle à distance a le contrôle total de la session de l’utilisateur, avec l’autorisation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-149">The user of remote control has full control of the user's session, with the user's permission.</span></span>

</dd> <dt>

<span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>

<span data-ttu-id="3c2ee-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-150"><span id="EnableInputNoNotify"></span><span id="enableinputnonotify"></span><span id="ENABLEINPUTNONOTIFY"></span>**EnableInputNoNotify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3c2ee-151">L’utilisateur du contrôle à distance a le contrôle total de la session de l’utilisateur ; l’autorisation de l’utilisateur n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-151">The user of remote control has full control of the user's session; the user's permission is not required.</span></span>

</dd> <dt>

<span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>

<span data-ttu-id="3c2ee-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-152"><span id="EnableNoInputNotify"></span><span id="enablenoinputnotify"></span><span id="ENABLENOINPUTNOTIFY"></span>**EnableNoInputNotify** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3c2ee-153">L’utilisateur du contrôle à distance peut afficher la session à distance, avec l’autorisation de l’utilisateur. l’utilisateur distant ne peut pas contrôler activement la session.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-153">The user of remote control can view the session remotely, with the user's permission; the remote user cannot actively control the session.</span></span>

</dd> <dt>

<span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>

<span data-ttu-id="3c2ee-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-154"><span id="EnableNoInputNoNotify"></span><span id="enablenoinputnonotify"></span><span id="ENABLENOINPUTNONOTIFY"></span>**EnableNoInputNoNotify** (4)</span></span>


</dt> <dd>

<span data-ttu-id="3c2ee-155">L’utilisateur du contrôle à distance peut afficher la session à distance, mais ne contrôle pas activement la session ; l’autorisation de l’utilisateur n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-155">The user of remote control can view the session remotely, but not actively control the session; the user's permission is not required.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3c2ee-156">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2ee-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c2ee-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c2ee-159">Nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-159">The name of the object.</span></span>

<span data-ttu-id="3c2ee-160">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3c2ee-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c2ee-161">**PolicySourceLevelOfControl**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-161">**PolicySourceLevelOfControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2ee-162">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c2ee-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c2ee-164">Indique si la propriété **LevelOfControl** est configurée par le serveur, la stratégie de groupe ou par défaut.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-164">Indicates whether the **LevelOfControl** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="3c2ee-165">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-165">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="3c2ee-166">Serveur</span><span class="sxs-lookup"><span data-stu-id="3c2ee-166">Server</span></span>

</dd> <dt>

<span data-ttu-id="3c2ee-167">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-167">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="3c2ee-168">Stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="3c2ee-168">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="3c2ee-169">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-169">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="3c2ee-170">Default</span><span class="sxs-lookup"><span data-stu-id="3c2ee-170">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3c2ee-171">**RemoteControlPolicy**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-171">**RemoteControlPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2ee-172">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-173">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3c2ee-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3c2ee-174">La stratégie utilisée par le serveur pour récupérer les paramètres de contrôle à distance.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-174">The policy the server uses to retrieve the remote control settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="3c2ee-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Par utilisateur** (0)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-175"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3c2ee-176">Les paramètres de contrôle à distance de l’utilisateur sont activés.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-176">The user's remote control settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="3c2ee-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Serveur-override** (1)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-177"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3c2ee-178">Les paramètres de contrôle à distance de l’utilisateur sont remplacés par le serveur.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-178">The user's remote control settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3c2ee-179">**État**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-179">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2ee-180">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c2ee-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-182">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-182">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="3c2ee-183">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-183">Current status of the object.</span></span> <span data-ttu-id="3c2ee-184">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-184">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="3c2ee-185">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="3c2ee-185">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="3c2ee-186">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="3c2ee-186">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="3c2ee-187">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-187">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="3c2ee-188">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-188">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="3c2ee-189">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="3c2ee-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="3c2ee-190">(« OK »)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-190">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3c2ee-191">(« Erreur »)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-191">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3c2ee-192">(« Détérioré »)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-192">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3c2ee-193">("Inconnu")</span><span class="sxs-lookup"><span data-stu-id="3c2ee-193">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3c2ee-194">(« Échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-194">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3c2ee-195">(« Démarrage »)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-195">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3c2ee-196">(« Arrêt »)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-196">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="3c2ee-197">(« Service »)</span><span class="sxs-lookup"><span data-stu-id="3c2ee-197">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3c2ee-198">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-198">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3c2ee-199">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3c2ee-200">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3c2ee-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3c2ee-201">Nom du terminal.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-201">The name of the terminal.</span></span>

<span data-ttu-id="3c2ee-202">Cette propriété est héritée de [**Win32 \_ TerminalSetting**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="3c2ee-202">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c2ee-203">Notes</span><span class="sxs-lookup"><span data-stu-id="3c2ee-203">Remarks</span></span>

<span data-ttu-id="3c2ee-204">Pour se connecter à \\ l' \\ \\ espace de noms licences TS cimv2 racine, le niveau d’authentification doit inclure la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-204">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="3c2ee-205">Pour les appels C/C++, il s’agit d’un niveau d’authentification de la **\_ \_ \_ \_ \_ confidentialité du niveau d’authentification RPC c**.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-205">For C/C++ calls, this would be an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="3c2ee-206">Pour les Visual Basic et les appels de script, il s’agit d’un niveau d’authentification **WbemAuthenticationLevelPktPrivacy** ou « PktPrivacy », avec une valeur de 6.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-206">For Visual Basic and scripting calls, this would be an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="3c2ee-207">L’exemple de Visual Basic Scripting Edition suivant (VBScript) montre comment se connecter à un ordinateur distant avec la confidentialité du paquet.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-207">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="3c2ee-208">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="3c2ee-208">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3c2ee-209">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-209">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3c2ee-210">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="3c2ee-210">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3c2ee-211">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3c2ee-211">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2ee-212">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c2ee-212">Requirements</span></span>



| <span data-ttu-id="3c2ee-213">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c2ee-213">Requirement</span></span> | <span data-ttu-id="3c2ee-214">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c2ee-214">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2ee-215">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c2ee-215">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2ee-216">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c2ee-216">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3c2ee-217">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c2ee-217">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2ee-218">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c2ee-218">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3c2ee-219">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3c2ee-219">Namespace</span></span><br/>                | <span data-ttu-id="3c2ee-220">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="3c2ee-220">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="3c2ee-221">MOF</span><span class="sxs-lookup"><span data-stu-id="3c2ee-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3c2ee-222"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ee-222"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3c2ee-223">DLL</span><span class="sxs-lookup"><span data-stu-id="3c2ee-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c2ee-224"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ee-224"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c2ee-225">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c2ee-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2ee-226">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-226">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="3c2ee-227">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="3c2ee-227">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

