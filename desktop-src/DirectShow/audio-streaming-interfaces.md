---
description: Interfaces de streaming audio
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Interfaces de streaming audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112158"
---
# <a name="audio-streaming-interfaces"></a>Interfaces de streaming audio

> [!Note]  
> Ces API sont déconseillées. les Applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.

 



| Interface                                        | Description                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | Contrôle les flux de média audio. Cette interface hérite de l’interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) et est utilisée pour créer un ou plusieurs objets [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) . Il est également utilisé pour définir et récupérer le format actuel des données de flux.                                                                                                            |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | Récupère des informations à partir des objets de données [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) sous-jacents.                                                                                                                                                                                                                                                                                                        |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | Contient des méthodes qui définissent et récupèrent les données de mémoire sur les objets de données audio. Les objets de données audio fournissent les données sous-jacentes auxquelles les exemples de flux accèdent. Cette interface fournit un moyen d’initialiser les mémoires tampons de mémoire et de définir les quantités réelles de données audio dans les objets. En outre, la méthode [**IMemoryData :: GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) peut être utilisée pour récupérer des données de mémoire audio. |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | Fournit des méthodes qui permettent aux applications de définir et d’extraire les données audio sous-jacentes auxquelles les flux audio feront référence. Le format de données audio est défini dans la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liste des interfaces de diffusion multimédia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
