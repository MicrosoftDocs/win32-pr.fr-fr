---
description: 'Deux types de terminaux de suivi sont définis : terminal d’enregistrement des pistes et terminal de lecture qui appartient respectivement à et sont gérés par le terminal d’enregistrement de fichier et le terminal de lecture de fichier.'
ms.assetid: 2c5c485e-d46f-4bfe-8651-5ed021b23b66
title: Suivre les terminaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5bec904b5ae7ac7528c4cf701139e30cc8da05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534664"
---
# <a name="track-terminals"></a><span data-ttu-id="9c94f-103">Suivre les terminaux</span><span class="sxs-lookup"><span data-stu-id="9c94f-103">Track Terminals</span></span>

<span data-ttu-id="9c94f-104">Deux types de terminaux de suivi sont définis : enregistrement du terminal de suivi et du terminal de lecture, qui, respectivement, appartiennent à et sont gérés par le terminal d’enregistrement de fichier et le terminal de lecture de fichier.</span><span class="sxs-lookup"><span data-stu-id="9c94f-104">Two types of track terminals are defined: Recording Track Terminal and Playback Track Terminal, which, respectively, belong to and are managed by File Recording Terminal and File Playback Terminal.</span></span>

<span data-ttu-id="9c94f-105">Tous les terminaux de suivi exposent les interfaces [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) et [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="9c94f-105">All track terminals expose the [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) and [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interfaces.</span></span> <span data-ttu-id="9c94f-106">L’interface **ITTerminal** permet de sélectionner des terminaux de suivi sur des flux ou des appels.</span><span class="sxs-lookup"><span data-stu-id="9c94f-106">The **ITTerminal** interface allows the selection of track terminals onto streams or calls.</span></span>

> [!Note]  
> <span data-ttu-id="9c94f-107">Les terminaux de suivi exposent également une interface privée, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), que le MSP utilise.</span><span class="sxs-lookup"><span data-stu-id="9c94f-107">Track terminals also expose a private interface, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), which the MSP uses.</span></span> <span data-ttu-id="9c94f-108">Les applications ne doivent pas tenter d’accéder à cette interface.</span><span class="sxs-lookup"><span data-stu-id="9c94f-108">Applications should not attempt to access this interface.</span></span>

 

 

 
