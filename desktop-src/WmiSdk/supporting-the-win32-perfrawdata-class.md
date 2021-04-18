---
description: Lors de l’écriture d’un fournisseur de haute performance qui dérive des classes de Win32 \_ PerfRawData, vous devez suivre des conventions spécifiques afin que WMI puisse fournir des données aux valeurs de propriété.
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: Prise en charge de la classe Win32_PerfRawData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 835815c9171097bfe088d22e4154ac668d790c0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533812"
---
# <a name="supporting-the-win32_perfrawdata-class"></a><span data-ttu-id="c8ae1-103">Prise en charge de la \_ classe Win32 PerfRawData</span><span class="sxs-lookup"><span data-stu-id="c8ae1-103">Supporting the Win32\_PerfRawData Class</span></span>

<span data-ttu-id="c8ae1-104">Lors de l’écriture d’un fournisseur de haute performance qui dérive des classes de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), vous devez suivre des conventions spécifiques afin que WMI puisse fournir des données aux valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-104">When writing a high-performance provider that derives classes from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata), you must follow specific conventions so that WMI can supply data to the property values.</span></span>

> [!Note]  
> <span data-ttu-id="c8ae1-105">L’écriture d’un fournisseur de performances élevées WMI pour créer des compteurs de performance n’est pas recommandée sur une version du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-105">Writing a WMI high-performance provider to create performance counters is not recommended on any version of the Windows operating system.</span></span> <span data-ttu-id="c8ae1-106">Pour plus d’informations, consultez [création d’un fournisseur d’instances dans un fournisseur de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)et [bibliothèques de performances et WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c8ae1-106">For more information, see [Making an Instance Provider into a High-Performance Provider](making-an-instance-provider-into-a-high-performance-provider.md)and [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span>

 

<span data-ttu-id="c8ae1-107">La procédure suivante décrit comment prendre en charge la classe [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) avec votre fournisseur hautes performances.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-107">The following procedure describes how to support the [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) class with your high-performance provider.</span></span>

<span data-ttu-id="c8ae1-108">**Pour prendre en charge la \_ classe Win32 PerfRawData**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-108">**To support the Win32\_PerfRawData class**</span></span>

1.  <span data-ttu-id="c8ae1-109">Créez votre classe dans l' \\ espace de noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-109">Create your class in the Root\\CIMv2 namespace.</span></span>

    <span data-ttu-id="c8ae1-110">La classe doit être dérivée de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et le qualificateur **HiPerf** doit avoir la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-110">The class must be derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and have the **Hiperf** qualifier set to **TRUE**.</span></span> <span data-ttu-id="c8ae1-111">Vous pouvez également ajouter des classes de données de performance WDM (pilote) à l' \\ espace de noms WMI racine.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-111">You can also add WDM (driver) performance data classes to the root\\wmi namespace.</span></span> <span data-ttu-id="c8ae1-112">Pour plus d’informations sur la création de votre propre classe pour WMI, consultez [conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="c8ae1-112">For more information about creating your own class for WMI, see [Designing Managed Object Format (MOF) Classes](designing-managed-object-format--mof--classes.md).</span></span>

2.  <span data-ttu-id="c8ae1-113">Spécifiez le fournisseur en tant que « NT5 \_ GenericPerfProvider \_ v1 » dans le qualificateur du **fournisseur** .</span><span class="sxs-lookup"><span data-stu-id="c8ae1-113">Specify the provider as "NT5\_GenericPerfProvider\_V1" in the **Provider** qualifier.</span></span>
3.  <span data-ttu-id="c8ae1-114">Spécifiez les qualificateurs au niveau de la classe suivants :</span><span class="sxs-lookup"><span data-stu-id="c8ae1-114">Specify the following class-level qualifiers:</span></span>

    -   <span data-ttu-id="c8ae1-115">**HiPerf**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-115">**HiPerf**</span></span>
    -   <span data-ttu-id="c8ae1-116">**Paramètres régionaux**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-116">**Locale**</span></span>
    -   <span data-ttu-id="c8ae1-117">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-117">**PerfDetail**</span></span>
    -   <span data-ttu-id="c8ae1-118">**Fournisseur**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-118">**Provider**</span></span>

    <span data-ttu-id="c8ae1-119">Pour plus d’informations, consultez [**qualificateurs de classe pour les classes de compteur de performance**](class-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c8ae1-119">For more information, see [**Class Qualifiers for Performance Counter Classes**](class-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="c8ae1-120">Ne définissez pas le qualificateur **GenericPerfCtr** , car il est réservé au processus adap qui transfère les données de la bibliothèque de performances dans des classes WMI.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-120">Do not define the **GenericPerfCtr** qualifier because that is reserved for the ADAP process that transfers performance library data into WMI classes.</span></span>

4.  <span data-ttu-id="c8ae1-121">Renseignez les propriétés timestamp et Frequency appropriées utilisées pour calculer des formules de type compteur.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-121">Populate the appropriate timestamp and frequency properties used to compute counter-type formulas.</span></span>

    <span data-ttu-id="c8ae1-122">Ces propriétés sont héritées de [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) et, si vous écrivez un fournisseur de haute performance, vous devez les remplir pour que la classe s’affiche dans le moniteur système.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-122">These properties are inherited from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) and, if you are writing a high-performance provider, you must fill these out for the class to be displayed in System Monitor.</span></span>

5.  <span data-ttu-id="c8ae1-123">Incluez une propriété de clé appelée **Name** dans votre classe (cette propriété n’est pas requise pour les classes singleton).</span><span class="sxs-lookup"><span data-stu-id="c8ae1-123">Include a key property called **Name** in your class (this property is not required for singleton classes).</span></span>

    <span data-ttu-id="c8ae1-124">Vous ne devez pas utiliser de propriété de clé autre que le **nom** de votre classe.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-124">You must not use any key property other than **Name** on your class.</span></span>

6.  <span data-ttu-id="c8ae1-125">Créer des propriétés données de type **DWORD** (**UInt32**) ou **QWord** (**UInt64**).</span><span class="sxs-lookup"><span data-stu-id="c8ae1-125">Create properties data-typed as either **DWORD** (**uint32**) or **QWORD** (**uint64**).</span></span> <span data-ttu-id="c8ae1-126">Ces propriétés deviennent des compteurs de performance lorsqu’elles sont transférées vers les bibliothèques de performances.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-126">These properties become performance counters when transferred to the performance libraries.</span></span>
7.  <span data-ttu-id="c8ae1-127">Spécifiez les qualificateurs de niveau de propriété suivants pour toutes les propriétés de votre classe :</span><span class="sxs-lookup"><span data-stu-id="c8ae1-127">Specify the following property level qualifiers for all properties in your class:</span></span>

    -   <span data-ttu-id="c8ae1-128">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-128">**DisplayName**</span></span>
    -   <span data-ttu-id="c8ae1-129">**CounterType**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-129">**CounterType**</span></span>
    -   <span data-ttu-id="c8ae1-130">**DefaultScale**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-130">**DefaultScale**</span></span>
    -   <span data-ttu-id="c8ae1-131">**Description**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-131">**Description**</span></span>
    -   <span data-ttu-id="c8ae1-132">**PerfDefault**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-132">**PerfDefault**</span></span>
    -   <span data-ttu-id="c8ae1-133">**PerfDetail**</span><span class="sxs-lookup"><span data-stu-id="c8ae1-133">**PerfDetail**</span></span>

    <span data-ttu-id="c8ae1-134">Pour plus d’informations, consultez [**qualificateurs de propriété pour les classes de compteur de performance**](property-qualifiers-for-performance-counter-classes.md).</span><span class="sxs-lookup"><span data-stu-id="c8ae1-134">For more information, see [**Property Qualifiers for Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md).</span></span> <span data-ttu-id="c8ae1-135">En outre, le fichier d’en-tête Winperf. h **contient des valeurs** que vous pouvez spécifier pour **PerfDetail** et.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-135">In addition, the Winperf.h header file contains values that you can specify for **PerfDetail** and **CounterType**.</span></span>

    <span data-ttu-id="c8ae1-136">WMI utilise les qualificateurs **DisplayName**, **locale** et **Description** pour la localisation.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-136">WMI uses the **DisplayName**, **Locale**, and **Description** qualifiers for localization.</span></span> <span data-ttu-id="c8ae1-137">Vous devez ajouter des qualificateurs modifiés à l' \_ espace de noms MS 409 (anglais) afin que le moniteur système puisse afficher correctement les données de votre classe.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-137">You must add amended qualifiers to the MS\_409 (English) namespace so that System Monitor can properly display your class data.</span></span> <span data-ttu-id="c8ae1-138">Cela signifie que vous modifiez la définition de propriété en ajoutant un qualificateur de **Description** avec un texte explicatif et en complétant la valeur **DisplayName** .</span><span class="sxs-lookup"><span data-stu-id="c8ae1-138">This means that you amend the property definition by adding a **Description** qualifier with explanatory text and fill in the **DisplayName** value.</span></span> <span data-ttu-id="c8ae1-139">Vous devez également ajouter des qualificateurs modifiés à tout autre espace de noms de paramètres régionaux pris en charge par votre classe.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-139">You must also add amended qualifiers to any other locale namespace that your class supports.</span></span> <span data-ttu-id="c8ae1-140">Si un utilisateur demande des données à partir de paramètres régionaux pour lesquels vous ne fournissez pas de qualificateurs modifiés, WMI prend par défaut les définitions spécifiées dans l' \_ espace de noms MS 409.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-140">If a user requests data from a locale for which you do not provide amended qualifiers, WMI defaults to the definitions specified in the MS\_409 namespace.</span></span>

8.  <span data-ttu-id="c8ae1-141">Créez une propriété de base pour toute propriété dont le type de compteur attend une valeur de base.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-141">Create a base property for any property that has a counter type expecting a base value.</span></span>

    <span data-ttu-id="c8ae1-142">Cette propriété suit immédiatement la propriété et est nommée \* PropertyName \***\_ base**.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-142">This property immediately follows the property and is named \*propertyname\***\_Base**.</span></span> <span data-ttu-id="c8ae1-143">Par exemple, la propriété moyenne **AvgDiskBytesPerRead** de la [**classe \_ \_ \_ disque logique Win32 PerfRawData Perfdisk**](./retrieving-raw-and-formatted-performance-data.md) requiert une propriété de base nommée **AvgDiskBytesPerRead \_ base** pour compter le nombre d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="c8ae1-143">For example, the average property **AvgDiskBytesPerRead** in the [**Win32\_PerfRawData\_PerfDisk\_LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md) class requires a base property named **AvgDiskBytesPerRead\_Base** to count the number of samples.</span></span> <span data-ttu-id="c8ae1-144">Pour déterminer si le type de compteur que vous souhaitez utiliser requiert une propriété de base, recherchez le type de compteur par nom ou valeur décimale dans les [types de compteurs de performance WMI](wmi-performance-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="c8ae1-144">To determine if the counter type you want to use requires a base property, locate the counter type by name or decimal value in [WMI Performance Counter Types](wmi-performance-counter-types.md).</span></span>

9.  <span data-ttu-id="c8ae1-145">Assurez-vous que votre fournisseur répond aux [exigences de performances](supporting-the-win32-perfformatteddata-class.md).</span><span class="sxs-lookup"><span data-stu-id="c8ae1-145">Make sure your provider meets the [performance requirements](supporting-the-win32-perfformatteddata-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8ae1-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c8ae1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8ae1-147">Création d’un fournisseur d’instances dans un fournisseur de High-Performance</span><span class="sxs-lookup"><span data-stu-id="c8ae1-147">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
