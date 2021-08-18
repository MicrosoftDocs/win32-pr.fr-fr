---
title: Considérations relatives aux marchés internationaux
description: Considérations relatives aux marchés internationaux
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Lecteur Windows Media magasins en ligne, marchés internationaux
- magasins en ligne, marchés internationaux
- types 1 magasins en ligne, marchés internationaux
- types 2 magasins en ligne, marchés internationaux
- marchés internationaux
- Lecteur Windows Media les magasins en ligne, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82e2db056f748e1257649716c57a2f1774ee0b1b149966dce3851a75d08c8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580509"
---
# <a name="considerations-for-international-markets"></a>Considérations relatives aux marchés internationaux

Si votre société crée des magasins en ligne pour plusieurs marchés, vous devez fournir à Microsoft l’URL d’un document ServiceInfo pour chaque marché. Vous pouvez procéder de l’une des deux manières suivantes :

-   Créez un document ServiceInfo distinct pour chaque marché. Dans ce cas, vous fournissez à Microsoft des URL qui pointent vers des documents ServiceInfo individuels pour chaque magasin en ligne de chaque marché.
-   Créez un seul document ServiceInfo pour tous les marchés. Dans ce cas, vous fournissez à Microsoft la même URL pour chaque marché. Votre document ServiceInfo, créé en tant que page ASP, peut détecter dynamiquement l’emplacement de l’utilisateur en fonction des paramètres de chaîne de requête.

Lecteur Windows Media ajoute une chaîne de requête à la demande d’URL ServiceInfo qui fournit des informations sur les paramètres régionaux et d’emplacement de l’utilisateur. Si votre magasin en ligne utilise ces informations pour déterminer le contenu à afficher, vous devez ajouter dynamiquement ces valeurs à vos propres URL dans votre document ServiceInfo. C’est la meilleure façon de s’assurer que les URL de votre page Web contiendront toujours les paramètres attendus.

Une fois que vous avez déterminé l’emplacement et la préférence de langue de l’utilisateur, vous souhaiterez peut-être conserver ces informations pour des sessions ultérieures. Vous pouvez le faire à l’aide de l’une des techniques que vous utiliseriez normalement dans une page Web, telle que les cookies, ou à l’aide de votre objet COM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du document ServiceInfo de manière dynamique**](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[**Informations communes aux magasins en ligne de type 1 et de type 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Élément ServiceInfo**](serviceinfo-element.md)
</dt> </dl>

 

 




