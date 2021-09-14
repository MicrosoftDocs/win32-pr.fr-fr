---
description: Il existe plusieurs formats de persistance générés par la plateforme Tablet PC qui sont utiles comme blocs de construction pour les formats répertoriés précédemment. Les formats suivants sont tous générés et consommés à l’aide des méthodes Load et Save de l’objet Ink.
ms.assetid: 76d42a3d-22f5-47f9-89e8-7c5c098ac62e
title: Blocs de construction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32e6121ddfaabfc860239019ce62df65bdc36c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294058"
---
# <a name="building-blocks"></a>Blocs de construction

Il existe plusieurs formats de persistance générés par la plateforme Tablet PC qui sont utiles comme blocs de construction pour les formats répertoriés précédemment. Les formats suivants sont tous générés et consommés à l’aide des méthodes [**Load**](/previous-versions/ms569609(v=vs.100)) et [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) de l’objet [**Ink**](/previous-versions/ms583670(v=vs.100)) .

-   Ink Serialized Format (ISF) : Ink Serialized Format (ISF) est la représentation de l’encre persistante la plus compacte. Vous pouvez incorporer ISF dans un format de document binaire ou le déplacer directement dans le presse-papiers. L’encre stockée dans ISF doit utiliser le système de coordonnées par défaut, qui est HIMETRIC, avec l’axe vertical inversé.
-   Format ISF en base-64 : vous pouvez utiliser le format ISF encodé en base-64 pour encoder l’encre directement dans un fichier Extensible Markup Language (XML) ou HTML.
-   Format GIF (Graphics Interchange Format) : le format gif enrichi est un fichier GIF qui contient le format ISF en tant que métadonnées incorporées dans le fichier. L’encre générée en tant que GIF viné peut être affichée dans les applications qui ne reconnaissent pas l’encre, et toutes les données d’encre sont conservées si l’encre retourne à une application qui reconnaît l’encre. Ce format est idéal pour le transport de contenu manuscrit dans un fichier HTML. L’encre est disponible pour n’importe quelle application, que l’application reconnaisse l’encre ou non.
-   GIF enrichi encodé en base 64 : ce format est fourni pour les développeurs qui souhaitent coder l’encre directement dans un fichier XML ou HTML, puis convertir le fichier en une image ultérieurement. Vous pouvez l’utiliser lorsque vous souhaitez qu’un fichier XML généré pour contenir toutes les informations relatives à l’encre et à utiliser comme moyen de générer du code HTML à l’aide de XSLT (Extensible Stylesheet Language Transformations).
    > [!Note]  
    > La technologie de compression et de décompression LZW est prétendument couverte par le brevet US no. 4 558 302 et ses brevets associés et étrangers équivalents (collectivement, les brevets LZW) appartenant à Unisys Corporation. Microsoft Corporation a obtenu une licence d’Unisys sous les brevets LZW pour utiliser la technologie GIF et la technologie LZW dans certains produits Microsoft. Toutefois, cette licence ne s’étend pas à des développeurs tiers utilisant des produits de développement Microsoft, tels que Microsoft Toolkit et les produits de développement de langage, pour fournir des fonctionnalités de lecture/écriture GIF ou d’autres fonctionnalités LZW dans leurs propres produits. Les développeurs tiers doivent faire leur propre détermination s’ils ont besoin d’une licence d’Unisys pour leurs produits.

     

Une application peut générer l’un de ces formats persistants en utilisant la méthode [Microsoft. Ink. Stroke. HitTest](/previous-versions/ms828460(v=msdn.10)) ou [Microsoft. Ink. Ink. HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) pour générer une collection de traits et :

-   Ajout de ces traits à un nouvel objet [**Ink**](/previous-versions/ms583670(v=vs.100)) à l’aide de la méthode [AddStrokesAtRectangle](/previous-versions/ms569548(v=vs.100)) .
-   Génération d’un nouvel objet [**Ink**](/previous-versions/ms583670(v=vs.100)) à l’aide de la méthode [ExtractStrokes](/previous-versions/dotnet/netframework-3.5/ms571326(v=vs.90)) .

La première convertit le rectangle de sélection en l’origine, tandis que le second ne le fait pas. L’application utilise ensuite la méthode [**Save**](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) de l’objet [**Ink**](/previous-versions/ms583670(v=vs.100)) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets sInk et tInk](sink-and-tink-objects.md)
</dt> </dl>

 

 
