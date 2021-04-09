---
title: Attribut de chaîne dans les tableaux
description: Vous pouvez utiliser l’attribut \ String \ pour les tableaux de caractères unidimensionnels, les tableaux à caractères larges et les tableaux d’octets qui représentent des chaînes de texte.
ms.assetid: 96cebb84-6123-4bf8-b70b-a4f6d48cce52
keywords:
- string
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e8bd2f7234b2713b6a7df05cfb5d6ae4c08b2d8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102004"
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

 

 