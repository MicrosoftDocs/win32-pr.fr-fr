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
# <a name="creating-a-new-instance-from-old-properties"></a>Création d’une nouvelle instance à partir d’anciennes propriétés

Une classe de vue de jointure contient des propriétés des instances de classe source qui sont connectées par une valeur de propriété commune, telle que **Class1. Prop1**  =  **Classe2. Prop2**. Chaque instance d’une classe de vue de jointure se compose de parties d’instances de classes différentes.

Vous pouvez baser une classe de vue de jointure sur l’inégalité des valeurs de propriété, telles que **Class1. Prop1**  <>  **Classe2. Prop2** où **Prop1** et **Prop2** ne sont pas mappés à la même propriété dans la classe de vue.

Une classe de vue de jointure est utile lorsque les informations que vous recherchez sont contenues dans des classes distinctes mais associées. Par exemple, si vous souhaitez obtenir des informations sur une imprimante et sur la configuration de l’imprimante, vous pouvez créer une classe de vue de jointure qui contient certaines des propriétés de la classe [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) et certaines des propriétés de la classe [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) . Sans le fournisseur d’affichage, vous devez récupérer et fusionner les propriétés des instances distinctes pour obtenir les informations dont vous avez besoin.

La procédure suivante décrit comment créer une classe de vue de jointure.

**Pour créer une classe de vue de jointure**

1.  Commencez une définition de classe par le qualificateur de chaîne [**JoinOn**](qualifiers-specific-to-the-view-provider.md) .

    Les qualificateurs [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association** et **Union** s’excluent mutuellement.

2.  Si nécessaire, filtrez les instances de votre choix dans la classe join en appliquant le qualificateur [**PostJoinFilter**](postjoinfilter-qualifier.md) .

    Le fournisseur [**PostJoinFilter**](postjoinfilter-qualifier.md) vous permet de limiter les instances d’une classe d’affichage aux instances qui répondent à des conditions spécifiques.

3.  Créez les requêtes qui définissent les instances source de la classe View avec le qualificateur [**ViewSources**](viewsources-qualifier.md) .
4.  Définissez les noms et les emplacements des espaces de noms où se trouvent les instances source à l’aide du qualificateur [**ViewSpaces**](viewspaces-qualifier.md) .
5.  Définissez les propriétés souhaitées dans une classe de vue de jointure avec le qualificateur [**PropertySources**](propertysources-qualifier.md) .

    Lorsque des propriétés sont ajoutées à la vue de jointure en fonction de l’égalité, les deux propriétés sources doivent être mappées dans un qualificateur [**PropertySources**](propertysources-qualifier.md) .

    L’exemple de code suivant montre deux propriétés mappées dans un qualificateur **PropertySources** .

    ``` syntax
    [PropertySources{"IDProcess", "IDProcess"}] Uint32 ProcessID;
    ```

    À l’aide du qualificateur [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) , vous pouvez baliser les propriétés qui appartiennent à une classe source.

L’exemple de code suivant montre une classe de vue de jointure créée à partir des classes du fournisseur de l’analyseur de performances [**Win32 \_ PerfRawData \_ perfproc \_ Process**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data) et [**Win32 \_ PerfRawData \_ perfproc \_ thread**](/previous-versions//aa394325(v=vs.85)) avec les propriétés des deux classes jointes par la propriété **ProcessID** .

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

 

 
