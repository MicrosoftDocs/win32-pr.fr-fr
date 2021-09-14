---
description: Vous permettent d’effectuer le suivi des cartes au sein des lecteurs. Ces routines utilisent généralement la \_ structure READERSTATE de cicatrices dans un tableau.
ms.assetid: b26b26bf-85ff-435f-a679-7529f19b1c1b
title: Fonctions de suivi des cartes à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde9bebfeea2718ce634d585c2740cb510500ce3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222436"
---
# <a name="smart-card-tracking-functions"></a>Fonctions de suivi des cartes à puce

Les fonctions suivantes vous permettent d’effectuer le suivi des cartes au sein des lecteurs. Ces routines utilisent généralement la structure [**\_ READERSTATE de cicatrices**](/windows/desktop/api/Winscard/ns-winscard-scard_readerstatea) dans un tableau.



| Rubrique                                                | Description                                                                                                                            |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**SCardLocateCards**](/windows/desktop/api/Winscard/nf-winscard-scardlocatecardsa)         | Recherchez une carte dont la [*chaîne ATR*](../secgloss/a-gly.md) correspond à un nom de carte fourni. |
| [**SCardGetStatusChange**](/windows/desktop/api/Winscard/nf-winscard-scardgetstatuschangea) | Bloquer l’exécution jusqu’à ce que la disponibilité actuelle des cartes change.                                                                       |
| [**SCardCancel**](/windows/desktop/api/Winscard/nf-winscard-scardcancel)                   | Terminez les actions en suspens.                                                                                                         |



 

 

 
