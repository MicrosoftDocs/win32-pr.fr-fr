---
title: Exclusion mutuelle
description: Exclusion mutuelle
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- Windows Media Format SDK, exclusion mutuelle
- ASF (Advanced Systems Format), exclusion mutuelle
- ASF (format des systèmes avancés), exclusion mutuelle
- Kit de développement logiciel (SDK) Windows Media format, exclusion mutuelle MBR
- ASF (Advanced Systems Format), exclusion mutuelle MBR
- ASF (format des systèmes avancés), exclusion mutuelle MBR
- Windows Media Format SDK, débit binaire multiple (MBR)
- ASF (Advanced Systems Format), à débit binaire multiple (MBR)
- ASF (format de systèmes avancés), débit binaire multiple (MBR)
- exclusion mutuelle, à propos de
- débit binaire multiple (MBR), exclusion mutuelle
- MBR (débit binaire multiple), exclusion mutuelle
- exclusion mutuelle, vitesse de transmission
- exclusion mutuelle, langue
- exclusion mutuelle, présentation
- exclusion mutuelle, inconnue
- exclusion mutuelle, fonctionnalités
- exclusion mutuelle, fonctionnalités avancées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840773"
---
# <a name="mutual-exclusion"></a>Exclusion mutuelle

Chaque fichier ASF contient un ou plusieurs flux, chacun contenant des données multimédias numériques. Dans des circonstances normales, chaque flux est associé à une seule sortie. Lors de la lecture, l’objet lecteur fournit des exemples pour chaque sortie. Ainsi, par défaut, chaque flux d’un fichier ASF est remis par le lecteur lors de la lecture.

Dans certains cas, vous ne souhaitez pas que tous les flux soient remis au client. Par exemple, si vous créez un fichier vidéo avec cinq flux audio, un pour chacune des cinq langues, vous n’avez besoin que d’un seul d’entre eux à la fois. L’exclusion mutuelle est une fonctionnalité du kit de développement logiciel (SDK) Windows Media format qui vous permet de spécifier un nombre de flux mutuellement exclusifs qui correspondent tous à la même sortie.

L’exclusion mutuelle est définie dans le profil utilisé pour créer un fichier. Vous configurez l’exclusion mutuelle dans un profil à l’aide d’objets d’exclusion mutuelle. Vous ajoutez des flux un à la fois à l’objet exclusion mutuelle, définissez le type et incluez l’objet dans le profil.

Le kit de développement logiciel (SDK) Windows Media format reconnaît quatre types d’exclusion mutuelle :

-   Vitesse de transmission
-   Language
-   Présentation
-   Unknown

## <a name="mutual-exclusion-by-bit-rate"></a>Exclusion mutuelle par vitesse de transmission

L’exclusion mutuelle de la vitesse de transmission est un type spécial d’exclusion mutuelle qui est plus communément appelée exclusion mutuelle de la vitesse de transmission multiple (MBR). Une exclusion mutuelle MBR contient un certain nombre de flux qui proviennent de la même entrée, mais qui sont encodés à des vitesses de transmission différentes. Lors de la lecture d’un fichier avec MBR, le lecteur détermine le meilleur flux à utiliser en fonction de la bande passante disponible.

Le kit de développement logiciel (SDK) Windows Media format prend en charge MBR pour les flux audio et vidéo. Le kit de développement logiciel (SDK) prend également en charge un type spécial de vidéo MBR appelée plusieurs MBR de taille vidéo. C’est comme une vidéo MBR normale, à la différence que les flux individuels peuvent avoir des tailles de frame différentes. Par exemple, vous pouvez avoir des flux à la taille vidéo 320 x 240 par défaut et d’autres avec des taux de bits plus élevés et une taille vidéo de 640 x 480.

## <a name="mutual-exclusion-by-language"></a>Exclusion mutuelle par langue

