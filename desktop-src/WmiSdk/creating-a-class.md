---
description: Dans WMI, une classe est un objet qui décrit certains aspects d’une entreprise, tels qu’un type spécial de lecteur de disque.
ms.assetid: 06b75910-f126-48b6-8e43-4a9ed4661732
ms.tgt_platform: multiple
title: Création d’une classe WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2274252715ce44b9d2b79e398c945ca723fe3f7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524434"
---
# <a name="creating-a-wmi-class"></a><span data-ttu-id="c75d5-103">Création d’une classe WMI</span><span class="sxs-lookup"><span data-stu-id="c75d5-103">Creating a WMI Class</span></span>

<span data-ttu-id="c75d5-104">Dans WMI, une classe est un objet qui décrit certains aspects d’une entreprise, tels qu’un type spécial de lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="c75d5-104">In WMI, a class is an object that describes some aspect of an enterprise, such as a special type of disk drive.</span></span> <span data-ttu-id="c75d5-105">Après avoir créé une définition de classe, écrivez votre DLL de fournisseur pour fournir des instances de la classe, des données de propriété et des méthodes d’exécution définies pour la classe.</span><span class="sxs-lookup"><span data-stu-id="c75d5-105">After you have created a class definition, write your provider DLL to supply instances of the class, property data, and execute methods defined for the class.</span></span> <span data-ttu-id="c75d5-106">Les scripts et les applications peuvent ensuite obtenir des données ou contrôler l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c75d5-106">Scripts and applications can then obtain data or control the device.</span></span> <span data-ttu-id="c75d5-107">Pour plus d’informations, consultez [développement d’un fournisseur WMI](developing-a-wmi-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c75d5-107">For more information, see [Developing a WMI Provider](developing-a-wmi-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="c75d5-108">Pour vous assurer que toutes les définitions de classe WMI pour les objets managés sont restaurées dans l' [*espace de stockage WMI*](gloss-w.md) en cas d’échec et de redémarrage de WMI, utilisez l’instruction de préprocesseur de l’instruction de [**\# récupération automatique pragma**](pragma-autorecover.md) dans votre fichier MOF.</span><span class="sxs-lookup"><span data-stu-id="c75d5-108">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) statement preprocessor instruction in your MOF file.</span></span>

 

## <a name="base-class"></a><span data-ttu-id="c75d5-109">Classe de base</span><span class="sxs-lookup"><span data-stu-id="c75d5-109">Base Class</span></span>

<span data-ttu-id="c75d5-110">Une classe de base représente un concept général.</span><span class="sxs-lookup"><span data-stu-id="c75d5-110">A base class represents some general concept.</span></span> <span data-ttu-id="c75d5-111">Par exemple, la classe [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) représente tous les types de lecteurs de CD-ROM dans WMI et contient des propriétés générales qui décrivent tous les types de lecteurs de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="c75d5-111">For example, the [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive) class represents all types of CD-ROM drives in WMI, and contains general properties that describe all kinds of CD-ROM drives.</span></span> <span data-ttu-id="c75d5-112">Pour plus d’informations, consultez [création d’une classe de base](creating-a-base-class.md).</span><span class="sxs-lookup"><span data-stu-id="c75d5-112">For more information, see [Creating a Base Class](creating-a-base-class.md).</span></span>

<span data-ttu-id="c75d5-113">Une classe dérivée hérite des propriétés et des méthodes d’une autre classe.</span><span class="sxs-lookup"><span data-stu-id="c75d5-113">A derived class inherits properties and methods from another class.</span></span> <span data-ttu-id="c75d5-114">Une classe dérivée représente généralement un cas spécifique d’une classe de base.</span><span class="sxs-lookup"><span data-stu-id="c75d5-114">A derived class usually represents a specific case of a base class.</span></span> <span data-ttu-id="c75d5-115">Par exemple, la classe [**Win32 \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) représente un lecteur de CD-ROM sur un système Windows.</span><span class="sxs-lookup"><span data-stu-id="c75d5-115">For example, the [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) class represents a CD-ROM drive on a Windows system.</span></span> <span data-ttu-id="c75d5-116">La classe **Win32 \_ CDROMDrive** est basée sur et hérite de nombreuses propriétés de [**CIM \_ CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span><span class="sxs-lookup"><span data-stu-id="c75d5-116">The **Win32\_CDROMDrive** class is based on and inherits many of properties from [**CIM\_CDROMDrive**](/windows/desktop/CIMWin32Prov/cim-cdromdrive).</span></span> <span data-ttu-id="c75d5-117">Toutefois, **les \_ CDROMDrive Win32**, comme d’autres classes dérivées, peuvent avoir des propriétés supplémentaires qui rendent la classe dérivée unique.</span><span class="sxs-lookup"><span data-stu-id="c75d5-117">However, **Win32\_CDROMDrive**, like other derived classes, can have additional properties that make the derived class unique.</span></span> <span data-ttu-id="c75d5-118">Pour plus d’informations, consultez [création d’une classe dérivée](creating-a-derived-class.md).</span><span class="sxs-lookup"><span data-stu-id="c75d5-118">For more information, see [Creating a Derived Class](creating-a-derived-class.md).</span></span>

## <a name="properties-and-methods"></a><span data-ttu-id="c75d5-119">Propriétés et méthodes</span><span class="sxs-lookup"><span data-stu-id="c75d5-119">Properties and Methods</span></span>

<span data-ttu-id="c75d5-120">La création d’une classe signifie la définition des propriétés qui décrivent cette classe.</span><span class="sxs-lookup"><span data-stu-id="c75d5-120">Creating a class means defining the properties that describe that class.</span></span> <span data-ttu-id="c75d5-121">Vous pouvez également définir des méthodes qui manipulent l’objet représenté par la classe.</span><span class="sxs-lookup"><span data-stu-id="c75d5-121">You can also define methods that manipulate the object represented by the class.</span></span>

<span data-ttu-id="c75d5-122">En général, une propriété représente un aspect de l’objet, tel qu’un numéro de série pour un appareil ou une taille en octets pour un processus, tandis qu’une méthode représente une action qui modifie l’État ou le comportement de l’appareil ou de l’entité logique.</span><span class="sxs-lookup"><span data-stu-id="c75d5-122">Generally, a property represents an aspect of the object, such as a serial number for a device or a size in bytes for a process, while a method represents an action that changes the state or behavior of the device or logical entity.</span></span>

<span data-ttu-id="c75d5-123">Chaque classe doit avoir au moins une propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="c75d5-123">Each class must have at least one key property.</span></span> <span data-ttu-id="c75d5-124">Alors qu’une classe peut avoir plusieurs clés, vous ne pouvez pas créer une instance d’une classe avec plus de 256 clés.</span><span class="sxs-lookup"><span data-stu-id="c75d5-124">While a class may have multiple keys, you cannot create an instance of a class with more than 256 keys.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c75d5-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c75d5-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c75d5-126">Conception de classes format MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="c75d5-126">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
