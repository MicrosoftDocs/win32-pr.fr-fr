---
description: Passez en revue la liste des valeurs du mode phrase de l’éditeur de méthode d’entrée (IME). Ces valeurs sont utilisées avec les fonctions ImmGetConversionStatus et ImmSetConversionStatus.
ms.assetid: 24b12936-7dfc-4c8d-970c-d8354ad46d1d
title: Valeurs du mode de phrase IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c471282ebf50657b45f7c1c22938b27fff5a62c08c48ab4191dd84048a4b6b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146128"
---
# <a name="ime-sentence-mode-values"></a>Valeurs du mode de phrase IME

Ces valeurs sont utilisées avec les fonctions [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) et [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .



| Constante                  | Définition                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| \_SMODE IME \_ automatique     | L’IME effectue le traitement de la conversion en mode automatique.               |
| \_SMODE IME \_ aucun          | Aucune information pour la phrase.                                               |
| IME \_ SMODE \_ PHRASEPREDICT | L’IME utilise les informations d’expression pour prédire le caractère suivant.             |
| IME \_ SMODE \_ PLURALCLAUSE  | L’IME utilise des informations de clause pluriel pour effectuer le traitement de la conversion. |
| IME \_ SMODE \_ SINGLECONVERT | L’IME effectue le traitement de la conversion en mode à un seul caractère.        |
| \_conversation SMODE \_ IME  | L’IME utilise le mode conversation. Cela est utile pour les applications de conversation.      |



 

Les bits 16 à 31 sont réservés à l’utilisation de l’IME.

 

 