L’exclusion mutuelle basée sur le langage est conçue pour être utilisée avec du contenu (généralement audio) enregistré dans plusieurs langues. Une exclusion mutuelle basée sur le langage comprend plusieurs flux provenant d’entrées uniques. Chaque entrée est du même contenu, mais dans une langue différente.

Pour que l’exclusion mutuelle par langue fonctionne, l’application de lecture doit inclure une logique pour sélectionner la langue appropriée. Si vous écrivez une application pour lire des fichiers ASF et que vous souhaitez prendre en charge des fichiers avec l’exclusion mutuelle basée sur la langue, vous devez sélectionner le flux approprié avant de commencer la lecture.

## <a name="mutual-exclusion-by-presentation"></a>Exclusion mutuelle par présentation

L’exclusion mutuelle basée sur la présentation est fournie pour prendre en charge les flux vidéo qui contiennent le même contenu encodé avec des proportions différentes. En règle générale, cette fonction est utilisée pour fournir une vidéo dans une version de bandes (proportions 16:9), ainsi qu’une mise en forme pour les écrans de télévision (proportions 4:3).

La sélection d’une présentation pour la lecture est généralement déterminée par l’utilisateur. Si vous écrivez une application pour lire des fichiers ASF et souhaitez prendre en charge des fichiers avec l’exclusion mutuelle basée sur une présentation, vous devez présenter à l’utilisateur la possibilité de sélectionner un type de présentation à afficher.

## <a name="unknown-mutual-exclusion"></a>Exclusion mutuelle inconnue

Vous pouvez créer une exclusion mutuelle en fonction des critères de votre choix. Tous les types d’exclusion mutuelle personnalisés doivent être créés à l’aide du type inconnu.

## <a name="advanced-mutual-exclusion-features"></a>Fonctionnalités avancées d’exclusion mutuelle

Vous pouvez également utiliser l’exclusion mutuelle pour affecter des flux à des groupes qui s’excluent mutuellement les uns des autres. Par exemple, vous souhaiterez peut-être avoir des flux audio dans plusieurs langues et affecter un flux de vidéo différent à chacun d’entre eux. Vous utilisez l’exclusion mutuelle pour regrouper chaque flux audio avec son flux vidéo correspondant et rendre tous les groupes mutuellement exclusifs.

Le lecteur sélectionne automatiquement les flux pour toutes les exclusions mutuelles. Pour tous les types d’exclusion mutuelle, à l’exception de MBR et de l’exclusion mutuelle basée sur le langage, le lecteur sélectionne toujours le flux par défaut, qui est le premier flux ajouté à l’objet d’exclusion mutuelle dans le profil. Pour MBR, le lecteur sélectionne le flux qui correspond le mieux à la bande passante disponible au moment de la lecture. Si vous ne souhaitez pas utiliser le flux par défaut, vous pouvez définir la sélection de flux sur manuel avant de commencer à lire un fichier.

La sélection manuelle de flux s’applique à l’ensemble du fichier. Des problèmes peuvent survenir lorsque vous avez des exclusions mutuelles de types différents dans le même fichier. Par exemple, un fichier peut contenir à la fois une exclusion mutuelle basée sur une vitesse de transmission et une exclusion mutuelle personnalisée. Pour sélectionner un flux autre que celui par défaut dans l’exclusion mutuelle personnalisée, vous devez utiliser la sélection manuelle des flux. Toutefois, si vous utilisez la sélection manuelle de flux, le lecteur ne sélectionne pas automatiquement le flux à plusieurs vitesses de transmission. Vous devez planifier cette éventualité dans votre application si vous envisagez de prendre en charge plusieurs types d’exclusion mutuelle dans un seul fichier. En général, cela implique la création de vos propres routines de sélection de flux pour les types automatiques automatiques d’exclusion mutuelle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Utilisation de l’exclusion mutuelle**](using-mutual-exclusion.md)
</dt> </dl>

 

 




