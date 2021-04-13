---
title: Clés de test et de production pour une boutique en ligne de type 1
description: Clés de test et de production pour une boutique en ligne de type 1
ms.assetid: 1a975c0b-16b8-4da7-8594-316ae34257d0
keywords:
- Windows Media Player Online stores, clés de test
- magasins en ligne, clés de test
- types 1 magasins en ligne, clés de test
- Windows Media Player Online stores, clés de production
- magasins en ligne, clés de production
- tapez 1 magasins en ligne, clés de production
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- clés de test
- clés de production
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e8ce8d049df78f186d336079f76eb00eb8bb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380276"
---
# <a name="test-and-production-keys-for-a-type-1-online-store"></a>Clés de test et de production pour une boutique en ligne de type 1

Lorsque vous commencez le développement de votre boutique en ligne, Microsoft vous propose deux clés numériques : une clé de test et une clé de production. En même temps, vous devez fournir à Microsoft deux URL : une qui pointe vers votre document ServiceInfo de test et une autre qui pointe vers votre document ServiceInfo de production.

Pendant la phase de développement et de test, votre magasin en ligne est visible dans le lecteur Windows Media uniquement si votre clé de test ou votre clé de production se trouve dans le registre sur l’ordinateur de l’utilisateur. Si votre clé de test est dans le registre, le lecteur Windows Media récupère votre document ServiceInfo de test, qui pointe vers le plug-in, les pages Web et les images qui appartiennent à votre magasin de test. Si votre clé de production se trouve dans le registre, le lecteur Windows Media récupère votre document ServiceInfo de production, qui pointe vers le plug-in, les pages Web et les images qui appartiennent à votre magasin de production.

Vous pouvez utiliser vos magasins de test et de production de quelque manière que ce soit. Toutefois, en règle générale, la distinction est la suivante :

-   Votre magasin de test est l’endroit où vous apportez des modifications quotidiennes à votre plug-in, vos pages Web, vos images et d’autres composants de votre service.
-   Votre magasin de production est l’endroit où vous gardez une version stable de votre service, qui comprend votre plug-in, vos pages Web, vos images et d’autres composants.

Pour que votre magasin en ligne puisse être publié dans le lecteur Windows Media, Microsoft doit vérifier que votre service fonctionne correctement. Au cours de la phase de validation, Microsoft utilise votre clé de production. Microsoft n’utilise pas votre clé de test pendant la phase de validation.

Lorsque votre magasin en ligne de production termine avec succès le processus de validation, Microsoft publie votre magasin, ce qui signifie que votre magasin de production apparaît dans le lecteur Windows Media pour tous les utilisateurs, et pas seulement ceux qui ont votre clé de production dans le registre. Une fois votre magasin publié, les clés de test et de production ne sont plus nécessaires.

> [!Note]  
> Les utilisateurs peuvent être en mesure de deviner la clé de test ou de production de votre boutique en ligne et d’afficher votre boutique pendant son développement. Vous devez faire attention à l’exposition des fonctionnalités que vous souhaitez conserver secrètes jusqu’à la publication publique.

 

Pour plus d’informations sur l’emplacement de vos clés de production et de test dans le registre de l’utilisateur, consultez [clés et entrées de Registre pour un magasin de type 1 en ligne](registry-keys-and-entries-for-a-type-1-online-store.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




