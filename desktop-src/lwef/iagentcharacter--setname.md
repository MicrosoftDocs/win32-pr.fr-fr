---
title: IAgentCharacter SetName
description: IAgentCharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d46a2210b14519a0595f37786725559d363cddaceb62ae93b80a52deb839e0b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725289"
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


 

 




