---
title: Élément BuyCD
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Élément BuyCD
ms.assetid: 01aaf20a-49ee-420b-a612-f09155390d4a
keywords:
- élément BuyCD Lecteur Windows Media
topic_type:
- apiref
api_name:
- BuyCD Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0b2af0f12b06c7d5701db3fcc073d7b7c330e8798408206b64a8b9811f27d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135842"
---
# <a name="buycd-element"></a>Élément BuyCD

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

l’élément **BuyCD** spécifie les url des pages web qui Lecteur Windows Media s’affichent lorsque l’utilisateur choisit d’effectuer un achat.

``` syntax
<BuyCD
    MediaPlayerURL = "URL"
    MediaCenterURL = "URL"
    BrowserURL = "URL"
/>
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="MediaPlayerURL__required_"></span><span id="mediaplayerurl__required_"></span><span id="MEDIAPLAYERURL__REQUIRED_"></span>**MediaPlayerURL** (obligatoire)
</dt> <dd>

URL de la page web que le magasin en ligne affiche pour proposer un CD ou un DVD à acheter dans Lecteur Windows Media.

</dd> <dt>

<span id="MediaCenterURL"></span><span id="mediacenterurl"></span><span id="MEDIACENTERURL"></span>**MediaCenterURL**
</dt> <dd>

URL de la page web que le magasin en ligne affiche pour proposer un CD ou un DVD à acheter dans Windows XP Media Center Edition 2004 Update.

</dd> <dt>

<span id="BrowserURL"></span><span id="browserurl"></span><span id="BROWSERURL"></span>**BrowserURL**
</dt> <dd>

URL de la page Web que le magasin en ligne affiche pour proposer un CD ou un DVD à acheter dans une fenêtre de navigateur distincte. cette URL est également utilisée par Windows XP Service Pack 2 ou une version ultérieure pour la fonctionnalité **online Shop for music** .

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément         |
|-----------------|-----------------|
| Éléments parents | **ServiceInfo** |
| Éléments enfants  | None            |



 

## <a name="remarks"></a>Remarques

quand l’utilisateur clique sur un bouton ou un lien dans Lecteur Windows Media pour acheter un CD ou un DVD, le lecteur envoie la demande d’URL à ServiceTask1 avec des paramètres attachés à l’aide d’un séparateur de chaîne de requête de point d’interrogation ( ?). Le tableau suivant détaille les paramètres envoyés avec la demande d’URL. D’autres peuvent être présents à des fins de compatibilité héritée.



| Nom         | Valeur                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Album*      | Valeur de l’attribut **WM/AlbumTitle** pour l’élément multimédia.                                                                                                        |
| *Peinture*     | Valeur de l’attribut **WM/AlbumArtist** , s’il en existe un, ou la valeur de l’attribut **Author** pour l’élément multimédia.                                         |
| *GeoId*      | Windows l’ID d’emplacement géographique. L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration. |
| *locale*     | ID de paramètres régionaux Lecteur Windows Media.                                                                                                                                     |
| *Titre*      | Valeur de l’attribut **title** pour l’élément multimédia.                                                                                                                |
| *UFID*       | Valeur de l’attribut **WM/UniqueFileIdentifier** pour l’élément multimédia.                                                                                              |
| *UserLocale* | ID de paramètres régionaux Windows. Les paramètres régionaux sont spécifiés par l’utilisateur dans la zone **standards et formats** des paramètres Options régionales et linguistiques du panneau de configuration.        |
| *version*    | Lecteur Windows Media numéro de version en utilisant le format suivant : 10.0. x. xxxx ou 11.0. x. xxxx.                                                                         |



 

Windows XP Media Center Edition 2004 fournit aux utilisateurs une interface utilisateur conçue pour être affichée à distance. Vous devez créer des pages Web pour le paramètre *MediaCenterURL* à afficher sur de grands écrans.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





