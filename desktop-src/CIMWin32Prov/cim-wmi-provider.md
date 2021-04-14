---
description: Ces classes WMI sont déclarées dans CimWin32. mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: Fournisseur WMI CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3249549e0915f51b6a9a6f2386c18ba695919a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523108"
---
# <a name="cim-wmi-provider"></a><span data-ttu-id="3fe9c-103">Fournisseur WMI CIM</span><span class="sxs-lookup"><span data-stu-id="3fe9c-103">CIM WMI Provider</span></span>

<span data-ttu-id="3fe9c-104">Ces classes WMI sont déclarées dans CimWin32. mof.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-104">These WMI classes are declared in CimWin32.mof.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3fe9c-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3fe9c-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="3fe9c-106">**\_Action CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-106">**CIM\_Action**</span></span>](cim-action.md)
</dt> <dd>

<span data-ttu-id="3fe9c-107">Une classe d' [**\_ action CIM**](cim-action.md) est une opération qui fait partie d’un processus de création d’un élément logiciel dans son état suivant ou d’élimination de l’élément logiciel dans l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-107">A [**CIM\_Action**](cim-action.md) class is an operation that is part of a process to either create a software element in its next state or to eliminate the software element in the current state.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-108">**\_ACTIONSEQUENCE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-108">**CIM\_ActionSequence**</span></span>](cim-actionsequence.md)
</dt> <dd>

<span data-ttu-id="3fe9c-109">L’Association [**CIM \_ ActionSequence**](cim-actionsequence.md) définit une série d’opérations qui font passer l’élément logiciel (référencé par l’Association [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) ) à son état suivant, ou supprime l’élément logiciel de son état actuel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-109">The [**CIM\_ActionSequence**](cim-actionsequence.md) association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-110">**\_ACTSASSPARE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-110">**CIM\_ActsAsSpare**</span></span>](cim-actsasspare.md)
</dt> <dd>

<span data-ttu-id="3fe9c-111">L’Association [**CIM \_ ActsAsSpare**](cim-actsasspare.md) indique les éléments qui peuvent être des éléments de rechange ou remplacer d’autres éléments agrégés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-111">The [**CIM\_ActsAsSpare**](cim-actsasspare.md) association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="3fe9c-112">Un Spare peut fonctionner en mode de « secours », comme spécifié élément par élément.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-112">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-113">**\_ADJACENTSLOTS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-113">**CIM\_AdjacentSlots**</span></span>](cim-adjacentslots.md)
</dt> <dd>

<span data-ttu-id="3fe9c-114">L’Association [**CIM \_ AdjacentSlots**](cim-adjacentslots.md) décrit la disposition des emplacements sur un tableau d’hébergement ou une carte d’adaptateur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-114">The [**CIM\_AdjacentSlots**](cim-adjacentslots.md) association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="3fe9c-115">Les informations, telles que la distance entre les emplacements et si elles sont « partagées » (si l’une d’elles est remplie, l’autre emplacement ne peut pas être utilisé), sont transmises en tant que propriétés d’association.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-115">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-116">**\_AGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-116">**CIM\_AggregatePExtent**</span></span>](cim-aggregatepextent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-117">La classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) fournit des informations récapitulatives sur les blocs logiques adressables, qui se trouvent dans le même groupe de redondance de stockage et qui se trouvent sur le même support physique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-117">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class provides summary information about addressable logical blocks, which are in the same storage redundancy group and located on the same physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-118">**\_AGGREGATEPSEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-118">**CIM\_AggregatePSExtent**</span></span>](cim-aggregatepsextent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-119">La classe [**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md) définit le nombre de blocs logiques adressables sur un dispositif de stockage unique, à l’exception des blocs logiques mappés en tant que données de vérification.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-119">The [**CIM\_AggregatePSExtent**](cim-aggregatepsextent.md) class defines the number of addressable logical blocks on a single storage device, excluding logical blocks mapped as check data.</span></span> <span data-ttu-id="3fe9c-120">Si des jeux de volumes sont définis, les blocs logiques sont contenus dans un seul ensemble de volumes.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-120">If volume sets are defined, the logical blocks are contained within a single volume set.</span></span> <span data-ttu-id="3fe9c-121">Il s’agit d’un autre regroupement pour les [**\_ ProtectedSpaceExtent CIM**](cim-protectedspaceextent.md), lorsque seules les informations de résumé sont nécessaires ou lorsque la configuration automatique est utilisée.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-121">This is an alternative grouping for [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md), when only summary information is needed or when automatic configuration is used.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-122">**\_AGGREGATEREDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-122">**CIM\_AggregateRedundancyComponent**</span></span>](cim-aggregateredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-123">La classe [**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) décrit l’étendue physique agrégée dans un groupe de redondance de stockage.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-123">The [**CIM\_AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) class describes the aggregate physical extent in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-124">**\_ALARMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-124">**CIM\_AlarmDevice**</span></span>](cim-alarmdevice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-125">La [**classe \_ AlarmDevice CIM**](cim-alarmdevice.md) est un appareil d’alarme qui émet des indications audibles ou visibles relatives à une situation problématique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-125">The [**CIM\_AlarmDevice**](cim-alarmdevice.md) class is an alarm device that emits audible or visible indications related to a problem situation.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-126">**\_ALLOCATEDRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-126">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dd>

<span data-ttu-id="3fe9c-127">La classe [**CIM \_ AllocatedResource**](cim-allocatedresource.md) représente une association entre les unités logiques et les ressources système et indique que la ressource est affectée à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-127">The [**CIM\_AllocatedResource**](cim-allocatedresource.md) class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-128">**\_APPLICATIONSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-128">**CIM\_ApplicationSystem**</span></span>](cim-applicationsystem.md)
</dt> <dd>

<span data-ttu-id="3fe9c-129">La classe [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) représente une application ou un système logiciel qui prend en charge une fonction commerciale particulière qui peut être gérée comme une unité indépendante.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-129">The [**CIM\_ApplicationSystem**](cim-applicationsystem.md) class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="3fe9c-130">Un tel système peut être décomposé en ses composants fonctionnels à l’aide de la classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-130">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="3fe9c-131">Les fonctionnalités logicielles d’une application ou d’un système logiciel particulier sont localisées à l’aide de l’Association [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-131">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-132">**\_APPLICATIONSYSTEMSOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-132">**CIM\_ApplicationSystemSoftwareFeature**</span></span>](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="3fe9c-133">La classe [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) représente une association qui identifie les fonctionnalités logicielles qui composent un système d’applications particulier.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-133">The [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) class represents an association that identifies the software features that make up a particular application system.</span></span> <span data-ttu-id="3fe9c-134">Les fonctionnalités du logiciel peuvent être incluses dans différents produits.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-134">The software features can be included in different products.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-135">**\_ASSOCIATEDALARM CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-135">**CIM\_AssociatedAlarm**</span></span>](cim-associatedalarm.md)
</dt> <dd>

<span data-ttu-id="3fe9c-136">La [**dépendance \_ AssociatedAlarm CIM**](cim-associatedalarm.md) associe une alarme à un appareil logique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-136">The [**CIM\_AssociatedAlarm**](cim-associatedalarm.md) dependency associates an alarm with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-137">**\_ASSOCIATEDBATTERY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-137">**CIM\_AssociatedBattery**</span></span>](cim-associatedbattery.md)
</dt> <dd>

<span data-ttu-id="3fe9c-138">La [**dépendance \_ AssociatedBattery CIM**](cim-associatedbattery.md) associe une batterie à une unité logique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-138">The [**CIM\_AssociatedBattery**](cim-associatedbattery.md) dependency associates a battery with a logical device.</span></span> <span data-ttu-id="3fe9c-139">Utilisez cette association pour modéliser les batteries individuelles qui composent un onduleur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-139">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-140">**\_ASSOCIATEDCOOLING CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-140">**CIM\_AssociatedCooling**</span></span>](cim-associatedcooling.md)
</dt> <dd>

<span data-ttu-id="3fe9c-141">L’Association [**CIM \_ AssociatedCooling**](cim-associatedcooling.md) indique quand des ventilateurs ou d’autres appareils de refroidissement sont spécifiques à un appareil (par rapport à la fourniture d’un boîtier ou d’un refroidissement d’armoire).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-141">The [**CIM\_AssociatedCooling**](cim-associatedcooling.md) association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-142">**\_ASSOCIATEDMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-142">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> <dd>

<span data-ttu-id="3fe9c-143">La [**classe \_ AssociateMemory CIM**](cim-associatedmemory.md) associe la mémoire installée ou associée, telle que la mémoire cache avec un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-143">The [**CIM\_AssociateMemory**](cim-associatedmemory.md) class associates installed or associated memory, such as cache memory with a logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-144">**\_ASSOCIATEDPROCESSORMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-144">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dd>

<span data-ttu-id="3fe9c-145">La classe [**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md) associe le processeur et la mémoire système, ou le cache d’un processeur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-145">The [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md) class associates the processor and system memory, or a processor's cache.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-146">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-146">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-147">La classe [**CIM \_ AssociatedSensor**](cim-associatedsensor.md) associe un capteur installé à un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-147">The [**CIM\_AssociatedSensor**](cim-associatedsensor.md) class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="3fe9c-148">Le capteur mesure les propriétés d’entrée et de sortie critiques et peut être inclus avec l’appareil ou installé à proximité.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-148">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-149">**\_ASSOCIATEDSUPPLYCURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-149">**CIM\_AssociatedSupplyCurrentSensor**</span></span>](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-150">La classe [**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) associe une alimentation à un capteur courant (intensité) qui surveille sa fréquence d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-150">The [**CIM\_AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md) class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-151">**\_ASSOCIATEDSUPPLYVOLTAGESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-151">**CIM\_AssociatedSupplyVoltageSensor**</span></span>](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-152">Associe une alimentation à un capteur de tension qui surveille sa tension d’entrée.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-152">Associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-153">**Basé sur CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-153">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> <dd>

<span data-ttu-id="3fe9c-154">La classe basée sur [**CIM \_**](cim-basedon.md) représente une association qui décrit comment les extensions de stockage peuvent être assemblées à partir d’extensions de niveau inférieur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-154">The [**CIM\_BasedOn**](cim-basedon.md) class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="3fe9c-155">Par exemple, les extensions physiques incluent des extensions d’espace protégé.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-155">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="3fe9c-156">Par conséquent, les jeux de volumes sont assemblés à partir d’une ou de plusieurs extensions d’espace physique ou protégé.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-156">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="3fe9c-157">La mémoire cache peut être définie indépendamment et réalisée dans un élément physique, ou elle peut être basée sur des extensions de stockage volatiles ou non volatiles.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-157">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-158">**\_Batterie CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-158">**CIM\_Battery**</span></span>](cim-battery.md)
</dt> <dd>

<span data-ttu-id="3fe9c-159">La classe de [**\_ batterie CIM**](cim-battery.md) représente les fonctionnalités et la gestion de l’unité logique de batterie.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-159">The [**CIM\_Battery**](cim-battery.md) class represents the capabilities and management of the battery logical device.</span></span> <span data-ttu-id="3fe9c-160">Cette classe s’applique aux batteries dans les systèmes d’ordinateurs portables et autres batteries internes et externes.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-160">This class applies to batteries in laptop systems and other internal and external batteries.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-161">**\_BINARYSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-161">**CIM\_BinarySensor**</span></span>](cim-binarysensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-162">La classe [**CIM \_ BinarySensor**](cim-binarysensor.md) fournit une sortie booléenne.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-162">The [**CIM\_BinarySensor**](cim-binarysensor.md) class provides a Boolean output.</span></span> <span data-ttu-id="3fe9c-163">Les propriétés **CurrentState** et **PossibleStates** ont été ajoutées pour le capteur, rendant ainsi la sous-classe **CIM \_ BinarySensor** plus nécessaire, bien qu’elle soit conservée pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-163">The **CurrentState** and **PossibleStates** properties were added for sensoring, thus making the **CIM\_BinarySensor** subclass no longer necessary, although, it is retained for backward compatibility.</span></span> <span data-ttu-id="3fe9c-164">Un capteur binaire peut être créé en instanciant un capteur avec deux États possibles.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-164">A binary sensor can be created by instantiating a sensor with two possible states.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-165">**\_BIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-165">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dd>

<span data-ttu-id="3fe9c-166">La classe [**CIM \_ BIOSElement**](cim-bioselement.md) représente le logiciel de bas niveau qui est chargé dans un stockage non volatile et utilisé pour démarrer et configurer un système informatique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-166">The [**CIM\_BIOSElement**](cim-bioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-167">**\_BIOSFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-167">**CIM\_BIOSFeature**</span></span>](cim-biosfeature.md)
</dt> <dd>

<span data-ttu-id="3fe9c-168">représente les fonctionnalités du logiciel de bas niveau utilisé pour démarrer et configurer un système informatique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-168">represents the capabilities of the low-level software that is used to start and configure a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-169">**\_BIOSFEATUREBIOSELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-169">**CIM\_BIOSFeatureBIOSElements**</span></span>](cim-biosfeaturebioselements.md)
</dt> <dd>

<span data-ttu-id="3fe9c-170">La classe [**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) associe une fonctionnalité BIOS et ses éléments BIOS agrégés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-170">The [**CIM\_BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) class associates a BIOS feature and its aggregated BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-171">**\_BIOSLOADEDINNV CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-171">**CIM\_BIOSLoadedInNV**</span></span>](cim-biosloadedinnv.md)
</dt> <dd>

<span data-ttu-id="3fe9c-172">La classe [**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md) associe un élément BIOS et le stockage non volatile dans lequel elle est chargée.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-172">The [**CIM\_BIOSLoadedInNV**](cim-biosloadedinnv.md) class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-173">**\_BOOTOSFROMFS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-173">**CIM\_BootOSFromFS**</span></span>](cim-bootosfromfs.md)
</dt> <dd>

<span data-ttu-id="3fe9c-174">La classe [**CIM \_ BootOSFromFS**](cim-bootosfromfs.md) associe le système d’exploitation et les systèmes de fichiers à partir desquels le système d’exploitation est chargé.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-174">The [**CIM\_BootOSFromFS**](cim-bootosfromfs.md) class associates the operating system and the file systems from which the operating system is loaded.</span></span> <span data-ttu-id="3fe9c-175">L’Association est de plusieurs-à-plusieurs ; un système d’exploitation distribué peut dépendre de plusieurs systèmes de fichiers pour se charger correctement et complètement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-175">The association is many-to-many; a distributed operating system can depend on several file systems to load correctly and completely.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-176">**\_BOOTSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-176">**CIM\_BootSAP**</span></span>](cim-bootsap.md)
</dt> <dd>

<span data-ttu-id="3fe9c-177">La classe [**CIM \_ BootSAP**](cim-bootsap.md) représente les points d’accès d’un service de démarrage.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-177">The [**CIM\_BootSAP**](cim-bootsap.md) class represents the access points of a boot service.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-178">**\_BOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-178">**CIM\_BootService**</span></span>](cim-bootservice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-179">La classe [**CIM \_ BootService**](cim-bootservice.md) représente la fonctionnalité fournie par un périphérique ou un logiciel, ou par un réseau, pour charger un système d’exploitation sur un système informatique unitaire.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-179">The [**CIM\_BootService**](cim-bootservice.md) class represents the functionality provided by a device or software, or by a network, to load an operating system on a unitary computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-180">**\_BOOTSERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-180">**CIM\_BootServiceAccessBySAP**</span></span>](cim-bootserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="3fe9c-181">La classe [**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) associe un service de démarrage et ses points d’accès.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-181">The [**CIM\_BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) class associates a boot service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-182">**\_CACHEMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-182">**CIM\_CacheMemory**</span></span>](cim-cachememory.md)
</dt> <dd>

<span data-ttu-id="3fe9c-183">La classe [**CIM \_ CacheMemory**](cim-cachememory.md) définit les fonctionnalités et la gestion de la mémoire cache.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-183">The [**CIM\_CacheMemory**](cim-cachememory.md) class defines the capabilities and management of cache memory.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-184">**\_Carte CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-184">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dd>

<span data-ttu-id="3fe9c-185">La classe de [**\_ carte CIM**](cim-card.md) représente un type de conteneur physique qui peut être branché dans une autre carte ou un autre tableau d’accueil, ou il s’agit d’une carte d’hébergement/carte mère dans un châssis.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-185">The [**CIM\_Card**](cim-card.md) class represents a type of physical container that can be plugged into another card or hosting board, or is itself a hosting board/motherboard in a chassis.</span></span> <span data-ttu-id="3fe9c-186">Cette classe comprend tout package capable de transporter des signaux et de fournir un point de montage pour les composants physiques, tels que les copeaux ou autres packages physiques, tels que les autres cartes.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-186">This class includes any package that is capable of carrying signals and providing a mounting point for physical components, such as chips or other physical packages, such as other cards.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-187">**\_CARDINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-187">**CIM\_CardInSlot**</span></span>](cim-cardinslot.md)
</dt> <dd>

<span data-ttu-id="3fe9c-188">La classe [**CIM \_ CardInSlot**](cim-cardinslot.md) associe une carte d’adaptateur au conteneur dans lequel elle est insérée.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-188">The [**CIM\_CardInSlot**](cim-cardinslot.md) class associates an adapter card with the container into which it is inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-189">**\_CARDONCARD CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-189">**CIM\_CardOnCard**</span></span>](cim-cardoncard.md)
</dt> <dd>

