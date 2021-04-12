---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310965"
---
# <a name="iagentballoonexsetnumcharsperline"></a>IAgentBalloonEx::SetNumCharsPerLine

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

Définit le nombre de caractères par ligne qui peuvent être affichés dans la bulle de texte du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.
-   Retourne E \_ INVALIDARG si le paramètre est inférieur à huit.

<dl> <dt>

<span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*
</dt> <dd>

Nombre de lignes à afficher dans la bulle de mot.

</dd> </dl>

La valeur minimale est 8 et la valeur maximale est 255. Si le texte spécifié dans la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) dépasse la taille de la bulle active, agent fait défiler automatiquement le texte dans l’info-bulle.

Le paramètre par défaut est basé sur les paramètres lorsque le caractère est compilé avec l’éditeur de caractères Microsoft Agent.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon::GetNumCharsPerLine**](iagentballoon--getnumcharsperline.md)


 

 




