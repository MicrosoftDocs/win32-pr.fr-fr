---
title: À propos des fichiers SAMI
description: À propos des fichiers SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Modèle objet du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Windows Media Player Mobile, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX du lecteur Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX Mobile Player Windows Media, SAMI (Synchronized Accessible Media Interchange)
- Contrôle ActiveX, SAMI (Synchronized Accessible Media Interchange)
- Fichiers de Media Interchange (SAMI) synchronisés, fichiers
- SAMI (Synchronized Accessible Media Interchange), fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840150"
---
# <a name="about-sami-files"></a>À propos des fichiers SAMI

Les fichiers SAMI sont des fichiers texte qui ont une extension de nom de fichier. SMI ou. sami. Ils contiennent les chaînes de texte utilisées pour les légendes fermées, les sous-titres et les descriptions audio synchronisées. Ils spécifient également les paramètres de minutage utilisés par le contrôle du lecteur Windows Media pour synchroniser le texte des sous-titres avec du contenu audio ou vidéo. Lorsqu’un fichier multimédia numérique atteint une heure désignée dans le fichier SAMI, le texte change en conséquence dans la zone d’affichage de la légende fermée de la page Web.

En dehors d’un simple éditeur de texte (tel que le bloc-notes Microsoft), aucun logiciel spécial n’est requis pour créer un fichier SAMI. SAMI et HTML partagent des éléments communs, tels que <HEAD> les <BODY> balises et. Comme en HTML, les balises utilisées dans les fichiers SAMI doivent toujours être utilisées par paires. Par exemple, un élément BODY commence par une <BODY> balise et doit toujours se terminer par une </BODY> balise.

Un fichier SAMI de base requiert trois balises fondamentales : <SAMI> , <HEAD> et <BODY> .

La <SAMI> balise identifie le document sous la forme d’un document sami afin que d’autres applications puissent reconnaître son format de fichier.

Entre les balises <HEAD> et </HEAD> , vous définissez des indications de base et d’autres informations de mise en forme pour le document sami, telles que le titre du document, des informations générales et des propriétés de style pour les sous-titres. Comme HTML, le contenu déclaré dans l’élément HEAD ne s’affiche pas comme OUTPUT.

Les éléments et les attributs définis entre les balises <BODY> et </BODY> affichent le contenu affiché par l’utilisateur. En same, l’élément BODY contient les paramètres de synchronisation et les chaînes de texte utilisées pour les sous-titres.

Défini dans l’élément HEAD, l’élément STYLE fournit des fonctionnalités ajoutées en SAMI. Entre les balises <STYLE> et </STYLE> , vous pouvez définir plusieurs sélecteurs de feuille de style en cascade (CSS) pour le style et la mise en page. Des propriétés de style telles que des polices, des tailles et des alignements peuvent être personnalisées pour offrir une expérience utilisateur riche tout en promouvant également l’accessibilité. Par exemple, la définition d’une classe de style de police de texte volumineux peut améliorer la lisibilité pour les utilisateurs qui éprouvent des difficultés à lire un texte de petite taille. En outre, en définissant plusieurs classes de langage différentes, vous pouvez aider les utilisateurs internationaux à mieux comprendre le contenu multimédia numérique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




