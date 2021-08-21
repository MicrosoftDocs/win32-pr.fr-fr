---
description: Interfaces de diffusion multimédia
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: Interfaces de diffusion multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b38200d98b0f01b7260508cbf7bd19c6e65efdfb3af78f2efff77be38294e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152955"
---
# <a name="multimedia-streaming-interfaces"></a>Interfaces de diffusion multimédia

> [!Note]  
> Ces API sont déconseillées. les Applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.

 

cette section contient des entrées de référence pour toutes les interfaces de diffusion multimédia en continu et leurs méthodes, y compris celles prises en charge par Microsoft DirectShow.



| Interface                                                  | Description                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | gère les connexions internes entre les filtres de DirectShow et les graphiques de filtre dans les applications qui utilisent la diffusion multimédia en continu.                            |
| [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | Contient des méthodes pour manipuler des exemples de flux avec des types de média arbitraires.                                                                            |
| [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | Contient des méthodes pour créer des flux multimédias avec des types de média arbitraires.                                                                            |
| [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | expose les fonctionnalités de DirectShow aux développeurs de flux multimédias.                                                                                       |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | Fournit des méthodes qui permettent aux applications de définir et d’extraire les données audio sous-jacentes auxquelles les flux audio feront référence.                                   |
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | Contrôle les flux de données multimédias audio en fournissant des méthodes qui définissent et obtiennent le format du flux.                                                                 |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | Récupère des informations à partir des objets de données [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) sous-jacents.                                                                |
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Contrôle les flux multimédias qui apparaissent sur les surfaces de® Microsoft® DirectDraw.                                                                                  |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Fournit des méthodes qui définissent et récupèrent des pointeurs vers la surface DirectDraw associée à l’exemple de flux actuel.                                    |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | Permet d’accéder aux caractéristiques d’un flux multimédia, telles que le type de média et l’ID d’objectif du flux. Il comporte également des méthodes qui créent des exemples de données. |
| [**IMediaStreamFilter**](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | Pris en charge par le filtre de flux multimédia, qui est utilisé en interne par l’objet de flux multimédia. .                                                       |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | Contient des méthodes qui définissent et récupèrent les données de mémoire sur les objets de données audio.                                                                               |
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | Fournit des méthodes qui contrôlent un flux multimédia et fournissent l’accès à ses flux de média sous-jacents.                                                   |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | Permet de contrôler le comportement des exemples de flux.                                                                                                   |



 

 

 