<span data-ttu-id="3fe9c-190">L’Association [**CIM \_ CardOnCard**](cim-cardoncard.md) décrit des relations sur les cartes qui peuvent être connectées à des cartes mères/cartes de Baseboard, daughtercards d’un adaptateur ou des cartes qui prennent en charge des modules spéciaux de type carte.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-190">The [**CIM\_CardOnCard**](cim-cardoncard.md) association describes relationships about cards that can be plugged into motherboards/baseboards, daughtercards of an adapter, or cards that support special card-like modules.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-191">**\_CDROMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-191">**CIM\_CDROMDrive**</span></span>](cim-cdromdrive.md)
</dt> <dd>

<span data-ttu-id="3fe9c-192">La classe [**CIM \_ CDROMDrive**](cim-cdromdrive.md) représente un lecteur de CD-ROM sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-192">The [**CIM\_CDROMDrive**](cim-cdromdrive.md) class represents a CD-ROM drive on the computer.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-193">**\_Châssis CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-193">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dd>

<span data-ttu-id="3fe9c-194">La classe de [**\_ châssis CIM**](cim-chassis.md) représente les éléments physiques qui englobent d’autres éléments et fournissent des fonctionnalités définissables, telles qu’un ordinateur de bureau, un nœud de traitement, des onduleurs, un stockage sur disque ou sur bande, ou une combinaison de ces éléments.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-194">The [**CIM\_Chassis**](cim-chassis.md) class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-195">**\_CHASSISINRACK CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-195">**CIM\_ChassisInRack**</span></span>](cim-chassisinrack.md)
</dt> <dd>

<span data-ttu-id="3fe9c-196">L’Association [**CIM \_ ChassisInRack**](cim-chassisinrack.md) représente la relation « contenant » entre un rack et un châssis qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-196">The [**CIM\_ChassisInRack**](cim-chassisinrack.md) association represents the "containing" relationship between a rack and a chassis that it contains.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-197">**\_Vérification CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-197">**CIM\_Check**</span></span>](cim-check.md)
</dt> <dd>

<span data-ttu-id="3fe9c-198">La classe de [**\_ vérification CIM**](cim-check.md) représente une condition ou une caractéristique supposée être vraie dans un environnement défini ou étendu par une instance d’une classe [**\_ ComputerSystem CIM**](cim-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-198">The [**CIM\_Check**](cim-check.md) class represents a condition or characteristic that is expected to be true in an environment defined or scoped by an instance of a [**CIM\_ComputerSystem**](cim-computersystem.md) class.</span></span> <span data-ttu-id="3fe9c-199">Les contrôles associés à un élément logiciel particulier sont organisés en l’un des deux groupes à l’aide de la propriété **phase** de l’Association [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-199">The checks associated with a particular software element are organized into one of two groups using the **Phase** property of the [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-200">**\_Puce CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-200">**CIM\_Chip**</span></span>](cim-chip.md)
</dt> <dd>

<span data-ttu-id="3fe9c-201">La classe de [**\_ puces CIM**](cim-chip.md) représente le type de matériel de circuit intégré, y compris les ASIC, les processeurs, les puces de mémoire, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-201">The [**CIM\_Chip**](cim-chip.md) class represents the type of integrated circuit hardware, including ASICs, processors, memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-202">**\_CLUSTERINGSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-202">**CIM\_ClusteringSAP**</span></span>](cim-clusteringsap.md)
</dt> <dd>

<span data-ttu-id="3fe9c-203">La classe [**CIM \_ ClusteringSAP**](cim-clusteringsap.md) représente les points d’accès d’un service de clustering.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-203">The [**CIM\_ClusteringSAP**](cim-clusteringsap.md) class represents the access points of a clustering service.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-204">**\_CLUSTERINGSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-204">**CIM\_ClusteringService**</span></span>](cim-clusteringservice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-205">La classe [**CIM \_ ClusteringService**](cim-clusteringservice.md) représente la fonctionnalité fournie par un cluster.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-205">The [**CIM\_ClusteringService**](cim-clusteringservice.md) class represents the functionality provided by a cluster.</span></span> <span data-ttu-id="3fe9c-206">Par exemple, la fonctionnalité de basculement peut être modélisée en tant que service d’un cluster de basculement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-206">For example, failover functionality can be modeled as a service of a failover cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-207">**\_CLUSTERSERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-207">**CIM\_ClusterServiceAccessBySAP**</span></span>](cim-clusterserviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="3fe9c-208">La classe [**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) représente la relation entre un service de clustering et ses points d’accès.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-208">The [**CIM\_ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) class represents the relationship between a clustering service and its access points.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-209">**\_COLLECTEDCOLLECTIONS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-209">**CIM\_CollectedCollections**</span></span>](cim-collectedcollections.md)
</dt> <dd>

<span data-ttu-id="3fe9c-210">La [**classe \_ CollectedCollections CIM**](cim-collectedcollections.md) est une association d’agrégation qui représente une collection d’éléments système gérés (MSE) contenus dans une collection de MSEs.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-210">The [**CIM\_CollectedCollections**](cim-collectedcollections.md) class is an aggregation association that represents a collection of Managed System Elements (MSE) contained in a collection of MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-211">**\_COLLECTEDMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-211">**CIM\_CollectedMSEs**</span></span>](cim-collectedmses.md)
</dt> <dd>

<span data-ttu-id="3fe9c-212">La classe d’association [**CIM \_ CollectedMSEs**](cim-collectedmses.md) représente les membres de l’objet de regroupement, une classe [**CollectionOfMSEs**](cim-collectionofmses.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-212">The [**CIM\_CollectedMSEs**](cim-collectedmses.md) association class represents the members of the grouping object, a [**CollectionOfMSEs**](cim-collectionofmses.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-213">**\_COLLECTIONOFMSES CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-213">**CIM\_CollectionOfMSEs**</span></span>](cim-collectionofmses.md)
</dt> <dd>

<span data-ttu-id="3fe9c-214">L’objet [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) autorise le regroupement d’objets [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) afin d’associer les paramètres et les configurations.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-214">The [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="3fe9c-215">Il est abstrait d’exiger une définition et un affinage sémantique supplémentaires dans les sous-classes.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-215">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-216">**\_COLLECTIONOFSENSORS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-216">**CIM\_CollectionOfSensors**</span></span>](cim-collectionofsensors.md)
</dt> <dd>

<span data-ttu-id="3fe9c-217">L’Association [**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md) représente les capteurs binaires qui composent le capteur à États multistates.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-217">The [**CIM\_CollectionOfSensors**](cim-collectionofsensors.md) association represents the binary sensors that make up the multistate sensor.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-218">**\_COLLECTIONSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-218">**CIM\_CollectionSetting**</span></span>](cim-collectionsetting.md)
</dt> <dd>

<span data-ttu-id="3fe9c-219">La classe [**CIM \_ CollectionSetting**](cim-collectionsetting.md) représente l’association entre un [**modèle CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) et la classe de paramètres définie pour eux.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-219">The [**CIM\_CollectionSetting**](cim-collectionsetting.md) class represents the association between a [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-220">**\_COMPATIBLEPRODUCT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-220">**CIM\_CompatibleProduct**</span></span>](cim-compatibleproduct.md)
</dt> <dd>

<span data-ttu-id="3fe9c-221">La [**classe \_ CompatibleProduct CIM**](cim-compatibleproduct.md) représente une association entre des produits qui indique si deux produits référencés sont interopérables, par exemple s’ils peuvent être installés ensemble ou si l’un peut être le conteneur physique de l’autre, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-221">The [**CIM\_CompatibleProduct**](cim-compatibleproduct.md) class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-222">**\_Composant CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-222">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dd>

<span data-ttu-id="3fe9c-223">L’Association de [**\_ composants CIM**](cim-component.md) représente les parties d’une relation entre les MSEs.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-223">The [**CIM\_Component**](cim-component.md) association represents the parts of a relationship between MSEs.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-224">**\_ComputerSystem CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-224">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dd>

<span data-ttu-id="3fe9c-225">Une [**classe \_ ComputerSystem CIM**](cim-computersystem.md) représente une collection spéciale d' [**instances \_ ManagedSystemElement CIM**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-225">A [**CIM\_ComputerSystem**](cim-computersystem.md) class represents a special collection of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) instances.</span></span> <span data-ttu-id="3fe9c-226">Cette collection fournit des fonctionnalités d’ordinateur et sert de point d’agrégation pour associer un ou plusieurs des éléments suivants : système de fichiers, système d’exploitation, processeur et mémoire (stockage volatile et non volatile).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-226">This collection provides computer capabilities and serves as an aggregation point to associate one or more of the following elements: file system, operating system, processor and memory (volatile and non-volatile storage).</span></span> <span data-ttu-id="3fe9c-227">Cette classe est dérivée [**du \_ système CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-227">This class is derived from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-228">**\_COMPUTERSYSTEMDMA CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-228">**CIM\_ComputerSystemDMA**</span></span>](cim-computersystemdma.md)
</dt> <dd>

<span data-ttu-id="3fe9c-229">La classe [**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) représente une association entre un système informatique et ses canaux DMA (Direct Memory Access) disponibles.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-229">The [**CIM\_ComputerSystemDMA**](cim-computersystemdma.md) class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-230">**\_COMPUTERSYSTEMIRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-230">**CIM\_ComputerSystemIRQ**</span></span>](cim-computersystemirq.md)
</dt> <dd>

<span data-ttu-id="3fe9c-231">La classe [**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md) représente une association entre un système informatique et ses lignes de requête d’interruption (IRQ) disponibles.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-231">The [**CIM\_ComputerSystemIRQ**](cim-computersystemirq.md) class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-232">**\_COMPUTERSYSTEMMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-232">**CIM\_ComputerSystemMappedIO**</span></span>](cim-computersystemmappedio.md)
</dt> <dd>

<span data-ttu-id="3fe9c-233">La classe [**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md) représente une association entre un système informatique et les ports d’e/s mappés en mémoire disponibles.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-233">The [**CIM\_ComputerSystemMappedIO**](cim-computersystemmappedio.md) class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-234">**\_COMPUTERSYSTEMPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-234">**CIM\_ComputerSystemPackage**</span></span>](cim-computersystempackage.md)
</dt> <dd>

<span data-ttu-id="3fe9c-235">La classe [**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md) représente une association qui définit explicitement la relation entre les systèmes informatiques unitaires et un ou plusieurs packages physiques.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-235">The [**CIM\_ComputerSystemPackage**](cim-computersystempackage.md) class represents an association that explicitly defines the relationship between unitary computer systems and one or more physical packages.</span></span> <span data-ttu-id="3fe9c-236">L’Association est semblable à la façon dont les unités logiques sont réalisées par les éléments physiques.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-236">The association is similar to the way that logical devices are realized by physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-237">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-237">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> <dd>

<span data-ttu-id="3fe9c-238">La classe [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md) représente une association entre un système informatique et les ressources système disponibles.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-238">The [**CIM\_ComputerSystemResource**](cim-computersystemresource.md) class represents an association between a computer system and its available system resources.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-239">**\_Configuration CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-239">**CIM\_Configuration**</span></span>](cim-configuration.md)
</dt> <dd>

<span data-ttu-id="3fe9c-240">L’objet de [**\_ configuration CIM**](cim-configuration.md) permet de regrouper des jeux de paramètres (définis dans les objets de [**\_ paramètre CIM**](cim-setting.md) ) et des dépendances pour un ou plusieurs éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-240">The [**CIM\_Configuration**](cim-configuration.md) object allows the grouping of parameter sets (defined in [**CIM\_Setting**](cim-setting.md) objects) and dependencies for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-241">**\_CONNECTEDTO CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-241">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> <dd>

<span data-ttu-id="3fe9c-242">La classe [**CIM \_ ConnectedTo**](cim-connectedto.md) représente une association qui indique que deux ou plusieurs connecteurs physiques sont connectés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-242">The [**CIM\_ConnectedTo**](cim-connectedto.md) class represents an association that indicates that two or more physical connectors are connected.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-243">**\_CONNECTORONPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-243">**CIM\_ConnectorOnPackage**</span></span>](cim-connectoronpackage.md)
</dt> <dd>

<span data-ttu-id="3fe9c-244">La classe [**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md) représente une association qui rend explicite la relation d’imbrication entre les connecteurs et les packages.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-244">The [**CIM\_ConnectorOnPackage**](cim-connectoronpackage.md) class represents an association that makes explicit the containment relationship between connectors and packages.</span></span> <span data-ttu-id="3fe9c-245">Les packages physiques contiennent des connecteurs et d’autres éléments physiques.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-245">Physical packages contain connectors as well as other physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-246">**\_Conteneur CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-246">**CIM\_Container**</span></span>](cim-container.md)
</dt> <dd>

<span data-ttu-id="3fe9c-247">La classe de [**\_ conteneur CIM**](cim-container.md) représente une association entre un élément physique contenu et un élément physique contenant.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-247">The [**CIM\_Container**](cim-container.md) class represents an association between a contained and a containing physical element.</span></span> <span data-ttu-id="3fe9c-248">Un objet conteneur doit être un package physique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-248">A containing object must be a physical package.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-249">**\_CONTROLLEDBY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-249">**CIM\_ControlledBy**</span></span>](cim-controlledby.md)
</dt> <dd>

<span data-ttu-id="3fe9c-250">La [**relation \_ ControlledBy CIM**](cim-controlledby.md) indique quels appareils sont demandés par l’unité logique du contrôleur, ou accessibles via celui-ci.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-250">The [**CIM\_ControlledBy**](cim-controlledby.md) relationship indicates which devices are commanded by, or accessed through, the controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-251">**\_Contrôleur CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-251">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-252">La classe de [**\_ contrôleur CIM**](cim-controller.md) est une classe parente permettant de regrouper divers appareils liés au contrôle.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-252">The [**CIM\_Controller**](cim-controller.md) class is a parent class for grouping miscellaneous control-related devices.</span></span> <span data-ttu-id="3fe9c-253">Les contrôleurs SCSI, les contrôleurs USB et les contrôleurs série sont des exemples de contrôleurs.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-253">Examples of controllers are SCSI controllers, USB controllers, and serial controllers.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-254">**\_COOLINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-254">**CIM\_CoolingDevice**</span></span>](cim-coolingdevice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-255">La classe [**CIM \_ CoolingDevice**](cim-coolingdevice.md) représente les fonctionnalités et la gestion des appareils de refroidissement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-255">The [**CIM\_CoolingDevice**](cim-coolingdevice.md) class represents the capabilities and management of cooling devices.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-256">**\_COPYFILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-256">**CIM\_CopyFileAction**</span></span>](cim-copyfileaction.md)
</dt> <dd>

