---
description: Représente le pilote système pour un service de base.
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Classe Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15be9b176680e8abb259d3d011da9d6cec0c2fa8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748404"
---
# <a name="win32_systemdriver-class"></a><span data-ttu-id="bd5f1-103">\_Classe SystemDriver Win32</span><span class="sxs-lookup"><span data-stu-id="bd5f1-103">Win32\_SystemDriver class</span></span>

<span data-ttu-id="bd5f1-104">La  [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemDriver** WMI représente le pilote système d’un service de base.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-104">The **Win32\_SystemDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the system driver for a base service.</span></span>

<span data-ttu-id="bd5f1-105">La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bd5f1-106">Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5f1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bd5f1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
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

## <a name="members"></a><span data-ttu-id="bd5f1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="bd5f1-108">Members</span></span>

<span data-ttu-id="bd5f1-109">La classe **Win32 \_ SystemDriver** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bd5f1-109">The **Win32\_SystemDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="bd5f1-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bd5f1-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="bd5f1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bd5f1-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bd5f1-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bd5f1-112">Methods</span></span>

<span data-ttu-id="bd5f1-113">La classe **Win32 \_ SystemDriver** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-113">The **Win32\_SystemDriver** class has these methods.</span></span>



| <span data-ttu-id="bd5f1-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="bd5f1-114">Method</span></span>                                                                              | <span data-ttu-id="bd5f1-115">Description</span><span class="sxs-lookup"><span data-stu-id="bd5f1-115">Description</span></span>                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bd5f1-116">**Modifiés**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-116">**Change**</span></span>](change-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="bd5f1-117">Méthode de classe qui modifie un service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-117">Class method that modifies a service.</span></span><br/>                                                |
| [<span data-ttu-id="bd5f1-118">**ChangeStartMode**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-118">**ChangeStartMode**</span></span>](changestartmode-method-in-class-win32-systemdriver.md)       | <span data-ttu-id="bd5f1-119">Méthode de classe qui modifie le mode de démarrage d’un service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-119">Class method that modifies the start mode of a service.</span></span><br/>                              |
| [<span data-ttu-id="bd5f1-120">**Créés**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-120">**Create**</span></span>](create-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="bd5f1-121">Méthode de classe qui crée un nouveau service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-121">Class method that creates a new service.</span></span><br/>                                             |
| [<span data-ttu-id="bd5f1-122">**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-122">**Delete**</span></span>](delete-method-in-class-win32-systemdriver.md)                         | <span data-ttu-id="bd5f1-123">Méthode de classe qui supprime un service existant.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-123">Class method that deletes an existing service.</span></span><br/>                                       |
| [<span data-ttu-id="bd5f1-124">**InterrogateService**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-124">**InterrogateService**</span></span>](interrogateservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="bd5f1-125">Méthode de classe qui demande que le service met à jour son État auprès du gestionnaire de service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-125">Class method that requests that the service update its state to the service manager.</span></span><br/> |
| [<span data-ttu-id="bd5f1-126">**PauseService**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-126">**PauseService**</span></span>](pauseservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="bd5f1-127">Méthode de classe qui tente de placer le service dans l’état suspendu.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-127">Class method that attempts to place the service in the paused state.</span></span><br/>                 |
| [<span data-ttu-id="bd5f1-128">**ResumeService**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-128">**ResumeService**</span></span>](resumeservice-method-in-class-win32-systemdriver.md)           | <span data-ttu-id="bd5f1-129">Méthode de classe qui tente de placer le service dans l’État repris.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-129">Class method that attempts to place the service in the resumed state.</span></span><br/>                |
| [<span data-ttu-id="bd5f1-130">**StartService**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-130">**StartService**</span></span>](startservice-method-in-class-win32-systemdriver.md)             | <span data-ttu-id="bd5f1-131">Méthode de classe qui tente de placer le service dans son état de démarrage.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-131">Class method that attempts to place the service into its startup state.</span></span><br/>              |
| [<span data-ttu-id="bd5f1-132">**StopService**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-132">**StopService**</span></span>](stopservice-method-in-class-win32-systemdriver.md)               | <span data-ttu-id="bd5f1-133">Méthode de classe qui place le service dans l’état arrêté.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-133">Class method that places the service in the stopped state.</span></span><br/>                           |
| [<span data-ttu-id="bd5f1-134">**UserControlService**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-134">**UserControlService**</span></span>](usercontrolservice-method-in-class-win32-systemdriver.md) | <span data-ttu-id="bd5f1-135">Méthode de classe qui tente d’envoyer un code de contrôle défini par l’utilisateur à un service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-135">Class method that attempts to send a user-defined control code to a service.</span></span><br/>         |



 

### <a name="properties"></a><span data-ttu-id="bd5f1-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="bd5f1-136">Properties</span></span>

<span data-ttu-id="bd5f1-137">La classe **Win32 \_ SystemDriver** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-137">The **Win32\_SystemDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd5f1-138">**AcceptPause**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-138">**AcceptPause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-139">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-140">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-141">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**service \_**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| service \_ accepter \_ pause \_ continue"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("service accepte pause")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_PAUSE\_CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-142">Le service peut être suspendu.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-142">Service can be paused.</span></span>

<span data-ttu-id="bd5f1-143">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-143">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-144">**AcceptStop**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-144">**AcceptStop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-145">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-145">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-146">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-147">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**service \_**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwControlsAccepted \| service \_ accepter \_ Stop"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("service accepte Stop")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwControlsAccepted\|SERVICE\_ACCEPT\_STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-148">Le service peut être arrêté.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-148">Service can be stopped.</span></span>

<span data-ttu-id="bd5f1-149">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-149">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-150">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-150">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-151">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-152">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-153">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Caption »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-153">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-154">Brève description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-154">Short description of the object.</span></span>

<span data-ttu-id="bd5f1-155">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-157">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-159">Qualificateurs : [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nom de la classe")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-159">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-160">Nom de la première classe concrète à afficher dans la chaîne d’héritage utilisée lors de la création d’une instance.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-160">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="bd5f1-161">Quand elle est utilisée avec les autres propriétés de clé de la classe, cette propriété autorise l’identification unique de toutes les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-161">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="bd5f1-162">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-162">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-163">**Description**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-163">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-164">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-165">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-166">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-166">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-167">Description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-167">Description of the object.</span></span>

<span data-ttu-id="bd5f1-168">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-168">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-169">**DesktopInteract**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-169">**DesktopInteract**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-170">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-171">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-172">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ configuration**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| \_ Process interactive \_ Process »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« interagit avec Desktop »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-172">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType\|SERVICE\_INTERACTIVE\_PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interacts With Desktop")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-173">Ce service peut créer ou communiquer avec Windows sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-173">This service can create or communicate with windows on the desktop.</span></span>

<span data-ttu-id="bd5f1-174">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-174">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-175">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-175">**DisplayName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-176">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-178">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Display Name »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-178">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Display Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-179">Nom complet du service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-179">Display name of the service.</span></span> <span data-ttu-id="bd5f1-180">Cette chaîne a une longueur maximale de 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-180">This string has a maximum length of 256 characters.</span></span> <span data-ttu-id="bd5f1-181">Le nom est conservé dans le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-181">The name is case-preserved in the Service Control Manager.</span></span> <span data-ttu-id="bd5f1-182">Les comparaisons **DisplayName** ne respectent jamais la casse.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-182">**DisplayName** comparisons are always case-insensitive.</span></span>

<span data-ttu-id="bd5f1-183">Contraintes : accepte la même valeur que la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="bd5f1-183">Constraints: Accepts the same value as the **Name** property.</span></span>

<span data-ttu-id="bd5f1-184">Exemple : « Atdisk »</span><span class="sxs-lookup"><span data-stu-id="bd5f1-184">Example: "Atdisk"</span></span>

<span data-ttu-id="bd5f1-185">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-185">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-186">**ErrorControl**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-186">**ErrorControl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-187">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-187">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-188">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-189">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« gravité de l’échec de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Severity Of Startup Failure")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-190">Gravité de l’erreur si ce service ne parvient pas à démarrer au démarrage.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-190">Severity of the error if this service fails to start during startup.</span></span> <span data-ttu-id="bd5f1-191">Cette valeur indique l’action entreprise par le programme de démarrage en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-191">This value indicates the action taken by the startup program if failure occurs.</span></span> <span data-ttu-id="bd5f1-192">Toutes les erreurs sont journalisées par le système informatique.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-192">All errors are logged by the computer system.</span></span>

<span data-ttu-id="bd5f1-193">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-193">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span data-ttu-id="bd5f1-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorer** ("ignorer")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-194"><span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignore** ("Ignore")</span></span>


</dt> <dd>

<span data-ttu-id="bd5f1-195">L'utilisateur n'est pas notifié.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-195">User is not notified.</span></span>

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="bd5f1-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (« normal »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-196"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")</span></span>


</dt> <dd>

<span data-ttu-id="bd5f1-197">L'utilisateur est notifié.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-197">User is notified.</span></span>

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span data-ttu-id="bd5f1-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** (« grave »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-198"><span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Severe** ("Severe")</span></span>


</dt> <dd>

<span data-ttu-id="bd5f1-199">Le système est redémarré avec la dernière bonne configuration connue.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-199">System is restarted with the last-known-good configuration.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="bd5f1-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critique** (« critique »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-200"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** ("Critical")</span></span>


</dt> <dd>

<span data-ttu-id="bd5f1-201">Le système tente de redémarrer avec une bonne configuration.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-201">System attempts to restart with a good configuration.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd5f1-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** ("Unknown")</span></span>


</dt> <dd>

<span data-ttu-id="bd5f1-203">La cause de l’échec est inconnue.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-203">Cause of the failure is unknown.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd5f1-204">**ExitCode**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-204">**ExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-205">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-206">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-207">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("code de sortie")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-207">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-208">Code d’erreur Windows définissant tout problème rencontré lors du démarrage ou de l’arrêt du service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-208">Windows error code defining any problems encountered in starting or stopping the service.</span></span> <span data-ttu-id="bd5f1-209">Cette propriété est définie sur **erreur \_ spécifique au service \_ \_** (1066) lorsque l’erreur est unique pour le service représenté par cette classe, et les informations sur l’erreur sont disponibles dans la propriété **ServiceSpecificExitCode** .</span><span class="sxs-lookup"><span data-stu-id="bd5f1-209">This property is set to **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066) when the error is unique to the service represented by this class, and information about the error is available in the **ServiceSpecificExitCode** property.</span></span> <span data-ttu-id="bd5f1-210">Le service définit cette valeur sur **aucune \_ erreur** lors de l’exécution, et à nouveau sur fin normale.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-210">The service sets this value to **NO\_ERROR** when running, and again upon normal termination.</span></span>

<span data-ttu-id="bd5f1-211">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-211">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-212">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-212">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-213">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-213">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-214">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-215">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" date d’installation ")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-215">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-216">L’objet a été installé.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-216">Object was installed.</span></span> <span data-ttu-id="bd5f1-217">Cette propriété n’a pas besoin d’une valeur pour indiquer que l’objet est installé.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-217">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="bd5f1-218">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-218">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-219">**Nom**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-220">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-221">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-222">Qualificateurs : [ **clé**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-222">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-223">Identificateur unique pour le service qui fournit une indication de la fonctionnalité gérée.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-223">Unique identifier for the service which provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="bd5f1-224">Cette fonctionnalité est décrite plus en détail dans la propriété **Description** de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-224">This functionality is described in more detail in the object **Description** property.</span></span>

<span data-ttu-id="bd5f1-225">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-225">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-226">**PathName**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-226">**PathName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-228">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-229">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("file path Name")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-229">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("File Path Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-230">Chemin d’accès complet au fichier binaire de service qui implémente le service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-230">Fully qualified path to the service binary file that implements the service.</span></span>

<span data-ttu-id="bd5f1-231">Exemple : " \\ systemroot \\ system32 \\ drivers \\afd.sys"</span><span class="sxs-lookup"><span data-stu-id="bd5f1-231">Example: "\\SystemRoot\\System32\\drivers\\afd.sys"</span></span>

<span data-ttu-id="bd5f1-232">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-232">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-233">**ServiceSpecificExitCode**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-233">**ServiceSpecificExitCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-234">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-234">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-235">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-235">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-236">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("code de sortie spécifique au serveur")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-236">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Server Specific Exit Code")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-237">Code d’erreur spécifique au service pour les erreurs qui se produisent pendant que le service est en cours de démarrage ou d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-237">Service-specific error code for errors that occur while the service is either starting or stopping.</span></span> <span data-ttu-id="bd5f1-238">Les codes de sortie sont définis par le service représenté par cette classe.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-238">The exit codes are defined by the service represented by this class.</span></span> <span data-ttu-id="bd5f1-239">Cette valeur est définie uniquement lorsque la valeur de la propriété **ExitCode** est erreur **\_ spécifique au service \_ \_** (1066).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-239">This value is only set when the **ExitCode** property value is **ERROR\_SERVICE\_SPECIFIC\_ERROR** (1066).</span></span>

<span data-ttu-id="bd5f1-240">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-240">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-241">**ServiceType**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-241">**ServiceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-244">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("type de service")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Type")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-245">Type de service fourni aux processus appelants.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-245">Type of service provided to calling processes.</span></span>

<span data-ttu-id="bd5f1-246">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-246">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="bd5f1-247">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="bd5f1-247">The values are:</span></span>

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span data-ttu-id="bd5f1-248">**Pilote de noyau** (« pilote de noyau »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-248">**Kernel Driver** ("Kernel Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span data-ttu-id="bd5f1-249">**Pilote du système de fichiers** (« pilote du système de fichiers »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-249">**File System Driver** ("File System Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span data-ttu-id="bd5f1-250">**Carte** (« adaptateur »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-250">**Adapter** ("Adapter")</span></span>


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span data-ttu-id="bd5f1-251">**Pilote de reconnaissance** (« pilote de reconnaissance »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-251">**Recognizer Driver** ("Recognizer Driver")</span></span>


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span data-ttu-id="bd5f1-252">**Propre processus** (« propre processus »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-252">**Own Process** ("Own Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span data-ttu-id="bd5f1-253">**Processus de partage** (« processus de partage »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-253">**Share Process** ("Share Process")</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

<span data-ttu-id="bd5f1-254">**Processus interactif** (« processus interactif »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-254">**Interactive Process** ("Interactive Process")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd5f1-255">**Cours**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-255">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-256">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-257">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-258">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-258">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-259">Le service a été démarré.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-259">Service has been started.</span></span>

<span data-ttu-id="bd5f1-260">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-260">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-261">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-261">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-262">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-264">Qualificateurs : [**DisplayName**](../wmisdk/standard-qualifiers.md) (« mode de démarrage »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-264">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-265">Mode de démarrage du pilote système.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-265">Start mode of the system driver.</span></span>

<span data-ttu-id="bd5f1-266">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-266">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span data-ttu-id="bd5f1-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Démarrage** (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-267"><span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** ("Boot")</span></span>


</dt> <dd>

<span data-ttu-id="bd5f1-268">Pilote de périphérique Démarré par le chargeur du système d’exploitation (valide uniquement pour les services de pilote).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-268">Device driver started by the operating system loader (valid only for driver services).</span></span>

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span data-ttu-id="bd5f1-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Système** (« système »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-269"><span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ("System")</span></span>


</dt> <dd>

<span data-ttu-id="bd5f1-270">Pilote de périphérique Démarré par le processus d’initialisation du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-270">Device driver started by the operating system initialization process.</span></span> <span data-ttu-id="bd5f1-271">Cette valeur est uniquement valide pour les services de pilote.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-271">This value is valid only for driver services.</span></span>

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span data-ttu-id="bd5f1-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** (« auto »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-272"><span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")</span></span>


</dt> <dd>

<span data-ttu-id="bd5f1-273">Service qui doit être démarré automatiquement par le gestionnaire de contrôle des services lors du démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-273">Service to be started automatically by the service control manager during system start up.</span></span>

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="bd5f1-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manuel** (« manuel »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-274"><span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")</span></span>


</dt> <dd>

<span data-ttu-id="bd5f1-275">Service qui doit être démarré par le gestionnaire de contrôle des services lorsqu’un processus appelle la méthode [**StartService**](startservice-method-in-class-win32-systemdriver.md) .</span><span class="sxs-lookup"><span data-stu-id="bd5f1-275">Service to be started by the service control manager when a process calls the [**StartService**](startservice-method-in-class-win32-systemdriver.md) method.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="bd5f1-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Désactivé** ("désactivé")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-276"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("Disabled")</span></span>


</dt> <dd>

<span data-ttu-id="bd5f1-277">Service qui ne peut plus être démarré.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-277">Service that can no longer be started.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bd5f1-278">**StartName**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-278">**StartName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-279">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-281">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« Starting Account Name »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-281">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|lpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Starting Account Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-282">Nom du compte sous lequel le service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-282">Account name under which the service runs.</span></span> <span data-ttu-id="bd5f1-283">Selon le type de service, le nom du compte peut se présenter sous la forme nom_domaine \\ nom_utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-283">Depending on the service type, the account name may be in the form of DomainName\\Username.</span></span> <span data-ttu-id="bd5f1-284">Le processus de service sera journalisé à l’aide de l’une de ces deux formes lorsqu’il s’exécute.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-284">The service process will be logged using one of these two forms when it runs.</span></span> <span data-ttu-id="bd5f1-285">Si le compte appartient au domaine intégré,. \\ Le nom d’utilisateur peut être spécifié.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-285">If the account belongs to the built-in domain, .\\Username can be specified.</span></span> <span data-ttu-id="bd5f1-286">Si **null** est spécifié, le service est connecté en tant que compte LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-286">If **NULL** is specified, the service will be logged on as the LocalSystem account.</span></span> <span data-ttu-id="bd5f1-287">Pour les pilotes au niveau du noyau ou du système, **StartName** contient le nom d’objet du pilote (c’est-à-dire, le \\ système de fichiers \\ RDR ou \\ \\ le pilote XNS) que le système d’entrée et de sortie utilise pour charger le pilote de périphérique.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-287">For kernel or system-level drivers, **StartName** contains the driver object name (that is, \\FileSystem\\Rdr or \\Driver\\Xns) which the input and output (I/O) system uses to load the device driver.</span></span> <span data-ttu-id="bd5f1-288">En outre, si **null** est spécifié, le pilote s’exécute avec un nom d’objet par défaut créé par le système d’e/s en fonction du nom du service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-288">Additionally, if **NULL** is specified, the driver runs with a default object name created by the I/O system based on the service name.</span></span>

<span data-ttu-id="bd5f1-289">Exemple : « DWDOM \\ admin »</span><span class="sxs-lookup"><span data-stu-id="bd5f1-289">Example: "DWDOM\\Admin"</span></span>

<span data-ttu-id="bd5f1-290">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-290">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-291">**State**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-291">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-292">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-292">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-293">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="bd5f1-293">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-294">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| service structures \| [**\_ Status service**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-294">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status)\|dwCurrentState "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-295">État actuel du service de base.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-295">Current state of the base service.</span></span>

<span data-ttu-id="bd5f1-296">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-296">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="bd5f1-297">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="bd5f1-297">The values are:</span></span>

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span data-ttu-id="bd5f1-298">**Arrêté** (« arrêté »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-298">**Stopped** ("Stopped")</span></span>


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

<span data-ttu-id="bd5f1-299">**Start Pending** (« Start Pending »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-299">**Start Pending** ("Start Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

<span data-ttu-id="bd5f1-300">**Arrêt en attente** (« arrêt en attente »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-300">**Stop Pending** ("Stop Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="bd5f1-301">**En cours d’exécution** (« en cours d’exécution »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-301">**Running** ("Running")</span></span>


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

<span data-ttu-id="bd5f1-302">**Poursuite en attente** ("continuer en attente")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-302">**Continue Pending** ("Continue Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

<span data-ttu-id="bd5f1-303">**Pause en attente** ("pause en attente")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-303">**Pause Pending** ("Pause Pending")</span></span>


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="bd5f1-304">**Suspendu** (« suspendu »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-304">**Paused** ("Paused")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd5f1-305">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-305">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd5f1-306">**État**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-306">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-308">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-309">Qualificateurs : [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-309">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-310">État actuel de l’objet.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-310">Current status of the object.</span></span> <span data-ttu-id="bd5f1-311">Divers États opérationnels et inopérationnels peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-311">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="bd5f1-312">Les États opérationnels sont les suivants : « OK », « détérioré » et « échec prévu » (un élément, tel qu’un lecteur de disque dur intelligent, peut fonctionner correctement, mais prédire une défaillance dans un avenir proche).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-312">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="bd5f1-313">Les États qui ne sont pas opérationnels sont les suivants : « erreur », « démarrage », « arrêt » et « service ».</span><span class="sxs-lookup"><span data-stu-id="bd5f1-313">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bd5f1-314">Le dernier, « service », peut s’appliquer pendant la réargentation en miroir d’un disque, le rechargement d’une liste d’autorisations utilisateur ou d’autres tâches administratives.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-314">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bd5f1-315">Tous les travaux de ce type ne sont pas en ligne, mais l’élément géré n’est ni « OK », ni de l’un des autres États.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-315">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bd5f1-316">Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-316">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bd5f1-317">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="bd5f1-317">The values are:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bd5f1-318">**OK** (« OK »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-318">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bd5f1-319">**Erreur** (« erreur »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-319">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bd5f1-320">**Détérioré** (« détérioré »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-320">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bd5f1-321">**Inconnu** ("inconnu")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-321">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bd5f1-322">**Échec** prévu (« échec prédit »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-322">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bd5f1-323">**Démarrage** en cours (« démarrage »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-323">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bd5f1-324">**Arrêt** en cours (« arrêt »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-324">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bd5f1-325">**Service** (« service »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-325">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bd5f1-326">**Stressed** (« stressed »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-326">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bd5f1-327">Non **récupéré** (« non récupéré »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-327">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bd5f1-328">**Aucun contact** (« aucun contact »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-328">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bd5f1-329">**Communication perdue** (« inversée comm »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-329">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bd5f1-330">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-330">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-331">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-331">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-332">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-332">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-333">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**CreationClassName**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Class Name ")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-333">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-334">Nom de type du système qui héberge ce service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-334">Type name of the system that hosts this service.</span></span>

<span data-ttu-id="bd5f1-335">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-335">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-336">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-336">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-337">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-338">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-338">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-339">Qualificateurs : [**Propaged**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ System**](cim-system.md).**Name**"), [**\_ clé CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="bd5f1-339">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-340">Nom du système qui héberge ce service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-340">Name of the system that hosts this service.</span></span>

<span data-ttu-id="bd5f1-341">Cette propriété est héritée [**du \_ service CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-341">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd5f1-342">**TagId**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-342">**TagId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd5f1-343">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-343">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-344">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="bd5f1-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd5f1-345">Qualificateurs : [**MappingStrings**](../wmisdk/standard-qualifiers.md) (« win32api \| service structures \| [**query \_ service \_ config**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId »), [**DisplayName**](../wmisdk/standard-qualifiers.md) (« ID de balise »)</span><span class="sxs-lookup"><span data-stu-id="bd5f1-345">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Service Structures\|[**QUERY\_SERVICE\_CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)\|dwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Tag Id")</span></span>
</dt> </dl>

<span data-ttu-id="bd5f1-346">Valeur de balise unique pour ce service dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-346">Unique tag value for this service in the group.</span></span> <span data-ttu-id="bd5f1-347">La valeur 0 (zéro) indique que la balise n’a pas été assignée au service.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-347">A value of 0 (zero) indicates that the service has not been assigned a tag.</span></span> <span data-ttu-id="bd5f1-348">Une balise peut être utilisée pour commander le démarrage du service dans un groupe d’ordre de chargement en spécifiant un vecteur d’ordre des balises dans le registre situé à l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="bd5f1-348">A tag can be used for ordering service startup within a load order group by specifying a tag order vector in the registry located at:</span></span>

<span data-ttu-id="bd5f1-349">Cette propriété est héritée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-349">This property is inherited from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

<span data-ttu-id="bd5f1-350">**HKEY \_ \_Contrôle CurrentControlSet du système de l’ordinateur local \\ \\ \\ \\ GroupOrderList**.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-350">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\GroupOrderList**.</span></span>

<span data-ttu-id="bd5f1-351">Les balises sont uniquement évaluées pour les services du pilote du noyau et du pilote du système de fichiers qui ont des modes de démarrage ou de démarrage du système.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-351">Tags are only evaluated for Kernel Driver and File System Driver start-type services that have Boot or System start modes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd5f1-352">Notes</span><span class="sxs-lookup"><span data-stu-id="bd5f1-352">Remarks</span></span>

<span data-ttu-id="bd5f1-353">La classe **Win32 \_ SystemDriver** est dérivée de [**Win32 \_ BaseService**](win32-baseservice.md).</span><span class="sxs-lookup"><span data-stu-id="bd5f1-353">The **Win32\_SystemDriver** class is derived from [**Win32\_BaseService**](win32-baseservice.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bd5f1-354">Exemples</span><span class="sxs-lookup"><span data-stu-id="bd5f1-354">Examples</span></span>

<span data-ttu-id="bd5f1-355">L’exemple de [liste de pilotes de système](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript affiche les pilotes système installés dans un fichier html.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-355">The [List System Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript sample Displays installed system drivers in an HTML file.</span></span>

<span data-ttu-id="bd5f1-356">L’exemple PowerShell suivant récupère un certain nombre de propriétés des pilotes système en cours d’exécution sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="bd5f1-356">The following PowerShell example retrieves a number of properties from the running system drivers on a computer.</span></span>


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
```



## <a name="requirements"></a><span data-ttu-id="bd5f1-357">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd5f1-357">Requirements</span></span>



| <span data-ttu-id="bd5f1-358">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd5f1-358">Requirement</span></span> | <span data-ttu-id="bd5f1-359">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd5f1-359">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5f1-360">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd5f1-360">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5f1-361">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd5f1-361">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd5f1-362">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd5f1-362">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5f1-363">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd5f1-363">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd5f1-364">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="bd5f1-364">Namespace</span></span><br/>                | <span data-ttu-id="bd5f1-365">\\Cimv2 racine</span><span class="sxs-lookup"><span data-stu-id="bd5f1-365">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd5f1-366">MOF</span><span class="sxs-lookup"><span data-stu-id="bd5f1-366">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd5f1-367"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd5f1-367"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd5f1-368">DLL</span><span class="sxs-lookup"><span data-stu-id="bd5f1-368">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd5f1-369"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd5f1-369"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd5f1-370">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd5f1-370">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5f1-371">**\_BaseService Win32**</span><span class="sxs-lookup"><span data-stu-id="bd5f1-371">**Win32\_BaseService**</span></span>](win32-baseservice.md)
</dt> <dt>

[<span data-ttu-id="bd5f1-372">Classes du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="bd5f1-372">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
