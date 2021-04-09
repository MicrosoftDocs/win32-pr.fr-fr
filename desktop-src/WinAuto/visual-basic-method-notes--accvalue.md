---
title: Remarques sur la méthode Visual Basic accValue
description: Le fichier ODL (Object Description Language), oleacc. ODL, contient des informations qui diffèrent de l’implémentation C/C++. Le fichier oleacc. ODL contient la définition suivante pour la version qui définit la propriété de la fonction.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce93bc5d4ff2a2e01da55e30630fda42c573b7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029059"
---
# <a name="visual-basic-method-notes-accvalue"></a><span data-ttu-id="47bf6-104">Remarques sur la méthode Visual Basic : accValue</span><span class="sxs-lookup"><span data-stu-id="47bf6-104">Visual Basic Method Notes: accValue</span></span>

<span data-ttu-id="47bf6-105">Le fichier ODL (Object Description Language), oleacc. ODL, contient des informations qui diffèrent de l’implémentation C/C++.</span><span class="sxs-lookup"><span data-stu-id="47bf6-105">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="47bf6-106">Le fichier oleacc. ODL contient la définition suivante pour la version qui définit la propriété de la fonction.</span><span class="sxs-lookup"><span data-stu-id="47bf6-106">The file Oleacc.odl contains the following definition for the version that sets the property of the function.</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



<span data-ttu-id="47bf6-107">Bien que le paramètre *varChild* soit indiqué comme étant facultatif dans le fichier ODL et dans l’Explorateur d’objets, vous devez l’inclure lors de l’appel de la version de paramètre de propriété de [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span><span class="sxs-lookup"><span data-stu-id="47bf6-107">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span></span>

 

 