<span data-ttu-id="3fe9c-257">La classe [**CIM \_ CopyFileAction**](cim-copyfileaction.md) représente le déplacement ou la copie de fichiers à partir d’un système informatique vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-257">The [**CIM\_CopyFileAction**](cim-copyfileaction.md) class represents moving or copying files from a computer system to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-258">**\_CREATEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-258">**CIM\_CreateDirectoryAction**</span></span>](cim-createdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="3fe9c-259">La classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) crée des répertoires vides pour les éléments logiciels à installer localement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-259">The [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class creates empty directories for software elements to be installed locally.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-260">**\_CURRENTSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-260">**CIM\_CurrentSensor**</span></span>](cim-currentsensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-261">La classe [**CIM \_ CurrentSensor**](cim-currentsensor.md) existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-261">The [**CIM\_CurrentSensor**](cim-currentsensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-262">**\_Fichier de fichier CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-262">**CIM\_DataFile**</span></span>](cim-datafile.md)
</dt> <dd>

<span data-ttu-id="3fe9c-263">La classe de [**\_ fichier**](cim-datafile.md) de données CIM représente une collection nommée de données ou du code exécutable.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-263">The [**CIM\_DataFile**](cim-datafile.md) class represents a named collection of data or executable code.</span></span> <span data-ttu-id="3fe9c-264">Seules les instances de fichiers sur des disques fixes locaux sont retournées</span><span class="sxs-lookup"><span data-stu-id="3fe9c-264">Only instances of files on local fixed disks will be returned</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-265">**\_Dépendance CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-265">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dd>

<span data-ttu-id="3fe9c-266">La classe de [**\_ dépendance CIM**](cim-dependency.md) représente une association qui établit des relations de dépendance entre des objets.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-266">The [**CIM\_Dependency**](cim-dependency.md) class represents an association that establishes dependency relationships between objects.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-267">**\_DEPENDENCYCONTEXT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-267">**CIM\_DependencyContext**</span></span>](cim-dependencycontext.md)
</dt> <dd>

<span data-ttu-id="3fe9c-268">La [**relation \_ DependencyContext CIM**](cim-dependencycontext.md) associe une classe de [**\_ dépendance CIM**](cim-dependency.md) à un ou plusieurs objets de [**\_ configuration CIM**](cim-configuration.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-268">The [**CIM\_DependencyContext**](cim-dependencycontext.md) relationship associates a [**CIM\_Dependency**](cim-dependency.md) class with one or more [**CIM\_Configuration**](cim-configuration.md) objects.</span></span> <span data-ttu-id="3fe9c-269">Par exemple, les dépendances d’un système informatique peuvent changer en fonction du réseau auquel le système est attaché.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-269">For example, a computer system's dependencies can change based on the network to which the system is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-270">**\_DESKTOPMONITOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-270">**CIM\_DesktopMonitor**</span></span>](cim-desktopmonitor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-271">La classe [**CIM \_ desktopmonitor**](cim-desktopmonitor.md) représente les fonctionnalités et la gestion de l’unité logique du moniteur Desktop (CRT).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-271">The [**CIM\_DesktopMonitor**](cim-desktopmonitor.md) class represents the capabilities and management of the desktop monitor (CRT) logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-272">**\_DEVICEACCESSEDBYFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-272">**CIM\_DeviceAccessedByFile**</span></span>](cim-deviceaccessedbyfile.md)
</dt> <dd>

<span data-ttu-id="3fe9c-273">La classe d’association [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) spécifie l’appareil logique accessible à l’aide de la classe [**CIM \_ DeviceFile**](cim-devicefile.md) référencée.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-273">The [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-274">**\_DEVICECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-274">**CIM\_DeviceConnection**</span></span>](cim-deviceconnection.md)
</dt> <dd>

<span data-ttu-id="3fe9c-275">La classe d’association [**CIM \_ DeviceConnection**](cim-deviceconnection.md) représente au moins deux appareils connectés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-275">The [**CIM\_DeviceConnection**](cim-deviceconnection.md) association class represents two or more connected devices.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-276">**\_DEVICEERRORCOUNTS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-276">**CIM\_DeviceErrorCounts**</span></span>](cim-deviceerrorcounts.md)
</dt> <dd>

<span data-ttu-id="3fe9c-277">La [**classe \_ DeviceErrorCounts CIM**](cim-deviceerrorcounts.md) est une classe statistique qui contient des compteurs relatifs aux erreurs pour un périphérique logique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-277">The [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="3fe9c-278">Les types d’erreurs sont définis par CCITT (Rec X. 733) et ISO (IEC 10164-4).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-278">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-279">**\_DEVICEFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-279">**CIM\_DeviceFile**</span></span>](cim-devicefile.md)
</dt> <dd>

<span data-ttu-id="3fe9c-280">La classe [**CIM \_ DeviceFile**](cim-devicefile.md) représente un type de fichier logique, qui représente un périphérique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-280">The [**CIM\_DeviceFile**](cim-devicefile.md) class represents a type of logical file, which represents a device.</span></span> <span data-ttu-id="3fe9c-281">Cette Convention est utile pour les systèmes d’exploitation qui gèrent des appareils à l’aide d’un modèle d’e/s de flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-281">This convention is useful for operating systems that manage devices using a byte stream I/O model.</span></span> <span data-ttu-id="3fe9c-282">L’appareil logique associé à ce fichier est spécifié à l’aide de la relation [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-282">The logical device that is associated with this file is specified using the [**CIM\_DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) relationship.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-283">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-283">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dd>

<span data-ttu-id="3fe9c-284">La classe [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) représente une association entre un point d’accès de service (SAP) et la façon dont il est implémenté.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-284">The [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="3fe9c-285">Lorsque de nombreux périphériques logiques sont associés à un SAP, les éléments fonctionnent conjointement pour fournir le point d’accès.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-285">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="3fe9c-286">Si différentes implémentations d’un SAP existent, chaque implémentation entraîne des instanciations individuelles de l’objet SAP.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-286">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-287">**\_DEVICESERVICEIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-287">**CIM\_DeviceServiceImplementation**</span></span>](cim-deviceserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="3fe9c-288">La classe [**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md) représente une association entre un service et la manière dont il est implémenté.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-288">The [**CIM\_DeviceServiceImplementation**](cim-deviceserviceimplementation.md) class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="3fe9c-289">Lorsque plusieurs appareils sont associés à un service, les éléments fonctionnent conjointement pour fournir le service.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-289">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="3fe9c-290">Si différentes implémentations d’un service existent, chaque implémentation produit des instanciations individuelles de l’objet de service.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-290">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-291">**\_DEVICESOFTWARE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-291">**CIM\_DeviceSoftware**</span></span>](cim-devicesoftware.md)
</dt> <dd>

<span data-ttu-id="3fe9c-292">La [**relation \_ DeviceSoftware CIM**](cim-devicesoftware.md) identifie les logiciels associés à un appareil, tels que les pilotes, les logiciels de configuration ou d’application, ou le microprogramme.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-292">The [**CIM\_DeviceSoftware**](cim-devicesoftware.md) relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-293">**\_Répertoire CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-293">**CIM\_Directory**</span></span>](cim-directory.md)
</dt> <dd>

<span data-ttu-id="3fe9c-294">La classe de [**\_ répertoire CIM**](cim-directory.md) représente un type de fichier qui regroupe logiquement les fichiers de données qu’elle contient et fournit des informations de chemin d’accès pour les fichiers groupés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-294">The [**CIM\_Directory**](cim-directory.md) class represents a file type that logically groups the data files that it contains and provides path information for the grouped files.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-295">**\_DIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-295">**CIM\_DirectoryAction**</span></span>](cim-directoryaction.md)
</dt> <dd>

<span data-ttu-id="3fe9c-296">La classe abstraite [**CIM \_ DirectoryAction**](cim-directoryaction.md) gère les répertoires.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-296">The [**CIM\_DirectoryAction**](cim-directoryaction.md) abstract class manages directories.</span></span> <span data-ttu-id="3fe9c-297">La création de répertoires est gérée par la classe [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) et la suppression des répertoires est gérée par la classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-297">Directory creation is handled by the [**CIM\_CreateDirectoryAction**](cim-createdirectoryaction.md) class and directory removal is handled by the [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-298">**\_DIRECTORYCONTAINSFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-298">**CIM\_DirectoryContainsFile**</span></span>](cim-directorycontainsfile.md)
</dt> <dd>

<span data-ttu-id="3fe9c-299">La classe [**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) représente une association entre un répertoire et des fichiers contenus dans ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-299">The [**CIM\_DirectoryContainsFile**](cim-directorycontainsfile.md) class represents an association between a directory and files contained within that directory.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-300">**\_DIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-300">**CIM\_DirectorySpecification**</span></span>](cim-directoryspecification.md)
</dt> <dd>

<span data-ttu-id="3fe9c-301">La classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) capture la principale structure de répertoires d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-301">The [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class captures the major directory structure of a software element.</span></span> <span data-ttu-id="3fe9c-302">Cette classe est utilisée pour organiser les fichiers d’un élément logiciel en unités gérables qui peuvent être déplacées sur un système informatique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-302">This class is used to organize the files of a software element into manageable units that can be relocated on a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-303">**\_DIRECTORYSPECIFICATIONFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-303">**CIM\_DirectorySpecificationFile**</span></span>](cim-directoryspecificationfile.md)
</dt> <dd>

<span data-ttu-id="3fe9c-304">L’Association [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) représente le répertoire qui contient le fichier spécifié en référençant la classe [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-304">The [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-305">**\_DISCRETESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-305">**CIM\_DiscreteSensor**</span></span>](cim-discretesensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-306">La classe [**CIM \_ DiscreteSensor**](cim-discretesensor.md) possède un ensemble de valeurs de chaîne valides qu’elle peut signaler.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-306">The [**CIM\_DiscreteSensor**](cim-discretesensor.md) class has a set of legal string values that it can report.</span></span> <span data-ttu-id="3fe9c-307">Les valeurs sont énumérées dans la propriété **PossibleValues** du capteur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-307">The values are enumerated in the sensor's **PossibleValues** property.</span></span> <span data-ttu-id="3fe9c-308">Un capteur discret a toujours une lecture actuelle qui correspond à l’une des valeurs énumérées.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-308">A discrete sensor always has a current reading that corresponds to one of the enumerated values.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-309">**\_DISKDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-309">**CIM\_DiskDrive**</span></span>](cim-diskdrive.md)
</dt> <dd>

<span data-ttu-id="3fe9c-310">La classe [**CIM \_ DiskDrive**](cim-diskdrive.md) représente un lecteur de disque physique tel qu’il est vu par le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-310">The [**CIM\_DiskDrive**](cim-diskdrive.md) class represents a physical disk drive as seen by the operating system.</span></span> <span data-ttu-id="3fe9c-311">Les fonctionnalités du lecteur de disque correspondent aux caractéristiques logiques et de gestion du lecteur, et dans certains cas, peuvent ne pas refléter les caractéristiques physiques de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-311">The disk drive features correspond to the logical and management characteristics of the drive, and in some cases, may not reflect the physical characteristics of the device.</span></span> <span data-ttu-id="3fe9c-312">Une interface vers un lecteur physique est un membre de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-312">An interface to a physical drive is a member of this class.</span></span> <span data-ttu-id="3fe9c-313">Toutefois, un objet basé sur un autre périphérique logique n’est pas un membre de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-313">However, an object based on another logical device is not a member of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-314">**\_DISKETTEDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-314">**CIM\_DisketteDrive**</span></span>](cim-diskettedrive.md)
</dt> <dd>

<span data-ttu-id="3fe9c-315">La classe [**CIM \_ DisketteDrive**](cim-diskettedrive.md) représente les fonctionnalités et la gestion d’un lecteur de disquette.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-315">The [**CIM\_DisketteDrive**](cim-diskettedrive.md) class represents the capabilities and management of a diskette drive.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-316">**\_DISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-316">**CIM\_DiskPartition**</span></span>](cim-diskpartition.md)
</dt> <dd>

<span data-ttu-id="3fe9c-317">La classe [**CIM \_ DiskPartition**](cim-diskpartition.md) représente une plage contiguë de blocs logiques qui est identifiable par le système d’exploitation par le biais des champs type et sous-type de la partition.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-317">The [**CIM\_DiskPartition**](cim-diskpartition.md) class represents a contiguous range of logical blocks that is identifiable by the operating system by way of the partition's type and subtype fields.</span></span> <span data-ttu-id="3fe9c-318">Les partitions de disque doivent être réalisées directement par le support physique (indiqué par l’Association [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) ) ou par les volumes de stockage.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-318">Disk partitions should be directly realized by physical media (indicated by the [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) association) or built on storage volumes.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-319">**\_DISKSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-319">**CIM\_DiskSpaceCheck**</span></span>](cim-diskspacecheck.md)
</dt> <dd>

<span data-ttu-id="3fe9c-320">La classe [**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) vérifie la quantité d’espace disque disponible du système et la spécifie dans la propriété **AvailableDiskSpace** .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-320">The [**CIM\_DiskSpaceCheck**](cim-diskspacecheck.md) class checks the system's amount of available disk space and specifies it in the **AvailableDiskSpace** property.</span></span> <span data-ttu-id="3fe9c-321">Les détails sont comparés à la valeur de la propriété **AvailableSpace** de l’objet [**CIM \_ FileSystem**](cim-filesystem.md) associé à l' [**objet \_ ComputerSystem CIM**](cim-computersystem.md) , qui décrit l’environnement système.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-321">Details are compared with the value in the **AvailableSpace** property of the [**CIM\_FileSystem**](cim-filesystem.md) object that is associated with the [**CIM\_ComputerSystem**](cim-computersystem.md) object, which describes the system environment.</span></span> <span data-ttu-id="3fe9c-322">Lorsque la valeur de la propriété **AvailableSpace** est supérieure ou égale à la valeur spécifiée dans la propriété **AvailableDiskSpace** , la condition est satisfaite.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-322">When the value of the **AvailableSpace** property is greater than or equal to the value specified in the **AvailableDiskSpace** property, the condition is satisfied.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-323">**\_Affichage CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-323">**CIM\_Display**</span></span>](cim-display.md)
</dt> <dd>

<span data-ttu-id="3fe9c-324">La classe d' [**\_ affichage CIM**](cim-display.md) est une classe parente permettant de regrouper divers périphériques d’affichage.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-324">The [**CIM\_Display**](cim-display.md) class is a parent class for grouping miscellaneous display devices.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-325">**\_DMA CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-325">**CIM\_DMA**</span></span>](cim-dma.md)
</dt> <dd>

<span data-ttu-id="3fe9c-326">La [**classe \_ DMA CIM**](cim-dma.md) représente l’accès direct à la mémoire (DMA) de l’architecture d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-326">The [**CIM\_DMA**](cim-dma.md) class represents computer architecture direct memory access (DMA).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-327">**\_Connexion CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-327">**CIM\_Docked**</span></span>](cim-docked.md)
</dt> <dd>

<span data-ttu-id="3fe9c-328">L’Association de la [**\_ station d’accueil CIM**](cim-docked.md) représente la relation entre deux châssis.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-328">The [**CIM\_Docked**](cim-docked.md) association represents the relationship between two chassis.</span></span> <span data-ttu-id="3fe9c-329">Par exemple, un ordinateur portable (un type de châssis) peut être ancré dans une station d’accueil (un autre type de châssis).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-329">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="3fe9c-330">Cette relation classique est décrite de manière explicite.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-330">This typical relationship is explicitly described.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-331">**\_ELEMENTCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-331">**CIM\_ElementCapacity**</span></span>](cim-elementcapacity.md)
</dt> <dd>

<span data-ttu-id="3fe9c-332">La classe [**CIM \_ ElementCapacity**](cim-elementcapacity.md) associe un objet [**\_ PhysicalCapacity CIM**](cim-physicalcapacity.md) à un ou plusieurs éléments physiques.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-332">The [**CIM\_ElementCapacity**](cim-elementcapacity.md) class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="3fe9c-333">Elle associe une description de la configuration matérielle minimale et maximale (ou des fonctionnalités) aux éléments physiques en cours de description.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-333">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-334">**\_ELEMENTCONFIGURATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-334">**CIM\_ElementConfiguration**</span></span>](cim-elementconfiguration.md)
</dt> <dd>

<span data-ttu-id="3fe9c-335">L’Association [**CIM \_ ElementConfiguration**](cim-elementconfiguration.md) associe un objet de [**\_ configuration CIM**](cim-configuration.md) à un ou plusieurs éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-335">The [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) association relates a [**CIM\_Configuration**](cim-configuration.md) object to one or more managed system elements.</span></span> <span data-ttu-id="3fe9c-336">L’objet de **\_ configuration CIM** représente un comportement spécifique ou un état fonctionnel souhaité pour le [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md)associé.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-336">The **CIM\_Configuration** object represents a certain behavior, or a desired functional state for the associated [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-337">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-337">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="3fe9c-338">La classe [**CIM \_ ElementSetting**](cim-elementsetting.md) représente l’association entre les éléments système gérés et la classe de paramètres définie pour eux.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-338">The [**CIM\_ElementSetting**](cim-elementsetting.md) class represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-339">**\_ELEMENTSLINKED CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-339">**CIM\_ElementsLinked**</span></span>](cim-elementslinked.md)
</dt> <dd>

<span data-ttu-id="3fe9c-340">L’Association [**CIM \_ ElementsLinked**](cim-elementslinked.md) représente des éléments physiques reliés par un lien physique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-340">The [**CIM\_ElementsLinked**](cim-elementslinked.md) association represents physical elements that are cabled together by a physical link.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-341">**\_ERRORCOUNTERSFORDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-341">**CIM\_ErrorCountersForDevice**</span></span>](cim-errorcountersfordevice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-342">La classe [**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md) associe la classe [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) à l’unité logique à laquelle elle s’applique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-342">The [**CIM\_ErrorCountersForDevice**](cim-errorcountersfordevice.md) class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-343">**\_EXECUTEPROGRAM CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-343">**CIM\_ExecuteProgram**</span></span>](cim-executeprogram.md)
</dt> <dd>

<span data-ttu-id="3fe9c-344">La classe [**CIM \_ ExecuteProgram**](cim-executeprogram.md) représente des fichiers qui peuvent être exécutés sur le système sur lequel l’élément logiciel est installé.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-344">The [**CIM\_ExecuteProgram**](cim-executeprogram.md) class represents files that can be executed on the system where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-345">**\_Exportation CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-345">**CIM\_Export**</span></span>](cim-export.md)
</dt> <dd>

<span data-ttu-id="3fe9c-346">La classe d' [**\_ exportation CIM**](cim-export.md) représente une association entre un système de fichiers local et ses répertoires, ce qui indique que les répertoires spécifiés sont disponibles pour le montage.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-346">The [**CIM\_Export**](cim-export.md) class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="3fe9c-347">Lorsque vous exportez un système de fichiers entier, le répertoire doit référencer le répertoire le plus haut du système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-347">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-348">**\_EXTRACAPACITYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-348">**CIM\_ExtraCapacityGroup**</span></span>](cim-extracapacitygroup.md)
</dt> <dd>

<span data-ttu-id="3fe9c-349">La classe [**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md) est dérivée d’un groupe de redondance qui indique que les éléments agrégés ont plus de capacité ou de capacité que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-349">The [**CIM\_ExtraCapacityGroup**](cim-extracapacitygroup.md) class is derived from a redundancy group that indicates the aggregated elements have more capacity or capability than is needed.</span></span> <span data-ttu-id="3fe9c-350">Voici un exemple de ce type de redondance : l’installation de N + 1 alimentations ou de ventilateurs dans un système.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-350">An example of this type of redundancy is the installation of N+1 power supplies or fans in a system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-351">**\_Ventilateur CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-351">**CIM\_Fan**</span></span>](cim-fan.md)
</dt> <dd>

<span data-ttu-id="3fe9c-352">La classe de [**\_ ventilateur CIM**](cim-fan.md) représente les fonctionnalités et la gestion d’un appareil de refroidissement de ventilateur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-352">The [**CIM\_Fan**](cim-fan.md) class represents the capabilities and management of a fan cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-353">**\_FILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-353">**CIM\_FileAction**</span></span>](cim-fileaction.md)
</dt> <dd>

