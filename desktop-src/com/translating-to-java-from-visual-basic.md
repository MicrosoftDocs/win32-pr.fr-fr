---
title: Conversion en Java à partir de Visual Basic
description: Conversion en Java à partir de Visual Basic
ms.assetid: 2bd61efc-f4f4-46f7-aa5a-f6cefc54d86b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f2660162500ba506fcf8b1a5c24819e60b8765439bb7d033fa9d5312711611e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793588"
---
# <a name="translating-to-java-from-visual-basic"></a>Conversion en Java à partir de Visual Basic

par défaut, Visual Basic transmet les paramètres par référence. Les paramètres qui sont destinés à être passés par valeur uniquement sont spécifiés par le mot clé **ByVal**.

Java ne prend pas en charge les tableaux multidimensionnels. Les méthodes qui acceptent ou retournent des tableaux multidimensionnels ne sont pas disponibles à partir de Java.

Java et Visual Basic diffèrent légèrement selon la façon dont ils représentent des propriétés. En Java, les propriétés sont représentées sous la forme d’un ensemble de fonctions d’accesseur, une qui définit la valeur de la propriété et une qui récupère la valeur de la propriété. dans Visual Basic, les propriétés sont représentées sous la forme d’un seul élément qui peut être utilisé pour récupérer ou définir la valeur de la propriété.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en Java](translating-to-java.md)
</dt> </dl>

 

 




