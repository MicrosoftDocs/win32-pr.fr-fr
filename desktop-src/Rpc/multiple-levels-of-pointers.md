---
title: Plusieurs niveaux de pointeurs
description: Utilisation de plusieurs niveaux de pointeurs dans l’appel de procédure distante (RPC).
ms.assetid: d45b9b20-3b21-4d46-9097-8aacb4e4e921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a61a917ee29c982505c601d7b0dd0721e94e4678
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119038"
---
# <a name="multiple-levels-of-pointers"></a>Plusieurs niveaux de pointeurs

Lorsqu’il existe plusieurs niveaux de pointeurs, les attributs sont associés au pointeur le plus proche du nom de la variable. Le client est toujours responsable de l’allocation de toute mémoire associée à la réponse.

L’exemple suivant permet au stub d’appeler le serveur sans savoir à l’avance la quantité de données qui seront retournées :

``` syntax
[
    uuid( ...),
    version(3.3),
]
interface AnInterface
{
    HRESULT GetBars([out] long * pSize,
             [out, size_is( , *pSize)]
             BAR ** ppBar);//BAR type defined elsewhere
}
```

Dans cet exemple, le stub transmet au serveur un pointeur unique, que le serveur Initialise à la **valeur null**. Le serveur alloue ensuite un bloc de barres, définit le pointeur, définit l’argument de taille et retourne. Notez que, pour que le serveur ait un effet sur l’appelant, vous devez passer un \[ \] pointeur Ref à un \[ [](/windows/desktop/Midl/unique) \] pointeur unique vers vos données. Notez également que la taille de la virgule \[ [**\_ est**](/windows/desktop/Midl/size-is)(, \* psize), ce qui \] indique que le pointeur de niveau supérieur n’est pas un pointeur de taille, mais que le pointeur de niveau inférieur est.

Côté client, le stub affecte la \* **valeur null** à ppBar avant d’appeler la procédure distante. Le stub alloue ensuite et démarshale le tableau en d’objets de la barre. L’argument Size indique la taille du bloc (et le nombre de barres non marshalées). Le client doit libérer le tableau retourné d’objets de barre lorsqu’il n’est plus nécessaire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**la taille \_ est**](/windows/desktop/Midl/size-is)
</dt> </dl>

 

 