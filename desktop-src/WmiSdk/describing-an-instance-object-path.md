---
description: Un chemin d’accès d’objet d’instance décrit l’emplacement d’une instance d’une classe donnée dans un espace de noms spécifique.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Description d’un chemin d’accès d’objet d’instance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319794"
---
# <a name="describing-an-instance-object-path"></a><span data-ttu-id="b60f3-103">Description d’un chemin d’accès d’objet d’instance</span><span class="sxs-lookup"><span data-stu-id="b60f3-103">Describing an Instance Object Path</span></span>

<span data-ttu-id="b60f3-104">Un chemin d’accès d’objet d’instance décrit l’emplacement d’une instance d’une classe donnée dans un espace de noms spécifique.</span><span class="sxs-lookup"><span data-stu-id="b60f3-104">An instance object path describes the location of an instance of a given class within a specific namespace.</span></span>

<span data-ttu-id="b60f3-105">Vous pouvez avoir plusieurs types différents de chemins d’accès d’objet d’instance :</span><span class="sxs-lookup"><span data-stu-id="b60f3-105">You can have several different kinds of instance object paths:</span></span>

-   <span data-ttu-id="b60f3-106">Complète</span><span class="sxs-lookup"><span data-stu-id="b60f3-106">Full</span></span>

    <span data-ttu-id="b60f3-107">Un chemin d’accès complet à un objet d’instance ajoute le nom et la valeur de la propriété de clé pour la classe à un chemin d’accès d’objet de classe complet.</span><span class="sxs-lookup"><span data-stu-id="b60f3-107">A full instance object path appends the name and value of the key property for the class to a full class object path.</span></span>

    <span data-ttu-id="b60f3-108">L’exemple suivant illustre la définition du chemin d’accès complet à l’objet instance.</span><span class="sxs-lookup"><span data-stu-id="b60f3-108">The following example shows the definition of the full instance object path.</span></span>

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   <span data-ttu-id="b60f3-109">Relatif</span><span class="sxs-lookup"><span data-stu-id="b60f3-109">Relative</span></span>

    <span data-ttu-id="b60f3-110">Un chemin d’accès relatif à un objet fait référence à une instance située dans l’espace de noms actuel sur le serveur actuel.</span><span class="sxs-lookup"><span data-stu-id="b60f3-110">A relative object path refers to an instance located in the current namespace on the current server.</span></span> <span data-ttu-id="b60f3-111">Le chemin d’accès relatif se compose du nom de la classe suivi des noms et des valeurs des propriétés de clé de cette instance.</span><span class="sxs-lookup"><span data-stu-id="b60f3-111">The relative path consists of the class name followed by the names and values of the key properties of this instance.</span></span>

    <span data-ttu-id="b60f3-112">L’exemple suivant illustre la définition du chemin d’accès de l’objet d’instance relative.</span><span class="sxs-lookup"><span data-stu-id="b60f3-112">The following example shows the definition of the relative instance object path.</span></span>

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   <span data-ttu-id="b60f3-113">Relatif avec une clé unique</span><span class="sxs-lookup"><span data-stu-id="b60f3-113">Relative with a single key</span></span>

    <span data-ttu-id="b60f3-114">Pour les classes avec une seule propriété désignée comme clé, vous pouvez omettre le nom de la propriété de clé.</span><span class="sxs-lookup"><span data-stu-id="b60f3-114">For classes with only one property designated as the key, you can omit the name of the key property.</span></span>

    <span data-ttu-id="b60f3-115">L’exemple suivant illustre la définition du chemin d’accès de l’objet d’instance relatif avec une clé unique.</span><span class="sxs-lookup"><span data-stu-id="b60f3-115">The following example shows the definition of the relative instance object path with a single key.</span></span>

    ``` syntax
    MyClass="e:"
    ```

