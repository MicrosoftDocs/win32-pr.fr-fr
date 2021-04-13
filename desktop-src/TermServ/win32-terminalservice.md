---
title: Win32_TerminalService, classe
description: Une sous-classe de la \_ classe de service Win32. Win32 \_ TerminalService représente la propriété d’élément de l' \_ Association Win32 TerminalServiceToSetting.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService de la classe Services Bureau à distance
- Win32_TerminalService de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466726"
---
# <a name="win32_terminalservice-class"></a><span data-ttu-id="63c66-106">\_Classe TerminalService Win32</span><span class="sxs-lookup"><span data-stu-id="63c66-106">Win32\_TerminalService class</span></span>

<span data-ttu-id="63c66-107">La classe WMI **\_ TerminalService** WMI est une sous-classe de la classe de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="63c66-107">The **Win32\_TerminalService** WMI class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="63c66-108">**Win32 \_ TerminalService** représente la propriété d' **élément** de l’Association [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="63c66-108">**Win32\_TerminalService** represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="63c66-109">La syntaxe suivante est simplifiée à partir du code MOF et comprend toutes les propriétés définies et héritées, par ordre alphabétique.</span><span class="sxs-lookup"><span data-stu-id="63c66-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c66-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63c66-110">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a><span data-ttu-id="63c66-111">Membres</span><span class="sxs-lookup"><span data-stu-id="63c66-111">Members</span></span>

<span data-ttu-id="63c66-112">La classe **Win32 \_ TerminalService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="63c66-112">The **Win32\_TerminalService** class has these types of members:</span></span>

-   [<span data-ttu-id="63c66-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="63c66-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="63c66-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63c66-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="63c66-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="63c66-115">Methods</span></span>

<span data-ttu-id="63c66-116">La classe **Win32 \_ TerminalService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="63c66-116">The **Win32\_TerminalService** class has these methods.</span></span>



| <span data-ttu-id="63c66-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="63c66-117">Method</span></span>                                                                       | <span data-ttu-id="63c66-118">Description</span><span class="sxs-lookup"><span data-stu-id="63c66-118">Description</span></span>                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63c66-119">**Modifiés**</span><span class="sxs-lookup"><span data-stu-id="63c66-119">**Change**</span></span>](win32-terminalservice-change.md)                               | <span data-ttu-id="63c66-120">Modifie un service.</span><span class="sxs-lookup"><span data-stu-id="63c66-120">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="63c66-121">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="63c66-121">**ChangeStartMode**</span></span>](win32-terminalservice-changestartmode.md)             | <span data-ttu-id="63c66-122">Modifie le mode de démarrage d’un service.</span><span class="sxs-lookup"><span data-stu-id="63c66-122">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="63c66-123">**Créés**</span><span class="sxs-lookup"><span data-stu-id="63c66-123">**Create**</span></span>](win32-terminalservice-create.md)                               | <span data-ttu-id="63c66-124">Crée un nouveau service.</span><span class="sxs-lookup"><span data-stu-id="63c66-124">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="63c66-125">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="63c66-125">**Delete**</span></span>](win32-terminalservice-delete.md)                               | <span data-ttu-id="63c66-126">Supprime un service existant.</span><span class="sxs-lookup"><span data-stu-id="63c66-126">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="63c66-127">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="63c66-127">**GetSecurityDescriptor**</span></span>](win32-terminalservice-getsecuritydescriptor.md) | <span data-ttu-id="63c66-128">Retourne le descripteur de sécurité qui contrôle l’accès au service.</span><span class="sxs-lookup"><span data-stu-id="63c66-128">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="63c66-129">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="63c66-129">**InterrogateService**</span></span>](win32-terminalservice-interrogateservice.md)       | <span data-ttu-id="63c66-130">Demande qu’un service met à jour son état dans Service Manager.</span><span class="sxs-lookup"><span data-stu-id="63c66-130">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="63c66-131">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="63c66-131">**PauseService**</span></span>](win32-terminalservice-pauseservice.md)                   | <span data-ttu-id="63c66-132">Tente de placer un service dans l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="63c66-132">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="63c66-133">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="63c66-133">**ResumeService**</span></span>](win32-terminalservice-resumeservice.md)                 | <span data-ttu-id="63c66-134">Tente de placer un service dans l’État repris.</span><span class="sxs-lookup"><span data-stu-id="63c66-134">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="63c66-135">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="63c66-135">**SetSecurityDescriptor**</span></span>](win32-terminalservice-setsecuritydescriptor.md) | <span data-ttu-id="63c66-136">Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.</span><span class="sxs-lookup"><span data-stu-id="63c66-136">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="63c66-137">**StartService**</span><span class="sxs-lookup"><span data-stu-id="63c66-137">**StartService**</span></span>](win32-terminalservice-startservice.md)                   | <span data-ttu-id="63c66-138">Tente de placer un service dans l’état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="63c66-138">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="63c66-139">**StopService**</span><span class="sxs-lookup"><span data-stu-id="63c66-139">**StopService**</span></span>](win32-terminalservice-stopservice.md)                     | <span data-ttu-id="63c66-140">Place un service dans l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="63c66-140">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="63c66-141">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="63c66-141">**UserControlService**</span></span>](win32-terminalservice-usercontrolservice.md)       | <span data-ttu-id="63c66-142">Tente d’envoyer un code de contrôle défini par l’utilisateur à un service.</span><span class="sxs-lookup"><span data-stu-id="63c66-142">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="63c66-143">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63c66-143">Properties</span></span>

