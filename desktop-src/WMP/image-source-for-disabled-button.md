---
title: Source de l’image pour le bouton désactivé
description: Source de l’image pour le bouton désactivé
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Lecteur Windows Media Skins mobiles, source d’image de bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a3b31a25eb40d82d33f241a6eaebf690fe11aa2128528739a7e7bbb4dc217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509259"
---
# <a name="image-source-for-disabled-button"></a>Source de l’image pour le bouton désactivé

Vous devez définir la source de l’image que vous souhaitez afficher lorsqu’un bouton est désactivé ou un État qui correspond à OFF. L’image provient du fichier que vous avez défini comme étant désactivé dans la section bitmaps. Vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace. Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées de l’angle supérieur gauche (en pixels) de l’image que vous souhaitez utiliser dans le fichier bitmap. L’emplacement d’affichage de l’image provient des coordonnées définies pour le bouton par rapport à l’image d’arrière-plan, mais l’emplacement à partir duquel elle provient est défini par les deux nombres suivants : « Disabled @ » et est relatif à l’image bitmap désactivée à partir de laquelle vous lisez l’image.

Par exemple, pour utiliser une image de la bitmap désactivée qui se trouve dans le fichier désactivé à un emplacement supérieur et gauche de 50, 60 pixels, utilisez le code suivant :


```C++
Disabled @ 50,60

```



Vous devez définir une image bitmap désactivée. Si vous ne souhaitez pas afficher une image différente, vous pouvez définir la bitmap d’arrière-plan en tant que bitmap désactivé avec un décalage de 0, 0 :


```C++
Disabled @ 50,60

```



Dans l’exemple précédent, 50, 60 correspond à l’emplacement du bouton que vous utilisez dans le fichier désactivé (dans ce cas, le même emplacement que le bouton sur la bitmap d’arrière-plan). Toutefois, il est fortement recommandé d’afficher une image désactivée pour tous les boutons afin de fournir à vos utilisateurs une indication visuelle, car de nombreux boutons ne sont pas utilisables dans certaines conditions, par exemple une sélection vide. Si les utilisateurs savent qu’un bouton est désactivé, ils n’essaient pas de cliquer dessus ou pensent que votre apparence ne fonctionne pas comme prévu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Boutons**](buttons.md)
</dt> </dl>

 

 




