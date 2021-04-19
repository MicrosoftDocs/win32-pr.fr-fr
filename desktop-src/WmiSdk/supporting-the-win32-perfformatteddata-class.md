---
description: Lors de l’écriture d’un fournisseur de haute performance qui dérive des classes de Win32 \_ PerfFormattedData, vous devez suivre des conventions spécifiques afin que WMI puisse calculer les valeurs de propriété.
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: Prise en charge de la classe Win32_PerfFormattedData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54911105f5c485d3a80ddb93b96f0af2637c9506
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521940"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a><span data-ttu-id="ea388-103">Prise en charge de la \_ classe Win32 PerfFormattedData</span><span class="sxs-lookup"><span data-stu-id="ea388-103">Supporting the Win32\_PerfFormattedData Class</span></span>

<span data-ttu-id="ea388-104">Lors de l’écriture d’un fournisseur de haute performance qui dérive des classes de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), vous devez suivre des conventions spécifiques afin que WMI puisse calculer les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="ea388-104">When writing a high-performance provider that derives classes from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata), you must follow specific conventions so that WMI can calculate the property values.</span></span>

> [!Note]  
> <span data-ttu-id="ea388-105">L’écriture d’un fournisseur de performances élevées WMI pour créer des compteurs de performance n’est pas recommandée sur une version du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="ea388-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="ea388-106">Pour plus d’informations, consultez [création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)et [bibliothèques de performances et WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ea388-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="ea388-107">La procédure suivante décrit comment prendre en charge la \_ classe Win32 PerfFormattedData.</span><span class="sxs-lookup"><span data-stu-id="ea388-107">The following procedure describes how to support the Win32\_PerfFormattedData class.</span></span>

<span data-ttu-id="ea388-108">**Pour prendre en charge la \_ classe Win32 PerfFormattedData**</span><span class="sxs-lookup"><span data-stu-id="ea388-108">**To support the Win32\_PerfFormattedData class**</span></span>