<span data-ttu-id="63c66-144">La classe **Win32 \_ TerminalService** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="63c66-144">The **Win32\_TerminalService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63c66-145">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="63c66-145">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-146">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63c66-146">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-147">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-148">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| service \_ accepter \_ pause \_ continue"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("service accepte pause")</span><span class="sxs-lookup"><span data-stu-id="63c66-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-149">Indique si le service peut être suspendu.</span><span class="sxs-lookup"><span data-stu-id="63c66-149">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="63c66-150">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-150">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-151">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="63c66-151">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-152">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63c66-152">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-153">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-154">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| service \_ accepter \_ Stop"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("service accepte Stop")</span><span class="sxs-lookup"><span data-stu-id="63c66-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-155">Indique si le service peut être arrêté.</span><span class="sxs-lookup"><span data-stu-id="63c66-155">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="63c66-156">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-156">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-157">**Caption**</span><span class="sxs-lookup"><span data-stu-id="63c66-157">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-158">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-159">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-160">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="63c66-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-161">Description succincte du service chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="63c66-161">Short description of the service  a one-line string.</span></span>

<span data-ttu-id="63c66-162">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="63c66-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-163">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="63c66-163">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-164">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63c66-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-166">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("check point Count")</span><span class="sxs-lookup"><span data-stu-id="63c66-166">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-167">Valeur que le service incrémente régulièrement pour signaler sa progression pendant une opération de démarrage, d’arrêt, de suspension ou de poursuite de longue durée.</span><span class="sxs-lookup"><span data-stu-id="63c66-167">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="63c66-168">Par exemple, le service incrémente cette valeur lors de la fin de chaque étape de son initialisation au démarrage.</span><span class="sxs-lookup"><span data-stu-id="63c66-168">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="63c66-169">Le programme d’interface utilisateur qui appelle l’opération sur le service utilise cette valeur pour suivre la progression du service au cours d’une opération de longue durée.</span><span class="sxs-lookup"><span data-stu-id="63c66-169">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="63c66-170">Cette valeur n’est pas valide et doit être égale à zéro lorsque l’opération de démarrage, d’arrêt, de suspension ou de reprise du service n’est pas en attente.</span><span class="sxs-lookup"><span data-stu-id="63c66-170">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

