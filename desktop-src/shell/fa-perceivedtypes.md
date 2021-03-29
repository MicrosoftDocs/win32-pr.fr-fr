---
description: Un type perçu est une catégorie de types de fichiers qui vous permet d’identifier votre type de fichier sur Windows (et les applications) comme une image, un fichier audio, un document ou tout autre type.
title: Types perçus (shell Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104991861"
---
# <a name="perceived-types-the-windows-shell"></a>Types perçus (shell Windows)

Un type perçu est une catégorie de types de fichiers qui vous permet d’identifier votre type de fichier sur Windows (et les applications) comme une image, un fichier audio, un document ou tout autre type. Les types perçus sont utilisés à plusieurs fins, notamment la détermination du type de dossier, qui est ensuite utilisé pour définir les paramètres d’affichage par défaut. Par exemple, un dossier contenant des fichiers dont l’image est de type perçue reçoit un mode d’affichage par défaut de miniatures.

Cette rubrique est organisée comme suit :

-   [À propos des types perçus](#about-perceived-types)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="about-perceived-types"></a>À propos des types perçus

Les types perçus, définis en tant que valeurs PerceivedType, sont similaires aux types de fichiers, à ceci près qu’ils font référence à des catégories larges de types de fichiers plutôt qu’à des types de fichiers spécifiques. Par exemple, l’image, le texte, l’audio et la compression sont des types perçus. Les types de fichiers (généralement des types de fichiers publics) peuvent être affectés à un type perçu et doivent toujours être affectés, le cas échéant. Par exemple, les types de fichiers image. bmp,. png,. jpg et. gif sont également perçus comme une image de type.

Les types perçus par défaut sont les suivants :

-   Dossier
-   Texte
-   Image
-   Audio
-   Vidéo
-   Compressé
-   Document
-   Système
-   Application
-   Gamemedia
-   Contacts

## <a name="additional-resources"></a>Ressources supplémentaires

-   Pour plus d’informations sur l’enregistrement des types perçus, consultez [inscription des applications](app-registration.md).
-   Pour obtenir la liste des types perçus par défaut, consultez l’énumération [**perçue**](/windows/win32/api/shtypes/ne-shtypes-perceived) .
-   Pour récupérer le type perçu d’un fichier en fonction de son extension de nom de fichier, consultez la fonction [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription de l’application](app-registration.md)
</dt> <dt>

[Types de fichiers](fa-file-types.md)
</dt> <dt>

[Fonctionnement des associations de fichiers](fa-how-work.md)
</dt> <dt>

[Affichage du contenu par type de fichier ou par type](prophand-content-view.md)
</dt> <dt>

[Vérificateur de type de fichier](file-type-verifier.md)
</dt> <dt>

[Gestionnaires de types de fichiers](fa-file-extensions.md)
</dt> <dt>

[Identificateurs programmatiques](fa-progids.md)
</dt> <dt>

[Tableaux d’association](fa-associationarray.md)
</dt> </dl>

 

 



