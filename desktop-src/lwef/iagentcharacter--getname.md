---
title: IAgentCharacter GetName
description: IAgentCharacter GetName
ms.assetid: 6c013a18-8c56-42a8-8723-31d83b3230cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33679577cfb5179a799ee61207f7ecd9b2be8a21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311602"
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


 

 




