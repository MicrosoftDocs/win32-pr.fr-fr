---
description: La méthode GetKaraokeChannelContent récupère une valeur qui indique le type de contenu dans le canal karaoké spécifié dans le flux spécifié.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Méthode GetKaraokeChannelContent
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0353ebda6469627b5f41209b780fc1403c51940705be72d6acaa139d8320f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812489"
---
# <a name="getkaraokechannelcontent-method"></a>Méthode GetKaraokeChannelContent

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `GetKaraokeChannelContent` méthode récupère une valeur qui indique le type de contenu dans le canal karaoké spécifié dans le flux spécifié.

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Spécifie le flux audio sous la forme d’un entier.

</dd> <dt>

<span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*
</dt> <dd>

Spécifie le canal sous la forme d’un entier. Les valeurs possibles pour chaque canal sont les suivantes :



| Valeur  | Description    |
|--------|----------------|
| 0x0001 | Guide vocal 1  |
| 0x0002 | Guide vocal 2  |
| 0x0004 | Guide mélodie 1 |
| 0x0008 | Guide mélodie 2 |
| 0x0010 | Guide mélodie A |
| 0x0020 | Guide mélodie B |
| 0x0040 | Effet sonore A |
| 0x0080 | Effet sonore B |



 

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière dont les bits individuels spécifient le contenu du canal karaoké.

## <a name="remarks"></a>Remarques

La numérotation des canaux audio DVD est basée sur zéro, donc les canaux 2, 3 et 4 sont les canaux karaoké auxiliaires. Une fois la méthode retournée, effectuez une opération and au niveau du bit sur *icontent* pour déterminer le contenu de chaque canal. Étant donné qu’un seul canal peut avoir plusieurs types de contenu enregistrés, vous devez tester toutes les valeurs possibles même si une correspondance est trouvée.

Une fois que l’utilisateur a connaissance du contenu de chaque canal, il doit être en mesure d’ajuster le volume ou d’activer ou de désactiver les canaux individuels en fonction des besoins. Implémentez cette fonctionnalité dans votre application à l’aide de la propriété [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) .

> [!Note]  
> pour lire des disques karaoké, le décodeur audio sur le système de l’utilisateur doit être compatible avec l’implémentation du karaoké DirectShow 8.

 

 

 



