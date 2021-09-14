---
description: Gestion des événements de redessin dans la capture vidéo
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Gestion des événements de redessin dans la capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119894"
---
# <a name="handling-repaint-events-in-video-capture"></a>Gestion des événements de redessin dans la capture vidéo

Si vous générez un graphique de capture vidéo sans utiliser l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) et que vous affichez un aperçu de la vidéo à l’aide de l’ancien filtre de convertisseur vidéo, vous devez remplacer la gestion par défaut des événements de [**\_ redessin ce**](ec-repaint.md) . interrogez le gestionnaire de Graph de filtre de l’interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) et appelez la méthode [**IMediaEvent :: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) avec la valeur EC \_ repaint :


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



Cela évite une erreur possible qui peut endommager votre fichier de capture. Si l’utilisateur couvre et Découvre la fenêtre d’aperçu, le filtre de convertisseur vidéo reçoit un message de \_ peinture WM. par défaut, le convertisseur vidéo demande un nouveau frame, et le gestionnaire de Graph de filtre met en pause le graphique pour signaler une autre image vidéo. Si cela se produit pendant que le graphique écrit un fichier, le fichier est endommagé. La substitution du comportement par défaut \_ de REDESSIN ce par défaut empêche le convertisseur de demander un nouveau Frame.

vous n’avez pas à effectuer cette étape si vous utilisez l’interface **ICaptureGraphBuilder2** , car le générateur de Graph de Capture le fait automatiquement pour vous. En outre, ce n’est pas obligatoire si vous utilisez le convertisseur de mixage vidéo (VMR) pour la version préliminaire. VMR a toujours le frame le plus récent disponible. il n’envoie donc pas d' \_ événements de REDESSIN ce.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées sur la capture](advanced-capture-topics.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



