---
title: Attributs directionnels (paramètre)
description: Les attributs directionnels décrivent si les données sont transmises du client au serveur, du serveur au client, ou les deux.
ms.assetid: 1e4f92ae-2d98-412f-a693-54bb09ae4674
keywords:
- Appel de procédure distante RPC, décrit, attributs directionnels
- commencer
- out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e08e9ff23e7e12acbd5cf301afe6786599268d2e149878a326a62f79cd91f7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930641"
---
# <a name="directional-parameter-attributes"></a>Attributs directionnels (paramètre)

Les attributs directionnels décrivent si les données sont transmises du client au serveur, du serveur au client, ou les deux. Tous les paramètres du prototype de fonction doivent être associés à des attributs directionnels. Les trois combinaisons possibles d’attributs directionnels sont : 1) \[ [**dans**](/windows/desktop/Midl/in) \] , 2) \[ [**out**](/windows/desktop/Midl/out-idl) \] et 3) \[ **dans**, **out** \] . Ils décrivent la manière dont les paramètres sont transmis entre les appels et les procédures appelées. Quand vous compilez en mode par défaut (Microsoft-Extended) et que vous omettez un attribut directionnel pour un paramètre, le compilateur MIDL utilise une valeur par défaut \[ **dans** \] .

Un \[ [](/windows/desktop/Midl/out-idl) \] paramètre de sortie doit être un pointeur. En fait, l' \[ attribut **out** \] n’est pas significatif lorsqu’il est appliqué à des paramètres qui n’agissent pas comme des pointeurs, car les paramètres de fonction C sont passés par valeur. En C, la fonction appelée reçoit une copie privée de la valeur de paramètre ; elle ne peut pas modifier la valeur de la fonction appelante pour ce paramètre. Toutefois, si le paramètre agit comme un pointeur, il peut être utilisé pour accéder à la mémoire et le modifier. L' \[ attribut **out** \] indique que la fonction serveur doit retourner la valeur à la fonction d’appel du client, et que la mémoire associée au pointeur doit être retournée conformément aux attributs assignés au pointeur.

L’interface suivante montre les trois combinaisons possibles d’attributs directionnels qui peuvent être appliquées à un paramètre. La fonction **InOutProc** est définie dans le fichier IDL comme suit :

``` syntax
void InOutProc ([in]       short     s1,
                [in, out]  short *  ps2,
                [out]      float *  pf3);
```

Le premier paramètre, *S1*, est \[ [**dans**](/windows/desktop/Midl/in) \] uniquement. Sa valeur est transmise à l’ordinateur distant, mais n’est pas retournée à la procédure d’appel. Bien que l’application serveur puisse modifier sa valeur pour *S1*, la valeur *S1* sur le client est identique avant et après l’appel.

Le deuxième paramètre, *PS2*, est défini dans le prototype de fonction en tant que pointeur avec les deux \[ attributs [**in**](/windows/desktop/Midl/in) \] et \[ [**out**](/windows/desktop/Midl/out-idl) \] . L' \[ attribut **in** \] indique que la valeur du paramètre est passée du client au serveur. L' \[ attribut **out** \] indique que la valeur désignée par *PS2* est retournée au client.

Le troisième paramètre est \[ uniquement [**sortant**](/windows/desktop/Midl/out-idl) \] . L’espace est alloué pour le paramètre sur le serveur, mais la valeur n’est pas définie à l’entrée. Comme indiqué ci-dessus, tous les paramètres de \[ **sortie** \] doivent être des pointeurs.

La procédure distante modifie la valeur des trois paramètres, mais seules les nouvelles valeurs des \[ [](/windows/desktop/Midl/out-idl) \] paramètres out et \[ [**in**](/windows/desktop/Midl/in) \] sont disponibles pour le client.


```C++
#define MAX 257

void InOutProc(short    s1,
               short * ps2,
               float * pf3)
{
    *pf3 = (float) s1 / (float) *ps2;
    *ps2 = (short) MAX - s1;
    s1++;  // in only; not changed on the client side
    return;
}
```



Au retour de l’appel à **InOutProc**, les deuxième et troisième paramètres sont modifiés. Le premier paramètre, qui est \[ uniquement [**dans**](/windows/desktop/Midl/in) \] , est inchangé.

![paramètres in](images/prog-a22.png)

![out (paramètres)](images/prog-a23.png)

![paramètres en sortie](images/prog-a21.png)

 

 