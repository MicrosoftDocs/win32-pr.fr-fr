---
description: Les mécanismes de gestion structurée des exceptions et de gestion des arrêts sont des parties entières du système. ils permettent au système d’être robuste. Vous pouvez utiliser ces mécanismes pour créer de manière cohérente des applications fiables et fiables.
ms.assetid: ab5bc1bd-107f-4ed2-b471-a229a76637fe
title: À propos de la gestion structurée des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a0f21a212e95df51dbf92a32073bdd91b771f3efaee864eadbe1a12c8a0fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131649"
---
# <a name="about-structured-exception-handling"></a>À propos de la gestion structurée des exceptions

Les mécanismes de gestion structurée des exceptions et de gestion des arrêts sont des parties entières du système. ils permettent au système d’être robuste. Vous pouvez utiliser ces mécanismes pour créer de manière cohérente des applications fiables et fiables.

La gestion structurée des exceptions est rendue disponible principalement via la prise en charge du compilateur. Par exemple, le compilateur d’optimisation Microsoft C/C++ prend en charge le mot clé **\_ \_ try** qui identifie un corps de code protégé, le mot clé **\_ \_ except** qui identifie un gestionnaire d’exceptions et le mot clé **\_ \_ finally** qui identifie un gestionnaire d’arrêt. Bien que cette vue d’ensemble utilise des exemples spécifiques au compilateur Microsoft C/C++, d’autres compilateurs fournissent également cette prise en charge.

-   [Gestion des exceptions](exception-handling.md)
-   [Gestion des exceptions basée sur des frames](frame-based-exception-handling.md)
-   [Gestion des exceptions vectorisées](vectored-exception-handling.md)
-   [Gestion des arrêts](termination-handling.md)
-   [Syntaxe du gestionnaire](handler-syntax.md)

 

 



