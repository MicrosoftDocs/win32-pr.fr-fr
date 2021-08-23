---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde86f9e1e60820aa7e1bc3a3f839dc920efda001f5b15e4f1ec7df4fc0cd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976449"
---
# <a name="iagentcharactergestureat"></a>IAgentCharacter::GestureAt

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

Lit l’animation d’état **gesturing** associée en fonction de l’emplacement spécifié.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi. Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordonnée x de l’emplacement spécifié, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordonnée y de l’emplacement spécifié, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de demande **GestureAt** .

</dd> </dl>

Le serveur détermine et lit automatiquement l’animation gesturing appropriée en fonction de la position actuelle du caractère et de l’emplacement spécifié. Lorsque vous utilisez le protocole HTTP pour accéder aux données de caractères et d’animation, utilisez la méthode [**Prepare**](iagentcharacter--prepare.md) pour vous assurer que les animations sont disponibles avant d’appeler cette méthode.

 

 




