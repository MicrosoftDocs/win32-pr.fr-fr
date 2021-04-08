---
title: Remarques sur la méthode Visual Basic accName
description: Le fichier ODL (Object Description Language), oleacc. ODL, contient des informations qui diffèrent de l’implémentation C/C++.
ms.assetid: f7960acd-cb1a-4c34-a392-0243155a100f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c404c093fc3b92b4d653b0b1258c62918af8e25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840133"
---
# <a name="visual-basic-method-notes-accname"></a><span data-ttu-id="ec4a7-103">Remarques sur la méthode Visual Basic : accName</span><span class="sxs-lookup"><span data-stu-id="ec4a7-103">Visual Basic Method Notes: accName</span></span>

<span data-ttu-id="ec4a7-104">Le fichier ODL (Object Description Language), oleacc. ODL, contient des informations qui diffèrent de l’implémentation C/C++.</span><span class="sxs-lookup"><span data-stu-id="ec4a7-104">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="ec4a7-105">Le fichier oleacc. ODL contient la définition suivante pour la version qui définit la propriété de la fonction :</span><span class="sxs-lookup"><span data-stu-id="ec4a7-105">The file Oleacc.odl contains the following definition for the version that sets the property of the function:</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



<span data-ttu-id="ec4a7-106">Bien que le paramètre *varChild* soit indiqué comme étant facultatif dans le fichier ODL et dans l’Explorateur d’objets, vous devez l’inclure lors de l’appel de la version de paramètre de propriété de [**accName**](https://www.bing.com/search?q=**accName**).</span><span class="sxs-lookup"><span data-stu-id="ec4a7-106">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accName**](https://www.bing.com/search?q=**accName**).</span></span>

 

 




