---
description: Représente un service sur un système informatique exécutant Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Classe Win32_Service
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b342282bfa3b49fe72e62cf79377a0ead11276eb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033605"
---
# <a name="win32_service-class"></a><span data-ttu-id="63259-103">\_Classe de service Win32</span><span class="sxs-lookup"><span data-stu-id="63259-103">Win32\_Service class</span></span>

<span data-ttu-id="63259-104">La [classe WMI](../wmisdk/retrieving-a-class.md) du **\_ service Win32** représente un service sur un système informatique exécutant Windows.</span><span class="sxs-lookup"><span data-stu-id="63259-104">The **Win32\_Service** [WMI class](../wmisdk/retrieving-a-class.md) represents a service on a computer system running Windows.</span></span>

<span data-ttu-id="63259-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="63259-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="63259-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="63259-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="63259-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63259-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a><span data-ttu-id="63259-108">Membres</span><span class="sxs-lookup"><span data-stu-id="63259-108">Members</span></span>

<span data-ttu-id="63259-109">La classe de **\_ service Win32** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="63259-109">The **Win32\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="63259-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="63259-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="63259-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63259-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="63259-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="63259-112">Methods</span></span>

<span data-ttu-id="63259-113">La classe de **\_ service Win32** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="63259-113">The **Win32\_Service** class has these methods.</span></span>