<span data-ttu-id="3fe9c-354">La classe [**CIM \_ FileAction**](cim-fileaction.md) permet à l’auteur de localiser des fichiers qui existent déjà sur l’ordinateur d’un utilisateur, puis de déplacer ou de copier ces fichiers vers un nouvel emplacement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-354">The [**CIM\_FileAction**](cim-fileaction.md) class allows the author to locate files that already exist on a user's computer, and then move or copy those files to a new location.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-355">**\_FILESPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-355">**CIM\_FileSpecification**</span></span>](cim-filespecification.md)
</dt> <dd>

<span data-ttu-id="3fe9c-356">La classe [**CIM \_ FileSpecification**](cim-filespecification.md) représente un fichier qui se trouve sur le système ou en est déconnectée.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-356">The [**CIM\_FileSpecification**](cim-filespecification.md) class represents a file that is either on or off of the system.</span></span> <span data-ttu-id="3fe9c-357">Le fichier se trouve dans le répertoire identifié par l’Association [**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-357">The file is located in the directory identified by the [**CIM\_DirectorySpecificationFile**](cim-directoryspecificationfile.md) association.</span></span> <span data-ttu-id="3fe9c-358">La méthode [**Invoke**](invoke-method-in-class-cim-filespecification.md) utilise les informations pour vérifier l’existence du fichier.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-358">The [**Invoke**](invoke-method-in-class-cim-filespecification.md) method uses the information to check for the file's existence.</span></span> <span data-ttu-id="3fe9c-359">Notez que les propriétés avec une valeur **null** ne sont pas vérifiées.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-359">Note that properties with a **Null** value are not checked.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-360">**\_FILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-360">**CIM\_FileStorage**</span></span>](cim-filestorage.md)
</dt> <dd>

<span data-ttu-id="3fe9c-361">L’Association [**CIM \_ FileStorage**](cim-filestorage.md) lie le système de fichiers et les fichiers logiques adressés via le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-361">The [**CIM\_FileStorage**](cim-filestorage.md) association links the file system and the logical files addressed through the file system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-362">**\_Système de fichiers CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-362">**CIM\_FileSystem**</span></span>](cim-filesystem.md)
</dt> <dd>

<span data-ttu-id="3fe9c-363">La classe de système de [**\_ fichiers CIM**](cim-filesystem.md) représente un fichier ou un jeu de données local sur un système informatique ou monté à distance à partir d’un serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-363">The [**CIM\_FileSystem**](cim-filesystem.md) class represents a file or data set local to a computer system or remotely mounted from a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-364">**\_Plataux CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-364">**CIM\_FlatPanel**</span></span>](cim-flatpanel.md)
</dt> <dd>

<span data-ttu-id="3fe9c-365">La classe d’écran plat [**CIM \_**](cim-flatpanel.md) représente les fonctionnalités et la gestion de l’appareil logique à écran plat.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-365">The [**CIM\_FlatPanel**](cim-flatpanel.md) class represents the capabilities and management of the flat panel logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-366">**\_FROMDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-366">**CIM\_FromDirectoryAction**</span></span>](cim-fromdirectoryaction.md)
</dt> <dd>

<span data-ttu-id="3fe9c-367">L’Association [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) identifie le répertoire source de l’action de fichier.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-367">The [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="3fe9c-368">Lorsque cette association est utilisée, l’hypothèse est que le répertoire source a été créé par une action précédente.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-368">When this association is used, the assumption is that the source directory was created by a previous action.</span></span> <span data-ttu-id="3fe9c-369">Cette association ne peut pas exister avec une association [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) ; une action de fichier ne peut impliquer qu’un seul répertoire source.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-369">This association cannot exist with a [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-370">**\_FROMDIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-370">**CIM\_FromDirectorySpecification**</span></span>](cim-fromdirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="3fe9c-371">L’Association [**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) identifie le répertoire source de l’action de fichier.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-371">The [**CIM\_FromDirectorySpecification**](cim-fromdirectoryspecification.md) association identifies the source directory for the file action.</span></span> <span data-ttu-id="3fe9c-372">Lorsque cette association est utilisée, l’hypothèse est que le répertoire source existe déjà.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-372">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="3fe9c-373">Cette association ne peut pas exister avec une association [**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md) ; une action de fichier ne peut impliquer qu’un seul répertoire source.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-373">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-374">**\_FRU CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-374">**CIM\_FRU**</span></span>](cim-fru.md)
</dt> <dd>

<span data-ttu-id="3fe9c-375">La [**classe \_ FRU CIM**](cim-fru.md) représente une collection définie par le fournisseur de produits et d’éléments physiques associés à une unité remplaçable sur site (FRU) pour la prise en charge, la maintenance ou la mise à niveau d’un produit à l’emplacement du client.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-375">The [**CIM\_FRU**](cim-fru.md) class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-376">**\_FRUINCLUDESPRODUCT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-376">**CIM\_FRUIncludesProduct**</span></span>](cim-fruincludesproduct.md)
</dt> <dd>

<span data-ttu-id="3fe9c-377">La classe [**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md) indique qu’une unité remplaçable sur site (FRU) peut être composée d’autres produits.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-377">The [**CIM\_FRUIncludesProduct**](cim-fruincludesproduct.md) class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-378">**\_FRUPHYSICALELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-378">**CIM\_FRUPhysicalElements**</span></span>](cim-fruphysicalelements.md)
</dt> <dd>

<span data-ttu-id="3fe9c-379">La classe [**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md) représente les éléments physiques qui composent une unité remplaçable sur site (FRU).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-379">The [**CIM\_FRUPhysicalElements**](cim-fruphysicalelements.md) class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-380">**\_Heatpipe CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-380">**CIM\_HeatPipe**</span></span>](cim-heatpipe.md)
</dt> <dd>

<span data-ttu-id="3fe9c-381">La classe [**CIM \_ Heatpipe**](cim-heatpipe.md) représente les fonctionnalités et la gestion d’un appareil de refroidissement de tuyauterie thermique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-381">The [**CIM\_HeatPipe**](cim-heatpipe.md) class represents the capabilities and management of a heat pipe cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-382">**\_HOSTEDACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-382">**CIM\_HostedAccessPoint**</span></span>](cim-hostedaccesspoint.md)
</dt> <dd>

<span data-ttu-id="3fe9c-383">La classe [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md) représente une association entre un point d’accès de service (SAP) et le système sur lequel il est fourni.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-383">The [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md) class represents an association between a service access point (SAP) and the system on which it is provided.</span></span> <span data-ttu-id="3fe9c-384">Chaque système peut héberger de nombreuses SAP.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-384">Each system may host many SAPs.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-385">**\_HOSTEDBOOTSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-385">**CIM\_HostedBootSAP**</span></span>](cim-hostedbootsap.md)
</dt> <dd>

<span data-ttu-id="3fe9c-386">La classe [**CIM \_ HostedBootSAP**](cim-hostedbootsap.md) définit le système informatique unitaire d’hébergement pour une classe [**CIM \_ BootSAP**](cim-bootsap.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-386">The [**CIM\_HostedBootSAP**](cim-hostedbootsap.md) class defines the hosting unitary computer system for a [**CIM\_BootSAP**](cim-bootsap.md) class.</span></span> <span data-ttu-id="3fe9c-387">Étant donné que cette relation est sous-classée à partir de [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), elle hérite du schéma d’étendue/d’attribution de noms défini pour le [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md), où un point d’accès défère au système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-387">Since this relationship is subclassed from [**CIM\_HostedAccessPoint**](cim-hostedaccesspoint.md), it inherits the scoping/naming scheme defined for [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md), where an access point defers to its hosting system.</span></span> <span data-ttu-id="3fe9c-388">Dans ce cas, **le \_ BootSAP CIM** doit être différé à sa classe [**\_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-388">In this case, **CIM\_BootSAP** must defer to its hosting [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-389">**\_HOSTEDBOOTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-389">**CIM\_HostedBootService**</span></span>](cim-hostedbootservice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-390">La classe [**CIM \_ HostedBootService**](cim-hostedbootservice.md) associe un système d’hébergement et un service de démarrage.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-390">The [**CIM\_HostedBootService**](cim-hostedbootservice.md) class associates a hosting system and a boot service.</span></span> <span data-ttu-id="3fe9c-391">Étant donné que cette relation est sous-classée à partir de [**CIM \_ service hébergé**](cim-hostedservice.md), elle hérite du schéma d’étendue/d’attribution de noms défini pour le service, où un service s’en remet au système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-391">Since this relationship is subclassed from [**CIM\_HostedService**](cim-hostedservice.md), it inherits the scoping/naming scheme defined for service, where a service defers to its hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-392">**\_HOSTEDFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-392">**CIM\_HostedFileSystem**</span></span>](cim-hostedfilesystem.md)
</dt> <dd>

<span data-ttu-id="3fe9c-393">L’Association [**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md) représente un lien entre le système informatique et le système de fichiers hébergé sur le système informatique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-393">The [**CIM\_HostedFileSystem**](cim-hostedfilesystem.md) association represents a link between the computer system and the file system hosted on the computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-394">**\_HOSTEDJOBDESTINATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-394">**CIM\_HostedJobDestination**</span></span>](cim-hostedjobdestination.md)
</dt> <dd>

<span data-ttu-id="3fe9c-395">La classe [**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md) représente une association entre une destination de travail et le système sur lequel elle réside.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-395">The [**CIM\_HostedJobDestination**](cim-hostedjobdestination.md) class represents an association between a job destination and the system on which it resides.</span></span> <span data-ttu-id="3fe9c-396">Un système peut héberger de nombreuses files d’attente de travaux.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-396">A system may host many job queues.</span></span> <span data-ttu-id="3fe9c-397">Les destinations du travail diffèrent au système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-397">Job destinations defer to the hosting system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-398">**\_Service hébergé CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-398">**CIM\_HostedService**</span></span>](cim-hostedservice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-399">La classe [**CIM \_ service hébergé**](cim-hostedservice.md) représente une association entre un service et le système sur lequel la fonctionnalité réside.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-399">The [**CIM\_HostedService**](cim-hostedservice.md) class represents an association between a service and the system on which the functionality resides.</span></span> <span data-ttu-id="3fe9c-400">Un système peut héberger de nombreux services, qui retardent le système d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-400">A system may host many services, which defer to the hosting system.</span></span> <span data-ttu-id="3fe9c-401">Le modèle ne représente pas les services hébergés sur plusieurs systèmes.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-401">The model does not represent services hosted across multiple systems.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-402">**\_INFRAREDCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-402">**CIM\_InfraredController**</span></span>](cim-infraredcontroller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-403">La classe [**CIM \_ InfraredController**](cim-infraredcontroller.md) représente les fonctionnalités et la gestion d’un contrôleur infrarouge.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-403">The [**CIM\_InfraredController**](cim-infraredcontroller.md) class represents the capabilities and management of an infrared controller.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-404">**CIM \_ installé**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-404">**CIM\_InstalledOS**</span></span>](cim-installedos.md)
</dt> <dd>

<span data-ttu-id="3fe9c-405">La classe d’association [**CIM \_ installos**](cim-installedos.md) représente un lien entre le système de l’ordinateur et le système d’exploitation installé.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-405">The [**CIM\_InstalledOS**](cim-installedos.md) association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="3fe9c-406">Un système d’exploitation est installé lorsqu’il se trouve dans l’extension de stockage d’un système d’ordinateur (par exemple, copié sur un lecteur de disque ou téléchargé en mémoire).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-406">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-407">**\_INSTALLEDSOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-407">**CIM\_InstalledSoftwareElement**</span></span>](cim-installedsoftwareelement.md)
</dt> <dd>

<span data-ttu-id="3fe9c-408">La classe [**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md) associe un système informatique à un élément logiciel installé.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-408">The [**CIM\_InstalledSoftwareElement**](cim-installedsoftwareelement.md) class associates a computer system with an installed software element.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-409">**\_IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-409">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dd>

<span data-ttu-id="3fe9c-410">La classe d' [**\_ IRQ CIM**](cim-irq.md) représente une ligne de demande d’interruption (IRQ) d’architecture Intel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-410">The [**CIM\_IRQ**](cim-irq.md) class represents an Intel architecture interrupt request line (IRQ).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-411">**\_Travail CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-411">**CIM\_Job**</span></span>](cim-job.md)
</dt> <dd>

<span data-ttu-id="3fe9c-412">La classe de [**\_ tâche CIM**](cim-job.md) représente une unité de travail pour un système, par exemple un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-412">The [**CIM\_Job**](cim-job.md) class represents a unit of work for a system, such as a print job.</span></span> <span data-ttu-id="3fe9c-413">Un travail est différent d’un processus, car un travail peut être planifié.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-413">A job is distinct from a process because a job can be scheduled.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-414">**\_JOBDESTINATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-414">**CIM\_JobDestination**</span></span>](cim-jobdestination.md)
</dt> <dd>

<span data-ttu-id="3fe9c-415">La classe [**CIM \_ JobDestination**](cim-jobdestination.md) représente l’emplacement où un travail est soumis pour traitement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-415">The [**CIM\_JobDestination**](cim-jobdestination.md) class represents where a job is submitted for processing.</span></span> <span data-ttu-id="3fe9c-416">Il peut faire référence à une file d’attente qui contient zéro travail ou plus, tel qu’une file d’attente à l’impression contenant des travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-416">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="3fe9c-417">Les destinations des travaux sont hébergées sur des systèmes, de la même façon que les services sont hébergés sur les systèmes.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-417">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-418">**\_JOBDESTINATIONJOBS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-418">**CIM\_JobDestinationJobs**</span></span>](cim-jobdestinationjobs.md)
</dt> <dd>

<span data-ttu-id="3fe9c-419">L’Association [**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md) décrit l’endroit où un travail est soumis pour traitement (c’est-à-dire la destination du travail).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-419">The [**CIM\_JobDestinationJobs**](cim-jobdestinationjobs.md) association describes where a job is submitted for processing (that is, to which job destination).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-420">**\_Clavier CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-420">**CIM\_Keyboard**</span></span>](cim-keyboard.md)
</dt> <dd>

<span data-ttu-id="3fe9c-421">La classe de [**\_ clavier CIM**](cim-keyboard.md) représente les fonctionnalités et la gestion du périphérique logique du clavier.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-421">The [**CIM\_Keyboard**](cim-keyboard.md) class represents the capabilities and management of the keyboard logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-422">**\_LINKHASCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-422">**CIM\_LinkHasConnector**</span></span>](cim-linkhasconnector.md)
</dt> <dd>

<span data-ttu-id="3fe9c-423">La classe [**CIM \_ LinkHasConnector**](cim-linkhasconnector.md) associe les câbles et les liens utilisés comme connecteurs physiques, qui connectent les éléments physiques.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-423">The [**CIM\_LinkHasConnector**](cim-linkhasconnector.md) class associates cables and links used as physical connectors, which connect the physical elements.</span></span> <span data-ttu-id="3fe9c-424">Cette association définit explicitement la relation des connecteurs pour [**les \_ PhysicalLink CIM**](cim-physicallink.md).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-424">This association explicitly defines the relationship of connectors for [**CIM\_PhysicalLink**](cim-physicallink.md).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-425">**\_LOCALFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-425">**CIM\_LocalFileSystem**</span></span>](cim-localfilesystem.md)
</dt> <dd>

<span data-ttu-id="3fe9c-426">La classe [**CIM \_ LocalFileSystem**](cim-localfilesystem.md) représente le magasin de fichiers contrôlé par un système informatique par le biais de moyens locaux (par exemple, accès direct au pilote de l’appareil).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-426">The [**CIM\_LocalFileSystem**](cim-localfilesystem.md) class represents the file store controlled by a computer system through local means (for example, direct device-driver access).</span></span> <span data-ttu-id="3fe9c-427">Le magasin de fichiers peut être géré directement par le système informatique, sans qu’un autre ordinateur n’ait besoin d’agir en tant que serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-427">The file store can be managed directly by the computer system, without the need for another computer to act as a file server.</span></span> <span data-ttu-id="3fe9c-428">Dans le cas d’un système de fichiers en cluster, toutefois, le système de fichiers est local et, par conséquent, diffère du cluster.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-428">For a clustered file system, however, the file system is local and, therefore, defers to the cluster.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-429">**\_Emplacement CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-429">**CIM\_Location**</span></span>](cim-location.md)
</dt> <dd>

<span data-ttu-id="3fe9c-430">La classe d' [**\_ emplacement CIM**](cim-location.md) représente la position et l’adresse d’un élément physique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-430">The [**CIM\_Location**](cim-location.md) class represents the position and address of a physical element.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-431">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-431">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-432">La classe [**CIM \_ LogicalDevice**](cim-logicaldevice.md) représente une entité matérielle qui peut ou ne peut pas être réalisée sur du matériel physique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-432">The [**CIM\_LogicalDevice**](cim-logicaldevice.md) class represents a hardware entity that may or may not be realized in physical hardware.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-433">**\_Disque logique CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-433">**CIM\_LogicalDisk**</span></span>](cim-logicaldisk.md)
</dt> <dd>

