---
title: IAgentCharacterEx GetVersion
description: IAgentCharacterEx GetVersion
ms.assetid: 78f6d7b6-f72d-4af8-a014-3acd185926f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c72d9304aa689cda83117d57f26c2da776c9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029023"
---
# <a name="iagentcharacterexgetversion"></a>IAgentCharacterEx :: GetVersion

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVersion(
   short * psMajor,  // address of major version
   short * psMinor   // address of minor version
);
```

Récupère le numéro de version de l’ensemble d’animations standard de caractères.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="psMajor"></span><span id="psmajor"></span><span id="PSMAJOR"></span>*psMajor*
</dt> <dd>

Adresse d’une variable qui reçoit la version principale.

</dd> <dt>

<span id="psMinor"></span><span id="psminor"></span><span id="PSMINOR"></span>*psMinor*
</dt> <dd>

Adresse d’une variable qui reçoit la version mineure.

</dd> </dl>

Le numéro de version du jeu d’animations standard est défini automatiquement quand vous le générez avec l’éditeur de caractères Microsoft Agent.

 

 