<span data-ttu-id="63c66-171">Cette propriété est héritée [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="63c66-171">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-172">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="63c66-172">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-173">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-174">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-175">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="63c66-175">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-176">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="63c66-176">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="63c66-177">Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="63c66-177">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="63c66-178">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="63c66-178">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-179">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="63c66-179">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-180">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63c66-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-181">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-182">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures service \| [**\_ retardées \_ \_ \_ informations de démarrage automatique**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« démarrage automatique retardé »)</span><span class="sxs-lookup"><span data-stu-id="63c66-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-183">Si la **valeur est true**, le service est démarré après le démarrage d’autres services à démarrage automatique, plus un bref délai.</span><span class="sxs-lookup"><span data-stu-id="63c66-183">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="63c66-184">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63c66-184">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

<span data-ttu-id="63c66-185">Cette propriété est héritée [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="63c66-185">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-186">**Description**</span><span class="sxs-lookup"><span data-stu-id="63c66-186">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-189">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="63c66-189">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-190">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63c66-190">Description of the object.</span></span>

<span data-ttu-id="63c66-191">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="63c66-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-192">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="63c66-192">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-193">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63c66-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-194">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-195">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ configuration**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| \_ Process interactive \_ Process »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« interagit avec Desktop »)</span><span class="sxs-lookup"><span data-stu-id="63c66-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-196">Indique si le service peut créer ou communiquer avec Windows sur le bureau, et par conséquent interagir de quelque manière avec un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63c66-196">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="63c66-197">Les services interactifs doivent s’exécuter sous le compte système local.</span><span class="sxs-lookup"><span data-stu-id="63c66-197">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="63c66-198">La plupart des services ne sont pas interactifs. autrement dit, ils ne communiquent pas avec l’utilisateur de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="63c66-198">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="63c66-199">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-199">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-200">**DisconnectedSessions**</span><span class="sxs-lookup"><span data-stu-id="63c66-200">**DisconnectedSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-201">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63c66-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-202">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63c66-203">Nombre de sessions déconnectées sur le serveur actuel.</span><span class="sxs-lookup"><span data-stu-id="63c66-203">The number of disconnected sessions on the current server.</span></span> <span data-ttu-id="63c66-204">Ces sessions peuvent toujours consommer activement les ressources du serveur, mais elles ne disposent pas actuellement d’une connexion réseau avec un client.</span><span class="sxs-lookup"><span data-stu-id="63c66-204">These sessions may still be actively consuming server resources, however they currently have no network connection with a client.</span></span>

</dd> <dt>

<span data-ttu-id="63c66-205">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="63c66-205">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-206">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-207">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-208">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Display Name »)</span><span class="sxs-lookup"><span data-stu-id="63c66-208">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-209">Nom du service tel qu’il est affiché dans le composant logiciel enfichable Services.</span><span class="sxs-lookup"><span data-stu-id="63c66-209">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="63c66-210">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="63c66-210">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="63c66-211">Notez que le nom d’affichage et le nom du service (qui est stocké dans le registre) ne sont pas toujours identiques.</span><span class="sxs-lookup"><span data-stu-id="63c66-211">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="63c66-212">Par exemple, le service client DHCP a le nom de service DHCP, mais le nom d’affichage client DHCP.</span><span class="sxs-lookup"><span data-stu-id="63c66-212">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="63c66-213">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="63c66-213">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="63c66-214">Toutefois, les comparaisons [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="63c66-214">However, [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) comparisons are always case-insensitive.</span></span>

<span data-ttu-id="63c66-215">Constraint : accepte la même valeur que la propriété [**Name**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="63c66-215">Constraint: Accepts the same value as the [**Name**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span>

<span data-ttu-id="63c66-216">Exemple : « Atdisk »</span><span class="sxs-lookup"><span data-stu-id="63c66-216">Example: "Atdisk"</span></span>

<span data-ttu-id="63c66-217">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-217">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-218">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="63c66-218">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-221">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« gravité de l’échec de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="63c66-221">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-222">Gravité de l’erreur si ce service ne parvient pas à démarrer au démarrage.</span><span class="sxs-lookup"><span data-stu-id="63c66-222">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="63c66-223">La valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="63c66-223">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="63c66-224">Toutes les erreurs sont journalisées par le système informatique.</span><span class="sxs-lookup"><span data-stu-id="63c66-224">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="63c66-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** ("ignorer")</span><span class="sxs-lookup"><span data-stu-id="63c66-225"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="63c66-226">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="63c66-226">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="63c66-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (« normal »)</span><span class="sxs-lookup"><span data-stu-id="63c66-227"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="63c66-228">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="63c66-228">User is notified.</span></span> <span data-ttu-id="63c66-229">Il s’agit généralement d’un message indiquant que l’utilisateur du problème est affiché.</span><span class="sxs-lookup"><span data-stu-id="63c66-229">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="63c66-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (« grave »)</span><span class="sxs-lookup"><span data-stu-id="63c66-230"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="63c66-231">Le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="63c66-231">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="63c66-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (« critique »)</span><span class="sxs-lookup"><span data-stu-id="63c66-232"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="63c66-233">Le système tente de redémarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="63c66-233">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="63c66-234">Si le service ne démarre pas une deuxième fois, le démarrage échoue.</span><span class="sxs-lookup"><span data-stu-id="63c66-234">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63c66-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="63c66-235"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="63c66-236">La gravité de l’erreur est inconnue.</span><span class="sxs-lookup"><span data-stu-id="63c66-236">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="63c66-237">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-237">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-238">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="63c66-238">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-239">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63c66-239">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-241">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("code de sortie")</span><span class="sxs-lookup"><span data-stu-id="63c66-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-242">Code d’erreur Windows qui définit les erreurs rencontrées lors du démarrage ou de l’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="63c66-242">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="63c66-243">Cette propriété est définie sur **erreur \_ spécifique au service \_ \_** (1066) lorsque l’erreur est unique pour le service représenté par cette classe, et les informations sur l’erreur sont disponibles dans la propriété [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="63c66-243">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the [**ServiceSpecificExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property.</span></span> <span data-ttu-id="63c66-244">Le service définit cette valeur sur **aucune \_ erreur** lors de l’exécution, et à nouveau sur fin normale.</span><span class="sxs-lookup"><span data-stu-id="63c66-244">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="63c66-245">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-245">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-246">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="63c66-246">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-247">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="63c66-247">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-248">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-249">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="63c66-249">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-250">L’objet date est installé.</span><span class="sxs-lookup"><span data-stu-id="63c66-250">Date object is installed.</span></span> <span data-ttu-id="63c66-251">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="63c66-251">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="63c66-252">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="63c66-252">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-253">**Nom**</span><span class="sxs-lookup"><span data-stu-id="63c66-253">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-254">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-254">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-255">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-255">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-256">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63c66-256">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63c66-257">Identificateur unique du service qui fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="63c66-257">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="63c66-258">Cette fonctionnalité est décrite dans la propriété [**Description**](/windows/desktop/CIMWin32Prov/win32-service) de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63c66-258">This functionality is described in the [**Description**](/windows/desktop/CIMWin32Prov/win32-service) property of the object.</span></span>

<span data-ttu-id="63c66-259">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="63c66-259">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-260">**PathName**</span><span class="sxs-lookup"><span data-stu-id="63c66-260">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-261">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-262">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-263">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file path Name")</span><span class="sxs-lookup"><span data-stu-id="63c66-263">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-264">Chemin d’accès complet au fichier binaire de service qui implémente le service.</span><span class="sxs-lookup"><span data-stu-id="63c66-264">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="63c66-265">Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="63c66-265">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="63c66-266">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-266">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-267">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="63c66-267">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-268">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63c66-268">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-270">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Process structures service \| [**\_ Status \_ Process**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process ID")</span><span class="sxs-lookup"><span data-stu-id="63c66-270">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-271">Identificateur de processus du service.</span><span class="sxs-lookup"><span data-stu-id="63c66-271">Process identifier of the service.</span></span>

<span data-ttu-id="63c66-272">Exemple : 324</span><span class="sxs-lookup"><span data-stu-id="63c66-272">Example: 324</span></span>

<span data-ttu-id="63c66-273">Cette propriété est héritée [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="63c66-273">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-274">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="63c66-274">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-275">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63c66-275">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-276">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-277">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("code de sortie spécifique au serveur")</span><span class="sxs-lookup"><span data-stu-id="63c66-277">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-278">Code d’erreur spécifique au service pour les erreurs qui se produisent pendant que le service est en cours de démarrage ou d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="63c66-278">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="63c66-279">Les codes de sortie sont définis par le service représenté par cette classe.</span><span class="sxs-lookup"><span data-stu-id="63c66-279">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="63c66-280">Cette valeur est définie uniquement lorsque la valeur de la propriété [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) est erreur **\_ spécifique au service \_ \_** (1066).</span><span class="sxs-lookup"><span data-stu-id="63c66-280">This value is only set when the [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="63c66-281">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-281">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-282">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="63c66-282">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-283">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-284">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-285">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de service")</span><span class="sxs-lookup"><span data-stu-id="63c66-285">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-286">Type de service fourni aux processus appelants.</span><span class="sxs-lookup"><span data-stu-id="63c66-286">Type of service provided to calling processes.</span></span>

<span data-ttu-id="63c66-287">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="63c66-287">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="63c66-288">**Pilote de noyau** (« pilote de noyau »)</span><span class="sxs-lookup"><span data-stu-id="63c66-288">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="63c66-289">**Pilote du système de fichiers** (« pilote du système de fichiers »)</span><span class="sxs-lookup"><span data-stu-id="63c66-289">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="63c66-290">**Carte** (« adaptateur »)</span><span class="sxs-lookup"><span data-stu-id="63c66-290">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="63c66-291">**Pilote de reconnaissance** (« pilote de reconnaissance »)</span><span class="sxs-lookup"><span data-stu-id="63c66-291">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="63c66-292">**Propre processus** (« propre processus »)</span><span class="sxs-lookup"><span data-stu-id="63c66-292">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="63c66-293">**Processus de partage** (« processus de partage »)</span><span class="sxs-lookup"><span data-stu-id="63c66-293">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="63c66-294">**Processus interactif** (« processus interactif »)</span><span class="sxs-lookup"><span data-stu-id="63c66-294">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="63c66-295"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="63c66-295"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="63c66-296">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-296">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-297">**Cours**</span><span class="sxs-lookup"><span data-stu-id="63c66-297">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-298">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63c66-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-299">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-300">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="63c66-300">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-301">Indique si le service est démarré ou non.</span><span class="sxs-lookup"><span data-stu-id="63c66-301">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="63c66-302">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="63c66-302">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-303">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="63c66-303">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-304">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-305">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-306">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« mode de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="63c66-306">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-307">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="63c66-307">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="63c66-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Démarrage** (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="63c66-308"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="63c66-309">Pilote de périphérique Démarré par le chargeur du système d’exploitation (valide uniquement pour les services de pilote).</span><span class="sxs-lookup"><span data-stu-id="63c66-309">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="63c66-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Système** (« système »)</span><span class="sxs-lookup"><span data-stu-id="63c66-310"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="63c66-311">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="63c66-311">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="63c66-312">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="63c66-312">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="63c66-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** (« auto »)</span><span class="sxs-lookup"><span data-stu-id="63c66-313"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="63c66-314">Le service doit être démarré automatiquement par le Gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="63c66-314">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="63c66-315">Les services automatiques sont démarrés même si un utilisateur ne se connecte pas.</span><span class="sxs-lookup"><span data-stu-id="63c66-315">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="63c66-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuel** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="63c66-316"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="63c66-317">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="63c66-317">Service to be started by the Service Control Manager when a process calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="63c66-318">Ces services ne démarrent pas à moins qu’un utilisateur se connecte et ne les démarre.</span><span class="sxs-lookup"><span data-stu-id="63c66-318">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="63c66-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")</span><span class="sxs-lookup"><span data-stu-id="63c66-319"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="63c66-320">Service qui ne peut pas être démarré tant que son StartMode n’a pas été modifié en auto ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="63c66-320">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="63c66-321">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="63c66-321">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-322">**StartName**</span><span class="sxs-lookup"><span data-stu-id="63c66-322">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-323">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-325">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Starting Account Name »)</span><span class="sxs-lookup"><span data-stu-id="63c66-325">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-326">Nom du compte sous lequel un service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="63c66-326">Account name under which a service runs.</span></span> <span data-ttu-id="63c66-327">Selon le type de service, le nom du compte peut se présenter sous la forme « nom_domaine \\ nom_utilisateur » ou au format UPN (« *Username@DomainName* »).</span><span class="sxs-lookup"><span data-stu-id="63c66-327">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="63c66-328">Le processus de service est enregistré à l’aide de l’une de ces deux formes lorsqu’il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="63c66-328">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="63c66-329">Si le compte appartient au domaine intégré, «. \\ Nom d’utilisateur» peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="63c66-329">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="63c66-330">Pour les pilotes au niveau du noyau ou du système, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contient le nom d’objet du pilote (c’est-à-dire « \\ FileSystem \\ RDR » ou « \\ Driver \\ XNS ») que le système d’e/s utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="63c66-330">For kernel or system-level drivers, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="63c66-331">En outre, si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.</span><span class="sxs-lookup"><span data-stu-id="63c66-331">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="63c66-332">Exemple : « DWDOM \\ admin »</span><span class="sxs-lookup"><span data-stu-id="63c66-332">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="63c66-333">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-333">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-334">**State**</span><span class="sxs-lookup"><span data-stu-id="63c66-334">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-335">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-336">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63c66-336">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="63c66-337">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span><span class="sxs-lookup"><span data-stu-id="63c66-337">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-338">État actuel du service de base.</span><span class="sxs-lookup"><span data-stu-id="63c66-338">Current state of the base service.</span></span>

<span data-ttu-id="63c66-339">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="63c66-339">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="63c66-340">**Arrêté** (« arrêté »)</span><span class="sxs-lookup"><span data-stu-id="63c66-340">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="63c66-341">**Start Pending** (« Start Pending »)</span><span class="sxs-lookup"><span data-stu-id="63c66-341">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="63c66-342">**Arrêt en attente** (« arrêt en attente »)</span><span class="sxs-lookup"><span data-stu-id="63c66-342">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="63c66-343">**En cours d’exécution** (« en cours d’exécution »)</span><span class="sxs-lookup"><span data-stu-id="63c66-343">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="63c66-344">**Poursuite en attente** ("continuer en attente")</span><span class="sxs-lookup"><span data-stu-id="63c66-344">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="63c66-345">**Pause en attente** ("pause en attente")</span><span class="sxs-lookup"><span data-stu-id="63c66-345">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="63c66-346">**Suspendu** (« suspendu »)</span><span class="sxs-lookup"><span data-stu-id="63c66-346">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63c66-347">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="63c66-347">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="63c66-348"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="63c66-348"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="63c66-349">**Windows Server 2008 et Windows Vista :** Cette propriété est en lecture seule avant Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="63c66-349">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="63c66-350">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-350">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-351">**État**</span><span class="sxs-lookup"><span data-stu-id="63c66-351">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-352">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-352">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-353">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-353">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-354">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="63c66-354">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-355">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63c66-355">Current status of the object.</span></span> <span data-ttu-id="63c66-356">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="63c66-356">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="63c66-357">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="63c66-357">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="63c66-358">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="63c66-358">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="63c66-359">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="63c66-359">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="63c66-360">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="63c66-360">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="63c66-361">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="63c66-361">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="63c66-362">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="63c66-362">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="63c66-363">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="63c66-363">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="63c66-364">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="63c66-364">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63c66-365">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="63c66-365">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="63c66-366">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="63c66-366">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="63c66-367">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="63c66-367">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="63c66-368">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="63c66-368">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="63c66-369">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="63c66-369">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="63c66-370">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="63c66-370">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="63c66-371">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="63c66-371">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="63c66-372">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="63c66-372">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="63c66-373">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="63c66-373">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="63c66-374"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="63c66-374"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="63c66-375">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="63c66-375">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-376">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="63c66-376">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-377">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-377">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-379">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName "), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="63c66-379">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).CreationClassName"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-380">Nom de type du système qui héberge ce service.</span><span class="sxs-lookup"><span data-stu-id="63c66-380">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="63c66-381">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="63c66-381">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-382">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="63c66-382">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-383">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63c66-383">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-384">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-384">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-385">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](/windows/desktop/CIMWin32Prov/cim-system). Name "), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="63c66-385">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system).Name"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-386">Nom du système qui héberge ce service.</span><span class="sxs-lookup"><span data-stu-id="63c66-386">Name of the system that hosts this service.</span></span>

<span data-ttu-id="63c66-387">Cette propriété est héritée [**du \_ service CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="63c66-387">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-388">**TagId**</span><span class="sxs-lookup"><span data-stu-id="63c66-388">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-389">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63c66-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-390">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-390">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-391">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« ID de balise »)</span><span class="sxs-lookup"><span data-stu-id="63c66-391">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-392">Valeur de balise unique pour ce service dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="63c66-392">Unique tag value for this service in the group.</span></span> <span data-ttu-id="63c66-393">La valeur 0 (zéro) indique que le service n’a pas de balise.</span><span class="sxs-lookup"><span data-stu-id="63c66-393">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="63c66-394">Une balise peut être utilisée pour ordonner le démarrage du service dans un groupe d’ordre de chargement en spécifiant un vecteur d’ordre des balises dans le registre à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="63c66-394">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="63c66-395">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local GroupOrderList    </span><span class="sxs-lookup"><span data-stu-id="63c66-395">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="63c66-396">Les balises sont uniquement évaluées pour les services de type démarrage du pilote du noyau et du pilote du système de fichiers qui ont des modes de démarrage ou de démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="63c66-396">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="63c66-397">Cette propriété est héritée de [**Win32 \_ BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span><span class="sxs-lookup"><span data-stu-id="63c66-397">This property is inherited from [**Win32\_BaseService**](/windows/desktop/CIMWin32Prov/win32-baseservice).</span></span>

</dd> <dt>

<span data-ttu-id="63c66-398">**TotalSessions**</span><span class="sxs-lookup"><span data-stu-id="63c66-398">**TotalSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-399">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63c66-399">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-400">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-400">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="63c66-401">Nombre total de sessions sur le serveur actuel.</span><span class="sxs-lookup"><span data-stu-id="63c66-401">The total number of sessions on the current server.</span></span> <span data-ttu-id="63c66-402">Cela comprend les sessions connectées et déconnectées.</span><span class="sxs-lookup"><span data-stu-id="63c66-402">This includes both connected and disconnected sessions.</span></span>

</dd> <dt>

<span data-ttu-id="63c66-403">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="63c66-403">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63c66-404">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63c66-404">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63c66-405">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63c66-405">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63c66-406">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« temps d’attente estimé »)</span><span class="sxs-lookup"><span data-stu-id="63c66-406">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="63c66-407">Durée estimée, en millisecondes, pour une opération de démarrage, d’arrêt, de suspension ou de continuation en attente.</span><span class="sxs-lookup"><span data-stu-id="63c66-407">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="63c66-408">Une fois le temps spécifié écoulé, le service effectue son prochain appel à la méthode **SetServiceStatus** avec une valeur [**de point de contrôle**](/windows/desktop/CIMWin32Prov/win32-service) incrémentée ou une modification dans **CurrentState**.</span><span class="sxs-lookup"><span data-stu-id="63c66-408">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented [**CheckPoint**](/windows/desktop/CIMWin32Prov/win32-service) value or a change in **CurrentState**.</span></span> <span data-ttu-id="63c66-409">Si la durée spécifiée par **WaitHint** passe, si le **point** de contrôle n’a pas été incrémenté ou si **CurrentState** n’a pas changé, le gestionnaire de contrôle des services ou le programme de contrôle des services suppose qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="63c66-409">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

<span data-ttu-id="63c66-410">Cette propriété est héritée [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).</span><span class="sxs-lookup"><span data-stu-id="63c66-410">This property is inherited from [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63c66-411">Notes</span><span class="sxs-lookup"><span data-stu-id="63c66-411">Remarks</span></span>

<span data-ttu-id="63c66-412">Étant donné que la classe **\_ TerminalService Win32** est une sous-classe de la classe de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) , la classe hérite de toutes les propriétés et méthodes du **\_ service Win32**.</span><span class="sxs-lookup"><span data-stu-id="63c66-412">Since the **Win32\_TerminalService** class is a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class, the class inherits all properties and methods of **Win32\_Service**.</span></span>

<span data-ttu-id="63c66-413">[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) est associé à **Win32 \_ TerminalService** en tant que propriété de **paramètre** de l’Association [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="63c66-413">[**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="63c66-414">[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) est associé à **Win32 \_ TerminalService** en tant que propriété de **paramètre** de l’Association [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="63c66-414">[**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) is associated to **Win32\_TerminalService** as the **Setting** property of the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) association.</span></span>

<span data-ttu-id="63c66-415">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="63c66-415">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="63c66-416">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="63c66-416">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="63c66-417">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="63c66-417">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="63c66-418">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="63c66-418">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="63c66-419">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63c66-419">Requirements</span></span>



| <span data-ttu-id="63c66-420">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63c66-420">Requirement</span></span> | <span data-ttu-id="63c66-421">Valeur</span><span class="sxs-lookup"><span data-stu-id="63c66-421">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63c66-422">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63c66-422">Minimum supported client</span></span><br/> | <span data-ttu-id="63c66-423">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63c66-423">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63c66-424">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63c66-424">Minimum supported server</span></span><br/> | <span data-ttu-id="63c66-425">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63c66-425">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63c66-426">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63c66-426">Namespace</span></span><br/>                | <span data-ttu-id="63c66-427">Racine\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="63c66-427">Root\\CIMv2</span></span><br/>                                                                  |
| <span data-ttu-id="63c66-428">MOF</span><span class="sxs-lookup"><span data-stu-id="63c66-428">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63c66-429"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63c66-429"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="63c66-430">DLL</span><span class="sxs-lookup"><span data-stu-id="63c66-430">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63c66-431"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63c66-431"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63c66-432">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63c66-432">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63c66-433">**\_Service Win32**</span><span class="sxs-lookup"><span data-stu-id="63c66-433">**Win32\_Service**</span></span>](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[<span data-ttu-id="63c66-434">**\_TerminalServiceToSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="63c66-434">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="63c66-435">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="63c66-435">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dt>

[<span data-ttu-id="63c66-436">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="63c66-436">**Win32\_BaseService**</span></span>](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[<span data-ttu-id="63c66-437">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="63c66-437">**CIM\_Service**</span></span>](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

