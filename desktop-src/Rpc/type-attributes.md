---
title: Attributs de type
description: Les attributs de type appel de procédure distante (RPC) et MIDL qui peuvent être appliqués aux déclarations de type.
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5da8f3beb62f443b95a42283d4625200812436bce1bc667edc07d68f2542544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011167"
---
# <a name="type-attributes"></a>Attributs de type

Les attributs de type sont les attributs MIDL qui peuvent être appliqués aux déclarations de type :

-   **\[**[**traitée**](/windows/desktop/Midl/handle)**\]**
-   **\[**[**handle de contexte \_**](/windows/desktop/Midl/context-handle)**\]**
-   **\[**[**type de commutateur \_**](/windows/desktop/Midl/switch-type)**\]**
-   [attributs de type pointeur](three-pointer-types.md)

L’attribut **\[ \_ type \] de commutateur** désigne le type d’un discriminateur d’Union. Cet attribut s’applique uniquement à une Union qui n’est pas encapsulée.

Un handle de contexte est un pointeur avec un attribut de **\[ \_ handle \] de contexte** . L’attribut **\[ \_ handle \] de contexte** vous permet d’écrire des procédures qui maintiennent les informations d’État entre les appels de procédure distante. Un descripteur de contexte avec une valeur non null représente un contexte enregistré et remplit deux fonctions :

-   Côté client, il contient les informations nécessaires à la bibliothèque Runtime RPC pour diriger l’appel au serveur.
-   Côté serveur, il sert de descripteur sur le contexte actif.

L' **\[** [](/windows/desktop/Midl/handle) **\]** attribut handle spécifie qu’un type peut se produire comme handle défini par l’utilisateur (Générique). Cette fonctionnalité permet de concevoir des handles significatifs pour l’application. L’utilisateur doit fournir des routines de liaison et d’annulation de liaison pour effectuer une conversion entre le type de handle défini par l’utilisateur et le type de handle de primitive RPC, **handle \_ t**. Un handle primitif contient des informations de destination significatives pour les bibliothèques Runtime RPC. Un descripteur défini par l’utilisateur ne peut être défini que dans une déclaration de type, et non dans une déclaration de fonction. Un paramètre avec l’attribut **\[ descripteur \]** a un double objectif. Elle est utilisée pour déterminer la liaison pour l’appel et elle est transmise à la procédure appelée en tant que paramètre de données normal.

 

 