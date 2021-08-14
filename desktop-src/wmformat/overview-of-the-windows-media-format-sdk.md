---
title: présentation du kit de développement logiciel (SDK) Windows Media Format
description: présentation du kit de développement logiciel (SDK) Windows Media Format
ms.assetid: 9e5d6254-6261-4ca8-84d6-38050c93db22
keywords:
- Windows Media Format SDK, création et modification de fichiers ASF
- ASF (Advanced Systems Format), création et modification de fichiers
- ASF (format de systèmes avancés), création et modification de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b80436415a6017d0429493b1d4b5be92dcb682f572796e5e9e1c3cfaa8795e66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846425"
---
# <a name="overview-of-the-windows-media-format-sdk"></a>présentation du kit de développement logiciel (SDK) Windows Media Format

le kit de développement logiciel (SDK) Windows Media Format contient des objets pour effectuer des tâches à trois points de la vie d’un fichier ASF : création, modification et lecture. certaines applications, notamment celles pour la modification vidéo, utiliseront les fonctionnalités étendues du kit de développement logiciel (SDK) de Format multimédia Windows pour lire le contenu des fichiers ASF, modifier ce contenu et écrire les résultats dans un nouveau fichier. Toutefois, il est plus facile de considérer ce kit de développement logiciel (SDK) dans les trois étapes de création, de modification et de lecture de fichiers.

## <a name="asf-file-creation-with-the-windows-media-format-sdk"></a>création de fichiers ASF avec le kit de développement logiciel (SDK) Windows Media Format

le processus d’écriture de fichiers ASF avec le kit de développement logiciel (SDK) Windows Media Format est, à un niveau élevé, assez simple. La création de fichier est gérée par un objet Writer. Vous indiquez à l’objet Writer le type de fichier que vous souhaitez créer en spécifiant un objet de profil à utiliser. Chaque objet de profil contient les paramètres d’un fichier ASF. Certains profils sont inclus dans ce kit de développement logiciel (SDK) et la prise en charge de la modification de profil est fournie par un certain nombre d’objets. Lorsque vous avez défini un profil pour l’objet Writer à utiliser, vous pouvez commencer à passer des exemples à l’enregistreur à des fins de traitement. Dans la plupart des cas, un échantillon est un morceau de fichier audio ou vidéo non compressé, mais un exemple peut être n’importe quel type de données.

En interne, le writer effectue trois tâches majeures. Tout d’abord, si le flux auquel appartient un échantillon doit être compressé, le writer communique avec la partie encodage du codec (compresseur/décompresseur) pour compresser l’exemple. Une fois que les échantillons se présentent sous la forme spécifiée par le profil, le writer divise les exemples en paquets de taille appropriée à diffuser sur un réseau. Enfin, les données des différents flux sont multiplexées ou entrelacées de sorte que les exemples présentant des temps de présentation similaires dans tous les flux sont proches les uns des autres dans la section des données du fichier ASF.

L’objet Writer n’écrit pas réellement un fichier lui-même. Il communique avec un ou plusieurs objets appelés récepteurs, qui délivrent les données du writer à sa destination. Dans le cas de fichiers locaux, un récepteur de fichiers gère l’écriture des données dans le fichier. Vous pouvez également configurer des récepteurs réseau pour distribuer les données ASF sur un réseau. En règle générale, plusieurs récepteurs sont utilisés. Par exemple, une application peut diffuser un fichier sur un réseau et enregistrer une copie en tant que fichier sur un disque local simultanément. à l’aide d’un récepteur de notifications push, vous pouvez diffuser du contenu à partir de votre application d’écriture sur un ou plusieurs serveurs exécutant Services Windows Media, qui distribuera ensuite le contenu aux utilisateurs.

## <a name="asf-file-editing-with-the-windows-media-format-sdk-metadata-editing"></a>édition de fichiers ASF avec le kit de développement logiciel (SDK) Windows Media Format (modification des métadonnées)

La modification du contenu de la section de données d’un fichier ASF implique la réécriture du fichier. le kit de développement logiciel (SDK) Windows Media Format ne fournit pas d’objets qui manipulent la section des données sur place. Pour les modifications simples, telles que la concaténation de deux fichiers ou le découpage du contenu d’un fichier, vous pouvez lire des exemples sans les décompresser, puis les écrire dans un nouveau fichier à l’aide des mêmes informations d’en-tête. Les modifications plus complexes impliquent d’apporter des modifications au profil utilisé pour le nouveau fichier.

