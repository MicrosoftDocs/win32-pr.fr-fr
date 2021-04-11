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
# <a name="file-playback-terminal-and-file-recording-terminal"></a><span data-ttu-id="be600-104">Terminal de lecture de fichier et terminal d’enregistrement de fichier</span><span class="sxs-lookup"><span data-stu-id="be600-104">File Playback Terminal and File Recording Terminal</span></span>

<span data-ttu-id="be600-105">Le terminal de lecture de fichier et le terminal d’enregistrement de fichiers exposent les interfaces [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) et [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) .</span><span class="sxs-lookup"><span data-stu-id="be600-105">The File Playback Terminal and File Recording Terminal expose the [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) and [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) interfaces.</span></span> <span data-ttu-id="be600-106">Ces objets exposent également l’interface [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) , qui fournit des méthodes d’arrêt, de démarrage et de navigation multimédia.</span><span class="sxs-lookup"><span data-stu-id="be600-106">These objects also expose the [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) interface, which provides methods for stopping, starting, and media navigation.</span></span>

<span data-ttu-id="be600-107">Le terminal de lecture de fichier expose l’interface [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) , qui a des méthodes spécifiques à la lecture.</span><span class="sxs-lookup"><span data-stu-id="be600-107">The File Playback Terminal exposes the [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) interface, which has playback-specific methods.</span></span>

<span data-ttu-id="be600-108">Le terminal d’enregistrement de fichier expose l’interface [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) , qui fournit des méthodes spécifiques à l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="be600-108">The File Recording Terminal exposes the [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) interface, which provides recording-specific methods.</span></span>

<span data-ttu-id="be600-109">Comme les [terminaux multipiste](multitrack-terminals.md), les terminaux d’enregistrement de fichiers et les terminaux de lecture de fichiers gèrent chacun un ensemble de [terminaux de suivi](track-terminals.md).</span><span class="sxs-lookup"><span data-stu-id="be600-109">As [multitrack terminals](multitrack-terminals.md), File Recording Terminal and File Playback Terminal each manage a collection of [track terminals](track-terminals.md).</span></span>

 

 