| <span data-ttu-id="63259-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="63259-114">Method</span></span>                                                                               | <span data-ttu-id="63259-115">Description</span><span class="sxs-lookup"><span data-stu-id="63259-115">Description</span></span>                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63259-116">**Modifiés**</span><span class="sxs-lookup"><span data-stu-id="63259-116">**Change**</span></span>](change-method-in-class-win32-service.md)                               | <span data-ttu-id="63259-117">Modifie un service.</span><span class="sxs-lookup"><span data-stu-id="63259-117">Modifies a service.</span></span><br/>                                                                       |
| [<span data-ttu-id="63259-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="63259-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-service.md)             | <span data-ttu-id="63259-119">Modifie le mode de démarrage d’un service.</span><span class="sxs-lookup"><span data-stu-id="63259-119">Modifies the start mode of a service.</span></span><br/>                                                     |
| [<span data-ttu-id="63259-120">**Créés**</span><span class="sxs-lookup"><span data-stu-id="63259-120">**Create**</span></span>](create-method-in-class-win32-service.md)                               | <span data-ttu-id="63259-121">Crée un nouveau service.</span><span class="sxs-lookup"><span data-stu-id="63259-121">Creates a new service.</span></span><br/>                                                                    |
| [<span data-ttu-id="63259-122">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="63259-122">**Delete**</span></span>](delete-method-in-class-win32-service.md)                               | <span data-ttu-id="63259-123">Supprime un service existant.</span><span class="sxs-lookup"><span data-stu-id="63259-123">Deletes an existing service.</span></span><br/>                                                              |
| [<span data-ttu-id="63259-124">**GetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="63259-124">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="63259-125">Retourne le descripteur de sécurité qui contrôle l’accès au service.</span><span class="sxs-lookup"><span data-stu-id="63259-125">Returns the security descriptor that controls access to the service.</span></span><br/>                      |
| [<span data-ttu-id="63259-126">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="63259-126">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-service.md)       | <span data-ttu-id="63259-127">Demande qu’un service met à jour son état dans Service Manager.</span><span class="sxs-lookup"><span data-stu-id="63259-127">Requests that a service update its state to the service manager.</span></span><br/>                          |
| [<span data-ttu-id="63259-128">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="63259-128">**PauseService**</span></span>](pauseservice-method-in-class-win32-service.md)                   | <span data-ttu-id="63259-129">Tente de placer un service dans l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="63259-129">Attempts to place a service in the paused state.</span></span><br/>                                          |
| [<span data-ttu-id="63259-130">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="63259-130">**ResumeService**</span></span>](resumeservice-method-in-class-win32-service.md)                 | <span data-ttu-id="63259-131">Tente de placer un service dans l’État repris.</span><span class="sxs-lookup"><span data-stu-id="63259-131">Attempts to place a service in the resumed state.</span></span><br/>                                         |
| [<span data-ttu-id="63259-132">**SetSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="63259-132">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-service.md) | <span data-ttu-id="63259-133">Écrit une version mise à jour du descripteur de sécurité qui contrôle l’accès au service.</span><span class="sxs-lookup"><span data-stu-id="63259-133">Writes an updated version of the security descriptor that controls access to the service.</span></span><br/> |
| [<span data-ttu-id="63259-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="63259-134">**StartService**</span></span>](startservice-method-in-class-win32-service.md)                   | <span data-ttu-id="63259-135">Tente de placer un service dans l’état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="63259-135">Attempts to place a service into the startup state.</span></span><br/>                                       |
| [<span data-ttu-id="63259-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="63259-136">**StopService**</span></span>](stopservice-method-in-class-win32-service.md)                     | <span data-ttu-id="63259-137">Place un service dans l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="63259-137">Places a service in the stopped state.</span></span><br/>                                                    |
| [<span data-ttu-id="63259-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="63259-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-service.md)       | <span data-ttu-id="63259-139">Tente d’envoyer un code de contrôle défini par l’utilisateur à un service.</span><span class="sxs-lookup"><span data-stu-id="63259-139">Attempts to send a user-defined control code to a service.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="63259-140">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63259-140">Properties</span></span>

<span data-ttu-id="63259-141">La classe de **\_ service Win32** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="63259-141">The **Win32\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63259-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="63259-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63259-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63259-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-145">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**service \_**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| service \_ accepter \_ pause \_ continue"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("service accepte pause")</span><span class="sxs-lookup"><span data-stu-id="63259-145">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="63259-146">Indique si le service peut être suspendu.</span><span class="sxs-lookup"><span data-stu-id="63259-146">Indicates whether the service can be paused.</span></span>

<span data-ttu-id="63259-147">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-147">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-148">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="63259-148">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-149">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63259-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63259-150">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-151">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**service \_**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| service \_ accepter \_ Stop"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("service accepte Stop")</span><span class="sxs-lookup"><span data-stu-id="63259-151">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="63259-152">Indique si le service peut être arrêté.</span><span class="sxs-lookup"><span data-stu-id="63259-152">Indicates whether the service can be stopped.</span></span>

<span data-ttu-id="63259-153">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-153">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-154">**Caption**</span><span class="sxs-lookup"><span data-stu-id="63259-154">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-155">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-156">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-157">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="63259-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="63259-158">Brève description du service : chaîne d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="63259-158">Short description of the service —a one-line string.</span></span>

<span data-ttu-id="63259-159">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63259-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-160">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="63259-160">**CheckPoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-161">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63259-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63259-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-163">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("check point Count")</span><span class="sxs-lookup"><span data-stu-id="63259-163">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")</span></span>
</dt> </dl>

<span data-ttu-id="63259-164">Valeur que le service incrémente régulièrement pour signaler sa progression pendant une opération de démarrage, d’arrêt, de suspension ou de poursuite de longue durée.</span><span class="sxs-lookup"><span data-stu-id="63259-164">Value that the service increments periodically to report its progress during a long start, stop, pause, or continue operation.</span></span> <span data-ttu-id="63259-165">Par exemple, le service incrémente cette valeur lors de la fin de chaque étape de son initialisation au démarrage.</span><span class="sxs-lookup"><span data-stu-id="63259-165">For example, the service increments this value as it completes each step of its initialization when it is starting up.</span></span> <span data-ttu-id="63259-166">Le programme d’interface utilisateur qui appelle l’opération sur le service utilise cette valeur pour suivre la progression du service au cours d’une opération de longue durée.</span><span class="sxs-lookup"><span data-stu-id="63259-166">The user interface program that invokes the operation on the service uses this value to track the progress of the service during a lengthy operation.</span></span> <span data-ttu-id="63259-167">Cette valeur n’est pas valide et doit être égale à zéro lorsque l’opération de démarrage, d’arrêt, de suspension ou de reprise du service n’est pas en attente.</span><span class="sxs-lookup"><span data-stu-id="63259-167">This value is not valid and should be zero when the service does not have a start, stop, pause, or continue operation pending.</span></span>

</dd> <dt>

<span data-ttu-id="63259-168">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="63259-168">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-170">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-171">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="63259-171">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="63259-172">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="63259-172">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="63259-173">Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="63259-173">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="63259-174">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="63259-174">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-175">**DelayedAutoStart**</span><span class="sxs-lookup"><span data-stu-id="63259-175">**DelayedAutoStart**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-176">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63259-176">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63259-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-178">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures service \| [**\_ retardées \_ \_ \_ informations de démarrage automatique**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« démarrage automatique retardé »)</span><span class="sxs-lookup"><span data-stu-id="63259-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_DELAYED\_AUTO\_START\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info)\|fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Delayed Auto-Start")</span></span>
</dt> </dl>

<span data-ttu-id="63259-179">Si la **valeur est true**, le service est démarré après le démarrage d’autres services à démarrage automatique, plus un bref délai.</span><span class="sxs-lookup"><span data-stu-id="63259-179">If **True**, the service is started after other auto-start services are started plus a short delay.</span></span>

<span data-ttu-id="63259-180">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista :** Cette propriété n’est pas prise en charge avant Windows Server 2016 et Windows 10.</span><span class="sxs-lookup"><span data-stu-id="63259-180">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> <dt>

<span data-ttu-id="63259-181">**Description**</span><span class="sxs-lookup"><span data-stu-id="63259-181">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-182">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-183">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-184">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="63259-184">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="63259-185">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63259-185">Description of the object.</span></span>

<span data-ttu-id="63259-186">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63259-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-187">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="63259-187">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-188">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63259-188">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63259-189">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-190">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ configuration**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| \_ Process interactive \_ Process »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« interagit avec Desktop »)</span><span class="sxs-lookup"><span data-stu-id="63259-190">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="63259-191">Indique si le service peut créer ou communiquer avec Windows sur le bureau, et par conséquent interagir de quelque manière avec un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63259-191">Indicates whether the service can create or communicate with windows on the desktop, and thus interact in some way with a user.</span></span> <span data-ttu-id="63259-192">Les services interactifs doivent s’exécuter sous le compte système local.</span><span class="sxs-lookup"><span data-stu-id="63259-192">Interactive services must run under the Local System account.</span></span> <span data-ttu-id="63259-193">La plupart des services ne sont pas interactifs. autrement dit, ils ne communiquent pas avec l’utilisateur de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="63259-193">Most services are not interactive; that is, they do not communicate with the user in any way.</span></span>

<span data-ttu-id="63259-194">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-194">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-195">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="63259-195">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-196">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-197">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-198">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Display Name »)</span><span class="sxs-lookup"><span data-stu-id="63259-198">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="63259-199">Nom du service tel qu’il est affiché dans le composant logiciel enfichable Services.</span><span class="sxs-lookup"><span data-stu-id="63259-199">Name of the service as viewed in the Services snap-in.</span></span> <span data-ttu-id="63259-200">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="63259-200">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="63259-201">Notez que le nom d’affichage et le nom du service (qui est stocké dans le registre) ne sont pas toujours identiques.</span><span class="sxs-lookup"><span data-stu-id="63259-201">Note that the display name and the service name (which is stored in the registry) are not always the same.</span></span> <span data-ttu-id="63259-202">Par exemple, le service client DHCP a le nom de service DHCP, mais le nom d’affichage client DHCP.</span><span class="sxs-lookup"><span data-stu-id="63259-202">For example, the DHCP Client service has the service name Dhcp but the display name DHCP Client.</span></span> <span data-ttu-id="63259-203">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="63259-203">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="63259-204">Toutefois, les comparaisons **DisplayName** ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="63259-204">However, **DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="63259-205">Constraint : accepte la même valeur que la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="63259-205">Constraint: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="63259-206">Exemple : « Atdisk »</span><span class="sxs-lookup"><span data-stu-id="63259-206">Example: "Atdisk"</span></span>

<span data-ttu-id="63259-207">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-207">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-208">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="63259-208">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-209">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-210">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-210">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-211">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« gravité de l’échec de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="63259-211">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="63259-212">Gravité de l’erreur si ce service ne parvient pas à démarrer au démarrage.</span><span class="sxs-lookup"><span data-stu-id="63259-212">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="63259-213">La valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="63259-213">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="63259-214">Toutes les erreurs sont journalisées par le système informatique.</span><span class="sxs-lookup"><span data-stu-id="63259-214">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="63259-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** ("ignorer")</span><span class="sxs-lookup"><span data-stu-id="63259-215"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="63259-216">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="63259-216">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="63259-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (« normal »)</span><span class="sxs-lookup"><span data-stu-id="63259-217"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="63259-218">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="63259-218">User is notified.</span></span> <span data-ttu-id="63259-219">Il s’agit généralement d’un message indiquant que l’utilisateur du problème est affiché.</span><span class="sxs-lookup"><span data-stu-id="63259-219">Usually this will be a message box display notifying the user of the problem.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="63259-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (« grave »)</span><span class="sxs-lookup"><span data-stu-id="63259-220"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="63259-221">Le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="63259-221">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="63259-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (« critique »)</span><span class="sxs-lookup"><span data-stu-id="63259-222"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="63259-223">Le système tente de redémarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="63259-223">System attempts to restart with a good configuration.</span></span> <span data-ttu-id="63259-224">Si le service ne démarre pas une deuxième fois, le démarrage échoue.</span><span class="sxs-lookup"><span data-stu-id="63259-224">If the service fails to start a second time, startup fails.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63259-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="63259-225"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="63259-226">La gravité de l’erreur est inconnue.</span><span class="sxs-lookup"><span data-stu-id="63259-226">Severity of the error is unknown.</span></span>

</dd> </dl>

<span data-ttu-id="63259-227">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-227">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-228">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="63259-228">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-229">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63259-229">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63259-230">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-231">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("code de sortie")</span><span class="sxs-lookup"><span data-stu-id="63259-231">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="63259-232">Code d’erreur Windows qui définit les erreurs rencontrées lors du démarrage ou de l’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="63259-232">Windows error code that defines errors encountered in starting or stopping the service.</span></span> <span data-ttu-id="63259-233">Cette propriété est définie sur **erreur \_ spécifique au service \_ \_** (1066) lorsque l’erreur est unique pour le service représenté par cette classe, et les informations sur l’erreur sont disponibles dans la propriété **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="63259-233">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="63259-234">Le service définit cette valeur sur **aucune \_ erreur** lors de l’exécution, et à nouveau sur fin normale.</span><span class="sxs-lookup"><span data-stu-id="63259-234">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="63259-235">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-235">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-236">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="63259-236">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-237">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="63259-237">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="63259-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-239">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="63259-239">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="63259-240">L’objet date est installé.</span><span class="sxs-lookup"><span data-stu-id="63259-240">Date object is installed.</span></span> <span data-ttu-id="63259-241">Cette propriété ne requiert pas de valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="63259-241">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="63259-242">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63259-242">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-243">**Nom**</span><span class="sxs-lookup"><span data-stu-id="63259-243">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-244">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-245">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-245">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-246">Qualificateurs : [ **clé**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="63259-246">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="63259-247">Identificateur unique du service qui fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="63259-247">Unique identifier of the service that provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="63259-248">Cette fonctionnalité est décrite dans la propriété **Description** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63259-248">This functionality is described in the **Description** property of the object.</span></span>

<span data-ttu-id="63259-249">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63259-249">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-250">**PathName**</span><span class="sxs-lookup"><span data-stu-id="63259-250">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-251">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-253">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("file path Name")</span><span class="sxs-lookup"><span data-stu-id="63259-253">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="63259-254">Chemin d’accès complet au fichier binaire de service qui implémente le service.</span><span class="sxs-lookup"><span data-stu-id="63259-254">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="63259-255">Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="63259-255">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="63259-256">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-256">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-257">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="63259-257">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-258">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63259-258">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63259-259">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-259">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-260">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Process structures service \| [**\_ Status \_ Process**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process ID")</span><span class="sxs-lookup"><span data-stu-id="63259-260">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS\_PROCESS**](/windows/win32/api/winsvc/ns-winsvc-service_status_process)\|dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Process Id")</span></span>
</dt> </dl>

