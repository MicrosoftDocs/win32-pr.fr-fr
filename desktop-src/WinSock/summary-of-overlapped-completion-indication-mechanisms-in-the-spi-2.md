---
description: Résumé des mécanismes d’indication de la saisie semi-automatique avec chevauchement dans le SPI de Windows Sockets (Winsock).
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Résumé des mécanismes d’indication de la saisie semi-automatique avec chevauchement dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112999"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a>Résumé des mécanismes d’indication de la saisie semi-automatique avec chevauchement dans le SPI

Le tableau suivant résume la sémantique de saisie semi-automatique pour un socket Overlapped, en présentant les différentes combinaisons de *lpOverlapped*, **hEvent** et *lpCompletionRoutine*.



| *lpOverlapped* | **hEvent**     | *lpCompletionRoutine* | Indication de la saisie semi-automatique                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | Non applicable | Ignoré               | L’opération se termine de façon synchrone, autrement dit, elle se comporte comme s’il s’agissait d’un socket nonoverlapped.                                                                                                                                 |
| non NULL       | NULL           | NULL                  | L’opération se termine, mais il n’existe pas de mécanisme de saisie semi-automatique pris en charge par Windows Sockets 2. Le mécanisme de port de terminaison (s’il est pris en charge) peut être utilisé dans ce cas, sinon aucune notification de fin d’exécution n’est appliquée. |
| non NULL       | non NULL       | NULL                  | L’opération termine la superposition, la notification par l’objet d’événement de signalisation.                                                                                                                                                      |
| non NULL       | Ignoré        | non NULL              | L’opération se termine par la routine de fin de la planification.                                                                                                                                               |



 

 

 



