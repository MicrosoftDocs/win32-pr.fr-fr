---
title: Éléments obligatoires
description: Éléments obligatoires
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Lecteur Windows Media Skins mobiles, éléments
- apparences, éléments
- fichiers de définition d’apparence, éléments
- éléments, fichiers de définition d’apparence
- éléments, Lecteur Windows Media Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010903"
---
# <a name="required-elements"></a>Éléments obligatoires

Vous devez fournir les éléments suivants dans votre fichier de définition d’apparence :

-   **Titre.** L’en-tête du fichier de définition d’apparence principal est requis. Pour plus d’informations sur la version de l’en-tête, consultez le tableau dans la section [création d’un fichier de définition d’apparence](creating-a-skin-definition-file.md) .
-   **Section Description.** la section Description est requise lors de la création d’habillages pour les Lecteur Windows Media 9 Series pour Windows Mobile. Il doit s’agir de la première section du fichier de définition d’apparence, et il doit spécifier des valeurs valides pour les dimensions. La spécification d’une valeur pour orientation est facultative.
-   **Section bitmaps.** La section bitmaps est obligatoire. En outre, la section bitmaps doit spécifier des noms valides pour les fichiers d’arrière-plan, désactivés, poussés, régionaux et de Super image.
-   **fichiers image.** Vous devez fournir des fichiers d’arrière-plan, désactivés, poussés, régionaux et de Super image dans le cadre de votre apparence. si vous créez des habillages pour Lecteur Windows Media 10 Mobile ou version ultérieure, vous n’avez pas besoin d’inclure des fichiers de région ou de Super image.

Si vous créez une apparence avec uniquement des images définies, l’apparence est visible, mais n’offre aucune fonctionnalité significative à l’utilisateur. Si vous décidez de créer une apparence sans boutons, par exemple pour empêcher l’utilisateur d’ignorer certains contenus, sachez qu’il est toujours possible de mapper les fonctionnalités sur les boutons matériels de l’appareil.

Les fichiers Thumb sont requis et votre trackbars ne peut pas être utilisé sans thumbs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichier de définition d’apparence**](skin-definition-file-mobile.md)
</dt> </dl>

 

 




