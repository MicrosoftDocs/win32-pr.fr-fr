---
title: Super fichiers
description: Super fichiers
ms.assetid: a5005d1a-4b87-482d-914e-3184a2c93267
keywords:
- Lecteur Windows Media Skins mobiles, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, fichiers de fichiers Super
- Lecteur Windows Media Skins mobiles, fichiers de fichiers Super
- apparences, Super fichiers
- Super fichiers dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece533f81f8866eb0f9848d7296cc23bcd37f453
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520257"
---
# <a name="super-files"></a>Super fichiers

Les fichiers Super sont utilisés pour stocker les images désactivées pour trackbars. Étant donné que l’image de TrackBar principale est affichée dans le fichier d’arrière-plan et que l’utilisateur appuie sur l’image Thumb, et non sur l’image TrackBar, seule l’image désactivée est nécessaire pour trackbars. Elle est stockée dans le fichier défini par Super dans la section bitmaps du fichier de définition d’apparence. Un fichier Super peut également stocker les images déplacées et désactivées pour d’autres boutons tels que muet, ce qui ne doit pas nécessairement être un bouton de type d’accès.

> [!Note]  
> les fichiers Super art ne sont pas utilisés dans les habillages pour Lecteur Windows Media 10 Mobile ou version ultérieure, car les images désactivées pour seek trackbars se trouvent dans le fichier seekthumb.

 

L’image suivante est un fichier Super standard.

![Super fichier](images/cesdksup.png)

Cela stocke les images désactivées pour trackbars et le bouton muet. Ces images sont décalées comme défini par la section bitmaps.

La zone d’arrière-plan de l’image TrackBar désactivée correspond exactement à la zone correspondante dans le fichier d’arrière-plan. C’est important, car le rectangle entier défini pour l’image TrackBar désactivée remplace la zone correspondante dans le fichier d’arrière-plan. Cela garantit que l’image TrackBar désactivée est mélangée de façon transparente dans l’image d’arrière-plan.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichiers art**](art-files-mobile.md)
</dt> </dl>

 

 




