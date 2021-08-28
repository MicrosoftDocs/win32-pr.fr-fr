---
description: Objet de diffusion multimédia en continu et hiérarchie d’interface
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Objet de diffusion multimédia en continu et hiérarchie d’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73da4777c2d05ff6455758ebde6e64a9a4c8277e8445ed59dca7f17088baea0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075765"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>Objet de diffusion multimédia en continu et hiérarchie d’interface

> [!Note]  
> Ces API sont déconseillées. les Applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.

 

Le diagramme suivant illustre la hiérarchie d’objets utilisée dans la diffusion multimédia en continu.

![hiérarchie d’objets multimediastreaming](images/mmstream02.png)

L’architecture de diffusion multimédia en continu définit trois types généraux d’objets :

-   L’objet **AMMultimediaStream** expose l’interface [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) . en interne, cet objet encapsule le graphique de filtre DirectShow.
-   Les objets de *flux de média* exposent l’interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) et sont spécifiques aux données. L’objet AMMultimediaStream contient un ou plusieurs flux de média.
-   Les exemples d’objets *Stream* contiennent les données d’un flux particulier.

Les objets de flux multimédia suivants sont pris en charge :

-   Flux audio. Expose l’interface [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) .
-   Flux DirectDraw. Représente un flux vidéo rendu sur une surface DirectDraw. Expose l’interface [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) .
-   Flux de type de média. Représente des données arbitraires. Expose l’interface [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) .

Chaque objet de flux de média crée son propre type d’objet de flux :

-   Les flux audio créent des échantillons audio qui exposent l’interface [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .
-   Les flux DirectDraw créent des exemples DirectDraw qui exposent l’interface [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) .
-   Les flux de type de média créent des exemples de type de média qui exposent l’interface [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) .

Le diagramme suivant illustre la hiérarchie d’interface pour les interfaces listées précédemment :

![hiérarchie de l’interface multimediastreaming](images/mmstream01.png)

 

 