<span data-ttu-id="63259-261">Identificateur de processus du service.</span><span class="sxs-lookup"><span data-stu-id="63259-261">Process identifier of the service.</span></span>

<span data-ttu-id="63259-262">Exemple : 324</span><span class="sxs-lookup"><span data-stu-id="63259-262">Example: 324</span></span>

</dd> <dt>

<span data-ttu-id="63259-263">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="63259-263">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-264">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63259-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63259-265">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-266">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("code de sortie spécifique au serveur")</span><span class="sxs-lookup"><span data-stu-id="63259-266">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="63259-267">Code d’erreur spécifique au service pour les erreurs qui se produisent pendant que le service est en cours de démarrage ou d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="63259-267">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="63259-268">Les codes de sortie sont définis par le service représenté par cette classe.</span><span class="sxs-lookup"><span data-stu-id="63259-268">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="63259-269">Cette valeur est définie uniquement lorsque la valeur de la propriété **ExitCode** est erreur **\_ spécifique au service \_ \_** (1066).</span><span class="sxs-lookup"><span data-stu-id="63259-269">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="63259-270">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-270">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-271">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="63259-271">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-272">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-272">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-273">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-273">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-274">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("type de service")</span><span class="sxs-lookup"><span data-stu-id="63259-274">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="63259-275">Type de service fourni aux processus appelants.</span><span class="sxs-lookup"><span data-stu-id="63259-275">Type of service provided to calling processes.</span></span>

