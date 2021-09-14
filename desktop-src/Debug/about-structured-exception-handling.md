---
description: Les mécanismes de gestion structurée des exceptions et de gestion des arrêts sont des parties entières du système. ils permettent au système d’être robuste. Vous pouvez utiliser ces mécanismes pour créer de manière cohérente des applications fiables et fiables.
ms.assetid: ab5bc1bd-107f-4ed2-b471-a229a76637fe
title: À propos de la gestion structurée des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161e60725f137f379b7d734485fae7cad39ae1be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114625"
---
# <a name="about-structured-exception-handling"></a>À propos de la gestion structurée des exceptions

Les mécanismes de gestion structurée des exceptions et de gestion des arrêts sont des parties entières du système. ils permettent au système d’être robuste. Vous pouvez utiliser ces mécanismes pour créer de manière cohérente des applications fiables et fiables.

La gestion structurée des exceptions est rendue disponible principalement via la prise en charge du compilateur. Par exemple, le compilateur d’optimisation Microsoft C/C++ prend en charge le mot clé **\_ \_ try** qui identifie un corps de code protégé, le mot clé **\_ \_ except** qui identifie un gestionnaire d’exceptions et le mot clé **\_ \_ finally** qui identifie un gestionnaire d’arrêt. Bien que cette vue d’ensemble utilise des exemples spécifiques au compilateur Microsoft C/C++, d’autres compilateurs fournissent également cette prise en charge.

-   [Gestion des exceptions](exception-handling.md)
-   [Gestion des exceptions basée sur des frames](frame-based-exception-handling.md)
-   [Gestion des exceptions vectorisées](vectored-exception-handling.md)
-   [Gestion des arrêts](termination-handling.md)
-   [Syntaxe du gestionnaire](handler-syntax.md)

 

 