<span data-ttu-id="3fe9c-434">La [**classe \_ LogicalDisk CIM**](cim-logicaldisk.md) représente une plage contiguë de blocs logiques qui est identifiable par un système de fichiers par le biais du champ **DeviceID** (Key) du disque.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-434">The [**CIM\_LogicalDisk**](cim-logicaldisk.md) class represents a contiguous range of logical blocks that is identifiable by a file system through the disk's **DeviceID** (key) field.</span></span> <span data-ttu-id="3fe9c-435">Par exemple, dans un environnement Windows, le champ **DeviceID** contient une lettre de lecteur. dans un environnement UNIX, elle contient le chemin d’accès ; dans un environnement NetWare, il contient le nom du volume.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-435">For example, in a Windows environment, the **DeviceID** field contains a drive letter; in a UNIX environment, it contains the access path; and in a NetWare environment, it contains the volume name.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-436">**\_LOGICALDISKBASEDONPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-436">**CIM\_LogicalDiskBasedOnPartition**</span></span>](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

<span data-ttu-id="3fe9c-437">La classe [**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) associe un disque logique à la partition de disque sur laquelle il réside.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-437">The [**CIM\_LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) class associates a logical disk with the disk partition on which it resides.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-438">**\_LOGICALDISKBASEDONVOLUMESET CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-438">**CIM\_LogicalDiskBasedOnVolumeSet**</span></span>](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

<span data-ttu-id="3fe9c-439">L’Association [**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) associe les disques logiques au volume sur lequel ils sont trouvés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-439">The [**CIM\_LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) association relates logical disks with the volume on which they are found.</span></span> <span data-ttu-id="3fe9c-440">Les disques logiques peuvent être basés sur un volume unique (par exemple, exposé par un gestionnaire de volume logiciel) ou sur une partition de disque.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-440">Logical disks can be based on a single volume (for example, exposed by a software volume manager) or a disk partition.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-441">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-441">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="3fe9c-442">La classe [**CIM \_ LogicalElement**](cim-logicalelement.md) est la classe de base pour tous les composants système qui représentent des composants système abstraits, tels que des profils, des processus ou des fonctionnalités système, sous la forme d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-442">The [**CIM\_LogicalElement**](cim-logicalelement.md) class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-443">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-443">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> <dd>

<span data-ttu-id="3fe9c-444">La classe [**CIM \_ LogicalFile**](cim-logicalfile.md) représente une collection nommée de données, qui peut être du code exécutable, qui se trouve dans un système de fichiers sur une extension de stockage.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-444">The [**CIM\_LogicalFile**](cim-logicalfile.md) class represents a named collection of data, which can be executable code, that is located in a file system on a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-445">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-445">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dd>

<span data-ttu-id="3fe9c-446">La [**classe \_ LogicalIdentity CIM**](cim-logicalidentity.md) est une association abstraite et générique qui indique que deux éléments logiques représentent différents aspects de la même entité sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-446">The [**CIM\_LogicalIdentity**](cim-logicalidentity.md) class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-447">**\_MAGNETOOPTICALDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-447">**CIM\_MagnetoOpticalDrive**</span></span>](cim-magnetoopticaldrive.md)
</dt> <dd>

<span data-ttu-id="3fe9c-448">La classe [**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) représente les fonctionnalités et la gestion d’un lecteur magnéto-optique, un sous-type de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-448">The [**CIM\_MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) class represents the capabilities and management of a magneto-optical drive, a subtype of the media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-449">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-449">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="3fe9c-450">La [**classe \_ ManagedSystemElement CIM**](cim-managedsystemelement.md) est la classe de base pour la hiérarchie des éléments système.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-450">The [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="3fe9c-451">Tout composant système distinctif est un candidat pour l’inclusion dans cette classe.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-451">Any distinguishable system component is a candidate for inclusion in this class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-452">**\_MANAGEMENTCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-452">**CIM\_ManagementController**</span></span>](cim-managementcontroller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-453">La classe [**CIM \_ ManagementController**](cim-managementcontroller.md) est associée aux fonctionnalités et à la gestion d’un contrôleur de gestion.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-453">The [**CIM\_ManagementController**](cim-managementcontroller.md) class relates to the capabilities and management of a management controller.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-454">**\_MEDIAACCESSDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-454">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-455">La classe [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) représente la possibilité d’accéder à un ou plusieurs médias, puis d’utiliser le média pour stocker et récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-455">The [**CIM\_MediaAccessDevice**](cim-mediaaccessdevice.md) class represents the ability to access one or more media, and then use the media to store and retrieve data.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-456">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-456">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-457">L’Association [**CIM \_ MediaPresent**](cim-mediapresent.md) décrit une relation dans laquelle une extension de stockage doit être accessible via un appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-457">The [**CIM\_MediaPresent**](cim-mediapresent.md) association describes a relationship where a storage extent must be accessed through a media access device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-458">**\_Mémoire CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-458">**CIM\_Memory**</span></span>](cim-memory.md)
</dt> <dd>

<span data-ttu-id="3fe9c-459">La classe de [**\_ mémoire CIM**](cim-memory.md) représente les fonctionnalités et la gestion des périphériques logiques liés à la mémoire.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-459">The [**CIM\_Memory**](cim-memory.md) class represents the capabilities and management of memory-related logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-460">**\_MEMORYCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-460">**CIM\_MemoryCapacity**</span></span>](cim-memorycapacity.md)
</dt> <dd>

<span data-ttu-id="3fe9c-461">La classe [**CIM \_ MemoryCapacity**](cim-memorycapacity.md) représente la mémoire qui peut être installée sur un élément physique et ses configurations minimale et maximale.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-461">The [**CIM\_MemoryCapacity**](cim-memorycapacity.md) class represents memory that can be installed on a physical element and its minimum and maximum configurations.</span></span> <span data-ttu-id="3fe9c-462">Les informations sur la mémoire qui est actuellement installée et les exigences minimales et maximales d’un élément se trouvent dans les instances de la classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-462">Information on memory that is currently installed and an element's minimum and maximum requirements is located in instances of the [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-463">**\_MEMORYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-463">**CIM\_MemoryCheck**</span></span>](cim-memorycheck.md)
</dt> <dd>

<span data-ttu-id="3fe9c-464">La classe [**CIM \_ MemoryCheck**](cim-memorycheck.md) spécifie une condition pour la quantité minimale de mémoire qui doit être disponible sur un système.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-464">The [**CIM\_MemoryCheck**](cim-memorycheck.md) class specifies a condition for the minimum amount of memory that must be available on a system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-465">**\_MEMORYMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-465">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dd>

<span data-ttu-id="3fe9c-466">La classe [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md) représente l’architecture d’ordinateur des e/s mappées en mémoire.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-466">The [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="3fe9c-467">Cette classe résout les ressources de mémoire et d’e/s de port.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-467">This class addresses memory and port I/O resources.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-468">**\_MEMORYONCARD CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-468">**CIM\_MemoryOnCard**</span></span>](cim-memoryoncard.md)
</dt> <dd>

<span data-ttu-id="3fe9c-469">La classe [**CIM \_ MemoryOnCard**](cim-memoryoncard.md) associe la mémoire physique située sur les cartes d’hébergement, les cartes d’adaptateur, etc.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-469">The [**CIM\_MemoryOnCard**](cim-memoryoncard.md) class associates physical memory located on hosting boards, adapter cards, and so on.</span></span> <span data-ttu-id="3fe9c-470">Cette association définit explicitement la relation entre la mémoire et les cartes.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-470">This association explicitly defines the relationship of memory to cards.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-471">**\_MEMORYWITHMEDIA CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-471">**CIM\_MemoryWithMedia**</span></span>](cim-memorywithmedia.md)
</dt> <dd>

<span data-ttu-id="3fe9c-472">La classe [**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md) associe la mémoire physique à un support physique et à sa cartouche.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-472">The [**CIM\_MemoryWithMedia**](cim-memorywithmedia.md) class associates physical memory with a physical media and its cartridge.</span></span> <span data-ttu-id="3fe9c-473">La mémoire fournit l’identification du média et stocke les données spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-473">The memory provides media identification and stores user-specific data.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-474">**\_MODIFYSETTINGACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-474">**CIM\_ModifySettingAction**</span></span>](cim-modifysettingaction.md)
</dt> <dd>

<span data-ttu-id="3fe9c-475">La classe [**CIM \_ ModifySettingAction**](cim-modifysettingaction.md) représente les informations pour la modification d’un fichier de paramètre spécifique, pour une entrée spécifique, avec une valeur spécifique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-475">The [**CIM\_ModifySettingAction**](cim-modifysettingaction.md) class represents the information for modifying a specific setting file, for a specific entry, with a specific value.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-476">**\_MONITORRESOLUTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-476">**CIM\_MonitorResolution**</span></span>](cim-monitorresolution.md)
</dt> <dd>

<span data-ttu-id="3fe9c-477">La classe [**CIM \_ MonitorResolution**](cim-monitorresolution.md) représente la relation entre les résolutions horizontales et verticales, ainsi que la fréquence d’actualisation et le mode d’analyse d’un moniteur d’ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-477">The [**CIM\_MonitorResolution**](cim-monitorresolution.md) class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="3fe9c-478">Les valeurs sont spécifiées dans l’objet de contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-478">Values are specified in the video controller object.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-479">**\_MONITORSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-479">**CIM\_MonitorSetting**</span></span>](cim-monitorsetting.md)
</dt> <dd>

<span data-ttu-id="3fe9c-480">La classe [**CIM \_ MonitorSetting**](cim-monitorsetting.md) associe la résolution du moniteur à l’analyseur de bureau à laquelle elle s’applique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-480">The [**CIM\_MonitorSetting**](cim-monitorsetting.md) class associates the monitor resolution with the desktop monitor to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-481">**\_Montage CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-481">**CIM\_Mount**</span></span>](cim-mount.md)
</dt> <dd>

<span data-ttu-id="3fe9c-482">La [**classe \_ Mount CIM**](cim-mount.md) représente une association entre un système de fichiers et un répertoire auquel elle est attachée.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-482">The [**CIM\_Mount**](cim-mount.md) class represents an association between a file system and a directory to which it is attached.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-483">**\_MULTISTATESENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-483">**CIM\_MultiStateSensor**</span></span>](cim-multistatesensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-484">La classe [**CIM \_ MultiStateSensor**](cim-multistatesensor.md) représente un jeu de capteurs binaires à plusieurs membres où chaque capteur binaire signale un résultat booléen.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-484">The [**CIM\_MultiStateSensor**](cim-multistatesensor.md) class represents a multi-member set of binary sensors where each binary sensor reports a Boolean result.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-485">**\_NETWORKADAPTER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-485">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dd>

<span data-ttu-id="3fe9c-486">La classe de la carte CIM est une classe abstraite qui définit les concepts généraux de matériel de mise en réseau (par exemple, une adresse permanente ou une vitesse de fonctionnement). [**\_**](cim-networkadapter.md)</span><span class="sxs-lookup"><span data-stu-id="3fe9c-486">The [**CIM\_NetworkAdapter**](cim-networkadapter.md) class is an abstract class that defines general networking hardware concepts (for example, permanent address or speed of operation).</span></span> <span data-ttu-id="3fe9c-487">Les informations sont transmises à l’aide de l’Association [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-487">The information is conveyed using the [**CIM\_DeviceSAPImplementation**](cim-devicesapimplementation.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-488">**\_NFS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-488">**CIM\_NFS**</span></span>](cim-nfs.md)
</dt> <dd>

<span data-ttu-id="3fe9c-489">La [**classe \_ NFS CIM**](cim-nfs.md) représente un système de fichiers distant monté, à l’aide du protocole NFS (Network File System), à partir d’un système informatique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-489">The [**CIM\_NFS**](cim-nfs.md) class represents a remote file system that is mounted, using the network file system (NFS) protocol, from a computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-490">**\_NONVOLATILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-490">**CIM\_NonVolatileStorage**</span></span>](cim-nonvolatilestorage.md)
</dt> <dd>

<span data-ttu-id="3fe9c-491">La classe [**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) représente les fonctionnalités et la gestion du stockage non volatile.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-491">The [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) class represents the capabilities and management of non-volatile storage.</span></span> <span data-ttu-id="3fe9c-492">La mémoire non volatile comprend en mode natif le stockage flash et ROM.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-492">Nonvolatile memory natively includes flash and ROM storage.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-493">**\_NUMERICSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-493">**CIM\_NumericSensor**</span></span>](cim-numericsensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-494">La classe [**CIM \_ NumericSensor**](cim-numericsensor.md) représente un capteur numérique qui retourne des lectures numériques et éventuellement prend en charge les paramètres de seuils.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-494">The [**CIM\_NumericSensor**](cim-numericsensor.md) class represents a numeric sensor that returns numeric readings and optionally supports thresholds settings.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-495">**\_OPERATINGSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-495">**CIM\_OperatingSystem**</span></span>](cim-operatingsystem.md)
</dt> <dd>

<span data-ttu-id="3fe9c-496">La classe [**CIM \_ OperatingSystem**](cim-operatingsystem.md) représente un système d’exploitation d’ordinateur, qui est constitué de logiciels et de microprogrammes permettant de rendre le matériel d’un système d’ordinateur utilisable.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-496">The [**CIM\_OperatingSystem**](cim-operatingsystem.md) class represents a computer operating system, which is made up of software and firmware that make a computer system's hardware usable.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-497">**\_OPERATINGSYSTEMSOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-497">**CIM\_OperatingSystemSoftwareFeature**</span></span>](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

<span data-ttu-id="3fe9c-498">La classe [**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) représente les fonctionnalités logicielles qui composent le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-498">The [**CIM\_OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) class represents the software features that make up the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-499">**\_OSPROCESS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-499">**CIM\_OSProcess**</span></span>](cim-osprocess.md)
</dt> <dd>

<span data-ttu-id="3fe9c-500">La classe [**CIM \_ OSProcess**](cim-osprocess.md) associe le système d’exploitation et un ou plusieurs processus en cours d’exécution dans le contexte du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-500">The [**CIM\_OSProcess**](cim-osprocess.md) class associates the operating system and one or more processes running in the context of the operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-501">**\_OSVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-501">**CIM\_OSVersionCheck**</span></span>](cim-osversioncheck.md)
</dt> <dd>

<span data-ttu-id="3fe9c-502">La classe [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) spécifie les versions du système d’exploitation qui peuvent prendre en charge un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-502">The [**CIM\_OSVersionCheck**](cim-osversioncheck.md) class specifies the versions of the operating system that can support a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-503">**\_PACKAGEALARM CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-503">**CIM\_PackageAlarm**</span></span>](cim-packagealarm.md)
</dt> <dd>

<span data-ttu-id="3fe9c-504">L’Association [**CIM \_ PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) représente la relation dans laquelle un appareil d’alarme est installé dans le cadre d’un package.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-504">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="3fe9c-505">L’installation indique des problèmes avec l’environnement du package : son état de sécurité ou son intégrité globale.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-505">The installation indicates issues with the package's environment—its security state or its overall health.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-506">**\_PACKAGECOOLING CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-506">**CIM\_PackageCooling**</span></span>](cim-packagecooling.md)
</dt> <dd>

<span data-ttu-id="3fe9c-507">L’Association [**CIM \_ PackageCooling**](cim-packagecooling.md) représente la relation dans laquelle un appareil de refroidissement est installé dans un package, tel qu’un châssis ou un rack, pour faciliter le refroidissement du package.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-507">The [**CIM\_PackageCooling**](cim-packagecooling.md) association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-508">**\_PACKAGEDCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-508">**CIM\_PackagedComponent**</span></span>](cim-packagedcomponent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-509">L’Association [**CIM \_ PackagedComponent**](cim-packagedcomponent.md) représente une relation explicite dans laquelle un composant est généralement contenu dans un package physique, tel qu’un châssis ou une carte.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-509">The [**CIM\_PackagedComponent**](cim-packagedcomponent.md) association represents an explicit relationship in which a component is typically contained by a physical package, such as a chassis or card.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-510">**\_PACKAGEINCHASSIS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-510">**CIM\_PackageInChassis**</span></span>](cim-packageinchassis.md)
</dt> <dd>

<span data-ttu-id="3fe9c-511">L’Association [**CIM \_ PackageInChassis**](cim-packageinchassis.md) représente la relation dans laquelle un châssis peut contenir d’autres packages, tels que d’autres châssis et cartes.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-511">The [**CIM\_PackageInChassis**](cim-packageinchassis.md) association represents the relationship in which a chassis can contain other packages, such as other chassis and cards.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-512">**\_PACKAGEINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-512">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> <dd>

<span data-ttu-id="3fe9c-513">L’Association [**CIM \_ PackageInSlot**](cim-packageinslot.md) représente la relation entre les cartes d’appareil et le châssis dans lequel elles sont montées.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-513">The [**CIM\_PackageInSlot**](cim-packageinslot.md) association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-514">**\_PACKAGETEMPSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-514">**CIM\_PackageTempSensor**</span></span>](cim-packagetempsensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-515">L’Association [**CIM \_ PackageTempSensor**](cim-packagetempsensor.md) représente la relation dans laquelle un capteur de température est souvent installé dans un package, tel qu’un châssis ou un rack, pour surveiller l’environnement du package.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-515">The [**CIM\_PackageTempSensor**](cim-packagetempsensor.md) association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-516">**\_PARALLELCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-516">**CIM\_ParallelController**</span></span>](cim-parallelcontroller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-517">L’Association [**CIM \_ ParallelController**](cim-parallelcontroller.md) se réfère aux fonctionnalités et à la gestion de l’unité logique de port parallèle.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-517">The [**CIM\_ParallelController**](cim-parallelcontroller.md) association relates to the capabilities and management of the parallel port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-518">**\_PARTICIPATESINSET CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-518">**CIM\_ParticipatesInSet**</span></span>](cim-participatesinset.md)
</dt> <dd>

