---
description: La propriété CurrentAudioStream définit ou récupère le numéro du flux audio activé.
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: Propriété CurrentAudioStream
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd814d5b560ed55ea312fbebb8678c67b1422b0cf3d47917fbf772f56a0d3afd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075969"
---
# <a name="currentaudiostream-property"></a>Propriété CurrentAudioStream

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `CurrentAudioStream` propriété définit ou récupère le numéro du flux audio activé.

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière comprise entre 0 et 7 indiquant le flux audio actuel.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture/écriture sans valeur par défaut. Avant de tenter de définir un nouveau flux audio, appelez [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) pour vérifier que le flux est disponible.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



