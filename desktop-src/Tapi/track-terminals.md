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
# <a name="track-terminals"></a>Suivre les terminaux

Deux types de terminaux de suivi sont définis : enregistrement du terminal de suivi et du terminal de lecture, qui, respectivement, appartiennent à et sont gérés par le terminal d’enregistrement de fichier et le terminal de lecture de fichier.

Tous les terminaux de suivi exposent les interfaces [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) et [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) . L’interface **ITTerminal** permet de sélectionner des terminaux de suivi sur des flux ou des appels.

> [!Note]  
> Les terminaux de suivi exposent également une interface privée, [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol), que le MSP utilise. Les applications ne doivent pas tenter d’accéder à cette interface.

 

 

 