<span data-ttu-id="63259-276">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="63259-276">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="63259-277">**Pilote de noyau** (« pilote de noyau »)</span><span class="sxs-lookup"><span data-stu-id="63259-277">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="63259-278">**Pilote du système de fichiers** (« pilote du système de fichiers »)</span><span class="sxs-lookup"><span data-stu-id="63259-278">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="63259-279">**Carte** (« adaptateur »)</span><span class="sxs-lookup"><span data-stu-id="63259-279">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="63259-280">**Pilote de reconnaissance** (« pilote de reconnaissance »)</span><span class="sxs-lookup"><span data-stu-id="63259-280">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="63259-281">**Propre processus** (« propre processus »)</span><span class="sxs-lookup"><span data-stu-id="63259-281">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="63259-282">**Processus de partage** (« processus de partage »)</span><span class="sxs-lookup"><span data-stu-id="63259-282">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="63259-283">**Processus interactif** (« processus interactif »)</span><span class="sxs-lookup"><span data-stu-id="63259-283">**Interactive Process** ("Interactive Process")</span></span>


<span data-ttu-id="63259-284"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="63259-284"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="63259-285">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-285">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-286">**Cours**</span><span class="sxs-lookup"><span data-stu-id="63259-286">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-287">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="63259-287">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="63259-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-289">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span><span class="sxs-lookup"><span data-stu-id="63259-289">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="63259-290">Indique si le service est démarré ou non.</span><span class="sxs-lookup"><span data-stu-id="63259-290">Indicates whether or not the service is started.</span></span>

