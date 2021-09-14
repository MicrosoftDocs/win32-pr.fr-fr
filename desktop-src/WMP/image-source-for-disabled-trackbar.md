---
title: Source de l’image pour le TrackBar désactivé
description: Source de l’image pour le TrackBar désactivé
ms.assetid: ecbe1670-2914-4b66-92bd-d854e6c1e897
keywords:
- Lecteur Windows Media Skins mobiles, trackbars
- habillages, trackbars
- informations de référence sur les habillages, trackbars
- trackbars dans les apparences, source d’image
- source de l’image pour les apparences, trackbars
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbae540f97c7d1f7241035b074f45e6267e51615
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416223"
---
# <a name="image-source-for-disabled-trackbar"></a>Source de l’image pour le TrackBar désactivé

Vous devez définir la source de l’image que vous souhaitez afficher lorsqu’un TrackBar est désactivé, à l’aide du type de bitmap à partir duquel vous souhaitez dessiner l’image. l’image que vous affichez se trouve généralement dans le fichier Super ou si vous créez une apparence pour Lecteur Windows Media 10 Mobile, l’image se trouve dans le fichier SeekThumb. Vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace. Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image à utiliser dans le type de bitmap à partir duquel vous dessinez.

Par exemple, pour utiliser une image de la bitmap SeekThumb qui a une position supérieure et gauche de 50, 60 pixels, tapez :


```C++
Disabled @ 50,60

```



Vous devez définir un emplacement d’image pour une image TrackBar désactivée. Si vous ne souhaitez pas afficher une nouvelle image, vous pouvez définir l’image d’arrière-plan en tant qu’image désactivée avec un décalage de 0, 0 :


```C++
Disabled @ 50,60

```



Dans l’exemple précédent, 50, 60 représente l’emplacement du bouton que vous utilisez dans le fichier SeekThumb (dans ce cas, le même emplacement que le bouton sur la bitmap d’arrière-plan). Toutefois, il est fortement recommandé d’afficher une image désactivée pour tous les trackbars afin de permettre à votre utilisateur d’indiquer visuellement, car trackbars ne sera pas utilisable dans certaines conditions. Par exemple, la recherche trackbars peut être désactivée lorsque la sélection actuelle est vide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




