---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461ebc4fa7c7e0ae9080544e9114db9f8c179925dae665925d893288f95de027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118478623"
---
# <a name="iagentballoongetnumlines"></a>IAgentBalloon::GetNumLines

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

Récupère la valeur du nombre de lignes affichées dans une bulle de texte.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*
</dt> <dd>

Adresse d’une variable qui reçoit le nombre de lignes affichées.

</dd> </dl>

Le serveur Microsoft Agent fait défiler automatiquement les lignes affichées pour la sortie parlée dans la bulle de texte. Le nombre de lignes pour une bulle de mot de caractères est défini dans l’éditeur de caractères Microsoft Agent. Elle ne peut pas être modifiée par une application.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