<span data-ttu-id="63259-291">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="63259-291">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-292">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="63259-292">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-293">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-294">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-295">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« mode de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="63259-295">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="63259-296">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="63259-296">Start mode of the Windows base service.</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="63259-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Démarrage** (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="63259-297"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="63259-298">Pilote de périphérique Démarré par le chargeur du système d’exploitation (valide uniquement pour les services de pilote).</span><span class="sxs-lookup"><span data-stu-id="63259-298">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="63259-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Système** (« système »)</span><span class="sxs-lookup"><span data-stu-id="63259-299"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="63259-300">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="63259-300">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="63259-301">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="63259-301">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="63259-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** (« auto »)</span><span class="sxs-lookup"><span data-stu-id="63259-302"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="63259-303">Le service doit être démarré automatiquement par le Gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="63259-303">Service to be started automatically by the service control manager during system startup.</span></span> <span data-ttu-id="63259-304">Les services automatiques sont démarrés même si un utilisateur ne se connecte pas.</span><span class="sxs-lookup"><span data-stu-id="63259-304">Auto services are started even if a user does not log on.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="63259-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuel** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="63259-305"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="63259-306">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="63259-306">Service to be started by the Service Control Manager when a process calls the [**StartService**](startservice-method-in-class-win32-service.md) method.</span></span> <span data-ttu-id="63259-307">Ces services ne démarrent pas à moins qu’un utilisateur se connecte et ne les démarre.</span><span class="sxs-lookup"><span data-stu-id="63259-307">These services do not start unless a user logs on and starts them.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="63259-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")</span><span class="sxs-lookup"><span data-stu-id="63259-308"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="63259-309">Service qui ne peut pas être démarré tant que son StartMode n’a pas été modifié en auto ou manuellement.</span><span class="sxs-lookup"><span data-stu-id="63259-309">Service that cannot be started until its StartMode is changed to either Auto or Manual.</span></span>

</dd> </dl>

<span data-ttu-id="63259-310">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="63259-310">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-311">**StartName**</span><span class="sxs-lookup"><span data-stu-id="63259-311">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-312">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-312">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-313">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-313">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-314">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Starting Account Name »)</span><span class="sxs-lookup"><span data-stu-id="63259-314">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="63259-315">Nom du compte sous lequel un service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="63259-315">Account name under which a service runs.</span></span> <span data-ttu-id="63259-316">Selon le type de service, le nom du compte peut se présenter sous la forme « nom_domaine \\ nom_utilisateur » ou au format UPN (« *Username@DomainName* »).</span><span class="sxs-lookup"><span data-stu-id="63259-316">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format ("*Username@DomainName*").</span></span> <span data-ttu-id="63259-317">Le processus de service est enregistré à l’aide de l’une de ces deux formes lorsqu’il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="63259-317">The service process is logged by using one of these two forms when it runs.</span></span> <span data-ttu-id="63259-318">Si le compte appartient au domaine intégré, «. \\ Nom d’utilisateur» peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="63259-318">If the account belongs to the built-in domain, then ".\\Username" can be specified.</span></span> <span data-ttu-id="63259-319">Pour les pilotes au niveau du noyau ou du système, **StartName** contient le nom d’objet du pilote (c’est-à-dire « \\ FileSystem \\ RDR » ou « \\ Driver \\ XNS ») que le système d’e/s utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="63259-319">For kernel or system-level drivers, **StartName** contains the driver object name (that is, "\\FileSystem\\Rdr" or "\\Driver\\Xns") which the I/O system uses to load the device driver.</span></span> <span data-ttu-id="63259-320">En outre, si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.</span><span class="sxs-lookup"><span data-stu-id="63259-320">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="63259-321">Exemple : « DWDOM \\ admin »</span><span class="sxs-lookup"><span data-stu-id="63259-321">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="63259-322">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-322">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-323">**State**</span><span class="sxs-lookup"><span data-stu-id="63259-323">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-324">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-325">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="63259-325">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="63259-326">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span><span class="sxs-lookup"><span data-stu-id="63259-326">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="63259-327">État actuel du service de base.</span><span class="sxs-lookup"><span data-stu-id="63259-327">Current state of the base service.</span></span>

