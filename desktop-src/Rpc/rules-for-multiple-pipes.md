---
title: Règles pour plusieurs canaux
description: Règles pour plusieurs canaux dans un appel unique dans un appel de procédure distante (RPC).
ms.assetid: 1d0b2aed-27cc-4e74-9307-ada86bda4596
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1fd2de7a44f63d5c943f1d6526ee328bbae3e63c99bac118ec843ad266d1f7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925976"
---
# <a name="rules-for-multiple-pipes"></a>Règles pour plusieurs canaux

Vous pouvez combiner des \[ paramètres [**in**](/windows/desktop/Midl/in), \] \[ [**out**](/windows/desktop/Midl/out-idl) \] et \[ **in, out** dans une \] combinaison d’un seul appel, mais vous devez traiter les canaux dans un ordre spécifique, comme illustré dans l’exemple de pseudo-code suivant :

> [!Note]  
> cette fonctionnalité n’est plus prise en charge dans les plateformes Windows Vista et versions ultérieures.

 

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

 

 