---
title: Types perçus (fonctionnalités héritées de l’environnement Windows)
description: PerceivedType est une propriété qui classifie un élément dans l’index.
ms.assetid: 47a5cf55-79f6-48e7-a585-72fc3d7d53d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afaf7d8b827495a94b441e5504762dd53dbe733c
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106518053"
---
# <a name="perceived-types-legacy-windows-environment-features"></a>Types perçus (fonctionnalités héritées de l’environnement Windows)

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez [Windows Search](../search/-search-3x-wds-overview.md) à la place.

`PerceivedType` est une propriété qui classifie un élément dans l’index. Cette classification est différente de la classification « Kind » utilisée par la [syntaxe de requête avancée](-search-2x-wds-aqsreference.md) , mais elle permet aux utilisateurs d’affiner leurs résultats de recherche. Le type AQS permet aux utilisateurs de limiter leur requête de recherche, tandis que la propriété PerceivedType permet aux utilisateurs de filtrer leur jeu de résultats.

## <a name="types"></a>Types

Utilisez la propriété PerceivedType pour classer votre type de fichier afin que les utilisateurs puissent filtrer leurs résultats de recherche par type. La sortie doit être l’une des chaînes suivantes :

-   contact
-   communications
-   Communications/courrier électronique
-   Communications/calendrier
-   Communications/tâche
-   Communications/messagerie instantanée
-   document
-   document/Remarque
-   document/texte
-   document/feuille de calcul
-   document/présentation
-   music
-   images
-   images/image
-   images/vidéo
-   dossier
-   programme

Par exemple, lorsque vous souhaitez créer un complément de filtre pour un nouveau type de fichier image, vous devez implémenter les éléments suivants dans votre interface [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter):

-   **GetChunk** pour retourner un FULLPROPSPEC qui comprend : D5CDD505-2E9C-101B-9397-08002B2CF9AE/PerceivedType
-   **GetValue** pour retourner un PROPVARIANT qui comprend : VT \_ LPWStr = "images/image"

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Développement de compléments IFilter](-search-2x-wds-ifilteraddins.md)
</dt> <dt>

[Développement de gestionnaires de protocole](-search-2x-wds-phaddins.md)
</dt> <dt>

[Syntaxe de requête avancée](-search-2x-wds-aqsreference.md)
</dt> <dt>

[SchemaTable](-search-2x-wds-schematable.md)
</dt> </dl>

 

 