<span data-ttu-id="3fe9c-519">La classe [**CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifie les éléments physiques qui doivent être remplacés ensemble.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-519">The [**CIM\_ParticipatesInSet**](cim-participatesinset.md) class identifies physical elements that should be replaced together.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-520">**\_PCICONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-520">**CIM\_PCIController**</span></span>](cim-pcicontroller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-521">La classe [**CIM \_ PCIController**](cim-pcicontroller.md) représente les propriétés et la gestion d’un contrôleur PCI.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-521">The [**CIM\_PCIController**](cim-pcicontroller.md) class represents the properties and management of a PCI controller.</span></span> <span data-ttu-id="3fe9c-522">Les propriétés de cette classe et de ses sous-classes sont définies dans les différentes spécifications PCI publiées par le SIG PCI.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-522">The properties in this class and its subclasses are defined in the various PCI specifications published by the PCI SIG.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-523">**\_PCMCIACONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-523">**CIM\_PCMCIAController**</span></span>](cim-pcmciacontroller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-524">La classe [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md) représente les fonctionnalités et la gestion d’un contrôleur PCMCIA (Personal Computer Memory Card International Association).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-524">The [**CIM\_PCMCIAController**](cim-pcmciacontroller.md) class represents the capabilities and management of a Personal Computer Memory Card International Association (PCMCIA) controller.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-525">**\_PCVIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-525">**CIM\_PCVideoController**</span></span>](cim-pcvideocontroller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-526">Le [**\_ PCVideoController CIM**](cim-pcvideocontroller.md) représente les fonctionnalités et la gestion d’un contrôleur vidéo d’ordinateur personnel, un sous-type d’un contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-526">The [**CIM\_PCVideoController**](cim-pcvideocontroller.md) represents the capabilities and management of a personal computer video controller, a subtype of a video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-527">**\_PEXTENTREDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-527">**CIM\_PExtentRedundancyComponent**</span></span>](cim-pextentredundancycomponent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-528">La classe [**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) représente les extensions physiques qui participent à un groupe de redondance de stockage.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-528">The [**CIM\_PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) class represents the physical extents that participate in a storage redundancy group.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-529">**\_PHYSICALCAPACITY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-529">**CIM\_PhysicalCapacity**</span></span>](cim-physicalcapacity.md)
</dt> <dd>

<span data-ttu-id="3fe9c-530">La [**classe \_ PhysicalCapacity CIM**](cim-physicalcapacity.md) est une classe abstraite qui représente les exigences minimales et maximales d’un élément physique, ainsi que sa capacité à prendre en charge différents types de matériel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-530">The [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="3fe9c-531">Par exemple, les exigences minimales et maximales en mémoire peuvent être modélisées en tant que sous-classe de **\_ PhysicalCapacity CIM**.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-531">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-532">**\_PHYSICALCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-532">**CIM\_PhysicalComponent**</span></span>](cim-physicalcomponent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-533">La classe [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md) représente un composant de base ou de bas niveau au sein d’un package.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-533">The [**CIM\_PhysicalComponent**](cim-physicalcomponent.md) class represents a low-level or basic component within a package.</span></span> <span data-ttu-id="3fe9c-534">Un élément physique qui n’est pas un lien, un connecteur ou un package est un descendant (ou membre) de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-534">A physical element that is not a link, connector, or package is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-535">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-535">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dd>

<span data-ttu-id="3fe9c-536">La classe [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) représente tout élément physique utilisé pour se connecter à d’autres éléments.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-536">The [**CIM\_PhysicalConnector**](cim-physicalconnector.md) class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="3fe9c-537">Tout objet qui peut se connecter et transmettre des signaux ou de la puissance entre deux ou plusieurs éléments physiques est un descendant (ou membre) de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-537">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-538">**\_PHYSICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-538">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> <dd>

<span data-ttu-id="3fe9c-539">Les sous-classes [**\_ PhysicalElement CIM**](cim-physicalelement.md) définissent tout composant d’un système qui a une identité physique distincte.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-539">The [**CIM\_PhysicalElement**](cim-physicalelement.md) subclasses define any component of a system that has a distinct physical identity.</span></span> <span data-ttu-id="3fe9c-540">Les instances de cette classe peuvent être définies en termes d’étiquettes qui peuvent être physiquement attachées à l’objet.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-540">Instances of this class can be defined in terms of labels that can be physically attached to the object.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-541">**\_PHYSICALELEMENTLOCATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-541">**CIM\_PhysicalElementLocation**</span></span>](cim-physicalelementlocation.md)
</dt> <dd>

<span data-ttu-id="3fe9c-542">La classe [**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md) associe un élément physique à un objet d' [**\_ emplacement CIM**](cim-location.md) à des fins d’inventaire ou de remplacement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-542">The [**CIM\_PhysicalElementLocation**](cim-physicalelementlocation.md) class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-543">**\_PHYSICALEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-543">**CIM\_PhysicalExtent**</span></span>](cim-physicalextent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-544">La classe [**CIM \_ PhysicalExtent**](cim-physicalextent.md) représente une implémentation RAID SCC.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-544">The [**CIM\_PhysicalExtent**](cim-physicalextent.md) class represents an SCC RAID implementation.</span></span> <span data-ttu-id="3fe9c-545">Il définit les adresses de bloc adressables consécutives sur un dispositif de stockage unique qui sont traitées comme une extension de stockage unique dans la même classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-545">It defines the consecutive addressable block addresses on a single storage device that are treated as a single storage extent in the same [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class.</span></span> <span data-ttu-id="3fe9c-546">Une alternative, lorsque la configuration automatique est utilisée, consiste à instancier ou étendre la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-546">An alternative, when automatic configuration is used, is to instantiate or extend the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-547">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-547">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> <dd>

<span data-ttu-id="3fe9c-548">La [**classe \_ PhysicalFrame CIM**](cim-physicalframe.md) est une classe parente de racks, de châssis et d’autres boîtiers de frames tels qu’ils sont définis dans les classes d’extension.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-548">The [**CIM\_PhysicalFrame**](cim-physicalframe.md) class is a parent class of rack, chassis, and other frame enclosures as they are defined in extension classes.</span></span> <span data-ttu-id="3fe9c-549">Les propriétés telles que **VisibleAlarm** et **AudibleAlarm**, ainsi que les données relatives aux violations de sécurité, sont incluses dans cette classe parente.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-549">Properties such as **VisibleAlarm** and **AudibleAlarm**, and data related to security breaches are included in this parent class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-550">**\_PHYSICALLINK CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-550">**CIM\_PhysicalLink**</span></span>](cim-physicallink.md)
</dt> <dd>

<span data-ttu-id="3fe9c-551">La classe [**CIM \_ PhysicalLink**](cim-physicallink.md) représente le câblage des éléments physiques.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-551">The [**CIM\_PhysicalLink**](cim-physicallink.md) class represents the cabling of physical elements.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-552">**\_PHYSICALMEDIA CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-552">**CIM\_PhysicalMedia**</span></span>](cim-physicalmedia.md)
</dt> <dd>

<span data-ttu-id="3fe9c-553">La classe [**CIM \_ PhysicalMedia**](cim-physicalmedia.md) représente les types de documentation et les supports de stockage, tels que les bandes, les CD-ROM, etc.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-553">The [**CIM\_PhysicalMedia**](cim-physicalmedia.md) class represents types of documentation and storage medium, such as tapes, CD ROMs, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-554">**\_PHYSICALMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-554">**CIM\_PhysicalMemory**</span></span>](cim-physicalmemory.md)
</dt> <dd>

<span data-ttu-id="3fe9c-555">La classe [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) représente des périphériques mémoire de bas niveau, tels que les SIMM, les DIMMs, les puces mémoire brutes, etc.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-555">The [**CIM\_PhysicalMemory**](cim-physicalmemory.md) class represents low-level memory devices, such as SIMMS, DIMMs, raw memory chips, and so on.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-556">**\_PHYSICALPACKAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-556">**CIM\_PhysicalPackage**</span></span>](cim-physicalpackage.md)
</dt> <dd>

<span data-ttu-id="3fe9c-557">La classe [**CIM \_ PhysicalPackage**](cim-physicalpackage.md) représente des éléments physiques qui contiennent ou hébergent d’autres composants.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-557">The [**CIM\_PhysicalPackage**](cim-physicalpackage.md) class represents physical elements that contain or host other components.</span></span> <span data-ttu-id="3fe9c-558">Il s’agit par exemple d’un boîtier en rack ou d’une carte adaptateur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-558">Examples are a rack enclosure or an adapter card.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-559">**\_POINTINGDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-559">**CIM\_PointingDevice**</span></span>](cim-pointingdevice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-560">La classe [**CIM \_ PointingDevice**](cim-pointingdevice.md) représente un appareil qui pointe vers des régions sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-560">The [**CIM\_PointingDevice**](cim-pointingdevice.md) class represents a device that points to regions on the display.</span></span> <span data-ttu-id="3fe9c-561">Tout appareil qui manipule un pointeur ou qui pointe vers des régions sur un affichage visuel, est un membre de cette classe.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-561">Any device that manipulates a pointer, or points to regions on a visual display, is a member of this class.</span></span> <span data-ttu-id="3fe9c-562">Par exemple, une souris, un stylet, un pavé tactile ou une tablette.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-562">For example, a mouse, stylus, touch pad, or tablet.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-563">**\_POTSMODEM CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-563">**CIM\_POTSModem**</span></span>](cim-potsmodem.md)
</dt> <dd>

<span data-ttu-id="3fe9c-564">La classe [**CIM \_ POTSModem**](cim-potsmodem.md) représente un appareil qui convertit les données binaires en modulations d’onde pour une transmission basée sur le son en se connectant au réseau pots (Plain Old Telephone System).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-564">The [**CIM\_POTSModem**](cim-potsmodem.md) class represents a device that translates binary data into wave modulations for sound-based transmission by connecting to the Plain Old Telephone System (POTS) network.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-565">**\_Alimentation CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-565">**CIM\_PowerSupply**</span></span>](cim-powersupply.md)
</dt> <dd>

<span data-ttu-id="3fe9c-566">La [**classe \_ d’alimentation CIM**](cim-powersupply.md) représente les fonctionnalités et la gestion de l’unité logique d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-566">The [**CIM\_PowerSupply**](cim-powersupply.md) class represents the capabilities and management of the power supply logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-567">**\_Imprimante CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-567">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dd>

<span data-ttu-id="3fe9c-568">La classe d' [**\_ imprimantes CIM**](cim-printer.md) représente les fonctionnalités et la gestion de l’unité logique d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-568">The [**CIM\_Printer**](cim-printer.md) class represents the capabilities and management of the printer logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-569">**\_Processus CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-569">**CIM\_Process**</span></span>](cim-process.md)
</dt> <dd>

<span data-ttu-id="3fe9c-570">La classe de [**\_ processus CIM**](cim-process.md) représente une instance unique d’un programme en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-570">The [**CIM\_Process**](cim-process.md) class represents a single instance of a running program.</span></span> <span data-ttu-id="3fe9c-571">Un utilisateur voit généralement un processus sous la forme d’une application ou d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-571">A user typically sees a process as an application or task.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-572">**\_PROCESSEXECUTABLE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-572">**CIM\_ProcessExecutable**</span></span>](cim-processexecutable.md)
</dt> <dd>

<span data-ttu-id="3fe9c-573">La classe [**CIM \_ ProcessExecutable**](cim-processexecutable.md) représente un lien entre un processus et un fichier de données, et indique que le fichier participe à l’exécution du processus.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-573">The [**CIM\_ProcessExecutable**](cim-processexecutable.md) class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-574">**\_Processeur CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-574">**CIM\_Processor**</span></span>](cim-processor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-575">La classe du [**\_ processeur CIM**](cim-processor.md) représente les fonctionnalités et la gestion du périphérique logique du processeur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-575">The [**CIM\_Processor**](cim-processor.md) class represents the capabilities and management of the processor logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-576">**\_PROCESSTHREAD CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-576">**CIM\_ProcessThread**</span></span>](cim-processthread.md)
</dt> <dd>

<span data-ttu-id="3fe9c-577">La classe [**CIM \_ ProcessThread**](cim-processthread.md) représente un lien entre un processus et les threads qui s’exécutent dans le contexte du processus.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-577">The [**CIM\_ProcessThread**](cim-processthread.md) class represents a link between a process and the threads running in the context of the process.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-578">**\_Produit CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-578">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dd>

<span data-ttu-id="3fe9c-579">La classe de [**\_ produit CIM**](cim-product.md) est une classe concrète qui représente une collection d’éléments physiques, de fonctionnalités logicielles et d’autres produits acquis en tant qu’unité.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-579">The [**CIM\_Product**](cim-product.md) class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="3fe9c-580">L’acquisition implique un accord entre le fournisseur et le consommateur, qui peut avoir des implications sur la licence, le support et la garantie du produit.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-580">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-581">**\_PRODUCTFRU CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-581">**CIM\_ProductFRU**</span></span>](cim-productfru.md)
</dt> <dd>

<span data-ttu-id="3fe9c-582">La classe [**CIM \_ ProductFRU**](cim-productfru.md) représente une association entre le produit et une unité remplaçable sur site (FRU), qui fournit des informations sur les composants du produit qui ont été ou sont remplacés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-582">The [**CIM\_ProductFRU**](cim-productfru.md) class represents an association between the product and a field replaceable unit (FRU), which provides information about product components that have been, or are being replaced.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-583">**\_PRODUCTPARENTCHILD CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-583">**CIM\_ProductParentChild**</span></span>](cim-productparentchild.md)
</dt> <dd>

<span data-ttu-id="3fe9c-584">L’Association [**CIM \_ ProductParentChild**](cim-productparentchild.md) définit une hiérarchie parent-enfant parmi les produits.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-584">The [**CIM\_ProductParentChild**](cim-productparentchild.md) association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="3fe9c-585">Par exemple, un produit peut être fourni avec d’autres produits.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-585">For example, a product can come bundled with other products.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-586">**\_PRODUCTPHYSICALELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-586">**CIM\_ProductPhysicalElements**</span></span>](cim-productphysicalelements.md)
</dt> <dd>

<span data-ttu-id="3fe9c-587">La classe [**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md) représente les éléments physiques qui composent un produit.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-587">The [**CIM\_ProductPhysicalElements**](cim-productphysicalelements.md) class represents the physical elements that make up a product.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-588">**\_PRODUCTPRODUCTDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-588">**CIM\_ProductProductDependency**</span></span>](cim-productproductdependency.md)
</dt> <dd>

<span data-ttu-id="3fe9c-589">La [**classe \_ ProductProductDependency CIM**](cim-productproductdependency.md) représente une association entre deux produits, ce qui indique qu’un doit être installé ou absent pour que l’autre fonctionne.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-589">The [**CIM\_ProductProductDependency**](cim-productproductdependency.md) class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="3fe9c-590">Il s’agit d’un concept équivalent à l’Association [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe9c-590">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-591">**\_PRODUCTSOFTWAREFEATURES CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-591">**CIM\_ProductSoftwareFeatures**</span></span>](cim-productsoftwarefeatures.md)
</dt> <dd>

<span data-ttu-id="3fe9c-592">L’Association [**CIM \_ ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) identifie les fonctionnalités logicielles pour un produit particulier.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-592">The [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association identifies the software features for a particular product.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-593">**\_PRODUCTSUPPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-593">**CIM\_ProductSupport**</span></span>](cim-productsupport.md)
</dt> <dd>

<span data-ttu-id="3fe9c-594">La classe [**CIM \_ ProductSupport**](cim-productsupport.md) représente une association entre le produit et l’accès au support qui indique comment le support est obtenu pour le produit.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-594">The [**CIM\_ProductSupport**](cim-productsupport.md) class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="3fe9c-595">Différents types de support sont disponibles pour un produit. le même objet de support peut fournir une assistance pour plusieurs produits.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-595">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-596">**\_PROTECTEDSPACEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-596">**CIM\_ProtectedSpaceExtent**</span></span>](cim-protectedspaceextent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-597">La classe [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) représente des adresses de blocs logiques adressables, qui sont traitées comme une extension de stockage unique, mais qui se trouvent sur une seule extension physique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-597">The [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) class represents addressable logical-block addresses, which are treated as a single storage extent, but are located on a single physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-598">**\_PSEXTENTBASEDONPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-598">**CIM\_PSExtentBasedOnPExtent**</span></span>](cim-psextentbasedonpextent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-599">La [**classe \_ PSExtentBasedOnPExtent CIM**](cim-psextentbasedonpextent.md) associe des extensions d’espace protégé basées sur une extension physique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-599">The [**CIM\_PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) class associates protected space extents that are based on a physical extent.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-600">**\_Rack CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-600">**CIM\_Rack**</span></span>](cim-rack.md)
</dt> <dd>

<span data-ttu-id="3fe9c-601">La classe de [**\_ rack CIM**](cim-rack.md) représente un rack (cadre physique ou boîtier) dans lequel les châssis sont stockés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-601">The [**CIM\_Rack**](cim-rack.md) class represents a rack (a physical frame or enclosure) in which chassis are stored.</span></span> <span data-ttu-id="3fe9c-602">En règle générale, un rack représente le boîtier. tous les composants fonctionnels sont empaquetés dans le châssis.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-602">Typically, a rack represents the enclosure; all functioning components are packaged in the chassis.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-603">**CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-603">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dd>

