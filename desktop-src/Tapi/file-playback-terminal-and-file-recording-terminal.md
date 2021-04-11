---
description: Le terminal de lecture de fichier et le terminal d’enregistrement de fichiers exposent les interfaces ITTerminal et ITMultiTrackTerminal. Ces objets exposent également l’interface ITMediaControl, qui fournit des méthodes d’arrêt, de démarrage et de navigation multimédia.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminal de lecture de fichier et terminal d’enregistrement de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a73c788e3e1750e44298c1020a088cf8111bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951964"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>Terminal de lecture de fichier et terminal d’enregistrement de fichier

Le terminal de lecture de fichier et le terminal d’enregistrement de fichiers exposent les interfaces [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) et [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) . Ces objets exposent également l’interface [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) , qui fournit des méthodes d’arrêt, de démarrage et de navigation multimédia.

Le terminal de lecture de fichier expose l’interface [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) , qui a des méthodes spécifiques à la lecture.

Le terminal d’enregistrement de fichier expose l’interface [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) , qui fournit des méthodes spécifiques à l’enregistrement.

Comme les [terminaux multipiste](multitrack-terminals.md), les terminaux d’enregistrement de fichiers et les terminaux de lecture de fichiers gèrent chacun un ensemble de [terminaux de suivi](track-terminals.md).

 

 
