---
title: GetDescription IAgentCharacter
description: GetDescription IAgentCharacter
ms.assetid: 729f54ac-1c60-4a7b-b993-5682a6ea2b3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23216f1a7b013a54de1e64351c2a9d3a3d3359d90e0516cd6852a003baa047c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716189"
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

 

 




