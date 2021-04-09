---
description: Une classe de vue de jointure contient des propriétés des instances de classe source qui sont connectées par une valeur de propriété commune, telle que Class1. Prop1 = Classe2. Prop2. Chaque instance d’une classe de vue de jointure se compose de parties d’instances de classes différentes.
ms.assetid: 4d35474d-0b80-4b00-9724-47a193bfd0fc
ms.tgt_platform: multiple
title: Création d’une nouvelle instance à partir d’anciennes propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552d05b9e8c96620ce41579eb14cc234eca675eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952863"
---
# <a name="creating-a-new-instance-from-old-properties"></a><span data-ttu-id="daa77-104">Création d’une nouvelle instance à partir d’anciennes propriétés</span><span class="sxs-lookup"><span data-stu-id="daa77-104">Creating a New Instance from Old Properties</span></span>

<span data-ttu-id="daa77-105">Une classe de vue de jointure contient des propriétés des instances de classe source qui sont connectées par une valeur de propriété commune, telle que **Class1. Prop1**  =  **Classe2. Prop2**.</span><span class="sxs-lookup"><span data-stu-id="daa77-105">A join view class contains properties from source class instances that are connected by a common property value, such as **Class1.Prop1** = **Class2.Prop2**.</span></span> <span data-ttu-id="daa77-106">Chaque instance d’une classe de vue de jointure se compose de parties d’instances de classes différentes.</span><span class="sxs-lookup"><span data-stu-id="daa77-106">Each instance in a join view class consists of parts of different class instances.</span></span>

<span data-ttu-id="daa77-107">Vous pouvez baser une classe de vue de jointure sur l’inégalité des valeurs de propriété, telles que **Class1. Prop1**  <>  **Classe2. Prop2** où **Prop1** et **Prop2** ne sont pas mappés à la même propriété dans la classe de vue.</span><span class="sxs-lookup"><span data-stu-id="daa77-107">You can base a join view class on inequality of property values, such as **Class1.Prop1** <> **Class2.Prop2** where **Prop1** and **Prop2** are not mapped to the same property in the view class.</span></span>

<span data-ttu-id="daa77-108">Une classe de vue de jointure est utile lorsque les informations que vous recherchez sont contenues dans des classes distinctes mais associées.</span><span class="sxs-lookup"><span data-stu-id="daa77-108">A join view class is helpful when the information you are looking for is contained in separate but related classes.</span></span> <span data-ttu-id="daa77-109">Par exemple, si vous souhaitez obtenir des informations sur une imprimante et sur la configuration de l’imprimante, vous pouvez créer une classe de vue de jointure qui contient certaines des propriétés de la classe [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) et certaines des propriétés de la classe [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) .</span><span class="sxs-lookup"><span data-stu-id="daa77-109">For example, if you want information about a printer and about the printer configuration, you can create a join view class that contains some of the properties of the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and some of the properties of the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) class.</span></span> <span data-ttu-id="daa77-110">Sans le fournisseur d’affichage, vous devez récupérer et fusionner les propriétés des instances distinctes pour obtenir les informations dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="daa77-110">Without the View Provider, you must retrieve and merge the properties of the separate instances to get the information you need.</span></span>

<span data-ttu-id="daa77-111">La procédure suivante décrit comment créer une classe de vue de jointure.</span><span class="sxs-lookup"><span data-stu-id="daa77-111">The following procedure describes how to create a join view class.</span></span>

<span data-ttu-id="daa77-112">**Pour créer une classe de vue de jointure**</span><span class="sxs-lookup"><span data-stu-id="daa77-112">**To create a join view class**</span></span>

