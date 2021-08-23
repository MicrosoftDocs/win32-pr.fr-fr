---
description: Négociation de type de média EVR
ms.assetid: 3a12b80d-7aac-437d-b515-aab37c1e81b2
title: Négociation de type de média EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6255a32f876a48d0c6193c0a9b470d20ee178ee0ae6fe4c0504b110a353075b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974488"
---
# <a name="evr-media-type-negotiation"></a>Négociation de type de média EVR

Cette rubrique décrit comment le convertisseur de vidéo amélioré (EVR) valide les types de médias.

-   pour le filtre DirectShow EVR, la négociation de type se produit lorsque les codes confidentiels du filtre sont connectés.

-   Pour le récepteur multimédia EVR, les types de média sont définis par le biais de l’interface [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) sur les récepteurs de flux. En général, le chargeur de topologie négocie les types de média, bien que l’application puisse également définir les types de média directement.

EVR ne signale aucun type de média préféré. Le client doit tester les types de média jusqu’à ce qu’il trouve un type acceptable. Le type de média du flux de référence doit être défini pour que les types puissent être définis sur l’un des sous-flux.

Pour le flux de référence, le mixeur EVR obtient une liste de formats de cible d’accélération vidéo compatible DirectX (DXVA). Le présentateur EVR utilise cette liste pour sélectionner le format de la chaîne de permutation Direct3D. Si aucun format de cible de rendu compatible ne peut être trouvé, le EVR rejette le type de média.

Pour les sous-flux, le mélangeur EVR demande si l’appareil DXVA prend en charge ce format de sous-flux en association avec le format de la cible de rendu qui a été sélectionné pour le flux de référence. Par conséquent, les formats de sous-flux disponibles peuvent changer en fonction du flux de référence.

Voici le processus plus en détail. Ces détails ne sont pas importants pour la plupart des applications, mais peuvent être utiles si vous écrivez un mélangeur ou un présentateur personnalisé.

Pour le flux de référence, la négociation se produit comme suit :

1.  EVR appelle [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) sur le mixer.

2.  Le mélangeur convertit le type de média en une description DXVA 2,0, à l’aide de la structure [**\_ VideoDesc DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) .

3.  Le mélangeur appelle [**IDirectXVideoProcessorService :: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) pour obtenir la liste des GUID de processeur vidéo.

4.  Pour chaque GUID de processeur vidéo, le mélangeur appelle [**IDirectXVideoProcessorService :: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) pour obtenir les formats de cible de rendu pris en charge.

5.  EVR appelle [**IMFVideoPresenter ::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) sur le présenteur avec le message MFVP \_ \_ INVALIDATEMEDIATYPE. Ce message force le présentateur à sélectionner un nouveau format.

6.  Le présentateur appelle [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) pour obtenir la liste des formats de sortie disponibles à partir du mélangeur. Le mélangeur génère cette liste à partir des formats obtenus à l’étape 4.

7.  Le présentateur sélectionne un format et appelle [**IMFTransform :: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sur le mélangeur.

Pour les sous-flux, le processus est plus simple :

1.  EVR appelle [**IMFTransform :: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) sur le mixer.

2.  Le mélangeur appelle [**IDirectXVideoProcessorService :: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) pour obtenir la liste des formats de sous-flux disponibles.

3.  Si le format proposé est contenu dans cette liste, le EVR accepte le type d’entrée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> </dl>

 

 



