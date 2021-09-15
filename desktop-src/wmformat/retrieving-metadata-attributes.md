---
title: Récupération des attributs de métadonnées
description: Récupération des attributs de métadonnées
ms.assetid: d1d2c8e0-7445-4ee1-94d9-4c1ed74f8fe2
keywords:
- Windows Media Format SDK, récupération des attributs de métadonnées
- ASF (Advanced Systems Format), récupération des attributs de métadonnées
- ASF (format des systèmes avancés), récupération des attributs de métadonnées
- métadonnées, récupérer des attributs
- flux, récupération des attributs de métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c918cb47e77c3fd69c64de586b84b7f6244e4c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294415"
---
# <a name="retrieving-metadata-attributes"></a>Récupération des attributs de métadonnées

Pour récupérer un attribut à partir d’un en-tête de fichier, vous devez connaître le numéro de flux et l’index de l’attribut. Vous pouvez utiliser la méthode [**IWMHeaderInfo3 :: GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) pour obtenir les index de tous les attributs portant le même nom ou tous les index dans la même langue. Comme les autres méthodes de [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), **GetAttributeIndices** traite avec un seul flux, ou avec tous les attributs de niveau fichier à l’aide de Stream 0. Vous pouvez utiliser 0xFFFF pour le numéro de flux pour obtenir des index globaux correspondant à vos critères dans tout le fichier, quel que soit le nombre de flux.

Lorsque vous connaissez l’index de l’attribut que vous souhaitez récupérer, appelez [**IWMHeaderInfo3 :: GetAttributeByIndexEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributebyindexex) pour obtenir l’attribut. Vous devez effectuer deux appels à **GetAttributeByIndexEx** pour chaque attribut récupéré. Lors du premier appel, transmettez **null** pour le nom et les pointeurs de tampon de données pour obtenir la taille nécessaire. Allouez ensuite des tampons de la taille indiquée et effectuez le deuxième appel pour récupérer le nom et les données.

Pour obtenir un exemple de code illustrant la récupération des attributs de métadonnées, consultez [pour récupérer toutes les métadonnées dans un fichier](to-retrieve-all-metadata-in-a-file.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation des métadonnées**](working-with-metadata.md)
</dt> </dl>

 

 




