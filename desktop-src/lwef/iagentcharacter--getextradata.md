---
title: IAgentCharacter GetExtraData
description: IAgentCharacter GetExtraData
ms.assetid: 83f69bae-0ae3-45c5-ba0d-71610993da60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea854479ab85630abc3d110c9c193716ddedd004
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100821"
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

 

 