<span data-ttu-id="3fe9c-604">La classe [**CIM \_ réalise**](cim-realizes.md) la représentation de l’Association qui définit le mappage entre un périphérique logique et le composant physique qui implémente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-604">The [**CIM\_Realizes**](cim-realizes.md) class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-605">**\_REALIZESAGGREGATEPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-605">**CIM\_RealizesAggregatePExtent**</span></span>](cim-realizesaggregatepextent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-606">L’Association [**CIM \_ RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) représente la relation dans laquelle la classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) est réalisée sur un support physique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-606">The [**CIM\_RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-607">**\_REALIZESDISKPARTITION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-607">**CIM\_RealizesDiskPartition**</span></span>](cim-realizesdiskpartition.md)
</dt> <dd>

<span data-ttu-id="3fe9c-608">La classe [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) représente une partition de disque sur un support physique qui modélise la création de partitions sur un disque SCSI ou IDE brut.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-608">The [**CIM\_RealizesDiskPartition**](cim-realizesdiskpartition.md) class represents a disk partition on a physical media that models the creation of partitions on a raw SCSI or IDE drive.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-609">**\_REALIZESPEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-609">**CIM\_RealizesPExtent**</span></span>](cim-realizespextent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-610">L’Association [**CIM \_ RealizesPExtent**](cim-realizespextent.md) représente la relation dans laquelle les extensions physiques sont réalisées sur un support physique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-610">The [**CIM\_RealizesPExtent**](cim-realizespextent.md) association represents the relationship in which physical extents are realized on a physical media.</span></span> <span data-ttu-id="3fe9c-611">En outre, l’adresse de début de l’étendue physique sur le support physique est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-611">In addition, the starting address of the physical extent on the physical media is specified.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-612">**\_REBOOTACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-612">**CIM\_RebootAction**</span></span>](cim-rebootaction.md)
</dt> <dd>

<span data-ttu-id="3fe9c-613">La classe [**CIM \_ rebootaction**](cim-rebootaction.md) provoque un redémarrage du système à l’emplacement où l’élément logiciel est installé.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-613">The [**CIM\_RebootAction**](cim-rebootaction.md) class causes a system reboot where the software element is installed.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-614">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-614">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-615">La classe [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) associe un groupe de redondance composé d’éléments système gérés et indique que, ensemble, les éléments assurent la redondance.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-615">The [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="3fe9c-616">Tous les éléments agrégés dans un groupe de redondance doivent être des instanciations de la même classe d’objets.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-616">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-617">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-617">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> <dd>

<span data-ttu-id="3fe9c-618">La [**classe \_ RedundancyGroup CIM**](cim-redundancygroup.md) représente une collection d’éléments système gérés, qui indique que les composants agrégés, ensemble, fournissent une redondance.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-618">The [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="3fe9c-619">Tous les éléments agrégés dans un groupe de redondance doivent être des instanciations de la même classe d’objets.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-619">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-620">**\_Réfrigération CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-620">**CIM\_Refrigeration**</span></span>](cim-refrigeration.md)
</dt> <dd>

<span data-ttu-id="3fe9c-621">La classe de [**\_ réfrigération CIM**](cim-refrigeration.md) représente les fonctionnalités et la gestion d’un appareil de refroidissement frigorifique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-621">The [**CIM\_Refrigeration**](cim-refrigeration.md) class represents the capabilities and management of a refrigeration cooling device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-622">**\_RELATEDSTATISTICS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-622">**CIM\_RelatedStatistics**</span></span>](cim-relatedstatistics.md)
</dt> <dd>

<span data-ttu-id="3fe9c-623">L’Association [**CIM \_ RelatedStatistics**](cim-relatedstatistics.md) représente les hiérarchies et les dépendances des classes [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md) associées.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-623">The [**CIM\_RelatedStatistics**](cim-relatedstatistics.md) association represents hierarchies and dependencies of related [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) classes.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-624">**\_REMOTEFILESYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-624">**CIM\_RemoteFileSystem**</span></span>](cim-remotefilesystem.md)
</dt> <dd>

<span data-ttu-id="3fe9c-625">La classe [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md) représente un système de fichiers distant accessible par le biais d’un service lié au réseau.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-625">The [**CIM\_RemoteFileSystem**](cim-remotefilesystem.md) class represents a remote file system that is accessed by way of a network-related service.</span></span> <span data-ttu-id="3fe9c-626">Dans ce cas, le magasin de fichiers est hébergé par un ordinateur qui joue le rôle de serveur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-626">In this case, the file store is hosted by a computer, which acts as a file server.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-627">**\_REMOVEDIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-627">**CIM\_RemoveDirectoryAction**</span></span>](cim-removedirectoryaction.md)
</dt> <dd>

<span data-ttu-id="3fe9c-628">La classe [**CIM \_ RemoveDirectoryAction**](cim-removedirectoryaction.md) supprime les répertoires pour les éléments logiciels.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-628">The [**CIM\_RemoveDirectoryAction**](cim-removedirectoryaction.md) class removes directories for software elements.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-629">**\_REMOVEFILEACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-629">**CIM\_RemoveFileAction**</span></span>](cim-removefileaction.md)
</dt> <dd>

<span data-ttu-id="3fe9c-630">La [**classe \_ RemoveFileAction CIM**](cim-removefileaction.md) désinstalle des fichiers.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-630">The [**CIM\_RemoveFileAction**](cim-removefileaction.md) class uninstalls files.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-631">**\_REPLACEMENTSET CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-631">**CIM\_ReplacementSet**</span></span>](cim-replacementset.md)
</dt> <dd>

<span data-ttu-id="3fe9c-632">La classe [**CIM \_ ReplacementSet**](cim-replacementset.md) agrège les éléments physiques qui doivent être remplacés ensemble.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-632">The [**CIM\_ReplacementSet**](cim-replacementset.md) class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="3fe9c-633">Par exemple, lors du remplacement d’une carte mémoire, les puces de mémoire du composant peuvent également être supprimées et remplacées.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-633">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="3fe9c-634">Cette association peut être utilisée pour remplacer ou mettre à niveau un ensemble de puces mémoire.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-634">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-635">**\_RESIDESONEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-635">**CIM\_ResidesOnExtent**</span></span>](cim-residesonextent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-636">La classe [**CIM \_ ResidesOnExtent**](cim-residesonextent.md) représente une association entre un système de fichiers et l’extension de stockage où elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-636">The [**CIM\_ResidesOnExtent**](cim-residesonextent.md) class represents an association between a file system and the storage extent where it is located.</span></span> <span data-ttu-id="3fe9c-637">En règle générale, un système de fichiers réside sur un disque logique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-637">Typically, a file system resides on a logical disk.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-638">**\_En cours d’exécution CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-638">**CIM\_RunningOS**</span></span>](cim-runningos.md)
</dt> <dd>

<span data-ttu-id="3fe9c-639">La classe CIM executos représente le système d’exploitation [**\_ en**](cim-runningos.md) cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-639">The [**CIM\_RunningOS**](cim-runningos.md) class represents the currently executing operating system.</span></span> <span data-ttu-id="3fe9c-640">Au maximum, un système d’exploitation peut s’exécuter à tout moment sur un système informatique. le système informatique n’est peut-être pas en cours de démarrage ou son système d’exploitation est peut-être inconnu.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-640">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-641">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-641">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> <dd>

<span data-ttu-id="3fe9c-642">La [**classe \_ SAPSAPDependency CIM**](cim-sapsapdependency.md) est une association entre deux points d’accès de service (SAP), qui indique que le deuxième SAP est requis pour que le premier SAP se connecte à son service.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-642">The [**CIM\_SAPSAPDependency**](cim-sapsapdependency.md) class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-643">**\_Scanneur CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-643">**CIM\_Scanner**</span></span>](cim-scanner.md)
</dt> <dd>

<span data-ttu-id="3fe9c-644">Le [**\_ scanneur CIM**](cim-scanner.md) représente les fonctionnalités et la gestion de l’unité logique du scanneur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-644">The [**CIM\_Scanner**](cim-scanner.md) represents the capabilities and management of the scanner logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-645">**\_SCSICONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-645">**CIM\_SCSIController**</span></span>](cim-scsicontroller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-646">La classe [**CIM \_ SCSIController**](cim-scsicontroller.md) représente les fonctionnalités et la gestion de l’unité logique du contrôleur SCSI.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-646">The [**CIM\_SCSIController**](cim-scsicontroller.md) class represents the capabilities and management of the SCSI controller logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-647">**\_SCSIINTERFACE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-647">**CIM\_SCSIInterface**</span></span>](cim-scsiinterface.md)
</dt> <dd>

<span data-ttu-id="3fe9c-648">représente une [**relation \_ ControlledBy CIM**](cim-controlledby.md) qui indique quels appareils sont accessibles via un contrôleur SCSI et les caractéristiques d’accès.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-648">represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through a SCSI controller and the access characteristics.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-649">**\_Capteur CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-649">**CIM\_Sensor**</span></span>](cim-sensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-650">La classe de [**\_ capteur CIM**](cim-sensor.md) représente un périphérique matériel capable de mesurer les caractéristiques d’une propriété physique (par exemple, les caractéristiques de température ou de tension d’un système informatique unitaire).</span><span class="sxs-lookup"><span data-stu-id="3fe9c-650">The [**CIM\_Sensor**](cim-sensor.md) class represents a hardware device that is capable of measuring the characteristics of a physical property (for example, the temperature or voltage characteristics of a unitary computer system).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-651">**\_SERIALCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-651">**CIM\_SerialController**</span></span>](cim-serialcontroller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-652">La classe [**CIM \_ SerialController**](cim-serialcontroller.md) représente les fonctionnalités et la gestion de l’unité logique de port série.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-652">The [**CIM\_SerialController**](cim-serialcontroller.md) class represents the capabilities and management of the serial port logical device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-653">**\_SERIALINTERFACE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-653">**CIM\_SerialInterface**</span></span>](cim-serialinterface.md)
</dt> <dd>

<span data-ttu-id="3fe9c-654">La classe [**CIM \_ SerialInterface**](cim-serialinterface.md) représente une [**relation \_ ControlledBy CIM**](cim-controlledby.md) qui indique quels appareils sont accessibles par le biais du contrôleur série et les caractéristiques de l’accès.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-654">The [**CIM\_SerialInterface**](cim-serialinterface.md) class represents a [**CIM\_ControlledBy**](cim-controlledby.md) relationship that indicates which devices are accessed through the serial controller and the characteristics of the access.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-655">**\_Service CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-655">**CIM\_Service**</span></span>](cim-service.md)
</dt> <dd>

<span data-ttu-id="3fe9c-656">La classe de [**\_ service CIM**](cim-service.md) représente un élément logique qui contient des informations pour représenter et gérer les fonctionnalités fournies par un périphérique ou une fonctionnalité logicielle.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-656">The [**CIM\_Service**](cim-service.md) class represents a logical element that contains information to represent and manage the functionality provided by a device or software feature.</span></span> <span data-ttu-id="3fe9c-657">Un service est un objet à usage général permettant de configurer et de gérer l’implémentation des fonctionnalités. il ne s’agit pas de la fonctionnalité elle-même.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-657">A service is a general-purpose object to configure and manage the implementation of functionality; it is not the functionality itself.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-658">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-658">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> <dd>

<span data-ttu-id="3fe9c-659">La classe d’association [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md) représente les points d’accès pour un service.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-659">The [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md) association class represents the access points for a service.</span></span> <span data-ttu-id="3fe9c-660">Par exemple, il est possible d’accéder à une imprimante par des points d’accès SAP, Macintosh ou de service Windows, qui sont potentiellement hébergés sur différents systèmes.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-660">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-661">**\_SERVICEACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-661">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> <dd>

<span data-ttu-id="3fe9c-662">La classe [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) représente la possibilité d’utiliser ou d’appeler un service.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-662">The [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="3fe9c-663">Les points d’accès représentent les services qui peuvent être utilisés par d’autres entités.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-663">Access points represent services that are available for use by other entities.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-664">**\_SERVICESAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-664">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> <dd>

<span data-ttu-id="3fe9c-665">La classe [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) représente une association entre un service et un point d’accès au service (SAP), qui indique que le SAP référencé est utilisé par le service pour fournir ses fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-665">The [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-666">**\_SERVICESERVICEDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-666">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dd>

<span data-ttu-id="3fe9c-667">La classe [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) représente une association entre deux services.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-667">The [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) class represents an association between two services.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-668">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-668">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="3fe9c-669">La classe de [**\_ paramètres CIM**](cim-setting.md) représente des paramètres de configuration et opérationnels pour un ou plusieurs éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-669">The [**CIM\_Setting**](cim-setting.md) class represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-670">**\_SETTINGCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-670">**CIM\_SettingCheck**</span></span>](cim-settingcheck.md)
</dt> <dd>

<span data-ttu-id="3fe9c-671">La classe [**CIM \_ SettingCheck**](cim-settingcheck.md) spécifie les informations nécessaires pour vérifier un fichier de paramètres particulier pour une entrée spécifique qui contient une valeur égale à la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-671">The [**CIM\_SettingCheck**](cim-settingcheck.md) class specifies information needed to check a particular setting file for a specific entry that contains a value equal to the value specified.</span></span> <span data-ttu-id="3fe9c-672">Toutes les comparaisons sont supposées ne pas respecter la casse.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-672">All comparisons are assumed to be case insensitive.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-673">**\_SETTINGCONTEXT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-673">**CIM\_SettingContext**</span></span>](cim-settingcontext.md)
</dt> <dd>

<span data-ttu-id="3fe9c-674">La [**classe \_ SettingContext CIM**](cim-settingcontext.md) associe les objets de configuration aux objets Setting.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-674">The [**CIM\_SettingContext**](cim-settingcontext.md) class associates configuration objects with setting objects.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-675">**\_Emplacement CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-675">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dd>

<span data-ttu-id="3fe9c-676">La classe d' [**\_ emplacement CIM**](cim-slot.md) représente les connecteurs dans lesquels des packages sont insérés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-676">The [**CIM\_Slot**](cim-slot.md) class represents connectors into which packages are inserted.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-677">**\_SLOTINSLOT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-677">**CIM\_SlotInSlot**</span></span>](cim-slotinslot.md)
</dt> <dd>

<span data-ttu-id="3fe9c-678">La [**relation \_ SlotInSlot CIM**](cim-slotinslot.md) représente la capacité d’un adaptateur spécial à étendre la structure d’emplacement existante afin d’activer les cartes non compatibles dans une trame ou un tableau d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-678">The [**CIM\_SlotInSlot**](cim-slotinslot.md) relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-679">**\_SOFTWAREELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-679">**CIM\_SoftwareElement**</span></span>](cim-softwareelement.md)
</dt> <dd>

<span data-ttu-id="3fe9c-680">La classe [**CIM \_ SoftwareElement**](cim-softwareelement.md) décompose un [**objet \_ SoftwareFeature CIM**](cim-softwarefeature.md) en un ensemble de parties gérables ou déployables individuellement pour une plateforme particulière.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-680">The [**CIM\_SoftwareElement**](cim-softwareelement.md) class decomposes a [**CIM\_SoftwareFeature**](cim-softwarefeature.md) object into a set of individually manageable or deployable parts for a particular platform.</span></span> <span data-ttu-id="3fe9c-681">La plateforme d’un élément logiciel est identifiée de manière unique par son architecture matérielle sous-jacente et son système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-681">A software element's platform is uniquely identified by its underlying hardware architecture and operating system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-682">**\_SOFTWAREELEMENTACTIONS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-682">**CIM\_SoftwareElementActions**</span></span>](cim-softwareelementactions.md)
</dt> <dd>

<span data-ttu-id="3fe9c-683">L’Association [**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md) identifie les actions d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-683">The [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association identifies the actions for a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-684">**\_SOFTWAREELEMENTCHECKS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-684">**CIM\_SoftwareElementChecks**</span></span>](cim-softwareelementchecks.md)
</dt> <dd>

<span data-ttu-id="3fe9c-685">La classe d’association [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) associe un élément logiciel à des informations sur la condition ou l’emplacement qu’une fonctionnalité peut nécessiter.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-685">The [**CIM\_SoftwareElementChecks**](cim-softwareelementchecks.md) association class relates a software element with condition or location information that a feature may require.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-686">**\_SOFTWAREELEMENTVERSIONCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-686">**CIM\_SoftwareElementVersionCheck**</span></span>](cim-softwareelementversioncheck.md)
</dt> <dd>

<span data-ttu-id="3fe9c-687">La classe [**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) représente un type d’élément logiciel qui doit exister dans l’environnement.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-687">The [**CIM\_SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) class represents a type of software element that must exist in the environment.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-688">**\_SOFTWAREFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-688">**CIM\_SoftwareFeature**</span></span>](cim-softwarefeature.md)
</dt> <dd>

<span data-ttu-id="3fe9c-689">La classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) représente une fonction ou une fonctionnalité particulière d’un produit ou d’un système d’application.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-689">The [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class represents a particular function or capability of a product or application system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-690">**\_SOFTWAREFEATURESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-690">**CIM\_SoftwareFeatureSAPImplementation**</span></span>](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

<span data-ttu-id="3fe9c-691">La classe [**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) représente une association entre un point d’accès de service (SAP) et la façon dont il est implémenté dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-691">The [**CIM\_SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) class represents an association between a service access point (SAP) and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-692">**\_SOFTWAREFEATURESERVICEIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-692">**CIM\_SoftwareFeatureServiceImplementation**</span></span>](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

