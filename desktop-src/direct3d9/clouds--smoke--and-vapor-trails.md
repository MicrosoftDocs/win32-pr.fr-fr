---
description: Les Clouds, les fumées et les traces de vapeur peuvent tous être créés par une extension de la technique de l’interrogation.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Clouds, fumées et traces de vapeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09da27ec1ba8f6ad8beb3c9a847226ffe63f1059c0b28dfe71e0d0582d56645f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118097157"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a>Clouds, fumées et traces de vapeur (Direct3D 9)

Les Clouds, les fumées et les traces de vapeur peuvent tous être créés par une extension de la technique de l’interrogation. Voir la rubrique sur les [panneaux (Direct3D 9)](billboarding.md). En faisant pivoter le panneau sur deux axes au lieu d’un, votre application peut permettre à l’utilisateur d’afficher un panneau à partir de n’importe quel angle. En règle générale, une application fait pivoter le panneau sur les axes horizontal et vertical.

Pour créer un Cloud simple, votre application peut faire pivoter une primitive rectangulaire sur un ou deux axes afin que la primitive soit face à l’utilisateur. Une texture de type Cloud peut ensuite être appliquée à la primitive avec transparence. Pour plus d’informations sur l’application de textures transparentes aux primitives, consultez [fusion de textures (Direct3D 9)](texture-blending.md). Vous pouvez animer le Cloud en appliquant une série de textures au fil du temps.

Une application peut créer des clouds plus complexes en les formant à partir d’un groupe de Primitives. Chaque partie du Cloud est une primitive rectangulaire. Les primitives peuvent être déplacées indépendamment dans le temps pour obtenir l’apparence d’un brouillard dynamique. L’illustration suivante montre ce concept.

![illustration des primitives qui forment des clouds plus complexes](images/cloud.png)

L’apparence de la fumée est affichée de manière similaire aux clouds. Elle nécessite généralement plusieurs panneaux, comme des clouds complexes. En général, la fumée Billows et augmente au fil du temps, de sorte que les panneaux qui composent la prune de fumée doivent se déplacer en conséquence. Vous devrez peut-être ajouter d’autres panneaux au fur et à mesure de l’augmentation et de la dispersion du prune.

Une piste de vapeur est un prune de fumée qui n’augmente pas. Toutefois, comme une sorte de fumée, elle est dispersée dans le temps. L’illustration suivante montre la technique consistant à utiliser des panneaux pour simuler une piste de vapeur.

![illustration des panneaux qui simulent une piste de vapeur](images/vapor.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples alpha](alpha-examples.md)
</dt> </dl>

 

 



