---
description: Un terminal multipiste peut être considéré comme un terminal qui est une collection d’autres terminaux. Chaque terminal enfant (un &\# 0034 ; track&\# 0034 ;) peut être un terminal multipiste ou un seul terminal.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: À propos des terminaux multipiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58042236c737f6ab0b933699d75e19358f6e6b81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517070"
---
# <a name="about-multitrack-terminals"></a>À propos des terminaux multipiste

Un terminal multipiste peut être considéré comme un terminal qui est une collection d’autres terminaux. Chaque terminal enfant (une « piste ») peut être un terminal multipiste ou un terminal simple.

Tous les terminaux multipiste exposent l’interface [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , qui comprend des méthodes génériques pour énumérer, créer et supprimer des terminaux de suivi d’un terminal multipiste. Tous les terminaux, une seule piste et multipiste, exposent l’interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .

Un client qui a un pointeur vers une interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) peut déterminer si le terminal est multipiste ou à une seule piste en interrogeant le terminal pour l’interface [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) , qui est exposée uniquement sur les terminaux multipiste.

Le terminal parent peut utiliser l’interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) de ses terminaux de suivi, ou il peut nécessiter le suivi des terminaux pour exposer des interfaces privées.

Pour plus d’informations, consultez [suivre des terminaux](track-terminals.md).

 

 
