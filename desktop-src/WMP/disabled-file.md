---
title: Fichier désactivé
description: Fichier désactivé
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Windows Media Player Mobile Skins, fichiers art
- apparences, fichiers artistiques
- fichiers pour les habillages, illustrations
- fichiers art pour les apparences, fichiers désactivés
- Windows Media Player Mobile Skins, fichiers désactivés
- apparences, fichiers désactivés
- Fichiers désactivés dans les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9608c67ded6625d46126955ad42a24548a9d002c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029460"
---
# <a name="disabled-file"></a>Fichier désactivé

Le fichier désactivé contient les images qui seront affichées lorsqu’une fonction de bouton particulière ne peut pas être utilisée ou qu’un état de bouton est désactivé. Par exemple, si une sélection vide est définie, les boutons **suivant** et **préc** s’affichent et ils doivent être affichés à l’aide d’une image désactivée. En outre, pour les boutons bascule, l’image désactivée est utilisée pour indiquer que l’État est désactivé.

L’image suivante est un fichier désactivé standard.

![fichier désactivé](images/cesdkdis.png)

Cela stocke les images des boutons de type d’accès qui sont désactivés. Les images sont similaires au fichier d’arrière-plan, mais les couleurs sont plus claires. À l’aide de l’offset défini dans la section bitmaps du fichier de définition d’apparence, le bouton images est aligné avec l’image de fichier d’arrière-plan.

Notez que l’arrière-plan de l’image de bouton correspond exactement à la zone correspondante dans le fichier d’arrière-plan. C’est important, car lorsqu’un bouton de type d’accès n’est pas disponible, le rectangle entier défini pour l’image désactivée remplace la zone correspondante dans le fichier d’arrière-plan. Conservez le graphique cohérent avec l’image d’arrière-plan pour vous assurer que seules les parties du bouton que vous souhaitez voir apparaître varient.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fichiers art**](art-files-mobile.md)
</dt> </dl>

 

 




