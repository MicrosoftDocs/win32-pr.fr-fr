---
title: Définition des attributs de métadonnées
description: Définition des attributs de métadonnées
ms.assetid: a5d99361-9919-4548-a24d-900ac65cc634
keywords:
- Windows Media Format SDK, définition des attributs de métadonnées
- ASF (Advanced Systems Format), définition des attributs de métadonnées
- ASF (format des systèmes avancés), définition des attributs de métadonnées
- métadonnées, définir des attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa352a83e758b97bde6088377f8461a62b2d5071314d45f4978035bec219a5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197509"
---
# <a name="setting-metadata-attributes"></a>Définition des attributs de métadonnées

Les attributs de métadonnées sont définis à l’aide de la méthode [**IWMHeaderInfo3 :: AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) .

Une langue est attribuée à tous les attributs dans la liste des langues du fichier. Vous pouvez accéder à la liste des langues à l’aide de l’interface [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) . Pour obtenir un pointeur vers une interface **IWMLanguageList** , appelez **QueryInterface** sur toute interface de l’objet à partir duquel vous avez obtenu [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3).

Vous pouvez ajouter des attributs avec n’importe quel nom de votre choix. toutefois, l’utilisation de noms d’attribut qui ne sont pas des noms standard pris en charge par le kit de développement logiciel (SDK) de Format de média Windows peut rendre vos métadonnées difficiles à découvrir par les utilisateurs. La plupart des applications qui jouent sur des médias vérifient les valeurs standard. Pour plus d’informations, consultez [métadonnées personnalisées](custom-metadata.md).

Vous ne pouvez pas utiliser le nombre de flux 0xFFFF pour ajouter un attribut globalement. Vous devez assigner chaque attribut à un numéro de flux spécifique, ou le flux 0 pour les attributs de niveau fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




