---
title: GetDescription IAgentCharacter
description: GetDescription IAgentCharacter
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423cd1f5c799cc1f0177f6d3d7922d5d14de1dbe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380447"
---
# <a name="iagentcharactergetdescription"></a>IAgentCharacter :: GetDescription

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetDescription(
   BSTR * pbszDescription   // address of buffer for character description
); 
```

Récupère la description du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszDescription"></span><span id="pbszdescription"></span><span id="PBSZDESCRIPTION"></span>*pbszDescription*
</dt> <dd>

Adresse d’un BSTR qui reçoit la valeur de la description du caractère. La description d’un caractère est définie lorsqu’elle est compilée avec l’éditeur de caractères Microsoft Agent. Le paramètre description est facultatif et ne peut pas être fourni pour tous les caractères.

</dd> </dl>

 

 




