---
description: La \_ classe WMI BaseService abstraite Win32 représente des objets exécutables qui sont installés dans une base de données de Registre gérée par le gestionnaire de contrôle des services.
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Classe Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b46f3b4bd37770a5f3a7c1a2d2faa93d49bc079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111371"
---
# <a name="win32_baseservice-class"></a><span data-ttu-id="60382-103">\_Classe BaseService Win32</span><span class="sxs-lookup"><span data-stu-id="60382-103">Win32\_BaseService class</span></span>

<span data-ttu-id="60382-104">La [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ BaseService** abstraite Win32 représente des objets exécutables qui sont installés dans une base de données de Registre gérée par le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="60382-104">The **Win32\_BaseService** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents executable objects that are installed in a registry database maintained by the Service Control Manager.</span></span> <span data-ttu-id="60382-105">Le fichier exécutable associé à un service peut être démarré au démarrage par un programme de démarrage ou par le système.</span><span class="sxs-lookup"><span data-stu-id="60382-105">The executable file associated with a service can be started at boot time by a boot program or by the system.</span></span> <span data-ttu-id="60382-106">Il peut également être démarré à la demande par le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="60382-106">It can also be started on-demand by the Service Control Manager.</span></span> <span data-ttu-id="60382-107">Tout service ou processus qui n’appartient pas à un utilisateur spécifique, et qui fournit une interface à certaines fonctionnalités prises en charge par le système informatique, est un descendant (ou membre) de cette classe.</span><span class="sxs-lookup"><span data-stu-id="60382-107">Any service or process that is not owned by a specific user, and that provides an interface to some functionality supported by the computer system, is a descendant (or member) of this class.</span></span>

<span data-ttu-id="60382-108">Exemple : service client DHCP (Dynamic Host Configuration Protocol) sur un système d’ordinateur exécutant Windows Server.</span><span class="sxs-lookup"><span data-stu-id="60382-108">Example: The dynamic host configuration protocol (DHCP) client service on a computer system running Windows Server.</span></span>

<span data-ttu-id="60382-109">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="60382-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="60382-110">Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="60382-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="60382-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="60382-111">Syntax</span></span>

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a><span data-ttu-id="60382-112">Membres</span><span class="sxs-lookup"><span data-stu-id="60382-112">Members</span></span>

<span data-ttu-id="60382-113">La classe **Win32 \_ BaseService** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="60382-113">The **Win32\_BaseService** class has these types of members:</span></span>

-   [<span data-ttu-id="60382-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="60382-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="60382-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="60382-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="60382-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="60382-116">Methods</span></span>

<span data-ttu-id="60382-117">La classe **Win32 \_ BaseService** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="60382-117">The **Win32\_BaseService** class has these methods.</span></span>



| <span data-ttu-id="60382-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="60382-118">Method</span></span>                                                                             | <span data-ttu-id="60382-119">Description</span><span class="sxs-lookup"><span data-stu-id="60382-119">Description</span></span>                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="60382-120">**Modifiés**</span><span class="sxs-lookup"><span data-stu-id="60382-120">**Change**</span></span>](change-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="60382-121">Modifie un service.</span><span class="sxs-lookup"><span data-stu-id="60382-121">Modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="60382-122">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="60382-122">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-baseservice.md)       | <span data-ttu-id="60382-123">Modifie le mode de démarrage d’un service.</span><span class="sxs-lookup"><span data-stu-id="60382-123">Modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="60382-124">**Créés**</span><span class="sxs-lookup"><span data-stu-id="60382-124">**Create**</span></span>](create-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="60382-125">Crée un nouveau service.</span><span class="sxs-lookup"><span data-stu-id="60382-125">Creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="60382-126">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="60382-126">**Delete**</span></span>](delete-method-in-class-win32-baseservice.md)                         | <span data-ttu-id="60382-127">Supprime un service existant.</span><span class="sxs-lookup"><span data-stu-id="60382-127">Deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="60382-128">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="60382-128">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="60382-129">Demande que le service met à jour son état dans Service Manager.</span><span class="sxs-lookup"><span data-stu-id="60382-129">Requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="60382-130">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="60382-130">**PauseService**</span></span>](pauseservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="60382-131">Tente de placer le service dans l'état de pause.</span><span class="sxs-lookup"><span data-stu-id="60382-131">Attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="60382-132">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="60382-132">**ResumeService**</span></span>](resumeservice-method-in-class-win32-baseservice.md)           | <span data-ttu-id="60382-133">Tente de placer le service dans l'état de reprise.</span><span class="sxs-lookup"><span data-stu-id="60382-133">Attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="60382-134">**StartService**</span><span class="sxs-lookup"><span data-stu-id="60382-134">**StartService**</span></span>](startservice-method-in-class-win32-baseservice.md)             | <span data-ttu-id="60382-135">Tente de placer le service dans son état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="60382-135">Attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="60382-136">**StopService**</span><span class="sxs-lookup"><span data-stu-id="60382-136">**StopService**</span></span>](stopservice-method-in-class-win32-baseservice.md)               | <span data-ttu-id="60382-137">Méthode de classe qui place le service dans l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="60382-137">Class method that places the service in the stopped state.</span></span><br/>         |
| [<span data-ttu-id="60382-138">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="60382-138">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-baseservice.md) | <span data-ttu-id="60382-139">Tente d’envoyer un code de contrôle défini par l’utilisateur à un service.</span><span class="sxs-lookup"><span data-stu-id="60382-139">Attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="60382-140">Propriétés</span><span class="sxs-lookup"><span data-stu-id="60382-140">Properties</span></span>

<span data-ttu-id="60382-141">La classe **Win32 \_ BaseService** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="60382-141">The **Win32\_BaseService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60382-142">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="60382-142">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="60382-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60382-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-145">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| service \_ accepter \_ pause \_ continue"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("service accepte pause")</span><span class="sxs-lookup"><span data-stu-id="60382-145">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="60382-146">Le service peut être suspendu.</span><span class="sxs-lookup"><span data-stu-id="60382-146">Service can be paused.</span></span>

</dd> <dt>

<span data-ttu-id="60382-147">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="60382-147">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-148">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="60382-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60382-149">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-150">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**service \_**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| service \_ accepter \_ Stop"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("service accepte Stop")</span><span class="sxs-lookup"><span data-stu-id="60382-150">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="60382-151">Le service peut être arrêté.</span><span class="sxs-lookup"><span data-stu-id="60382-151">Service can be stopped.</span></span>

</dd> <dt>

<span data-ttu-id="60382-152">**Caption**</span><span class="sxs-lookup"><span data-stu-id="60382-152">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-153">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-154">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-155">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="60382-155">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="60382-156">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="60382-156">Short description of the object.</span></span>

<span data-ttu-id="60382-157">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60382-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60382-158">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="60382-158">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-159">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-160">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-161">Qualificateurs : [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="60382-161">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="60382-162">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="60382-162">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="60382-163">Lorsqu’elle est utilisée avec les autres propriétés de clé de la classe, la propriété permet d’identifier de manière unique toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="60382-163">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="60382-164">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="60382-164">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="60382-165">**Description**</span><span class="sxs-lookup"><span data-stu-id="60382-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-166">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-167">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-168">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span><span class="sxs-lookup"><span data-stu-id="60382-168">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="60382-169">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="60382-169">Description of the object.</span></span>

<span data-ttu-id="60382-170">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60382-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60382-171">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="60382-171">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-172">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="60382-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60382-173">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-174">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ configuration**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| \_ Process interactive \_ Process »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« interagit avec Desktop »)</span><span class="sxs-lookup"><span data-stu-id="60382-174">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="60382-175">Le service peut créer ou communiquer avec Windows sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="60382-175">Service can create or communicate with windows on the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="60382-176">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="60382-176">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-177">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-178">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-179">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Display Name »)</span><span class="sxs-lookup"><span data-stu-id="60382-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="60382-180">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="60382-180">Display name of the service.</span></span> <span data-ttu-id="60382-181">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="60382-181">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="60382-182">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="60382-182">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="60382-183">Les comparaisons de **DisplayName** ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="60382-183">Comparisons of **DisplayName** are always case-insensitive.</span></span>

<span data-ttu-id="60382-184">Contraintes : accepte la même valeur que la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="60382-184">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="60382-185">Exemple : « Atdisk »</span><span class="sxs-lookup"><span data-stu-id="60382-185">Example: "Atdisk"</span></span>

</dd> <dt>

<span data-ttu-id="60382-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="60382-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-189">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« gravité de l’échec de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="60382-189">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="60382-190">Gravité de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="60382-190">Severity of the error.</span></span> <span data-ttu-id="60382-191">Échec du démarrage du service.</span><span class="sxs-lookup"><span data-stu-id="60382-191">Service fails to start.</span></span> <span data-ttu-id="60382-192">La valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="60382-192">The value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="60382-193">Toutes les erreurs sont journalisées par le système informatique.</span><span class="sxs-lookup"><span data-stu-id="60382-193">All errors are logged by the computer system.</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="60382-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** ("ignorer")</span><span class="sxs-lookup"><span data-stu-id="60382-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="60382-195">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="60382-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="60382-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (« normal »)</span><span class="sxs-lookup"><span data-stu-id="60382-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="60382-197">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="60382-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="60382-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (« grave »)</span><span class="sxs-lookup"><span data-stu-id="60382-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="60382-199">Le système a redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="60382-199">System restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="60382-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (« critique »)</span><span class="sxs-lookup"><span data-stu-id="60382-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="60382-201">Le système tente de redémarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="60382-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60382-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="60382-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="60382-203">L’action effectuée n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="60382-203">Action taken is unspecified.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="60382-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="60382-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-205">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60382-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60382-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-207">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("code de sortie")</span><span class="sxs-lookup"><span data-stu-id="60382-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="60382-208">Définition des problèmes rencontrés lors du démarrage ou de l’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="60382-208">Defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="60382-209">Cette propriété est définie sur **erreur \_ spécifique au service \_ \_** (1066) lorsque l’erreur est unique pour le service représenté par cette classe, et les informations sur l’erreur sont disponibles dans la propriété **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="60382-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="60382-210">Le service définit cette valeur sur **aucune \_ erreur** lors de l’exécution, et à nouveau sur fin normale.</span><span class="sxs-lookup"><span data-stu-id="60382-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

</dd> <dt>

<span data-ttu-id="60382-211">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="60382-211">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-212">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="60382-212">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="60382-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-214">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="60382-214">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="60382-215">L’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="60382-215">Object was installed.</span></span> <span data-ttu-id="60382-216">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="60382-216">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="60382-217">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60382-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60382-218">**Nom**</span><span class="sxs-lookup"><span data-stu-id="60382-218">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-219">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-220">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-221">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="60382-221">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="60382-222">Identificateur unique du service, qui fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="60382-222">Unique identifier of the service, which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="60382-223">Cette fonctionnalité est décrite plus en détail dans la propriété **Description** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="60382-223">This functionality is described in more detail in the object's **Description** property.</span></span>

<span data-ttu-id="60382-224">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60382-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="60382-225">**PathName**</span><span class="sxs-lookup"><span data-stu-id="60382-225">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-226">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-226">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-227">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-228">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("file path Name")</span><span class="sxs-lookup"><span data-stu-id="60382-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="60382-229">Chemin d’accès complet au fichier binaire de service qui implémente le service.</span><span class="sxs-lookup"><span data-stu-id="60382-229">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="60382-230">Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="60382-230">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

</dd> <dt>

<span data-ttu-id="60382-231">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="60382-231">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-232">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60382-232">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60382-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-233">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-234">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("code de sortie spécifique au serveur")</span><span class="sxs-lookup"><span data-stu-id="60382-234">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="60382-235">Code d’erreur spécifique au service pour les erreurs qui se produisent pendant que le service est en cours de démarrage ou d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="60382-235">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="60382-236">Les codes de sortie sont définis par le service représenté par cette classe.</span><span class="sxs-lookup"><span data-stu-id="60382-236">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="60382-237">Cette valeur est définie uniquement lorsque la valeur **ExitCodeproperty** est **erreur \_ spécifique au SERVICE d' \_ \_ erreur** (1066).</span><span class="sxs-lookup"><span data-stu-id="60382-237">This value is only set when the **ExitCodeproperty** value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

</dd> <dt>

<span data-ttu-id="60382-238">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="60382-238">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-239">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-239">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-240">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-240">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-241">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("type de service")</span><span class="sxs-lookup"><span data-stu-id="60382-241">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="60382-242">Service fourni aux processus appelant.</span><span class="sxs-lookup"><span data-stu-id="60382-242">Service provided to calling processes.</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="60382-243">**Pilote de noyau** (« pilote de noyau »)</span><span class="sxs-lookup"><span data-stu-id="60382-243">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="60382-244">**Pilote du système de fichiers** (« pilote du système de fichiers »)</span><span class="sxs-lookup"><span data-stu-id="60382-244">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="60382-245">**Carte** (« adaptateur »)</span><span class="sxs-lookup"><span data-stu-id="60382-245">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="60382-246">**Pilote de reconnaissance** (« pilote de reconnaissance »)</span><span class="sxs-lookup"><span data-stu-id="60382-246">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="60382-247">**Propre processus** (« propre processus »)</span><span class="sxs-lookup"><span data-stu-id="60382-247">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="60382-248">**Processus de partage** (« processus de partage »)</span><span class="sxs-lookup"><span data-stu-id="60382-248">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="60382-249">**Processus interactif** (« processus interactif »)</span><span class="sxs-lookup"><span data-stu-id="60382-249">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60382-250">**Cours**</span><span class="sxs-lookup"><span data-stu-id="60382-250">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-251">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="60382-251">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60382-252">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-252">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-253">Qualificateurs : [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span><span class="sxs-lookup"><span data-stu-id="60382-253">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="60382-254">Le service a été démarré.</span><span class="sxs-lookup"><span data-stu-id="60382-254">Service has been started.</span></span>

<span data-ttu-id="60382-255">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="60382-255">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="60382-256">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="60382-256">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-259">Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("startMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("mode de démarrage")</span><span class="sxs-lookup"><span data-stu-id="60382-259">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="60382-260">Mode de démarrage du service de base Windows.</span><span class="sxs-lookup"><span data-stu-id="60382-260">Start mode of the Windows base service.</span></span>

<span data-ttu-id="60382-261">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="60382-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="60382-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Démarrage** (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="60382-262"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="60382-263">Pilote de périphérique Démarré par le chargeur du système d’exploitation (valide uniquement pour les services de pilote).</span><span class="sxs-lookup"><span data-stu-id="60382-263">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="60382-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Système** (« système »)</span><span class="sxs-lookup"><span data-stu-id="60382-264"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="60382-265">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="60382-265">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="60382-266">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="60382-266">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="60382-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** (« auto »)</span><span class="sxs-lookup"><span data-stu-id="60382-267"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="60382-268">Service qui doit être démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="60382-268">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="60382-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuel** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="60382-269"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="60382-270">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-baseservice.md) .</span><span class="sxs-lookup"><span data-stu-id="60382-270">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-baseservice.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="60382-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")</span><span class="sxs-lookup"><span data-stu-id="60382-271"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="60382-272">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="60382-272">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="60382-273">**StartName**</span><span class="sxs-lookup"><span data-stu-id="60382-273">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-274">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-274">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-275">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-275">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-276">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« Starting Account Name »)</span><span class="sxs-lookup"><span data-stu-id="60382-276">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="60382-277">Nom du compte sous lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="60382-277">Account name under which the service runs.</span></span> <span data-ttu-id="60382-278">Selon le type de service, le nom du compte peut se présenter sous la forme « nom_domaine \\ nom_utilisateur » ou UPN ( Username@DomainName ).</span><span class="sxs-lookup"><span data-stu-id="60382-278">Depending on the service type, the account name may be in the form of "DomainName\\Username" or UPN format (Username@DomainName).</span></span> <span data-ttu-id="60382-279">Le processus de service sera journalisé à l’aide de l’une de ces deux formes lorsqu’il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="60382-279">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="60382-280">Si le compte appartient au domaine intégré,». \\ Nom d’utilisateur» peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="60382-280">If the account belongs to the built-in domain, ".\\Username" can be specified.</span></span> <span data-ttu-id="60382-281">Si **null** est spécifié, le service est connecté en tant que compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="60382-281">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="60382-282">Pour les pilotes au niveau du noyau ou du système, **StartName** contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou \\ \\ le pilote XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="60382-282">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="60382-283">En outre, si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.</span><span class="sxs-lookup"><span data-stu-id="60382-283">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span> <span data-ttu-id="60382-284">Exemple : « DWDOM \\ admin ».</span><span class="sxs-lookup"><span data-stu-id="60382-284">Example: "DWDOM\\Admin".</span></span>

</dd> <dt>

<span data-ttu-id="60382-285">**State**</span><span class="sxs-lookup"><span data-stu-id="60382-285">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-286">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-286">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-287">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="60382-287">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="60382-288">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| service structures \| [**\_ Status service**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span><span class="sxs-lookup"><span data-stu-id="60382-288">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="60382-289">État actuel du service de base.</span><span class="sxs-lookup"><span data-stu-id="60382-289">Current state of the base service.</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="60382-290">**Arrêté** (« arrêté »)</span><span class="sxs-lookup"><span data-stu-id="60382-290">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="60382-291">**Start Pending** (« Start Pending »)</span><span class="sxs-lookup"><span data-stu-id="60382-291">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="60382-292">**Arrêt en attente** (« arrêt en attente »)</span><span class="sxs-lookup"><span data-stu-id="60382-292">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="60382-293">**En cours d’exécution** (« en cours d’exécution »)</span><span class="sxs-lookup"><span data-stu-id="60382-293">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="60382-294">**Poursuite en attente** ("continuer en attente")</span><span class="sxs-lookup"><span data-stu-id="60382-294">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="60382-295">**Pause en attente** ("pause en attente")</span><span class="sxs-lookup"><span data-stu-id="60382-295">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="60382-296">**Suspendu** (« suspendu »)</span><span class="sxs-lookup"><span data-stu-id="60382-296">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60382-297">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="60382-297">**Unknown** ("Unknown")</span></span>


<span data-ttu-id="60382-298"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="60382-298"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="60382-299">**Windows Server 2008 et Windows Vista :** Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="60382-299">**Windows Server 2008 and Windows Vista:** This property is read-only.</span></span>

</dd> <dt>

<span data-ttu-id="60382-300">**État**</span><span class="sxs-lookup"><span data-stu-id="60382-300">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-301">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-301">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-302">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-303">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span><span class="sxs-lookup"><span data-stu-id="60382-303">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="60382-304">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="60382-304">Current status of the object.</span></span> <span data-ttu-id="60382-305">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="60382-305">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="60382-306">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="60382-306">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="60382-307">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="60382-307">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="60382-308">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="60382-308">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="60382-309">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="60382-309">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="60382-310">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="60382-310">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="60382-311">Les valeurs sont notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="60382-311">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="60382-312">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="60382-312">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="60382-313">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="60382-313">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="60382-314">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="60382-314">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60382-315">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="60382-315">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="60382-316">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="60382-316">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="60382-317">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="60382-317">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="60382-318">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="60382-318">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="60382-319">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="60382-319">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="60382-320">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="60382-320">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="60382-321">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="60382-321">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="60382-322">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="60382-322">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="60382-323">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="60382-323">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60382-324">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="60382-324">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-325">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-325">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-326">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-326">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-327">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="60382-327">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="60382-328">Nom de type du système qui héberge ce service.</span><span class="sxs-lookup"><span data-stu-id="60382-328">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="60382-329">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="60382-329">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="60382-330">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="60382-330">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="60382-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="60382-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-333">Qualificateurs : [**Propaged**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="60382-333">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="60382-334">Nom du système qui héberge ce service.</span><span class="sxs-lookup"><span data-stu-id="60382-334">Name of the system that hosts this service.</span></span>

<span data-ttu-id="60382-335">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="60382-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="60382-336">**TagId**</span><span class="sxs-lookup"><span data-stu-id="60382-336">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60382-337">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="60382-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="60382-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="60382-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="60382-339">Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId »), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (« ID de balise »)</span><span class="sxs-lookup"><span data-stu-id="60382-339">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="60382-340">Valeur de balise unique pour ce service dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="60382-340">Unique tag value for this service in the group.</span></span> <span data-ttu-id="60382-341">La valeur 0 (zéro) indique que la balise n’a pas été assignée au service.</span><span class="sxs-lookup"><span data-stu-id="60382-341">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="60382-342">Une balise peut être utilisée pour le tri du service Star tallation dans un groupe d’ordre de chargement en spécifiant un vecteur d’ordre des balises dans le registre situé à l’emplacement suivant : HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ Control \\ GroupOrderList.</span><span class="sxs-lookup"><span data-stu-id="60382-342">A tag can be used for ordering service star tup within a load order group by specifying a tag order vector in the registry located at: HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList.</span></span> <span data-ttu-id="60382-343">Les balises sont uniquement évaluées pour les services du pilote du noyau et du pilote du système de fichiers qui ont des modes de démarrage ou de démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="60382-343">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60382-344">Notes</span><span class="sxs-lookup"><span data-stu-id="60382-344">Remarks</span></span>

<span data-ttu-id="60382-345">La classe **Win32 \_ BaseService** est dérivée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="60382-345">The **Win32\_BaseService** class is derived from [**CIM\_Service**](cim-service.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60382-346">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="60382-346">Requirements</span></span>



| <span data-ttu-id="60382-347">Condition requise</span><span class="sxs-lookup"><span data-stu-id="60382-347">Requirement</span></span> | <span data-ttu-id="60382-348">Valeur</span><span class="sxs-lookup"><span data-stu-id="60382-348">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60382-349">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60382-349">Minimum supported client</span></span><br/> | <span data-ttu-id="60382-350">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60382-350">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60382-351">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="60382-351">Minimum supported server</span></span><br/> | <span data-ttu-id="60382-352">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60382-352">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60382-353">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="60382-353">Namespace</span></span><br/>                | <span data-ttu-id="60382-354">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="60382-354">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60382-355">MOF</span><span class="sxs-lookup"><span data-stu-id="60382-355">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60382-356"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60382-356"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60382-357">DLL</span><span class="sxs-lookup"><span data-stu-id="60382-357">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60382-358"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60382-358"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60382-359">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60382-359">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60382-360">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="60382-360">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dt>

<span data-ttu-id="60382-361">[Classes du système d’exploitation](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="60382-361">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