<span data-ttu-id="63259-328">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="63259-328">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="63259-329">**Arrêté** (« arrêté »)</span><span class="sxs-lookup"><span data-stu-id="63259-329">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="63259-330">**Start Pending** (« Start Pending »)</span><span class="sxs-lookup"><span data-stu-id="63259-330">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="63259-331">**Arrêt en attente** (« arrêt en attente »)</span><span class="sxs-lookup"><span data-stu-id="63259-331">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="63259-332">**En cours d’exécution** (« en cours d’exécution »)</span><span class="sxs-lookup"><span data-stu-id="63259-332">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="63259-333">**Poursuite en attente** ("continuer en attente")</span><span class="sxs-lookup"><span data-stu-id="63259-333">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="63259-334">**Pause en attente** ("pause en attente")</span><span class="sxs-lookup"><span data-stu-id="63259-334">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="63259-335">**Suspendu** (« suspendu »)</span><span class="sxs-lookup"><span data-stu-id="63259-335">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63259-336">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="63259-336">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="63259-337"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="63259-337"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="63259-338">**Windows Server 2008 et Windows Vista :** Cette propriété est en lecture seule avant Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="63259-338">**Windows Server 2008 and Windows Vista:** This property is read-only before Windows 7 and Windows Server 2008 R2.</span></span>

<span data-ttu-id="63259-339">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-339">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-340">**État**</span><span class="sxs-lookup"><span data-stu-id="63259-340">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-341">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-341">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-342">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-342">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-343">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="63259-343">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="63259-344">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="63259-344">Current status of the object.</span></span> <span data-ttu-id="63259-345">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="63259-345">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="63259-346">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="63259-346">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="63259-347">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="63259-347">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="63259-348">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="63259-348">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="63259-349">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="63259-349">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="63259-350">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="63259-350">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="63259-351">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="63259-351">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="63259-352">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="63259-352">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="63259-353">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="63259-353">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="63259-354">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="63259-354">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="63259-355">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="63259-355">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="63259-356">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="63259-356">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="63259-357">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="63259-357">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="63259-358">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="63259-358">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="63259-359">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="63259-359">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="63259-360">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="63259-360">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="63259-361">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="63259-361">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="63259-362">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="63259-362">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="63259-363">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="63259-363">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="63259-364">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="63259-364">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-365">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-366">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-366">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-367">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="63259-367">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="63259-368">Nom de type du système qui héberge ce service.</span><span class="sxs-lookup"><span data-stu-id="63259-368">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="63259-369">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="63259-369">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-370">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="63259-370">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-371">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="63259-371">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63259-372">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-373">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="63259-373">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="63259-374">Nom du système qui héberge ce service.</span><span class="sxs-lookup"><span data-stu-id="63259-374">Name of the system that hosts this service.</span></span>

<span data-ttu-id="63259-375">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="63259-375">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-376">**TagId**</span><span class="sxs-lookup"><span data-stu-id="63259-376">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-377">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63259-377">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63259-378">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-379">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« ID de balise »)</span><span class="sxs-lookup"><span data-stu-id="63259-379">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="63259-380">Valeur de balise unique pour ce service dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="63259-380">Unique tag value for this service in the group.</span></span> <span data-ttu-id="63259-381">La valeur 0 (zéro) indique que le service n’a pas de balise.</span><span class="sxs-lookup"><span data-stu-id="63259-381">A value of 0 (zero) indicates that the service does not have a tag.</span></span> <span data-ttu-id="63259-382">Une balise peut être utilisée pour ordonner le démarrage du service dans un groupe d’ordre de chargement en spécifiant un vecteur d’ordre des balises dans le registre à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="63259-382">A tag can be used to order service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="63259-383">**HKEY \_ \_** \\  \\  \\ **Contrôle** CurrentControlSet du système \\  de l’ordinateur local GroupOrderList    </span><span class="sxs-lookup"><span data-stu-id="63259-383">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **GroupOrderList**</span></span>

<span data-ttu-id="63259-384">Les balises sont uniquement évaluées pour les services de type démarrage du pilote du noyau et du pilote du système de fichiers qui ont des modes de démarrage ou de démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="63259-384">Tags are only evaluated for Kernel Driver and File System Driver start type services that have Boot or System start modes.</span></span>

<span data-ttu-id="63259-385">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-385">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="63259-386">**WaitHint**</span><span class="sxs-lookup"><span data-stu-id="63259-386">**WaitHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63259-387">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63259-387">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63259-388">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="63259-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63259-389">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« temps d’attente estimé »)</span><span class="sxs-lookup"><span data-stu-id="63259-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Estimated Wait Time")</span></span>
</dt> </dl>

