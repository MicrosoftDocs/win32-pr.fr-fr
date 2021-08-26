---
description: Le terminal de lecture de fichier et le terminal d’enregistrement de fichiers exposent les interfaces ITTerminal et ITMultiTrackTerminal. Ces objets exposent également l’interface ITMediaControl, qui fournit des méthodes d’arrêt, de démarrage et de navigation multimédia.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminal de lecture de fichier et terminal d’enregistrement de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad07ea46e2abf13465ac3344e69f586673c3b29463eac8bdd324966fb838368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100589"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>Terminal de lecture de fichier et terminal d’enregistrement de fichier

Le terminal de lecture de fichier et le terminal d’enregistrement de fichiers exposent les interfaces [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) et [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) . Ces objets exposent également l’interface [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) , qui fournit des méthodes d’arrêt, de démarrage et de navigation multimédia.

Le terminal de lecture de fichier expose l’interface [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) , qui a des méthodes spécifiques à la lecture.

Le terminal d’enregistrement de fichier expose l’interface [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) , qui fournit des méthodes spécifiques à l’enregistrement.

Comme les [terminaux multipiste](multitrack-terminals.md), les terminaux d’enregistrement de fichiers et les terminaux de lecture de fichiers gèrent chacun un ensemble de [terminaux de suivi](track-terminals.md).

 

 
