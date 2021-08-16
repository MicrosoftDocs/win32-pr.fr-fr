---
title: Source de l’image Push
description: Source de l’image Push
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Lecteur Windows Media Skins mobiles, source d’image de bouton
- apparences, source de l’image du bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, source d’image
- source d’image pour les apparences, boutons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b336f19900b53a4ae9fff39ce76af9fe52daac4de9e94fb09dcf7b0561f1dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861839"
---
# <a name="pushed-image-source"></a>Source de l’image Push

Vous devez définir la source de l’image que vous souhaitez afficher lorsque l’utilisateur exécute un push sur un bouton. L’image provient du fichier que vous avez défini comme faisant l’objet d’un push dans la section bitmaps. Vous devez entrer le type d’image suivi d’un espace et du symbole @ et d’un autre espace. Vous devez ensuite entrer deux entiers positifs qui définissent les coordonnées supérieure et gauche (en pixels) de l’image que vous souhaitez utiliser dans le fichier d’image faisant l’objet d’un push. L’emplacement d’affichage de l’image provient des coordonnées définies pour le bouton par rapport à l’image d’arrière-plan. Toutefois, l’emplacement à partir duquel il provient est défini par les deux nombres suivants « push @ » et est relatif à l’image Poussée à partir de laquelle vous lisez l’image.

Par exemple, pour utiliser une image de l’image faisant l’objet d’un push qui se trouve dans le fichier ayant fait l’objet d’un push dont l’emplacement en haut à gauche est de 50, 60, utilisez le code suivant :


```C++
Pushed @ 50,60

```



Si vous ne souhaitez pas afficher une autre image, vous pouvez définir la bitmap d’arrière-plan en tant que bitmap push. Pour ce faire, spécifiez le fichier d’arrière-plan comme fichier faisant l’objet d’un push et spécifiez le décalage vers l’angle supérieur gauche du bouton :


```C++
Pushed @ 50,60

```



Si vous procédez ainsi, aucun de vos boutons ne peut afficher une image faisant l’objet d’un push. Nous vous recommandons d’afficher une image Push pour tous les boutons pour donner une indication visuelle à votre utilisateur, car il n’est pas toujours évident de savoir si un TAP produit un résultat, en particulier lorsque la musique est jouée ou que le bruit de frappe est désactivé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Boutons**](buttons.md)
</dt> </dl>

 

 




