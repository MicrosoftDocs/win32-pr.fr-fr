---
title: Récepteurs
description: Récepteurs
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- Windows Media Format SDK, récepteurs
- Windows Media Format SDK, récepteurs de fichiers
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- ASF (Advanced Systems Format), récepteurs de fichiers
- ASF (format des systèmes avancés), récepteurs de fichiers
- Windows Media Format SDK, récepteurs réseau
- Windows Media Format SDK, récepteurs Push
- ASF (Advanced Systems Format), récepteurs réseau
- ASF (format des systèmes avancés), récepteurs réseau
- ASF (Advanced Systems Format), récepteurs Push
- ASF (format avancé des systèmes), récepteurs Push
- récepteurs, à propos de
- récepteurs de fichiers, à propos de
- récepteurs réseau
- récepteurs Push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030828"
---
# <a name="sinks"></a>Récepteurs

L’objet Writer du kit de développement logiciel (SDK) du format Windows Media fournit le contenu traité aux récepteurs. Chaque récepteur est un objet qui fournit des données. Le point de remise dépend du type de récepteur. Il existe trois types de récepteurs : les récepteurs de fichiers, les récepteurs réseau et les récepteurs de notifications push.

## <a name="file-sinks"></a>Récepteurs de fichiers

Les récepteurs de fichiers écrivent du contenu ASF dans un fichier sur un lecteur local ou réseau. Lorsque vous utilisez l’objet Writer pour écrire un fichier sans ajouter explicitement un récepteur de fichiers, le writer en crée un pour vous en utilisant le nom que vous transmettez à [**IWMWriter :: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename). Vous pouvez assigner plusieurs récepteurs de fichiers à un objet Writer pour écrire le contenu dans plusieurs fichiers à la fois.

À l’aide d’un récepteur de fichiers, vous pouvez contrôler de nombreux aspects du fichier. Les fonctionnalités suivantes sont disponibles via un récepteur de fichiers.

-   Analyse des statistiques de fichiers. Vous pouvez surveiller la taille et la durée des fichiers au fur et à mesure de leur création.
-   Création partielle du fichier de contenu. Les récepteurs de fichiers peuvent être configurés pour commencer à écrire du contenu à un moment donné et pour terminer l’écriture à un moment donné. Cela vous permet de créer plusieurs fichiers contenant différentes sections du même contenu dans le même test d’écriture.

## <a name="network-sinks"></a>Récepteurs réseau

Les récepteurs réseau diffusent du contenu vers une adresse réseau. La lecture des clients peut se connecter à l’adresse pour recevoir la diffusion.

## <a name="push-sinks"></a>Récepteurs Push

Les récepteurs de notifications push délivrent le contenu du writer à un serveur exécutant Windows Media Services. Les récepteurs de notifications push sont généralement utilisés dans les scénarios où un ordinateur encode le contenu dynamique et le remet à un ou plusieurs serveurs pour une distribution étendue. L’utilisation d’un récepteur de notifications Push vous permet de dédier des ordinateurs à des tâches spécifiques, économisant ainsi la bande passante et la puissance de traitement sur chaque serveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités d’écriture de fichier**](file-writing-features.md)
</dt> <dt>

[**Utilisation des récepteurs d’écriture**](working-with-writer-sinks.md)
</dt> </dl>

 

 




