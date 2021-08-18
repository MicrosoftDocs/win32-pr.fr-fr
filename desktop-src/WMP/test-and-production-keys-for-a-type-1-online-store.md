---
title: Clés de test et de production pour une boutique en ligne de type 1
description: Clés de test et de production pour une boutique en ligne de type 1
ms.assetid: 1a975c0b-16b8-4da7-8594-316ae34257d0
keywords:
- Lecteur Windows Media des magasins en ligne, clés de test
- magasins en ligne, clés de test
- types 1 magasins en ligne, clés de test
- Lecteur Windows Media les magasins en ligne, clés de production
- magasins en ligne, clés de production
- tapez 1 magasins en ligne, clés de production
- Lecteur Windows Media les magasins en ligne, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- clés de test
- clés de production
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00fcd1af52f7400b7f20a1eb3115bfc38d8b997bfbc85c5d6e36f08fcf59f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118529"
---
# <a name="test-and-production-keys-for-a-type-1-online-store"></a>Clés de test et de production pour une boutique en ligne de type 1

Lorsque vous commencez le développement de votre boutique en ligne, Microsoft vous propose deux clés numériques : une clé de test et une clé de production. En même temps, vous devez fournir à Microsoft deux URL : une qui pointe vers votre document ServiceInfo de test et une autre qui pointe vers votre document ServiceInfo de production.

pendant la phase de développement et de test, votre magasin en ligne est visible dans Lecteur Windows Media uniquement si votre clé de test ou votre clé de production se trouve dans le registre sur l’ordinateur de l’utilisateur. si votre clé de test se trouve dans le registre, Lecteur Windows Media récupère votre document ServiceInfo de test, qui pointe vers le plug-in, les pages web et les images qui appartiennent à votre magasin de test. si votre clé de production se trouve dans le registre, Lecteur Windows Media récupère votre document ServiceInfo de production, qui pointe vers le plug-in, les pages web et les images qui appartiennent à votre magasin de production.

Vous pouvez utiliser vos magasins de test et de production de quelque manière que ce soit. Toutefois, en règle générale, la distinction est la suivante :

-   Votre magasin de test est l’endroit où vous apportez des modifications quotidiennes à votre plug-in, vos pages Web, vos images et d’autres composants de votre service.
-   Votre magasin de production est l’endroit où vous gardez une version stable de votre service, qui comprend votre plug-in, vos pages Web, vos images et d’autres composants.

pour que votre magasin en ligne puisse être publié dans Lecteur Windows Media, Microsoft doit vérifier que votre service fonctionne correctement. Au cours de la phase de validation, Microsoft utilise votre clé de production. Microsoft n’utilise pas votre clé de test pendant la phase de validation.

lorsque votre magasin en ligne de production termine avec succès le processus de validation, Microsoft publie votre magasin, ce qui signifie que votre magasin de production apparaît dans Lecteur Windows Media pour tous les utilisateurs, pas seulement ceux qui ont votre clé de production dans le registre. Une fois votre magasin publié, les clés de test et de production ne sont plus nécessaires.

> [!Note]  
> Les utilisateurs peuvent être en mesure de deviner la clé de test ou de production de votre boutique en ligne et d’afficher votre boutique pendant son développement. Vous devez faire attention à l’exposition des fonctionnalités que vous souhaitez conserver secrètes jusqu’à la publication publique.

 

Pour plus d’informations sur l’emplacement de vos clés de production et de test dans le registre de l’utilisateur, consultez [clés et entrées de Registre pour un magasin de type 1 en ligne](registry-keys-and-entries-for-a-type-1-online-store.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 1**](about-type-1-online-stores.md)
</dt> </dl>

 

 