<span data-ttu-id="63259-390">Durée estimée, en millisecondes, pour une opération de démarrage, d’arrêt, de suspension ou de continuation en attente.</span><span class="sxs-lookup"><span data-stu-id="63259-390">Estimated time required, in milliseconds, for a pending start, stop, pause, or continue operation.</span></span> <span data-ttu-id="63259-391">Une fois le temps spécifié écoulé, le service effectue son prochain appel à la méthode **SetServiceStatus** avec une valeur **de point de contrôle** incrémentée ou une modification dans **CurrentState**.</span><span class="sxs-lookup"><span data-stu-id="63259-391">After the specified time has elapsed, the service makes its next call to the **SetServiceStatus** method with either an incremented **CheckPoint** value or a change in **CurrentState**.</span></span> <span data-ttu-id="63259-392">Si la durée spécifiée par **WaitHint** passe, si le **point** de contrôle n’a pas été incrémenté ou si **CurrentState** n’a pas changé, le gestionnaire de contrôle des services ou le programme de contrôle des services suppose qu’une erreur s’est produite.</span><span class="sxs-lookup"><span data-stu-id="63259-392">If the amount of time specified by **WaitHint** passes, and **CheckPoint** has not been incremented, or **CurrentState** has not changed, the service control manager or service control program assumes that an error has occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63259-393">Notes</span><span class="sxs-lookup"><span data-stu-id="63259-393">Remarks</span></span>

<span data-ttu-id="63259-394">La classe de **\_ service Win32** est dérivée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="63259-394">The **Win32\_Service** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="63259-395">La façon dont vous gérez un ordinateur spécifique dépend beaucoup du rôle joué par l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="63259-395">The way in which you manage a specific computer depends greatly on the role that computer plays.</span></span> <span data-ttu-id="63259-396">Par exemple, vous surveillez généralement les différents aspects d’un serveur DNS par rapport à un serveur DHCP.</span><span class="sxs-lookup"><span data-stu-id="63259-396">For example, you generally monitor different aspects of a DNS server than a DHCP server.</span></span> <span data-ttu-id="63259-397">Bien qu’aucune propriété unique ne vous indique si un ordinateur particulier est un serveur de base de données, un serveur de messagerie ou un serveur multimédia, vous pouvez souvent identifier le rôle joué par un ordinateur en identifiant les services installés sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="63259-397">Although no single property can tell you whether a particular computer is a database server, an e-mail server, or a multimedia server, you can often identify the role a computer plays by identifying the services installed on it.</span></span>

<span data-ttu-id="63259-398">Dans les grandes organisations, un seul des principaux services (tels que le courrier électronique) est susceptible d’être installé sur un seul ordinateur.</span><span class="sxs-lookup"><span data-stu-id="63259-398">In large organizations, only one of the major services (such as e-mail) is likely to be installed on a single computer.</span></span> <span data-ttu-id="63259-399">Il serait rare qu’un serveur de messagerie s’exécute également en tant que serveur pour Microsoft® les fichiers du lecteur Windows Media® Technologies.</span><span class="sxs-lookup"><span data-stu-id="63259-399">It would be unusual for a mail server to also perform as a server for Microsoft® Windows Media® technologies player files.</span></span> <span data-ttu-id="63259-400">Pour cette raison, l’identification d’un service installé sur un ordinateur peut aider à identifier le rôle de l’ordinateur sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="63259-400">Because of this, identifying a service installed on a computer can help identify the computer's role in the network.</span></span> <span data-ttu-id="63259-401">Si le service Microsoft® Exchange Server est installé et en cours d’exécution sur un ordinateur, il est généralement possible de supposer que cet ordinateur fonctionne comme un serveur de messagerie.</span><span class="sxs-lookup"><span data-stu-id="63259-401">If the Microsoft® Exchange Server service is installed and running on a computer, it is generally safe to assume that this computer functions as a mail server.</span></span>

<span data-ttu-id="63259-402">Vous pouvez utiliser la classe WMI **Win32 \_ service** pour énumérer les services installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="63259-402">You can use the WMI **Win32\_Service** class to enumerate the services installed on a computer.</span></span> <span data-ttu-id="63259-403">En outre, vous pouvez utiliser cette classe pour déterminer si ces services sont en cours d’exécution et pour retourner toutes les autres informations requises sur ce service et la manière dont il a été configuré.</span><span class="sxs-lookup"><span data-stu-id="63259-403">In addition, you can use this class to determine whether those services are currently running and to return any other required information about that service and how it has been configured.</span></span>

<span data-ttu-id="63259-404">Une application de service est conforme aux règles d’interface du gestionnaire de contrôle des services (SCM) et peut être démarrée automatiquement par un utilisateur au démarrage du système via l’utilitaire du panneau de configuration des services ou par une application qui utilise les fonctions de service incluses dans l’API Windows.</span><span class="sxs-lookup"><span data-stu-id="63259-404">A service application conforms to the interface rules of the Service Control Manager (SCM), and can be started by a user automatically at system start through the Services control panel utility, or by an application that uses the service functions included in the Windows API.</span></span> <span data-ttu-id="63259-405">Les services peuvent démarrer quand aucun utilisateur n’est connecté à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="63259-405">Services can start when there are no users logged on to the computer.</span></span>

