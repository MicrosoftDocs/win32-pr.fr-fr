---
description: Un tableau est une liste indexée des valeurs de données qui sont du même type de données, que vous pouvez référencer. En plus des tableaux de type chaîne et numérique, MOF prend en charge les tableaux d’objets incorporés et de références.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: Tableaux MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010451"
---
# <a name="mof-arrays"></a>Tableaux MOF

Un tableau est une liste indexée des valeurs de données qui sont du même type de données, que vous pouvez référencer. En plus des tableaux de type chaîne et numérique, MOF prend en charge les tableaux d’objets incorporés et de références.

Les règles suivantes définissent un tableau MOF :

-   Les crochets utilisés après l’identificateur de propriété spécifient un tableau dans une définition de classe.

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   Tous les tableaux doivent être unidimensionnels.
-   Les tableaux peuvent être illimités ou avoir une taille explicite.

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    WMI implémente des tableaux délimités et non liés en tant que structures **SAFEARRAY** , ce qui permet à WMI de modifier les dimensions du tableau au moment de l’exécution. Lorsque vous déclarez un tableau avec une taille explicite, WMI stocke la taille comme qualificateur et traite la taille comme la taille maximale suggérée. Toutefois, WMI peut étendre la taille si nécessaire. La modification de la taille explicite n’a aucun effet sur les données réelles.

-   Les tableaux sont initialisés en spécifiant les valeurs du type approprié dans une liste séparée par des virgules.

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   Un tableau de références est déclaré en tant que tableau de chaînes de chemin d’accès à l’objet.

    Lors de la déclaration d’une chaîne de chemin d’accès d’objet, ne placez pas d’espace blanc entre les éléments du chemin d’accès de l’objet. L’exemple suivant décrit comment déclarer une référence de chemin d’accès à un objet.

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   Vous pouvez utiliser un tableau en tant que paramètre pour une méthode, mais pas comme valeur de retour pour un paramètre d’entrée ou d’entrée-sortie.
-   Tous les éléments d’un tableau sont créés en tant que valeurs du même type.

    Si les éléments d’un tableau sont du type d' **objet** , vous pouvez placer n’importe quel type d’objet dans le tableau. En revanche, si vous déclarez un type spécifique d’objet, WMI autorise uniquement les objets de cette classe ou de cette sous-classe dans le tableau. Les exemples suivants montrent des déclarations de tableau qui incluent l’utilisation du type d' **objet** .

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



