---
title: Attribut de chaîne dans les tableaux
description: Vous pouvez utiliser l’attribut \ String \ pour les tableaux de caractères unidimensionnels, les tableaux à caractères larges et les tableaux d’octets qui représentent des chaînes de texte.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d56099c9cc2be3638642b20f6d3572786ea0a93f47f8660c2e847c4c06dd3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016659"
---
# <a name="the-string-attribute-in-arrays"></a>\[ \] Attribut de chaîne dans les tableaux

Vous pouvez utiliser l' \[ [](/windows/desktop/Midl/string) \] attribut de chaîne pour les tableaux de caractères unidimensionnels, les tableaux de caractères larges et les tableaux d’octets qui représentent des chaînes de texte. Si vous utilisez l’attribut de **\[ chaîne \]** , le stub client utilise les fonctions **strlen** ou **wstrlen** de la bibliothèque C pour compter le nombre de caractères de la chaîne. Pour éviter des incohérences possibles, MIDL ne vous permet pas d’utiliser l’attribut de **\[ chaîne \]** en même temps que les \[ [premiers attributs \_ is](/windows/desktop/Midl/first-is) \] , \[ [Last \_ is](/windows/desktop/Midl/last-is) \] et \[ [size \_ is](/windows/desktop/Midl/size-is) \] .

Avec les chaînes terminées par un caractère null en C, vous devez autoriser l’espace pour le caractère null à la fin de la chaîne. Par exemple, lorsque vous déclarez une chaîne qui contient jusqu’à 80 caractères, allouez 81 caractères. L’exemple de fichier IDL suivant montre comment déclarer des tableaux avec l’attribut de **\[ chaîne \]** .

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(8.0)
]
interface arraytest
{
  void fArray8([in, out, string] char achArray[]);
}
```

 

 