<span data-ttu-id="63259-406">Un utilisateur qui se connecte à partir d’un ordinateur distant doit disposer du privilège de **\_ \_ connexion SC Manager** pour pouvoir énumérer cette classe.</span><span class="sxs-lookup"><span data-stu-id="63259-406">A user connecting from a remote computer must have the **SC\_MANAGER\_CONNECT** privilege enabled to be able to enumerate this class.</span></span> <span data-ttu-id="63259-407">Pour plus d’informations, consultez [sécurité des services et droits d’accès](../services/service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="63259-407">For more information, see [Service Security and Access Rights](../services/service-security-and-access-rights.md).</span></span>

## <a name="examples"></a><span data-ttu-id="63259-408">Exemples</span><span class="sxs-lookup"><span data-stu-id="63259-408">Examples</span></span>

<span data-ttu-id="63259-409">La [requête PS-WMI qui retourne le service « État » sur un groupe d’appareils](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) exemple PowerShell dans la Galerie TechNet utilise le **\_ service Win32** pour créer une liste d’appareils à partir de Active Directory, puis interroger chaque appareil qui répond avec pingfor un service spécifique en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="63259-409">The [PS- WMI Query that returns Service 'State' on a group of devices](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) PowerShell sample on TechNet Gallery uses **Win32\_Service** to create a list of devices from Active Directory, and then query each device that responds with pingfor a specific service running.</span></span>

<span data-ttu-id="63259-410">L’exemple PowerShell de [rapport de serveur](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) de la Galerie TechNet utilise le **\_ service Win32** pour rassembler des informations sur le serveur et les publier dans un document Word.</span><span class="sxs-lookup"><span data-stu-id="63259-410">The [Server Report](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell sample on TechNet Gallery uses **Win32\_Service** to gather server information and publish in Word document.</span></span>

<span data-ttu-id="63259-411">L’exemple de code VBScript suivant affiche tous les services actuellement installés.</span><span class="sxs-lookup"><span data-stu-id="63259-411">The following VBScript code sample displays all currently installed services.</span></span>


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



<span data-ttu-id="63259-412">L’exemple de code VBScript suivant décrit les services suspendus, en cours d’exécution et arrêtés sur l’ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="63259-412">The following VBScript code sample describes the paused, running, and stopped services on the specified computer.</span></span>


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



<span data-ttu-id="63259-413">Le script perl suivant montre comment récupérer une liste de services en cours d’exécution à partir d’instances du **\_ service Win32**.</span><span class="sxs-lookup"><span data-stu-id="63259-413">The following Perl script demonstrates how to retrieve a list of running services from instances of **Win32\_Service**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="63259-414">L’exemple c suivant \# utilise [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) pour récupérer tous les services en cours d’exécution sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="63259-414">The following c\# sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) to retrieve all the running services on the local machine.</span></span>


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



<span data-ttu-id="63259-415">L' \# exemple de code C suivant utilise l’espace de noms [System. Management](/dotnet/api/system.management) pour récupérer tous les services en cours d’exécution sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="63259-415">The following C\# code sample uses [System.Management](/dotnet/api/system.management) namespace to retrieve all running services on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="63259-416">[System. Management](/dotnet/api/system.management) contient les classes d’origine utilisées pour accéder à WMI. Toutefois, ils sont considérés comme plus lents et ne sont généralement pas mis à l’échelle, ainsi que leurs équivalents [Microsoft. Management. infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="63259-416">[System.Management](/dotnet/api/system.management) contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
```



## <a name="requirements"></a><span data-ttu-id="63259-417">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63259-417">Requirements</span></span>



| <span data-ttu-id="63259-418">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63259-418">Requirement</span></span> | <span data-ttu-id="63259-419">Valeur</span><span class="sxs-lookup"><span data-stu-id="63259-419">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63259-420">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63259-420">Minimum supported client</span></span><br/> | <span data-ttu-id="63259-421">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63259-421">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63259-422">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63259-422">Minimum supported server</span></span><br/> | <span data-ttu-id="63259-423">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63259-423">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63259-424">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63259-424">Namespace</span></span><br/>                | <span data-ttu-id="63259-425">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="63259-425">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="63259-426">MOF</span><span class="sxs-lookup"><span data-stu-id="63259-426">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63259-427"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63259-427"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="63259-428">DLL</span><span class="sxs-lookup"><span data-stu-id="63259-428">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63259-429"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63259-429"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63259-430">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63259-430">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63259-431">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="63259-431">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="63259-432">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="63259-432">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="63259-433">Tâches WMI : services</span><span class="sxs-lookup"><span data-stu-id="63259-433">WMI Tasks: Services</span></span>](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