-   <span data-ttu-id="b60f3-116">Relatif à plusieurs clés</span><span class="sxs-lookup"><span data-stu-id="b60f3-116">Relative with multiple keys</span></span>

    <span data-ttu-id="b60f3-117">Utilisez une virgule pour faire la distinction entre les clés d’une instance avec plusieurs clés.</span><span class="sxs-lookup"><span data-stu-id="b60f3-117">Use a comma to distinguish between the keys of an instance with multiple keys.</span></span>

    <span data-ttu-id="b60f3-118">L’exemple suivant montre les définitions du chemin d’accès de l’objet d’instance relatif avec plusieurs clés.</span><span class="sxs-lookup"><span data-stu-id="b60f3-118">The following example shows the definitions of the relative instance object path with multiple keys.</span></span>

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   <span data-ttu-id="b60f3-119">Relatif pour une classe singleton</span><span class="sxs-lookup"><span data-stu-id="b60f3-119">Relative for a singleton class</span></span>

    <span data-ttu-id="b60f3-120">Le chemin d’accès relatif d’un objet pour une classe singleton se compose du nom de la classe suivi de la notation « = @ ».</span><span class="sxs-lookup"><span data-stu-id="b60f3-120">The relative object path for a singleton class consists of the class name followed by the "=@" notation.</span></span>

    <span data-ttu-id="b60f3-121">L’exemple suivant illustre la définition du chemin d’accès de l’objet d’instance relative pour une classe singleton.</span><span class="sxs-lookup"><span data-stu-id="b60f3-121">The following example shows the definition of the relative instance object path for a singleton class.</span></span>

    ``` syntax
    MySingletonClass=@
    ```

<span data-ttu-id="b60f3-122">La procédure suivante décrit comment récupérer une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="b60f3-122">The following procedure describes how to retrieve a class instance.</span></span>

<span data-ttu-id="b60f3-123">**Pour récupérer une instance de classe**</span><span class="sxs-lookup"><span data-stu-id="b60f3-123">**To retrieve a class instance**</span></span>

1.  <span data-ttu-id="b60f3-124">Initialisez une chaîne qui contient le chemin d’accès de l’objet avec un appel à la fonction [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) .</span><span class="sxs-lookup"><span data-stu-id="b60f3-124">Initialize a string that contains the object path with a call to the [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) function.</span></span>
2.  <span data-ttu-id="b60f3-125">Initialise un objet qui recevra l’instance.</span><span class="sxs-lookup"><span data-stu-id="b60f3-125">Initialize an object that will receive the instance.</span></span>
3.  <span data-ttu-id="b60f3-126">Récupérez l’objet à l’aide d’un appel à [**IWbemServices :: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) ou [**IWbemServices :: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="b60f3-126">Retrieve the object with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="b60f3-127">Pour utiliser [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), vous devez implémenter l’interface [**IWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="b60f3-127">To use [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), you must implement the [**IWbemSink**](swbemsink.md) interface.</span></span>

<span data-ttu-id="b60f3-128">L' \# instruction include suivante est requise pour le code qui est indiqué plus loin dans cette rubrique pour compiler correctement.</span><span class="sxs-lookup"><span data-stu-id="b60f3-128">The following \#include statement is required for the code that is listed later in this topic to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="b60f3-129">L’exemple de code suivant décrit comment récupérer une instance de classe à l’aide d’un chemin d’accès à un objet.</span><span class="sxs-lookup"><span data-stu-id="b60f3-129">The following code example describes how to retrieve a class instance using an object path.</span></span>


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



<span data-ttu-id="b60f3-130">Pour les instances de classes qui spécifient plusieurs propriétés en tant que clé, WMI ne requiert aucun classement spécifique des propriétés de clé dans les chemins d’accès aux objets.</span><span class="sxs-lookup"><span data-stu-id="b60f3-130">For instances of classes that specify multiple properties as the key, WMI requires no specific ordering of key properties in object paths.</span></span> <span data-ttu-id="b60f3-131">Vous devez uniquement spécifier la valeur de chacune des propriétés dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b60f3-131">You need only specify the value of each of the properties in the object path.</span></span>

<span data-ttu-id="b60f3-132">L’exemple de code suivant décrit deux descriptions de clé équivalentes.</span><span class="sxs-lookup"><span data-stu-id="b60f3-132">The following code example describes two equivalent key descriptions.</span></span>

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
