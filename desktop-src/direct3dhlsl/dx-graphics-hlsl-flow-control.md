---
title: Contrôle de flux
description: La plupart du matériel est conçu pour exécuter le code de nuanceur ligne par ligne, en exécutant chaque instruction HLSL une seule fois.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916304"
---
# <a name="flow-control"></a>Contrôle de flux

La plupart du matériel est conçu pour exécuter le code de nuanceur ligne par ligne, en exécutant chaque instruction HLSL une seule fois. Une instruction Flow-Control détermine au moment de l’exécution le bloc d’instructions HLSL à exécuter ensuite. À l’aide d’une instruction de contrôle de Flow, un nuanceur peut parcourir un ensemble d’instructions ou sauter (branche) à une instruction autre que celle sur la ligne suivante. Certaines instructions de contrôle de Flow prennent en charge le contrôle statique spécifié au moment de la compilation. d’autres proposent un contrôle prédicat qui est une décision par composant effectuée au moment de l’exécution, et d’autres encore prennent en charge le contrôle dynamique, qui est une décision prise au moment de l’exécution en fonction du contenu d’une variable.

Le langage HLSL prend en charge les instructions de contrôle de Flow suivantes.

-   [break](dx-graphics-hlsl-break.md)
-   [pouvoir](dx-graphics-hlsl-continue.md)
-   [refuser](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md)
-   [switch](dx-graphics-hlsl-switch.md)
-   [durant](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Syntaxe du langage (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




