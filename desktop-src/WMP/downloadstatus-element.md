---
title: Élément DownloadStatus (msfeeds. h)
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Élément DownloadStatus (msfeeds. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Élément DownloadStatus Windows Media Player
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532673"
---
# <a name="downloadstatus-element"></a>Élément DownloadStatus

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément **DownloadStatus** spécifie une URL que le lecteur Windows Media affiche sous la forme d’un lien pour permettre aux utilisateurs d’afficher l’état du téléchargement.

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="URL"></span><span id="url"></span>URL
</dt> <dd>

URL de la page Web que le magasin en ligne affiche pour afficher l’état du téléchargement à l’utilisateur.

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément         |
|-----------------|-----------------|
| Éléments parents | **ServiceInfo** |
| Éléments enfants  | Aucune            |



 

## <a name="remarks"></a>Notes

Le lecteur Windows Media affiche un message aux utilisateurs lorsqu’un téléchargement est en cours. Si les services actifs actuels définissent une URL d’état de téléchargement, l’utilisateur peut cliquer sur le texte du message. Lorsque l’utilisateur clique sur le message, le lecteur accède à l’URL spécifiée par l’élément **DownloadStatus** afin que le magasin actif actuel puisse fournir des détails sur les téléchargements en cours.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure<br/>                                          |
| En-tête<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





