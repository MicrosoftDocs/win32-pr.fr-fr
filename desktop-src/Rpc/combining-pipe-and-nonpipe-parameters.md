---
title: Combinaison de paramètres de canal et de pas de canal
description: Combinaison de paramètres de canal et de canalisation dans un appel de procédure distante (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842586"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a>Combinaison de paramètres de canal et de pas de canal

Lorsque vous combinez des types de canal et d’autres types dans un appel de procédure distante, les données sont transmises en fonction de la direction du paramètre :

-   Dans le **\[ \] sens,** les données de tous les arguments non-pipe sont transmises en premier, suivies des données de canal.
-   Dans le **\[ \] sens inverse, le serveur** envoie d’abord les données de canal. Une fois que la routine Manager a été retournée, le serveur transmet les données sans canal.
-   Lorsqu’il y a **\[ dans, \]** les arguments de canal sortant combinés avec **\[ in, out \]** arguments sans canal, d’abord les données d’entrée sont transmises dans son intégralité, comme décrit précédemment. Ensuite, les données de sortie sont transmises comme décrit précédemment.

La restriction suivante s’applique à cette implémentation (MIDL 3,0) de canaux : quand vous combinez des types de canal et d’autres types dans un appel de procédure distante unique, les paramètres non-pipe doivent avoir une taille bien définie pour permettre au compilateur MIDL de calculer la taille de la mémoire tampon nécessaire. Par exemple, vous ne pouvez pas combiner des paramètres de canal à l’aide d’un \[ [](/windows/desktop/Midl/unique) \] pointeur unique ou d’une structure conforme, car leur taille ne peut pas être déterminée au moment de la compilation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[canal](/windows/desktop/Midl/pipe)
</dt> <dt>

[/Oi](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 