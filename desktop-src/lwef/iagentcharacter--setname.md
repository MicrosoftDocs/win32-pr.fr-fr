---
title: IAgentCharacter SetName
description: IAgentCharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106538792"
---
# <a name="iagentcharactersetname"></a>IAgentCharacter :: SetName

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

Définit le nom du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

BSTR qui définit le nom du caractère. Le nom par défaut d’un caractère est défini lorsqu’il est compilé avec l’éditeur de caractères Microsoft Agent. Vous pouvez le modifier à l’aide de **IAgentCharacter :: SetName**; Toutefois, cela modifie le nom de caractère pour tous les clients actuels du caractère. Cette propriété n’est pas persistante (stockée définitivement). Le nom du caractère revient à son nom par défaut chaque fois que le caractère est chargé pour la première fois par un client.

Le nom du caractère peut également dépendre de son ID de langue. Les caractères peuvent être compilés avec des noms différents dans différentes langues.

Le serveur utilise le paramètre de nom du caractère dans des parties de l’interface de l’agent Microsoft, telles que le titre de la fenêtre commandes vocales lorsque le caractère est en entrée-actif et dans le menu contextuel de la barre des tâches de l’agent Microsoft.

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: GetName**](iagentcharacter--getname.md)


 

 




