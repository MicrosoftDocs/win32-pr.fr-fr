---
description: Un IME implémente une fonctionnalité appelée &\# 0034 ; reconversion&\# 0034 ;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Utilisation de la reconversion avec un IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd5a0453b6ac94da805e00639d2a7a56fd79deca4027d23d47e33aab93e4009b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146842"
---
# <a name="using-reconversion-with-an-ime"></a>Utilisation de la reconversion avec un IME

Un IME implémente une fonctionnalité appelée « reconversion ». Normalement, le IMM détermine les listes de candidats en fonction uniquement des entrées tapées par l’utilisateur. La reconversion permet au IMM de déterminer un ou plusieurs candidats en fonction de la phrase contenante (le contexte). Les types de reconversion définis sont simple, normal et amélioré.

La reconversion est utile lorsqu’un utilisateur constate une erreur de composition dans un document. L’utilisateur peut sélectionner l’erreur et choisir reconversion dans un menu. L’IME utilise le contexte pour déterminer le meilleur remplacement. L’application peut utiliser [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) pour prendre en charge la reconversion.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du gestionnaire de méthode d’entrée](using-input-method-manager.md)
</dt> </dl>

 

 



