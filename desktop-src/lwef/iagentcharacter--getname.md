---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107e6fdb6be3e79dee14177d9f56ee7d258f3455d578641e7d3a3b3cf044c741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962271"
---
# <a name="iagentcharactergetname"></a>IAgentCharacter :: GetName

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetName(
   BSTR * pbszName   // address of buffer for character name
);
```

Récupère le nom du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszName"></span><span id="pbszname"></span><span id="PBSZNAME"></span>*pbszName*
</dt> <dd>

Adresse d’un BSTR qui reçoit la valeur du nom pour le caractère.

</dd> </dl>

Le nom par défaut d’un caractère est défini lorsqu’il est compilé avec l’éditeur de caractères Microsoft Agent. Le nom d’un caractère peut varier en fonction de l’ID de langue du caractère. Les caractères peuvent être compilés avec des noms différents dans différentes langues.

Vous pouvez également définir le nom du caractère à l’aide de **IAgentCharacter : SetName**; Toutefois, cela modifie le nom de tous les clients actuels du caractère.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: SetName**](iagentcharacter--setname.md)


 

 




