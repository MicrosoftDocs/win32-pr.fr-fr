---
description: La propriété AudioStreamsAvailable récupère le nombre de flux audio disponibles dans le titre actuel.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Propriété AudioStreamsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07025a3a3bf54ad98d32c54ee3c147bc36489822ef451965e1e0e0da8fe586c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586729"
---
# <a name="audiostreamsavailable-property"></a>Propriété AudioStreamsAvailable

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

La `AudioStreamsAvailable` propriété récupère le nombre de flux audio disponibles dans le titre actuel.

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a>Valeur renvoyée

Retourne une valeur entière comprise entre 1 et 8 représentant le nombre de flux audio disponibles dans le titre actuel.

## <a name="remarks"></a>Remarques

Cette propriété est en lecture seule sans valeur par défaut. L’utilisation principale de plusieurs flux audio consiste à fournir des pistes vidéo dans plusieurs langues. En règle générale, tous les flux audio ne sont pas activés sur un disque. Par exemple, le film de fonctionnalité peut comporter des pistes audio dans trois langues différentes, mais les codes de fin ne peuvent avoir qu’une seule bande anglaise. Pour qu’un utilisateur puisse sélectionner un flux, l’application doit déterminer les flux disponibles dans le titre en cours. Notez que des flux particuliers sont identifiés par un index de 0 à 7.

Les disques présentent généralement un menu présentant les bandes-son disponibles, ce qui permet à l’utilisateur de sélectionner le flux audio à activer.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



