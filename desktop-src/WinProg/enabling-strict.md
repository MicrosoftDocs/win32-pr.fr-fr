---
title: Activation du STRICT
description: Lorsque vous définissez le symbole STRICT, vous activez des fonctionnalités qui requièrent plus de soin pour déclarer et utiliser des types.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295091"
---
# <a name="enabling-strict"></a>Activation du STRICT

Lorsque vous définissez le symbole **strict** , vous activez des fonctionnalités qui requièrent plus de soin pour déclarer et utiliser des types. Cela vous permet d’écrire du code plus portable. Cela permet également de réduire le temps de débogage. L’activation de **strict** redéfinit certains types de données afin que le compilateur n’autorise pas l’affectation d’un type à un autre sans cast explicite. cela est particulièrement utile avec Windows code. Les erreurs lors du passage de types de données sont signalées au moment de la compilation au lieu de provoquer des erreurs irrécupérables au moment de l’exécution.

Avec Visual C++, la vérification de type **stricte** est définie par défaut.

pour définir **STRICT** au niveau fichier par fichier, insérez une instruction **\# define** avant d’inclure Windows. h :


```C++
#define STRICT
#include <windows.h>
```



Lorsque **strict** est défini, les définitions de [type de données](windows-data-types.md) changent comme suit :

-   Les types de handles spécifiques sont définis comme s’excluant mutuellement ; par exemple, vous ne pourrez pas passer un **HWND** où un argument de type **HDC** est requis. Sans **strict**, tous les handles sont définis comme **handle**, donc le compilateur ne vous empêche pas d’utiliser un type de handle où un autre type est attendu.
-   Tous les types de fonctions de rappel (tels que les procédures de dialogue, les procédures de fenêtre et les procédures de Hook) sont définis avec des prototypes complets. Cela vous empêche de déclarer des fonctions de rappel avec des listes de paramètres incorrectes.
-   Les types de paramètre et de valeur de retour qui doivent utiliser un pointeur générique sont déclarés correctement comme **LPVOID** au lieu de **LPSTR** ou d’un autre type de pointeur.
-   La structure [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) est déclarée en fonction de la norme ANSI.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Désactivation de STRICT](disabling-strict.md)
</dt> <dt>

[Conformité STRICTe](strict-compliance.md)
</dt> </dl>

 

 
