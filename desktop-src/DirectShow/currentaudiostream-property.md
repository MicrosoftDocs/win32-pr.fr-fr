---
description: La propriété CurrentAudioStream définit ou récupère le numéro du flux audio activé.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Propriété CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512865"
---
# <a name="currentaudiostream-property"></a>Propriété CurrentAudioStream

> [!Note]  
> Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CurrentAudioStream` propriété définit ou récupère le numéro du flux audio activé.

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière comprise entre 0 et 7 indiquant le flux audio actuel.

## <a name="remarks"></a>Notes

Cette propriété est en lecture/écriture sans valeur par défaut. Avant de tenter de définir un nouveau flux audio, appelez [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) pour vérifier que le flux est disponible.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



