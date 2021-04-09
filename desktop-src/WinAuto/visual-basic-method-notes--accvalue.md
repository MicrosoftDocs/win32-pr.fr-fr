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
# <a name="visual-basic-method-notes-accvalue"></a>Remarques sur la méthode Visual Basic : accValue

Le fichier ODL (Object Description Language), oleacc. ODL, contient des informations qui diffèrent de l’implémentation C/C++. Le fichier oleacc. ODL contient la définition suivante pour la version qui définit la propriété de la fonction.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Bien que le paramètre *varChild* soit indiqué comme étant facultatif dans le fichier ODL et dans l’Explorateur d’objets, vous devez l’inclure lors de l’appel de la version de paramètre de propriété de [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).

 

 




