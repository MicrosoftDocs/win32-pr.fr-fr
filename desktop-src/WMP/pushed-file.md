---
title: Fichier Push
description: Fichier Push
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Lecteur Windows Media Skins mobiles, fichiers artistiques
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, les fichiers envoyés
- Lecteur Windows Media Skins mobiles, fichiers envoyés
- apparences, fichiers envoyés
- Fichiers faisant l’objet d’un push dans des habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013232"
---
# <a name="pushed-file"></a>Fichier Push

Le fichier faisant l’objet d’un push contient les images qui seront affichées lorsque l’utilisateur appuie sur un bouton. Vous pouvez également inclure les images normales et faisant l’objet d’un push pour l’état de pause du bouton PlayPause.

L’image suivante est un fichier Push type.

![fichier Push](images/cesdkpus.png)

Cela permet de stocker les images qui seront affichées lorsque les boutons de type d’accès sont frappés. Également stocké dans ce fichier sont les images normales et Push de l’image suspendue du bouton PlayPause. À l’exception des images secondaires PlayPause sur la droite, les autres images de bouton sont alignées avec l’image d’arrière-plan, à l’aide de l’offset défini dans la section bitmaps du fichier de définition d’apparence.

Notez que l’arrière-plan de l’image de bouton correspond exactement à la zone correspondante dans le fichier d’arrière-plan. Cela est important, car quand l’utilisateur appuie sur un bouton de type d’accès, le rectangle entier défini pour l’image Push remplace la zone correspondante dans le fichier d’arrière-plan. Conservez le graphique cohérent avec l’image d’arrière-plan pour vous assurer que seules les parties du bouton que vous souhaitez voir apparaître varient.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichiers art**](art-files-mobile.md)
</dt> </dl>

 

 




