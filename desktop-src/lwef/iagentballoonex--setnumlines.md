---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3951cd4a8593d5e043e1571cdf24e14fdd9d93aef690c057860c2889022aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848719"
---
# <a name="iagentballoonexsetnumlines"></a>IAgentBalloonEx::SetNumLines

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

Définit le nombre de lignes de sortie de texte qui peuvent être affichées dans la bulle de mot du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.
-   Retourne E \_ INVALIDARG si le paramètre est égal à zéro.

<dl> <dt>

<span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*
</dt> <dd>

Nombre de lignes à afficher dans la bulle de mot.

</dd> </dl>

La valeur minimale est 1 et la valeur maximale est 128. Si le texte spécifié dans la méthode [**Speak**](speak-method.md) ou [**Song**](think-method.md) dépasse la taille de la bulle active, agent fait défiler automatiquement le texte dans l’info-bulle.

Cette méthode échoue si le bit de style **SizeToText** Balloon est défini.

Le paramètre par défaut est basé sur les paramètres lorsque le caractère est compilé avec l’éditeur de caractères Microsoft Agent.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon :: GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx :: getStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx :: SetStyle**](iagentballoonex--setstyle.md)


 

 