le kit de développement logiciel (SDK) de Format multimédia Windows prend en charge la modification des parties de la section d’en-tête sans réécriture du fichier. L’en-tête d’un fichier ASF contient de nombreux types de données différents. Les plus couramment modifiés sont des attributs de métadonnées, qui sont des paires nom/valeur qui décrivent les aspects du contenu et les personnes impliquées dans sa création. vous pouvez modifier les métadonnées à l’aide de l’objet de l’éditeur de métadonnées du kit de développement logiciel (SDK) Windows Media Format Cet objet ouvre un fichier ASF, vous permet de modifier une partie du contenu de l’en-tête, d’écrire les modifications dans le fichier et de fermer le fichier. La modification des métadonnées est très simple, avec des appels de méthode simples pour récupérer et définir des valeurs.

## <a name="asf-file-reading-with-the-windows-media-format-sdk"></a>lecture de fichiers ASF avec le kit de développement logiciel (SDK) Windows Media Format

le kit de développement logiciel (SDK) Windows Media Format fournit deux objets distincts pour la lecture des fichiers ASF : l’objet lecteur et l’objet lecteur synchrone. l’objet lecteur est disponible dans toutes les versions du kit de développement logiciel (sdk), tandis que l’objet lecteur synchrone requiert le kit de développement logiciel (sdk) de la série 9 Windows Media Format 9 ou une version ultérieure. La principale différence entre les deux est que l’objet lecteur fournit des exemples à votre application en déclenchant des événements vers une méthode de rappel, tandis que le lecteur synchrone fournit des échantillons individuels en réponse aux appels de méthode.

Pour utiliser l’objet lecteur, vous devez implémenter plusieurs méthodes de rappel pour réagir à l’État et aux exemples de messages de l’objet lecteur. Vous configurez le lecteur pour remettre le contenu comme vous le souhaitez, démarrez le lecteur et attendez les exemples de messages. Le processus de récupération des exemples d’un fichier ASF est fondamentalement l’inverse du processus d’écriture. L’objet lecteur communique avec les codecs requis pour décoder tous les flux compressés et fournit des données non compressées à votre application. Vous pouvez également configurer l’objet lecteur pour remettre des exemples dans leur état compressé, afin que vous puissiez inclure un flux précédemment encodé dans un nouveau fichier.

L’objet lecteur synchrone fonctionne à peu près de la même façon que l’objet lecteur. Mais au lieu de configurer des rappels, vous devez demander chaque exemple du lecteur synchrone individuellement. L’utilisation du lecteur synchrone requiert un seul thread, tandis que l’utilisation du lecteur requiert plusieurs threads. L’objet lecteur synchrone présente plusieurs avantages par rapport à l’objet lecteur dans certaines circonstances, principalement pour les applications de modification de contenu qui doivent accéder rapidement à différentes parties d’un fichier et copier des données entre des fichiers. L’objet lecteur synchrone est bien plus simple à utiliser et vous permet de rechercher facilement des emplacements spécifiques dans la section de données. Toutefois, le lecteur synchrone ne prend pas en charge la lecture de fichiers sur un réseau et ne prend pas en charge la gestion des droits numériques.

## <a name="other-operations-with-the-windows-media-format-sdk"></a>autres opérations avec le kit de développement logiciel (SDK) Windows Media Format

outre les trois principales zones fonctionnelles décrites, le kit de développement logiciel (SDK) du Format de média Windows possède des objets pour effectuer d’autres opérations relatives aux fichiers ASF. L’objet gestionnaire de profils est utilisé pour créer des profils et y accéder, et les enregistrer. L’objet indexeur crée des objets index dans des fichiers ASF qui permettent de rechercher dans des fichiers vidéo. Enfin, l’objet lecteur et l’objet Writer prennent en charge la gestion des droits numériques pour protéger les droits de la intellectuelle des créateurs de contenu.

**Remarque** L’objectif de la structure de fichiers ASF et de ce kit de développement logiciel (SDK) est de produire des fichiers multimédias numériques contenant du son et de la vidéo, et cette documentation est écrite avec cela à l’esprit. Toutefois, la structure de fichiers ASF fonctionne également pour d’autres types de contenu. Vous pouvez trouver de nombreuses applications pour les fichiers ASF qui ne sont pas liées à l’audio et à la vidéo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**à propos du kit de développement logiciel (SDK) Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




