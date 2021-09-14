---
description: Développement d’encodeur et de décodeur
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Développement d’encodeur et de décodeur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094773"
---
# <a name="encoder-and-decoder-development"></a>Développement d’encodeur et de décodeur

Cette section contient des articles sur le développement d’encodeurs et de décodeurs pour DirectShow. Ces rubriques ne sont pas pertinentes pour les développeurs d’applications.

un décodeur logiciel qui prend en charge DirectX Video Acceleration (VA) doit être implémenté en tant que DirectShow filtre de copie de copie. Si le décodeur ne prend pas en charge DirectX VA, il peut également être implémenté en tant qu’objet de média DirectX (DMO). Un décodeur qui se connecte à un convertisseur vidéo ne doit pas être implémenté comme un filtre TRANS-in-place, car cela entraîne une dégradation significative des performances. Pour plus d’informations sur l’écriture d’un filtre de transformation de copie, consultez [écriture de filtres de transformation](writing-transform-filters.md).

Les encodeurs logiciels peuvent être implémentés en tant que filtres de transformation ou DMOs. Les encodeurs n’utilisent pas DirectX VA, car DirectX VA est actuellement utilisé uniquement pour la décompression. La spécification de l’API d’encodeur décrite dans cette section s’applique aux encodeurs matériels et logiciels.

Cette section contient les rubriques suivantes :

-   [API d’encodeur](encoder-api.md)
-   [Interfaces et spécifications du décodeur](decoder-interfaces-and-specifications.md)
-   [décodeur Paramètres pour Windows édition Media Center](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation de VMR pour les développeurs de filtre DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



