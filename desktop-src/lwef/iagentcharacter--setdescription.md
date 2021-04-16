---
title: IAgentCharacter SetDescription
description: IAgentCharacter SetDescription
ms.assetid: ae01b9e6-1616-4806-9125-ceb4cb54aab1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9815e5c0e01537c7db2b400326f86da37af003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380439"
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


 

 




