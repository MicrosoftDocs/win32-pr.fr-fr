---
title: Visual Basic Notes de méthode accValue
description: Le fichier ODL (Object Description Language), oleacc. ODL, contient des informations qui diffèrent de l’implémentation C/C++. Le fichier oleacc. ODL contient la définition suivante pour la version qui définit la propriété de la fonction.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f5a79740e71984b4d9beaba9faad23142b2c9afc78a7378e9b11be4dc521
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744779"
---
# <a name="visual-basic-method-notes-accvalue"></a>Visual Basic Remarques sur la méthode : accValue

Le fichier ODL (Object Description Language), oleacc. ODL, contient des informations qui diffèrent de l’implémentation C/C++. Le fichier oleacc. ODL contient la définition suivante pour la version qui définit la propriété de la fonction.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Bien que le paramètre *varChild* soit indiqué comme étant facultatif dans le fichier ODL et dans l’Explorateur d’objets, vous devez l’inclure lors de l’appel de la version de paramètre de propriété de [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).

 

 




