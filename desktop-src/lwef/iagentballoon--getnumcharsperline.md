---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62415c5e51cbf6642b4a348de2060fccb6bac41467dd00b7671888d06b8e71f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888397"
---
# <a name="iagentballoongetnumcharsperline"></a>IAgentBalloon::GetNumCharsPerLine

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

Récupère la valeur pour le nombre moyen de caractères par ligne affichée dans une bulle de texte.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*
</dt> <dd>

Adresse d’une variable qui reçoit le nombre de caractères par ligne.

</dd> </dl>

Le serveur Microsoft Agent fait défiler automatiquement les lignes affichées pour la sortie parlée dans la bulle de texte. Le nombre moyen de caractères par ligne pour la bulle de texte d’un caractère est défini dans l’éditeur de caractères Microsoft Agent. Elle ne peut pas être modifiée par une application.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md)


 

 




