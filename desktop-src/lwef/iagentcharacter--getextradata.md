---
title: IAgentCharacter GetExtraData
description: IAgentCharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12032eb7d4587b4d9ccc7260699e5e11bd816e6239d4b49d3ad4692882e4827
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962309"
---
# <a name="iagentcharactergetextradata"></a>IAgentCharacter::GetExtraData

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetExtraData(
   BSTR * pbszExtraData   // address of buffer for additional character data
); 
```

Récupère des données supplémentaires stockées dans le cadre du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszExtraData"></span><span id="pbszextradata"></span><span id="PBSZEXTRADATA"></span>*pbszExtraData*
</dt> <dd>

Adresse d’un BSTR qui reçoit la valeur des données supplémentaires pour le caractère. Les données supplémentaires d’un caractère sont définies lorsqu’elles sont compilées avec l’éditeur de caractères Microsoft Agent. Un développeur de caractères peut fournir cette chaîne en modifiant le. Fichier ACD pour un caractère. Le paramètre est facultatif et ne peut pas être fourni pour tous les caractères, ni être défini ou modifié au moment de l’exécution. En outre, la signification des données fournies est définie par le développeur de caractères.

</dd> </dl>

 

 




