---
title: Règles pour plusieurs canaux
description: Règles pour plusieurs canaux dans un appel unique dans un appel de procédure distante (RPC).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d804c132d7fc859906f065e4c9dc39dd3159519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463530"
---
# <a name="rules-for-multiple-pipes"></a>Règles pour plusieurs canaux

Vous pouvez combiner des \[ paramètres [**in**](/windows/desktop/Midl/in), \] \[ [**out**](/windows/desktop/Midl/out-idl) \] et \[ **in, out** dans une \] combinaison d’un seul appel, mais vous devez traiter les canaux dans un ordre spécifique, comme illustré dans l’exemple de pseudo-code suivant :

> [!Note]  
> Cette fonctionnalité n’est plus prise en charge dans Windows Vista et les plateformes ultérieures.

 

-   Récupérez les données à partir de chaque canal d’entrée, en commençant par le premier paramètre (le plus à gauche) \[ et **en** \] continuant dans l’ordre, en drainant chaque canal avant de commencer à traiter le suivant.
-   Une fois que chaque canal d’entrée a été entièrement traité, envoyez les données pour les canaux de sortie, en commençant à nouveau par le premier \[  \] paramètre out, puis en continuant dans l’ordre, en remplissant chaque canal avant de commencer à traiter le suivant.

``` syntax
//in .IDL file:
void InOutUCharPipe( [in,out] UCHAR_PIPE *uchar_pipe_1, 
                     [out] UCHAR_PIPE * uchar_pipe_2, 
                     [in] UCHAR_PIPE uchar_pipe_3);
 
//remote procedure:
void InOutUCharPipe( UCHAR_PIPE *param1,
                     UCHAR_PIPE *param2,
                     UCHAR_PIPE  param3)
{
    while(!END_OF_PIPE1)
    {
        param1->pull (. . .);
        . . .
    };

    while(!END_OF_PIPE3)
    {
        param3.pull (. . .);
        . . .
    };

    while(!END_OF_PIPE1)
    {
        param1->push (. . .);
        . . .
    };

    while(!END_OF_PIPE2)
    {
        param2->push(. . .);
        . . .
    };
} //end InOutUCharPipe
```

 

 