<span data-ttu-id="3fe9c-693">La classe [**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) représente une association entre un service et la manière dont il est implémenté dans le logiciel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-693">The [**CIM\_SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) class represents an association between a service and how it is implemented in software.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-694">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-694">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

<span data-ttu-id="3fe9c-695">L’Association [**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) identifie les éléments logiciels qui composent une fonctionnalité logicielle spécifique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-695">The [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) association identifies the software elements that make up a specific software feature.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-696">**\_SPAREGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-696">**CIM\_SpareGroup**</span></span>](cim-sparegroup.md)
</dt> <dd>

<span data-ttu-id="3fe9c-697">La classe [**CIM \_ SpareGroup**](cim-sparegroup.md) est dérivée de la classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) et indique qu’un ou plusieurs éléments agrégés peuvent être détachés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-697">The [**CIM\_SpareGroup**](cim-sparegroup.md) class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-698">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-698">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dd>

<span data-ttu-id="3fe9c-699">La [**classe \_ StatisticalInformation CIM**](cim-statisticalinformation.md) est une classe racine pour la collection arbitraire de données statistiques ou de mesures applicables à un ou plusieurs éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-699">The [**CIM\_StatisticalInformation**](cim-statisticalinformation.md) class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-700">**\_Statistiques CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-700">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> <dd>

<span data-ttu-id="3fe9c-701">La classe de [**\_ statistiques CIM**](cim-statistics.md) représente une association qui associe les éléments système gérés aux groupes statistiques qui s’y appliquent.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-701">The [**CIM\_Statistics**](cim-statistics.md) class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-702">**\_STORAGEDEFECT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-702">**CIM\_StorageDefect**</span></span>](cim-storagedefect.md)
</dt> <dd>

<span data-ttu-id="3fe9c-703">L’agrégation [**CIM \_ StorageDefect**](cim-storagedefect.md) collecte les erreurs de stockage pour une étendue de stockage.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-703">The [**CIM\_StorageDefect**](cim-storagedefect.md) aggregation collects the storage errors for a storage extent.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-704">**\_STORAGEERROR CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-704">**CIM\_StorageError**</span></span>](cim-storageerror.md)
</dt> <dd>

<span data-ttu-id="3fe9c-705">La classe [**CIM \_ StorageError**](cim-storageerror.md) représente des blocs d’espace de média ou de mémoire qui sont mappés hors de l’utilisation en raison d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-705">The [**CIM\_StorageError**](cim-storageerror.md) class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="3fe9c-706">La clé de la classe est la **propriété de l’erreur** de taille des octets erronés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-706">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-707">**\_STORAGEEXTENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-707">**CIM\_StorageExtent**</span></span>](cim-storageextent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-708">La classe [**CIM \_ StorageExtent**](cim-storageextent.md) représente les fonctionnalités et la gestion des différents médias qui existent pour stocker des données et permettre la récupération des données.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-708">The [**CIM\_StorageExtent**](cim-storageextent.md) class represents the capabilities and management of the various media that exist to store data and allow data retrieval.</span></span> <span data-ttu-id="3fe9c-709">Cette classe parente peut représenter les différents composants de RAID (matériel ou logiciel) ou une extension logique brute sur les supports physiques.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-709">This parent class can represent the various components of RAID (hardware or software) or a raw logical extent on top of physical media.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-710">**\_STORAGEREDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-710">**CIM\_StorageRedundancyGroup**</span></span>](cim-storageredundancygroup.md)
</dt> <dd>

<span data-ttu-id="3fe9c-711">La classe [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) représente des informations de redondance relatives au stockage de masse.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-711">The [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) class represents mass storage-related redundancy information.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-712">**\_SUPPORTACCESS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-712">**CIM\_SupportAccess**</span></span>](cim-supportaccess.md)
</dt> <dd>

<span data-ttu-id="3fe9c-713">La classe [**CIM \_ SupportAccess**](cim-supportaccess.md) définit comment obtenir de l’aide pour un produit.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-713">The [**CIM\_SupportAccess**](cim-supportaccess.md) class defines how to obtain assistance for a product.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-714">**\_SWAPSPACECHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-714">**CIM\_SwapSpaceCheck**</span></span>](cim-swapspacecheck.md)
</dt> <dd>

<span data-ttu-id="3fe9c-715">La classe [**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) spécifie la quantité d’espace d’échange qui doit être disponible sur le système.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-715">The [**CIM\_SwapSpaceCheck**](cim-swapspacecheck.md) class specifies the amount of swap space that must be available on the system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-716">**\_Système CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-716">**CIM\_System**</span></span>](cim-system.md)
</dt> <dd>

<span data-ttu-id="3fe9c-717">La [**classe \_ système CIM**](cim-system.md) agrège un ensemble énumérable d’éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-717">The [**CIM\_System**](cim-system.md) class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="3fe9c-718">L’agrégation fonctionne comme un ensemble fonctionnel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-718">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="3fe9c-719">Dans une sous-classe particulière du système, il existe une liste bien définie de classes d’éléments système gérés dont les instances doivent être agrégées.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-719">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-720">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-720">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dd>

<span data-ttu-id="3fe9c-721">classe d’association Common Information Model (CIM) qui établit les relations entre un système et les éléments système gérés dont il est composé.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-721">a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-722">**\_SYSTEMDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-722">**CIM\_SystemDevice**</span></span>](cim-systemdevice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-723">L’Association [**CIM \_ SystemDevice**](cim-systemdevice.md) représente une relation explicite dans laquelle les périphériques logiques peuvent être agrégés par un système.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-723">The [**CIM\_SystemDevice**](cim-systemdevice.md) association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-724">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-724">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dd>

<span data-ttu-id="3fe9c-725">La classe [**CIM \_ SystemResource**](cim-systemresource.md) représente une entité gérée par le BIOS, ou un système d’exploitation qui peut être utilisé par des périphériques logiciels et logiques.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-725">The [**CIM\_SystemResource**](cim-systemresource.md) class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-726">**\_Tachymètre CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-726">**CIM\_Tachometer**</span></span>](cim-tachometer.md)
</dt> <dd>

<span data-ttu-id="3fe9c-727">La classe du [**\_ tachymètre CIM**](cim-tachometer.md) existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-727">The [**CIM\_Tachometer**](cim-tachometer.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-728">**CIM \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-728">**CIM\_TapeDrive**</span></span>](cim-tapedrive.md)
</dt> <dd>

<span data-ttu-id="3fe9c-729">La [**classe \_ CIM CIM**](cim-tapedrive.md) représente un lecteur de bande sur le système.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-729">The [**CIM\_TapeDrive**](cim-tapedrive.md) class represents a tape drive on the system.</span></span> <span data-ttu-id="3fe9c-730">Les lecteurs de bande sont principalement distingués dans le fait qu’ils sont accessibles uniquement de façon séquentielle.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-730">Tape drives are primarily distinguished in that they can only be accessed sequentially.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-731">**\_Capteur CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-731">**CIM\_TemperatureSensor**</span></span>](cim-temperaturesensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-732">La classe [**CIM \_ capteur**](cim-temperaturesensor.md) existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-732">The [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) class exists for backward compatibility with earlier CIM schema definitions.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-733">**\_Thread CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-733">**CIM\_Thread**</span></span>](cim-thread.md)
</dt> <dd>

<span data-ttu-id="3fe9c-734">La classe de [**\_ thread CIM**](cim-thread.md) représente la capacité d’exécuter des unités d’un processus ou d’une tâche, en parallèle.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-734">The [**CIM\_Thread**](cim-thread.md) class represents the ability to execute units of a process or task, in parallel.</span></span> <span data-ttu-id="3fe9c-735">Un processus peut avoir de nombreux threads, chacun d’entre eux étant faible au processus.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-735">A process can have many threads, each of which is weak to the process.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-736">**\_TODIRECTORYACTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-736">**CIM\_ToDirectoryAction**</span></span>](cim-todirectoryaction.md)
</dt> <dd>

<span data-ttu-id="3fe9c-737">L’Association [**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md) identifie le répertoire cible de l’action de fichier.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-737">The [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-738">**\_TODIRECTORYSPECIFICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-738">**CIM\_ToDirectorySpecification**</span></span>](cim-todirectoryspecification.md)
</dt> <dd>

<span data-ttu-id="3fe9c-739">L’Association [**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md) identifie le répertoire cible de l’action de fichier.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-739">The [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association identifies the target directory for the file action.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-740">**\_UNINTERRUPTIBLEPOWERSUPPLY CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-740">**CIM\_UninterruptiblePowerSupply**</span></span>](cim-uninterruptiblepowersupply.md)
</dt> <dd>

<span data-ttu-id="3fe9c-741">La classe [**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) représente les fonctionnalités et la gestion d’un onduleur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-741">The [**CIM\_UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) class represents the capabilities and management of an uninterruptible power supply (UPS).</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-742">**\_UNITARYCOMPUTERSYSTEM CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-742">**CIM\_UnitaryComputerSystem**</span></span>](cim-unitarycomputersystem.md)
</dt> <dd>

<span data-ttu-id="3fe9c-743">La classe [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) représente un ordinateur de bureau, mobile, réseau, serveur ou tout autre type de système informatique à nœud unique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-743">The [**CIM\_UnitaryComputerSystem**](cim-unitarycomputersystem.md) class represents a desktop, mobile, network computer, server, or other type of single-node computer system.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-744">**\_USBCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-744">**CIM\_USBController**</span></span>](cim-usbcontroller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-745">La classe [**CIM \_ USBController**](cim-usbcontroller.md) représente les fonctionnalités et la gestion d’un contrôleur USB.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-745">The [**CIM\_USBController**](cim-usbcontroller.md) class represents the capabilities and management of a USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-746">**\_USBCONTROLLERHASHUB CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-746">**CIM\_USBControllerHasHub**</span></span>](cim-usbcontrollerhashub.md)
</dt> <dd>

<span data-ttu-id="3fe9c-747">La classe [**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md) définit les hubs en aval du contrôleur USB.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-747">The [**CIM\_USBControllerHasHub**](cim-usbcontrollerhashub.md) class defines the hubs that are downstream of the USB controller.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-748">**\_USBDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-748">**CIM\_USBDevice**</span></span>](cim-usbdevice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-749">La classe [**CIM \_ USBDevice**](cim-usbdevice.md) représente les caractéristiques de gestion d’un périphérique USB.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-749">The [**CIM\_USBDevice**](cim-usbdevice.md) class represents the management characteristics of a USB device.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-750">**\_Usbhub CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-750">**CIM\_USBHub**</span></span>](cim-usbhub.md)
</dt> <dd>

<span data-ttu-id="3fe9c-751">La classe [**CIM \_ USBHub**](cim-usbhub.md) représente les fonctionnalités et la gestion d’un concentrateur USB.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-751">The [**CIM\_USBHub**](cim-usbhub.md) class represents the capabilities and management of a USB hub.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-752">**\_USERDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-752">**CIM\_UserDevice**</span></span>](cim-userdevice.md)
</dt> <dd>

<span data-ttu-id="3fe9c-753">La [**classe \_ UserDevice CIM**](cim-userdevice.md) est une classe parente à partir de laquelle d’autres classes, telles que le [**\_ clavier CIM**](cim-keyboard.md) ou [**CIM \_ desktopmonitor**](cim-desktopmonitor.md), descendent.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-753">The [**CIM\_UserDevice**](cim-userdevice.md) class is a parent class from which other classes, such as [**CIM\_Keyboard**](cim-keyboard.md) or [**CIM\_DesktopMonitor**](cim-desktopmonitor.md), descend.</span></span> <span data-ttu-id="3fe9c-754">Les appareils utilisateur sont des périphériques logiques qui permettent à l’utilisateur d’un système informatique d’entrer, d’afficher ou d’entendre des données.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-754">User devices are logical devices that allow a computer system's user to input, view, or hear data.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-755">**\_VERSIONCOMPATIBILITYCHECK CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-755">**CIM\_VersionCompatibilityCheck**</span></span>](cim-versioncompatibilitycheck.md)
</dt> <dd>

<span data-ttu-id="3fe9c-756">La [**classe \_ VersionCompatibilityCheck CIM**](cim-versioncompatibilitycheck.md) spécifie s’il est autorisé de créer l’état suivant d’un élément logiciel.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-756">The [**CIM\_VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) class specifies whether it is permissible to create the next state of a software element.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-757">**\_VIDEOBIOSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-757">**CIM\_VideoBIOSElement**</span></span>](cim-videobioselement.md)
</dt> <dd>

<span data-ttu-id="3fe9c-758">La classe [**CIM \_ VideoBIOSElement**](cim-videobioselement.md) représente le logiciel de bas niveau qui est chargé dans un stockage non volatile et utilisé pour configurer et accéder au contrôleur vidéo et à l’affichage d’un système informatique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-758">The [**CIM\_VideoBIOSElement**](cim-videobioselement.md) class represents the low-level software that is loaded into non-volatile storage and used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-759">**\_VIDEOBIOSFEATURE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-759">**CIM\_VideoBIOSFeature**</span></span>](cim-videobiosfeature.md)
</dt> <dd>

<span data-ttu-id="3fe9c-760">La classe [**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) représente les fonctionnalités du logiciel de bas niveau utilisé pour configurer et accéder au contrôleur vidéo et à l’affichage d’un système informatique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-760">The [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) class represents the capabilities of the low-level software used to configure and access a computer system's video controller and display.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-761">**\_VIDEOBIOSFEATUREVIDEOBIOSELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-761">**CIM\_VideoBIOSFeatureVideoBIOSElements**</span></span>](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

<span data-ttu-id="3fe9c-762">La classe [**CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) associe une fonctionnalité BIOS vidéo et ses éléments BIOS vidéo agrégés.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-762">The [**CIM\_VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-763">**\_VIDEOCONTROLLER CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-763">**CIM\_VideoController**</span></span>](cim-videocontroller.md)
</dt> <dd>

<span data-ttu-id="3fe9c-764">La classe [**CIM \_ VideoController**](cim-videocontroller.md) représente les fonctionnalités et la gestion du contrôleur vidéo.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-764">The [**CIM\_VideoController**](cim-videocontroller.md) class represents the capabilities and management of the video controller.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-765">**\_VIDEOCONTROLLERRESOLUTION CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-765">**CIM\_VideoControllerResolution**</span></span>](cim-videocontrollerresolution.md)
</dt> <dd>

<span data-ttu-id="3fe9c-766">La classe [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) représente les différents modes vidéo qu’un contrôleur vidéo peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-766">The [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) class represents the various video modes that a video controller can support.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-767">**\_VIDEOSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-767">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dd>

<span data-ttu-id="3fe9c-768">La classe [**CIM \_ VideoSetting**](cim-videosetting.md) associe l’objet de paramètre [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) au contrôleur auquel il s’applique.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-768">The [**CIM\_VideoSetting**](cim-videosetting.md) class associates the [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) setting object with the controller to which it applies.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-769">**\_VOLATILESTORAGE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-769">**CIM\_VolatileStorage**</span></span>](cim-volatilestorage.md)
</dt> <dd>

<span data-ttu-id="3fe9c-770">La classe [**CIM \_ VolatileStorage**](cim-volatilestorage.md) représente les fonctionnalités et la gestion du stockage volatile.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-770">The [**CIM\_VolatileStorage**](cim-volatilestorage.md) class represents the capabilities and management of volatile storage.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-771">**\_Capteur CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-771">**CIM\_VoltageSensor**</span></span>](cim-voltagesensor.md)
</dt> <dd>

<span data-ttu-id="3fe9c-772">La classe [**CIM \_ capteur**](cim-voltagesensor.md) existe pour la compatibilité descendante avec les définitions de schéma CIM antérieures.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-772">The [**CIM\_VoltageSensor**](cim-voltagesensor.md) class exists for backward compatibility to earlier CIM schema definitions.</span></span> <span data-ttu-id="3fe9c-773">Avec les ajouts [**au \_ capteur CIM**](cim-sensor.md) et aux classes [**\_ NumericSensor CIM**](cim-numericsensor.md) dans la version 2,2, il n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-773">With additions to the [**CIM\_Sensor**](cim-sensor.md) and [**CIM\_NumericSensor**](cim-numericsensor.md) classes in version 2.2, it is no longer necessary.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-774">**\_VOLUMESET CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-774">**CIM\_VolumeSet**</span></span>](cim-volumeset.md)
</dt> <dd>

<span data-ttu-id="3fe9c-775">La classe [**CIM \_ VolumeSet**](cim-volumeset.md) représente une plage contiguë de blocs logiques présentée à l’environnement d’exploitation pour la lecture et l’écriture de données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-775">The [**CIM\_VolumeSet**](cim-volumeset.md) class represents a contiguous range of logical blocks presented to the operating environment for reading and writing user data.</span></span>

</dd> <dt>

[<span data-ttu-id="3fe9c-776">**\_WORMDRIVE CIM**</span><span class="sxs-lookup"><span data-stu-id="3fe9c-776">**CIM\_WORMDrive**</span></span>](cim-wormdrive.md)
</dt> <dd>

<span data-ttu-id="3fe9c-777">La classe [**CIM \_ WORMDrive**](cim-wormdrive.md) représente les fonctionnalités et la gestion d’un lecteur Worm, un sous-type de l’appareil d’accès aux médias.</span><span class="sxs-lookup"><span data-stu-id="3fe9c-777">The [**CIM\_WORMDrive**](cim-wormdrive.md) class represents the capabilities and management of a WORM drive, a subtype of the media access device.</span></span>

</dd> </dl>

 

 
