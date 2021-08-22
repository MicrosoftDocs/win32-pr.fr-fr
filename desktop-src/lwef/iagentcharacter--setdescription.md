---
title: IAgentCharacter SetDescription
description: IAgentCharacter SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d96765d3faddafef00a28826ec5a9fdd92acb6884ac3aa659ad88ba2c091a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609819"
---
# <a name="iagentcharactersetdescription"></a>IAgentCharacter :: SetDescription

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetDescription(
   BSTR bszDescription   // character description
); 
```

Définit la description du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszDescription"></span><span id="bszdescription"></span><span id="BSZDESCRIPTION"></span>*bszDescription*
</dt> <dd>

BSTR qui définit la description du caractère. La description par défaut d’un caractère est définie lorsqu’elle est compilée avec l’éditeur de caractères Microsoft Agent. Le paramètre description est facultatif et ne peut pas être fourni pour tous les caractères. Vous pouvez modifier la description du caractère à l’aide de **IAgentCharacter :: SetDescription**; Toutefois, cette valeur n’est pas persistante (stockée de façon permanente). La description du caractère revient à sa valeur par défaut chaque fois que le caractère est chargé pour la première fois par un client.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: GetDescription**](iagentcharacter--getdescription.md)


 

 




