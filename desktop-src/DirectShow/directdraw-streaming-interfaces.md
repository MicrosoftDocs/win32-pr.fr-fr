---
description: Interfaces de streaming DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Interfaces de streaming DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006648"
---
# <a name="directdraw-streaming-interfaces"></a>Interfaces de streaming DirectDraw

> [!Note]  
> Ces API sont déconseillées. les Applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.

 

Si vous utilisez des formats vidéo pris en charge par DirectDraw dans vos flux, les interfaces suivantes vous offrent un contrôle plus puissant des données que les interfaces de base plus génériques.



| Interface                                                  | Description                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Définit et récupère le format de flux et l’objet DirectDraw associé au flux multimédia ; Cette interface est dérivée de [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream). Vous pouvez également utiliser cette interface pour créer des exemples vidéo. |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Vous permet d’attacher des échantillons vidéo à des surfaces DirectDraw ; Cette interface est dérivée de l’interface [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) . Chaque surface attachée comprend un rectangle de découpage pour faciliter le rendu. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liste des interfaces de diffusion multimédia](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



