---
description: Représente un élément logique qui contient des informations pour représenter et gérer les fonctionnalités fournies par un périphérique ou une fonctionnalité logicielle.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: Classe CIM_Service (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ee3c51b6af50d77e94bb0a29bd1c8148cda8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527195"
---
# <a name="cim_service-class-hyper-v-management"></a><span data-ttu-id="0c3d0-103">Classe CIM_Service (gestion Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="0c3d0-103">CIM_Service class (Hyper-V management)</span></span>

<span data-ttu-id="0c3d0-104">Représente un élément logique qui contient des informations pour représenter et gérer les fonctionnalités fournies par un périphérique ou une fonctionnalité logicielle.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-104">Represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="0c3d0-105">Un service est un objet à usage général permettant de configurer et de gérer l’implémentation des fonctionnalités. il ne s’agit pas de la fonctionnalité elle-même.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-105">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c3d0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c3d0-106">Syntax</span></span>

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a><span data-ttu-id="0c3d0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="0c3d0-107">Members</span></span>

<span data-ttu-id="0c3d0-108">La classe de **\_ service CIM** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0c3d0-108">The **CIM\_Service** class has these types of members:</span></span>

-   [<span data-ttu-id="0c3d0-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0c3d0-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="0c3d0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0c3d0-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0c3d0-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0c3d0-111">Methods</span></span>

<span data-ttu-id="0c3d0-112">La classe de **\_ service CIM** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-112">The **CIM\_Service** class has these methods.</span></span>



| <span data-ttu-id="0c3d0-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="0c3d0-113">Method</span></span>                                           | <span data-ttu-id="0c3d0-114">Description</span><span class="sxs-lookup"><span data-stu-id="0c3d0-114">Description</span></span>                    |
|:-------------------------------------------------|:-------------------------------|
| [<span data-ttu-id="0c3d0-115">**StartService**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-115">**StartService**</span></span>](cim-service-startservice.md) | <span data-ttu-id="0c3d0-116">démarre le service.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-116">Starts the service.</span></span><br/> |
| [<span data-ttu-id="0c3d0-117">**StopService**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-117">**StopService**</span></span>](cim-service-stopservice.md)   | <span data-ttu-id="0c3d0-118">arrête le service.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-118">Stops the service.</span></span><br/>  |



 

### <a name="properties"></a><span data-ttu-id="0c3d0-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="0c3d0-119">Properties</span></span>

<span data-ttu-id="0c3d0-120">La classe de **\_ service CIM** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-120">The **CIM\_Service** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c3d0-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3d0-122">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-123">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c3d0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-124">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0c3d0-124">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0c3d0-125">Nom de classe utilisé pour créer une instance de cette classe.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-125">The class name used to create an instance of this class.</span></span> <span data-ttu-id="0c3d0-126">**CreationClassName** est combiné avec d’autres propriétés de clé de cette classe pour identifier de manière unique les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-126">**CreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="0c3d0-127">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-127">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3d0-128">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-129">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c3d0-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-130">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="0c3d0-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="0c3d0-131">Identificateur unique du service qui indique les fonctionnalités du service.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-131">A unique identifier of the service that indicates the functionality of the service.</span></span>

</dd> <dt>

<span data-ttu-id="0c3d0-132">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-132">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3d0-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-134">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c3d0-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-135">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations générales sur DMTF \| 001,4»)</span><span class="sxs-lookup"><span data-stu-id="0c3d0-135">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="0c3d0-136">Informations de contact pour le propriétaire principal du service.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-136">Contact information for the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="0c3d0-137">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-137">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3d0-138">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-139">Type d’accès : lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="0c3d0-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-140">Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informations générales sur DMTF \| 001,3»)</span><span class="sxs-lookup"><span data-stu-id="0c3d0-140">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|General Information\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="0c3d0-141">Nom du propriétaire principal du service.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-141">The name of the primary owner of the service.</span></span>

</dd> <dt>

<span data-ttu-id="0c3d0-142">**Cours**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-142">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3d0-143">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-144">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c3d0-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c3d0-145">**true** si le service a été démarré ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-145">**true** if the service has been started; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="0c3d0-146">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-146">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3d0-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c3d0-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-149">Qualificateurs : [**déconseillé**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ service CIM**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0c3d0-149">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_Service**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0c3d0-150">Cette propriété est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-150">This property is deprecated.</span></span> <span data-ttu-id="0c3d0-151">Utilisez plutôt la propriété **EnabledDefault** héritée de [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="0c3d0-151">Instead, use the **EnabledDefault** property that is inherited from [**CIM\_EnabledLogicalElement**](cim-enabledlogicalelement.md).</span></span>

> [!Note]  
> <span data-ttu-id="0c3d0-152">Description déconseillée : indique si le service est démarré automatiquement (par exemple, par un système d’exploitation) ou s’il est démarré uniquement à la demande.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-152">Deprecated description: Indicates whether the service is automatically started (for example, by an operating system) or only started upon request.</span></span>

 

<dt>



 <span data-ttu-id="0c3d0-153">(« Automatique »)</span><span class="sxs-lookup"><span data-stu-id="0c3d0-153">("Automatic")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0c3d0-154">(« Manuel »)</span><span class="sxs-lookup"><span data-stu-id="0c3d0-154">("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0c3d0-155">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3d0-156">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-157">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c3d0-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-158">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**CreationClassName**»)</span><span class="sxs-lookup"><span data-stu-id="0c3d0-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="0c3d0-159">Nom de la classe utilisé pour créer une instance du système qui contient le service.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-159">The class name used to create an instance of the system that contains the service.</span></span> <span data-ttu-id="0c3d0-160">**SystemCreationClassName** est combiné avec d’autres propriétés de clé de cette classe pour identifier de manière unique les instances de cette classe et de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-160">**SystemCreationClassName** is combined with other key properties of this class to uniquely identify instances of this class and its subclasses.</span></span>

</dd> <dt>

<span data-ttu-id="0c3d0-161">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-161">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c3d0-162">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-163">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="0c3d0-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c3d0-164">Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagée**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ système CIM**](cim-system.md).**Name**»)</span><span class="sxs-lookup"><span data-stu-id="0c3d0-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="0c3d0-165">Nom du système d’étendue.</span><span class="sxs-lookup"><span data-stu-id="0c3d0-165">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c3d0-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c3d0-166">Requirements</span></span>



| <span data-ttu-id="0c3d0-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c3d0-167">Requirement</span></span> | <span data-ttu-id="0c3d0-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c3d0-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c3d0-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c3d0-169">Minimum supported client</span></span><br/> | <span data-ttu-id="0c3d0-170">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0c3d0-170">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0c3d0-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c3d0-171">Minimum supported server</span></span><br/> | <span data-ttu-id="0c3d0-172">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0c3d0-172">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0c3d0-173">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0c3d0-173">Namespace</span></span><br/>                | <span data-ttu-id="0c3d0-174">\\Virtualisation racine \\ v2</span><span class="sxs-lookup"><span data-stu-id="0c3d0-174">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0c3d0-175">MOF</span><span class="sxs-lookup"><span data-stu-id="0c3d0-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c3d0-176"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c3d0-176"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c3d0-177">DLL</span><span class="sxs-lookup"><span data-stu-id="0c3d0-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c3d0-178"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c3d0-178"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0c3d0-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c3d0-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c3d0-180">**\_ENABLEDLOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0c3d0-180">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> </dl>

 

