---
title: Adressage relatif (référence HLSL VS)
description: Pour les nuanceurs de vertex, la syntaxe \ \ ne peut être utilisée que dans les types de registres qui peuvent être traités relativement dans certains modèles de nuanceur.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2bbba694878ba84ac3c2fa9c4e8058bb0d91830e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406692"
---
# <a name="relative-addressing-hlsl-vs-reference"></a>Adressage relatif (référence HLSL VS)

La \[ \] syntaxe peut être utilisée uniquement dans les types de registres qui peuvent être traités relativement dans certains modèles de nuanceur. Les formes de syntaxe prises en charge \[ \] sont répertoriées comme suit :

Où :

-   « R » désigne tout type de Registre pouvant être relativement adressé.
-   « A » désigne tout registre pouvant être utilisé en tant qu’index pour adresser de manière relativement à d’autres registres.
-   N0-ni, M0-MJ et k sont des entiers >= 0.



| \[\]syntaxe                              | Index effectif                       | Exemples                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| R \[ A + M0 +... + MJ \]                  | A + M0 +... + MJ                     | c \[ a0. x + 3 + 7 \]              |
| R \[ k \] (= RK)                         | k                                     | c \[ 10 \] (= C10)              |
| R \[ A \]                                  | Un                                     | c \[ a0. y \]                      |
| RK \[ N0 +... + ni + A + M0 +... + MJ \] | A + k + N0 +... + ni + M0 +... + MJ | C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \] |
| R \[ N0 +... + ni + A + M0 +... + MJ \]  | A + N0 +... + ni + M0 +... + MJ     | c \[ 2 + 1 + al + 3 + 4 + 5 \]    |
| RK \[ A \]                                 | A + k                                 | C12 \[ Al \] , C0 \[ a0. z \]        |
| RK \[ A + M0 +... + MJ \]                 | A + k + M0 +... + MJ                 | v1 \[ al + 4 + 8 \]               |
| R \[ N0 +... + ni + A \]                  | A + N0 +... + ni                     | o \[ 3 + 1 + al \]                |
| RK \[ N0 +... + ni + A \]                 | A + k + N0 +... + ni                 | O1 \[ 2 + 1 + 3 + al \]           |



 

Les registres sont disponibles dans les versions suivantes :



| Type de Registre | Versions de nuanceur vertex |
|---------------|------------------------|
| a0            | Tous                    |
| &            | vs \_ 2 \_ 0 et supérieure    |
| cn            | vs \_ 1 \_ 1 et versions ultérieures    |
| sur            | vs \_ 3 \_ 0               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




