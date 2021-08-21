---
title: Conversion en Java à partir de C++
description: À l’aide du langage de programmation C++, les développeurs peuvent accéder directement à la mémoire qui stocke une variable particulière. Les pointeurs de mémoire fournissent cet accès direct. En Java, les pointeurs sont gérés pour vous.
ms.assetid: 2c8de3d9-3410-4153-b612-4afab8a69a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73efe022fa09ce13a2d5e4e04978033fc3ab8f33abb6afb3b5abf493dab12178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047747"
---
# <a name="translating-to-java-from-c"></a>Conversion en Java à partir de C++

À l’aide du langage de programmation C++, les développeurs peuvent accéder directement à la mémoire qui stocke une variable particulière. Les pointeurs de mémoire fournissent cet accès direct. En Java, les pointeurs sont gérés pour vous.

En Java, les types de données composites **struct**, **Union** et **typedef** sont gérés exclusivement par le biais de l’utilisation de classes. Par exemple, le type de données **Variant** C++ est mappé à **com. ms. com. variant** dans Java.

En C++, les chaînes sont un tableau de caractères. En Java, les chaînes sont des objets. Les méthodes qui agissent sur les chaînes traitent la chaîne comme un objet complet.

Les méthodes COM retournent une valeur connue sous le nom de **HRESULT**, qui est un code d’erreur 32 bits. La prise en charge de Java pour Microsoft Internet Explorer définit une classe, **com. ms. com. COMException**, qui encapsule le code d’erreur **HRESULT** .

Java ne prend pas en charge les types de données non signés, à l’exception de **char**, qui est un entier non signé 16 bits. Les méthodes qui acceptent ou retournent d’autres types de données non signés ne peuvent pas être utilisées à partir de Java.

Java ne prend pas en charge les tableaux multidimensionnels. Les méthodes qui acceptent ou retournent des tableaux multidimensionnels ne sont pas disponibles à partir de Java.

Les valeurs booléennes dans Java ne peuvent pas être converties en 0 et 1.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en Java](translating-to-java.md)
</dt> </dl>

 

 




