---
title: À propos des fichiers SAMI
description: À propos des fichiers SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Lecteur Windows Media, SAMI (synchronized Accessible Media Interchange)
- modèle objet Lecteur Windows Media, SAMI (synchronized Accessible Media Interchange)
- modèle objet, SAMI (Synchronized Accessible Media Interchange)
- Lecteur Windows Media Mobile, accessible en SAMI (Synchronized Accessible Media Interchange)
- contrôle de ActiveX Lecteur Windows Media, SAMI (synchronized Accessible Media Interchange)
- Lecteur Windows Media contrôle Mobile ActiveX, SAMI (synchronized Accessible Media Interchange)
- contrôle de ActiveX, SAMI (synchronized Accessible Media Interchange)
- Fichiers de Media Interchange (SAMI) synchronisés, fichiers
- SAMI (Synchronized Accessible Media Interchange), fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68bcb4823ee02a501254218a9b7c4d9aaf347894d895bc193c8ce763658db174
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470459"
---
# <a name="about-sami-files"></a>À propos des fichiers SAMI

Les fichiers SAMI sont des fichiers texte qui ont une extension de nom de fichier. SMI ou. sami. Ils contiennent les chaînes de texte utilisées pour les légendes fermées, les sous-titres et les descriptions audio synchronisées. elles spécifient également les paramètres de minutage utilisés par le contrôle Lecteur Windows Media pour synchroniser le texte de légende fermé avec du contenu audio ou vidéo. Lorsqu’un fichier multimédia numérique atteint une heure désignée dans le fichier SAMI, le texte change en conséquence dans la zone d’affichage de la légende fermée de la page Web.

en dehors d’un simple éditeur de texte (par exemple, Microsoft Bloc-notes), aucun logiciel spécial n’est requis pour créer un fichier SAMI. SAMI et HTML partagent des éléments communs, tels que <HEAD> et <BODY> MetaTags. Comme en HTML, les balises utilisées dans les fichiers SAMI doivent toujours être utilisées par paires. Par exemple, un élément BODY commence par un <BODY> tag et doit toujours se terminer par un </BODY> balise.

Un fichier SAMI de base requiert trois étiquettes principales : <SAMI> , <HEAD> et <BODY>.

La <SAMI> balise identifie le document sous la forme d’un document sami afin que d’autres applications puissent reconnaître son format de fichier.

Entre les <HEAD> et </HEAD> les balises, vous définissez des instructions de base et d’autres informations de mise en forme pour le document SAMI, telles que le titre du document, des informations générales et des propriétés de style pour les sous-titres. Comme HTML, le contenu déclaré dans l’élément HEAD ne s’affiche pas comme OUTPUT.

Éléments et attributs définis entre <BODY> et </BODY> les balises affichent le contenu affiché par l’utilisateur. En same, l’élément BODY contient les paramètres de synchronisation et les chaînes de texte utilisées pour les sous-titres.

Défini dans l’élément HEAD, l’élément STYLE fournit des fonctionnalités ajoutées en SAMI. Entre les balises <STYLE> et </STYLE> , vous pouvez définir plusieurs sélecteurs de feuille de style en cascade (CSS) pour le style et la mise en page. Des propriétés de style telles que des polices, des tailles et des alignements peuvent être personnalisées pour offrir une expérience utilisateur riche tout en promouvant également l’accessibilité. Par exemple, la définition d’une classe de style de police de texte volumineux peut améliorer la lisibilité pour les utilisateurs qui éprouvent des difficultés à lire un texte de petite taille. En outre, en définissant plusieurs classes de langage différentes, vous pouvez aider les utilisateurs internationaux à mieux comprendre le contenu multimédia numérique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Ajout de sous-titres à des médias numériques**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




