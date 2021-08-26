---
title: Vue d’ensemble du format ASF
description: Vue d’ensemble du format ASF
ms.assetid: ef22a493-d6cf-40d2-ab17-d87159066d1d
keywords:
- Windows Media Format SDK, vue d’ensemble du format ASF
- ASF (Advanced Systems Format), vue d’ensemble du format
- ASF (format des systèmes avancés), vue d’ensemble du format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee075330e9c68ef1fbdadea12c70fd8deec584f99f8dadd31cb55070dc11eee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930559"
---
# <a name="overview-of-the-asf-format"></a>Vue d’ensemble du format ASF

ASF (Advanced Systems Format) est un format de fichier extensible conçu principalement pour le stockage et la diffusion de flux multimédias numériques synchronisés et leur transmission sur des réseaux. ASF est le format de conteneur pour Windows Media Audio et le contenu basé sur Windows Media Video. l’extension wma ou wmv est utilisée pour spécifier un fichier ASF qui contient le contenu encodé avec les codecs Windows Media Audio et/ou Windows Media Video. le kit de développement logiciel (SDK) du Format de média Windows peut être utilisé pour créer et lire des fichiers multimédias Windows, ainsi que des fichiers ASF qui contiennent d’autres types de données compressées ou non compressées.

Cette section fournit une description générale du format ASF en tant qu’informations générales. Étant donné que les objets lecteur et Writer gèrent toutes les tâches de mise en forme et d’analyse de fichier de bas niveau, il n’est pas nécessaire d’avoir une compréhension détaillée de ASF avant d’utiliser ce kit de développement logiciel (SDK) pour créer des fichiers ASF. La spécification ASF complète se trouve sur le [site Web de Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

Les principaux objectifs du format ASF sont les suivants :

-   Pour prendre en charge une lecture efficace à partir de serveurs multimédias, de serveurs HTTP et de périphériques de stockage locaux.
-   Pour prendre en charge des types de médias évolutifs, tels que des données audio et vidéo.
-   Pour permettre à une composition multimédia unique d’être présentée sur un large éventail de bandes passantes.
-   Pour permettre le contrôle de la création de relations de flux de média, en particulier dans les scénarios de bande passante limitée.
-   Être indépendant du système de composition multimédia, du système d’exploitation de l’ordinateur ou du protocole de communication des données.

Un fichier ASF peut contenir plusieurs flux indépendants ou dépendants, y compris plusieurs flux audio pour le son multicanaux, ou des flux vidéo à vitesses de transmission multiples pouvant être transmis sur des bandes passantes différentes. Les flux peuvent être dans n’importe quel format compressé ou non compressé ; toutefois, la compression optimale s’effectue avec les codecs de série Microsoft Windows Media Audio et Video 9. Outre les types de flux de données audio et vidéo standard, un fichier ASF peut également contenir des flux de texte, des pages Web et des commandes de script, ainsi que tout autre type de données arbitraire. ASF prend en charge le contenu multimédia en direct et à la demande. Il peut être utilisé comme un véhicule pour enregistrer ou lire H. 32X (par exemple, H. 323 et H. 324) ou des conférences MBONE.

Un fichier ASF est organisé en sections appelées « objets ». Il existe trois objets de niveau supérieur, un objet d’en-tête et un objet de données (les deux obligatoires), ainsi qu’un objet d’index facultatif. L’objet d’en-tête contient des informations générales sur le fichier, telles que la taille de fichier, le nombre de flux, les méthodes de correction d’erreur et les codecs utilisés. Les métadonnées sont également stockées ici. L’objet d’en-tête est le seul objet de niveau supérieur qui peut contenir d’autres objets. L’objet de données contient les données de flux, organisées en paquets. L’objet index simple contient une liste de paires index/clés associées qui permettent aux applications de rechercher efficacement un fichier. L’index associé à chaque image clé peut être une heure de présentation, un numéro d’image vidéo ou un horodatage de référence.

Chaque objet de niveau supérieur ou de niveau inférieur commence par un identificateur global unique (GUID) et une valeur de taille. Ces numéros permettent au lecteur de fichier d’analyser les informations à des emplacements appropriés dans des objets identifiables. En raison de ces GUID, les objets de niveau inférieur peuvent être envoyés dans n’importe quel ordre et sont toujours reconnus. Le format ASF est conçu pour surmonter la réception de données inexactes. Un fichier ASF partiellement téléchargé peut toujours être lu, à condition qu’il contienne l’objet d’en-tête et au moins un objet de données.

Informations détaillées sur ASF dans la spécification ASF. Vous pouvez télécharger la spécification à partir du [site Web Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**à propos du kit de développement logiciel (SDK) Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




