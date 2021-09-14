---
title: conversion en Visual Basic à partir de C++
description: conversion en Visual Basic à partir de C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095486"
---
# <a name="translating-to-visual-basic-from-c"></a>conversion en Visual Basic à partir de C++

À l’aide du langage de programmation C++, les développeurs peuvent accéder directement à la mémoire qui stocke une variable particulière. Les pointeurs de mémoire fournissent cet accès direct. dans Visual Basic, les pointeurs sont gérés pour vous. par exemple, un paramètre déclaré en tant que pointeur vers un **int** en C++ est équivalent à un paramètre déclaré dans Visual Basic en tant qu' **entier** **ByRef** .

un paramètre déclaré **comme chaîne** dans Visual Basic est déclaré en tant que pointeur vers un **BSTR** en C++. La définition d’un pointeur de chaîne sur **null** en C++ équivaut à définir la chaîne sur la constante **vbNullString** dans Visual Basic. Le passage d’une chaîne de longueur nulle ("") à une fonction conçue pour recevoir la **valeur null** ne fonctionne pas, car il passe un pointeur vers une chaîne de longueur nulle au lieu d’un pointeur zéro.

C++ prend en charge les conteneurs de données, à savoir les structures et les unions, qui n’ont pas d’équivalent dans les premières versions de Visual Basic. C’est la raison pour laquelle les objets COM encapsulent généralement des informations qui sont généralement stockées dans des structures et des unions dans des classes d’objets. Toutefois, certains objets COM peuvent contenir des structures, ce qui entraîne l’inaccessibilité des parties de la fonctionnalité ou des méthodes de l’objet pour Visual Basic.

certains types de données C++ ne sont pas pris en charge dans Visual Basic, par exemple les types non signés et les types **HWND** . Les méthodes qui acceptent ou retournent ces types de données ne sont pas disponibles dans Visual Basic.

Visual Basic utilise des types de données compatibles Automation en tant que types de données internes. Ainsi, les types de données C++ compatibles Automation sont également compatibles avec Visual Basic. Les types de données qui ne sont pas compatibles Automation risquent de ne pas pouvoir être convertis en Visual Basic.

le tableau suivant répertorie les types de données pris en charge par Visual Basic et leurs équivalents **VARTYPE** . **VarType** est une énumération qui répertorie les types variant Automation.



| Type de données Visual Basic  | Équivalent VARTYPE                |
|-------------------------|-----------------------------------|
| **Integer**<br/>  | 16 bits, signé, VT \_ I2<br/> |
| **Long**<br/>     | 32 bits, signés, VT \_ I4<br/> |
| **Date**<br/>     | \_Date VT<br/>               |
| **Devise**<br/> | VT \_ ca<br/>                 |
| **Object**<br/>   | \*\_distribution vt<br/>         |
| **Chaîne**<br/>   | VT \_ BSTR<br/>               |
| **Booléen**<br/>  | VT \_ bool<br/>               |
| **Devise**<br/> | \_valeur décimale VT<br/>            |
| **Unique**<br/>   | VT \_ R4<br/>                 |
| **Double**<br/>   | VT \_ R8<br/>                 |
| **Décimal**<br/>  | \_valeur décimale VT<br/>            |
| **Byte**<br/>     | \_valeur décimale VT<br/>            |
| **Variant**<br/>  | \_variante VT<br/>            |



 

tous les paramètres de Visual Basic, sauf s’ils sont étiquetés avec le mot clé **ByVal**, sont passés par référence (en tant que pointeurs) et non par valeur.

C++ et Visual Basic diffèrent légèrement dans la façon dont ils représentent des propriétés. En C++, les propriétés sont représentées sous la forme d’un ensemble de fonctions d’accesseur, une qui définit la valeur de la propriété et une qui récupère la valeur de la propriété. dans Visual Basic, les propriétés sont représentées sous la forme d’un seul élément qui peut être utilisé pour récupérer ou définir la valeur de la propriété.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en Visual Basic](translating-to-visual-basic.md)
</dt> </dl>

 

 





