---
title: Clés de test et de production pour un magasin de type 2 en ligne
description: Clés de test et de production pour un magasin de type 2 en ligne
ms.assetid: 4fce47e2-d73d-4484-9bda-48257268ed96
keywords:
- Windows Media Player Online stores, clés de test
- magasins en ligne, clés de test
- type 2 magasins en ligne, clés de test
- Windows Media Player Online stores, clés de production
- magasins en ligne, clés de production
- type 2 magasins en ligne, clés de production
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- clés de test
- clés de production
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f009e1b0ca58a66820e193e3b66f8ca50ccadc43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940237"
---
# <a name="test-and-production-keys-for-a-type-2-online-store"></a>Clés de test et de production pour un magasin de type 2 en ligne

Lorsque vous commencez le développement de votre boutique en ligne, Microsoft vous propose deux clés numériques : une clé de test et une clé de production. En même temps, vous devez fournir à Microsoft deux URL : une qui pointe vers votre document ServiceInfo de test et une autre qui pointe vers votre document ServiceInfo de production.

Pendant la phase de développement et de test, votre magasin en ligne est visible dans le lecteur Windows Media uniquement si votre clé de test ou votre clé de production se trouve dans le registre sur l’ordinateur de l’utilisateur. Si votre clé de test est dans le registre, le lecteur Windows Media récupère votre document ServiceInfo de test, qui pointe vers le plug-in, les pages Web et les images qui appartiennent à votre magasin de test. Si votre clé de production se trouve dans le registre, le lecteur Windows Media récupère votre document ServiceInfo de production, qui pointe vers le plug-in, les pages Web et les images qui appartiennent à votre magasin de production.

Vous pouvez utiliser vos magasins de test et de production de la manière qui vous convient. Toutefois, en règle générale, la distinction est la suivante :

-   Votre magasin de test est l’endroit où vous apportez des modifications quotidiennes à votre plug-in, vos pages Web, vos images et d’autres composants de votre service.
-   Votre magasin de production est l’endroit où vous gardez une version stable de votre service, qui comprend votre plug-in, vos pages Web, vos images et d’autres composants.

Pour que votre magasin en ligne puisse être publié dans le lecteur Windows Media, Microsoft doit vérifier que votre service fonctionne correctement. Au cours de la phase de validation, Microsoft utilise votre clé de production. Microsoft n’utilise pas votre clé de test pendant la phase de validation.

Lorsque votre magasin en ligne de production termine avec succès le processus de validation, Microsoft publie votre magasin, ce qui signifie que votre magasin de production apparaît dans le lecteur Windows Media pour tous les utilisateurs, et pas seulement ceux qui ont votre clé de production dans le registre. Une fois votre magasin publié, les clés de test et de production ne sont plus nécessaires.

> [!Note]  
> Les utilisateurs peuvent être en mesure de deviner la clé de test ou de production de votre boutique en ligne et d’afficher votre boutique pendant son développement. Vous devez faire attention à l’exposition des fonctionnalités que vous souhaitez conserver secrètes jusqu’à la publication publique.

 

Pour plus d’informations sur l’emplacement de vos clés de production et de test dans le registre de l’utilisateur, consultez [clés et entrées de Registre pour un magasin de type 2 en ligne](registry-keys-and-entries-for-a-type-2-online-store.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos des magasins en ligne de type 2**](about-type-2-online-stores.md)
</dt> <dt>

[**Exemples de magasins en ligne de type 2**](type-2-online-store-samples.md)
</dt> </dl>

 

 




