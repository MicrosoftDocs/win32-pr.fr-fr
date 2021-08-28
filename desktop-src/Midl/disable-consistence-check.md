---
title: Attribut disable_consistency_check
description: Indique à RPC de ne pas appliquer la vérification de cohérence de corrélation.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc88112ac80462daa6c1babdd29799ccf05e33bb4edb52de1ffbbbb00e71352b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807224"
---
# <a name="disable_consistency_check-attribute"></a>désactiver \_ l' \_ attribut de vérification de cohérence

Indique à RPC de ne pas appliquer la vérification de cohérence de corrélation.

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

Pour les paramètres corrélés, RPC s’impose qu’une mémoire tampon non null est transmise lorsque la variable de nombre de corrélations est non null.

## <a name="example"></a>Exemples

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

Si *myString* a la **valeur null**, RPC rejette l’appel, sauf si length a la valeur 0. Notez que RPC autorise la *longueur* à être égale à 0 alors que *MYSTRING* est non null et que RPC traite *myString* comme une allocation de mémoire tampon de longueur 0.

## <a name="remarks"></a>Remarques

Pour désactiver cette vérification, l’IDL peut contenir l' \[ attribut désactiver la \_ \_ vérification \] de cohérence sur un type de paramètre, typedef ou pointeur. Cela permet à RPC de ne pas appliquer la cohérence entre le pointeur de mémoire tampon et la variable de corrélation pour la mémoire tampon vers laquelle pointe le paramètre ou le pointeur.

Pour désactiver la vérification de cohérence pour l’intégralité de la compilation MIDL (et désactiver l’application de la vérification dans tous les cas), vous pouvez utiliser le commutateur de ligne de commande MIDL [/Backward \_ compat MAYBENULL \_ Size](-backward-compat.md) . Cela requiert que la cible de la compilation MIDL soit au moins â € «Target NT60.

 

 




