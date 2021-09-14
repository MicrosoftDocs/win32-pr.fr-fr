---
title: " define"
description: La directive \ define assigne la valeur donnée au nom spécifié. Toutes les occurrences ultérieures du nom sont remplacées par la valeur.
ms.assetid: 2699d2dc-caf8-47d6-8b2e-526357962532
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 557c6b486d9c2bd07b0b012c17e806f5d9eaae91
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294155"
---
# <a name="define"></a>\#définition

La directive **\# define** assigne la valeur donnée au nom spécifié. Toutes les occurrences ultérieures du nom sont remplacées par la valeur.

``` syntax
#define name value
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nomme*
</dt> <dd>

Nom à définir. Cette valeur correspond à toute combinaison de lettres, de chiffres et de signes de ponctuation valide pour le préprocesseur C/C++.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*ajoutée*
</dt> <dd>

Entier, chaîne de caractères ou ligne de texte.

</dd> </dl>

## <a name="example"></a>Exemple

Cet exemple assigne des valeurs à des noms non nuls et USERCLASS :

``` syntax
#define     NONZERO     1
#define     USERCLASS   "MyControlClass"
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur](preprocessor-directives.md)
</dt> </dl>

 

 