1.  <span data-ttu-id="ea388-109">Créez votre classe dans le même espace de noms que la classe brute correspondante.</span><span class="sxs-lookup"><span data-stu-id="ea388-109">Create your class in the same namespace as the corresponding raw class.</span></span> <span data-ttu-id="ea388-110">La classe doit être dérivée de [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) et le qualificateur **HiPerf** doit avoir la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="ea388-110">The class must be derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) and have the **HiPerf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="ea388-111">Pour plus d’informations sur la création de votre propre classe pour WMI, consultez [conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="ea388-111">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>
2.  <span data-ttu-id="ea388-112">Spécifiez « HiPerfCooker \_ v1 » dans le qualificateur du [**fournisseur**](class-qualifiers-for-performance-counter-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="ea388-112">Specify "HiPerfCooker\_v1" in the [**Provider**](class-qualifiers-for-performance-counter-classes.md) qualifier.</span></span>
3.  <span data-ttu-id="ea388-113">Spécifiez les qualificateurs au niveau de la classe suivants en plus des qualificateurs utilisés pour les classes brutes :</span><span class="sxs-lookup"><span data-stu-id="ea388-113">Specify the following class-level qualifiers in addition to the qualifiers used for the raw classes:</span></span>

    -   [<span data-ttu-id="ea388-114">**Cook automatique**</span><span class="sxs-lookup"><span data-stu-id="ea388-114">**AutoCook**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-115">**RawClass autocook \_**</span><span class="sxs-lookup"><span data-stu-id="ea388-115">**Autocook\_RawClass**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-116">**Cuisson**</span><span class="sxs-lookup"><span data-stu-id="ea388-116">**Cooked**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-117">**Réduis**</span><span class="sxs-lookup"><span data-stu-id="ea388-117">**Costly**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-118">**Dynamique**</span><span class="sxs-lookup"><span data-stu-id="ea388-118">**Dynamic**</span></span>](dynamic-qualifier.md)
    -   [<span data-ttu-id="ea388-119">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="ea388-119">**HiPerf**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-120">**Paramètres régionaux**</span><span class="sxs-lookup"><span data-stu-id="ea388-120">**Locale**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-121">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="ea388-121">**PerfDefault**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-122">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="ea388-122">**Provider**</span></span>](class-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-123">**Singleton**</span><span class="sxs-lookup"><span data-stu-id="ea388-123">**Singleton**</span></span>](standard-wmi-qualifiers.md)

    > [!Note]  
    > <span data-ttu-id="ea388-124">Ne définissez pas de valeur pour **GenericPerfCtr**, **PerfIndex** ou **HelpIndex** , car ceux-ci seront définis par le processus adap.</span><span class="sxs-lookup"><span data-stu-id="ea388-124">Do not set any value for **GenericPerfCtr**, **PerfIndex**, or **HelpIndex** because these will be set by the ADAP process.</span></span> <span data-ttu-id="ea388-125">Pour plus d’informations, consultez [**qualificateurs de classe pour les classes de compteur de performance**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ea388-125">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span>

     

4.  <span data-ttu-id="ea388-126">Incluez une propriété de clé appelée **Name** dans votre classe (cette propriété n’est pas requise pour les classes singleton).</span><span class="sxs-lookup"><span data-stu-id="ea388-126">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="ea388-127">La valeur de la propriété **Name** doit être la même que la classe brute correspondante.</span><span class="sxs-lookup"><span data-stu-id="ea388-127">The value of the **Name** property must be the same as the corresponding raw class.</span></span> <span data-ttu-id="ea388-128">Vous ne devez pas utiliser de propriété de clé autre que le **nom** de votre classe.</span><span class="sxs-lookup"><span data-stu-id="ea388-128">You must not use any key property other than **Name** on your class.</span></span>

5.  <span data-ttu-id="ea388-129">Créer des propriétés de données de type **DWORD** (**UInt32**) ou **QWord** (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="ea388-129">Create properties data typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span>

    <span data-ttu-id="ea388-130">Les propriétés doivent correspondre à une propriété de la classe brute ou à une propriété de la classe que vous créez.</span><span class="sxs-lookup"><span data-stu-id="ea388-130">The properties must correspond either to a property in the raw class or a property in the class you are creating.</span></span>

6.  <span data-ttu-id="ea388-131">Spécifiez les qualificateurs de niveau de propriété suivants pour toutes les propriétés de votre classe en plus des qualificateurs **PerfIndex** et **PerfDetail** utilisés pour les propriétés de la classe brute :</span><span class="sxs-lookup"><span data-stu-id="ea388-131">Specify the following property level qualifiers for all properties in your class in addition to the **PerfIndex** and **PerfDetail** qualifiers used for the raw class properties:</span></span>

    -   [<span data-ttu-id="ea388-132">**Base**</span><span class="sxs-lookup"><span data-stu-id="ea388-132">**Base**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-133">**CookingType**</span><span class="sxs-lookup"><span data-stu-id="ea388-133">**CookingType**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-134">**Compteur**</span><span class="sxs-lookup"><span data-stu-id="ea388-134">**Counter**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-135">**PerfTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="ea388-135">**PerfTimeStamp**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-136">**PerfTimeFreq**</span><span class="sxs-lookup"><span data-stu-id="ea388-136">**PerfTimeFreq**</span></span>](property-qualifiers-for-performance-counter-classes.md)
    -   [<span data-ttu-id="ea388-137">**SampleWindow**</span><span class="sxs-lookup"><span data-stu-id="ea388-137">**SampleWindow**</span></span>](property-qualifiers-for-performance-counter-classes.md)

    <span data-ttu-id="ea388-138">Pour plus d’informations, consultez [**qualificateurs de propriété pour les classes de compteur de performance**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="ea388-138">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="ea388-139">En outre, le fichier d’en-tête Winperf. h **contient des valeurs** que vous pouvez spécifier pour **PerfDetail** et.</span><span class="sxs-lookup"><span data-stu-id="ea388-139">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

7.  <span data-ttu-id="ea388-140">Assurez-vous que votre fournisseur répond aux [exigences de performances](#performance-requirements).</span><span class="sxs-lookup"><span data-stu-id="ea388-140">Make sure your provider meets the [performance requirements](#performance-requirements).</span></span>

## <a name="performance-requirements"></a><span data-ttu-id="ea388-141">Exigences en matière de performances</span><span class="sxs-lookup"><span data-stu-id="ea388-141">Performance Requirements</span></span>

<span data-ttu-id="ea388-142">Lorsque vous écrivez un fournisseur à hautes performances, ses performances doivent remplir les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="ea388-142">When you write a high-performance provider, its performance must meet the following requirements:</span></span>

-   <span data-ttu-id="ea388-143">L’ouverture du fichier DLL à hautes performances ne peut pas durer plus de 100 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="ea388-143">Opening the high-performance DLL file can take no more than 100 milliseconds.</span></span> <span data-ttu-id="ea388-144">Globalement, l’ouverture de chaque fournisseur de performances et de la bibliothèque de performances ne peut pas dépasser 5 secondes.</span><span class="sxs-lookup"><span data-stu-id="ea388-144">Overall, opening each the high-performance provider and performance library cannot exceed 5 seconds.</span></span>
-   <span data-ttu-id="ea388-145">L’actualisation des données ne peut pas durer plus de 10 millisecondes par collecte.</span><span class="sxs-lookup"><span data-stu-id="ea388-145">Data refresh can take no more than 10 milliseconds per collect.</span></span> <span data-ttu-id="ea388-146">Dans le cas d’une opération d’actualisation et de collecte globale, l’ensemble des fournisseurs hautes performances ne peut pas prendre plus de 800 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="ea388-146">On an overall refresh and collect operation, all the high-performance providers together cannot take more than 800 milliseconds.</span></span>
-   <span data-ttu-id="ea388-147">La charge de l’UC globale pour tous les fournisseurs à hautes performances ne peut pas dépasser 6-7% de la surcharge de l’UC de manière interactive ou 5% pour la journalisation.</span><span class="sxs-lookup"><span data-stu-id="ea388-147">The overall CPU load for all high-performance providers cannot exceed 6-7% CPU overhead interactively or 5% for logging.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ea388-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ea388-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea388-149">Création d’un fournisseur d’instances dans un fournisseur de High-Performance</span><span class="sxs-lookup"><span data-stu-id="ea388-149">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
