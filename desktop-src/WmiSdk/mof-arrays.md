---
description: Un tableau est une liste indexée des valeurs de données qui sont du même type de données, que vous pouvez référencer. En plus des tableaux de type chaîne et numérique, MOF prend en charge les tableaux d’objets incorporés et de références.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: Tableaux MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201820"
---
# <a name="mof-arrays"></a><span data-ttu-id="dcb9a-104">Tableaux MOF</span><span class="sxs-lookup"><span data-stu-id="dcb9a-104">MOF Arrays</span></span>

<span data-ttu-id="dcb9a-105">Un tableau est une liste indexée des valeurs de données qui sont du même type de données, que vous pouvez référencer.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-105">An array is an indexed list of data values that are of the same data type, which you can reference.</span></span> <span data-ttu-id="dcb9a-106">En plus des tableaux de type chaîne et numérique, MOF prend en charge les tableaux d’objets incorporés et de références.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-106">In addition to string and numeric arrays, MOF supports arrays of embedded objects and references.</span></span>

<span data-ttu-id="dcb9a-107">Les règles suivantes définissent un tableau MOF :</span><span class="sxs-lookup"><span data-stu-id="dcb9a-107">The following rules define a MOF array:</span></span>

-   <span data-ttu-id="dcb9a-108">Les crochets utilisés après l’identificateur de propriété spécifient un tableau dans une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-108">Brackets used after the property identifier specify an array in a class definition.</span></span>

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   <span data-ttu-id="dcb9a-109">Tous les tableaux doivent être unidimensionnels.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-109">All arrays must be one-dimensional.</span></span>
-   <span data-ttu-id="dcb9a-110">Les tableaux peuvent être illimités ou avoir une taille explicite.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-110">Arrays can be unbounded or have an explicit size.</span></span>

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    <span data-ttu-id="dcb9a-111">WMI implémente des tableaux délimités et non liés en tant que structures **SAFEARRAY** , ce qui permet à WMI de modifier les dimensions du tableau au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-111">WMI implements bounded and unbounded arrays as **SAFEARRAY** structures, which allows WMI to vary array dimensions at run time.</span></span> <span data-ttu-id="dcb9a-112">Lorsque vous déclarez un tableau avec une taille explicite, WMI stocke la taille comme qualificateur et traite la taille comme la taille maximale suggérée.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-112">When you declare an array with an explicit size, WMI stores the size as a qualifier, and treats the size as the suggested maximum size.</span></span> <span data-ttu-id="dcb9a-113">Toutefois, WMI peut étendre la taille si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-113">However, WMI can expand the size if necessary.</span></span> <span data-ttu-id="dcb9a-114">La modification de la taille explicite n’a aucun effet sur les données réelles.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-114">Changing the explicit size has no effect on the actual data.</span></span>

-   <span data-ttu-id="dcb9a-115">Les tableaux sont initialisés en spécifiant les valeurs du type approprié dans une liste séparée par des virgules.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-115">Arrays are initialized by specifying values of the appropriate type in a comma-separated list.</span></span>

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   <span data-ttu-id="dcb9a-116">Un tableau de références est déclaré en tant que tableau de chaînes de chemin d’accès à l’objet.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-116">An array of references is declared as an array of object path strings.</span></span>

    <span data-ttu-id="dcb9a-117">Lors de la déclaration d’une chaîne de chemin d’accès d’objet, ne placez pas d’espace blanc entre les éléments du chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-117">When declaring an object path string, do not place white space between the elements of the object path.</span></span> <span data-ttu-id="dcb9a-118">L’exemple suivant décrit comment déclarer une référence de chemin d’accès à un objet.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-118">The following example describes how to declare an object path reference.</span></span>

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

-   <span data-ttu-id="dcb9a-119">Vous pouvez utiliser un tableau en tant que paramètre pour une méthode, mais pas comme valeur de retour pour un paramètre d’entrée ou d’entrée-sortie.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-119">You can use an array as a parameter for a method, but not as a return value for an input or input-output parameter.</span></span>
-   <span data-ttu-id="dcb9a-120">Tous les éléments d’un tableau sont créés en tant que valeurs du même type.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-120">All elements in an array are created as values of the same type.</span></span>

    <span data-ttu-id="dcb9a-121">Si les éléments d’un tableau sont du type d' **objet** , vous pouvez placer n’importe quel type d’objet dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-121">If the elements of an array are of the **object** type, then you can place any kind of object in the array.</span></span> <span data-ttu-id="dcb9a-122">En revanche, si vous déclarez un type spécifique d’objet, WMI autorise uniquement les objets de cette classe ou de cette sous-classe dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="dcb9a-122">On the other hand, if you declare a specific type of object, then WMI allows only objects of that class or subclass in the array.</span></span> <span data-ttu-id="dcb9a-123">Les exemples suivants montrent des déclarations de tableau qui incluent l’utilisation du type d' **objet** .</span><span class="sxs-lookup"><span data-stu-id="dcb9a-123">The following examples show array declarations that includes using the **object** type.</span></span>

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

 

 



