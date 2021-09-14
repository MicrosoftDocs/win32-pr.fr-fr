---
title: Conversion en C++ à partir de Visual Basic
description: Visual Basic gère les pointeurs implicitement. En C++, votre application est chargée d’effectuer les opérations arithmétiques de pointeur nécessaires.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221649"
---
# <a name="translating-to-c-from-visual-basic"></a>Conversion en C++ à partir de Visual Basic

Visual Basic gère les pointeurs implicitement. En C++, votre application est chargée d’effectuer les opérations arithmétiques de pointeur nécessaires.

par défaut, Visual Basic transmet les paramètres par référence (en tant que pointeurs). Les paramètres qui sont destinés à être passés par valeur uniquement sont spécifiés par le mot clé **ByVal**. par exemple, un paramètre de **type entier** **ByVal** â dans Visual Basic équivaut à un paramètre **short** en C++, alors qu’un paramètre de **type entier** **ByRef** â dans Visual Basic équivaut à un paramètre **short \*** .

un paramètre déclaré **comme chaîne** dans Visual Basic est déclaré en tant que pointeur vers un **BSTR** en C++. La définition d’un pointeur de chaîne sur **null** en C++ équivaut à définir la chaîne sur la constante **vbNullString** dans Visual Basic. La transmission d’une chaîne de longueur nulle ("") à une fonction conçue pour recevoir la **valeur null** ne fonctionne pas, car elle passe un pointeur vers une chaîne de longueur nulle au lieu d’un pointeur zéro.

C++ et Visual Basic diffèrent légèrement dans la façon dont ils représentent des propriétés. En C++, les propriétés sont représentées sous la forme d’un ensemble de fonctions d’accesseur, une qui définit la valeur de la propriété et une qui récupère la valeur de la propriété. dans Visual Basic, les propriétés sont représentées sous la forme d’un seul élément qui peut être utilisé pour récupérer ou définir la valeur de la propriété.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traduire en C++](translating-to-c--.md)
</dt> </dl>

 

 