1.  <span data-ttu-id="daa77-113">Commencez une définition de classe par le qualificateur de chaîne [**JoinOn**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="daa77-113">Begin a class definition with the [**JoinOn**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="daa77-114">Les qualificateurs [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association** et **Union** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="daa77-114">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="daa77-115">Si nécessaire, filtrez les instances de votre choix dans la classe join en appliquant le qualificateur [**PostJoinFilter**](postjoinfilter-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="daa77-115">If necessary, filter the instances that you want in the join class by applying the [**PostJoinFilter**](postjoinfilter-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="daa77-116">Le fournisseur [**PostJoinFilter**](postjoinfilter-qualifier.md) vous permet de limiter les instances d’une classe d’affichage aux instances qui répondent à des conditions spécifiques.</span><span class="sxs-lookup"><span data-stu-id="daa77-116">The [**PostJoinFilter**](postjoinfilter-qualifier.md) provider allows you to restrict the instances of a view class to instances that meet specific conditions.</span></span>

3.  <span data-ttu-id="daa77-117">Créez les requêtes qui définissent les instances source de la classe View avec le qualificateur [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="daa77-117">Create the queries that define source instances of the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="daa77-118">Définissez les noms et les emplacements des espaces de noms où se trouvent les instances source à l’aide du qualificateur [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="daa77-118">Define the names and locations of the namespaces where the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
5.  <span data-ttu-id="daa77-119">Définissez les propriétés souhaitées dans une classe de vue de jointure avec le qualificateur [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="daa77-119">Define the properties that you want in a join view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="daa77-120">Lorsque des propriétés sont ajoutées à la vue de jointure en fonction de l’égalité, les deux propriétés sources doivent être mappées dans un qualificateur [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="daa77-120">When properties are added to the join view based on equality, the two source properties must be mapped in one [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="daa77-121">L’exemple de code suivant montre deux propriétés mappées dans un qualificateur **PropertySources** .</span><span class="sxs-lookup"><span data-stu-id="daa77-121">The following code example shows two properties that are mapped in one **PropertySources** qualifier.</span></span>

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    <span data-ttu-id="daa77-122">À l’aide du qualificateur [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) , vous pouvez baliser les propriétés qui appartiennent à une classe source.</span><span class="sxs-lookup"><span data-stu-id="daa77-122">By using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier, you can tag the properties that belong to a source class.</span></span>

<span data-ttu-id="daa77-123">L’exemple de code suivant montre une classe de vue de jointure créée à partir des classes du fournisseur de l’analyseur de performances [**Win32 \_ PerfRawData \_ perfproc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) et [**Win32 \_ PerfRawData \_ perfproc \_ thread**](/previous-versions//aa394325(v=vs.85)) avec les propriétés des deux classes jointes par la propriété **ProcessID** .</span><span class="sxs-lookup"><span data-stu-id="daa77-123">The following code example shows a join view class created from the Performance Monitor provider classes [**Win32\_PerfRawData\_PerfProc\_Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) and [**Win32\_PerfRawData\_PerfProc\_Thread**](/previous-versions//aa394325(v=vs.85)) with properties of both classes joined by the **ProcessID** property.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\cimv2")

instance of __Win32Provider as $DataProv
{
    Name = "MS_VIEW_INSTANCE_PROVIDER";
    ClsId = "{AA70DDF4-E11C-11D1-ABB0-00C04FD9159E}";
    ImpersonationLevel = 1;
    PerUserInitialization = "True";
    
};

instance of __InstanceProviderRegistration
{
    Provider = $DataProv;
    SupportsPut = True;
    SupportsGet = True;
    SupportsDelete = True;
    SupportsEnumeration = True;
    QuerySupportLevels = {"WQL:UnarySelect"};
};

[JoinOn("Win32_PerfRawData_PerfProc_Process.IDProcess = 
    Win32_PerfRawData_PerfProc_Thread.IDProcess"), 
ViewSources{"SELECT Name, IDProcess, PriorityBase 
    FROM Win32_PerfRawData_PerfProc_Process", 
    "SELECT Name, IDProcess, ThreadState, 
    PriorityCurrent FROM Win32_PerfRawData_PerfProc_Thread"},
ViewSpaces{"\\\\.\\root\\cimv2", "\\\\.\\root\\cimv2"},
dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class JoinedProcessThread
{
    [PropertySources{"IDProcess", "IDProcess"}] 
        Uint32 ProcessID;
    [PropertySources{"Name", ""}] 
        String PName;
    [PropertySources{"", "Name"}, key]   
        String TName;
    [PropertySources{"", "ThreadState"}] 
        Uint32 State;
    [PropertySources{"PriorityBase", ""}] 
        Uint32 BasePriority;
    [PropertySources{"", "PriorityCurrent"}] 
        Uint32 CurrentPriority;    
};
```

 

 
