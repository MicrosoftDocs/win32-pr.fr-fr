---
title: Journalisation binaire centralisée
description: La journalisation binaire centralisée est un type de journalisation côté serveur qui peut être activé sur la session serveur.
ms.assetid: 957a7bc4-9db3-4153-b0a9-e53b3cc514c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2006270a6bdb2b06748214bff6170b369de791456577caeb62a9abc4b625bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047569"
---
# <a name="centralized-binary-logging"></a>Journalisation binaire centralisée

La journalisation binaire centralisée est un type de journalisation côté serveur qui peut être activé sur la session serveur. La journalisation binaire centralisée fonctionne comme une forme centralisée de journalisation pour tous les groupes d’URL créés dans le cadre de la session de serveur, et permet à tous les groupes d’URL sous la session serveur d’envoyer des données de journal binaires non formatées à un seul fichier journal. Ce type de journalisation peut être activé uniquement sur la session serveur. elle ne peut pas être activée sur le groupe d’URL.

## <a name="when-to-use-centralized-binary-logging"></a>Quand utiliser la journalisation binaire centralisée

Lorsque la session serveur comporte de nombreux groupes d’URL, le processus de création de centaines de fichiers journaux mis en forme pour des groupes d’URL individuels et l’écriture des données du journal sur un disque peut rapidement consommer des ressources processeur et mémoire précieuses, ce qui entraîne des problèmes de performances et d’évolutivité. La journalisation binaire centralisée réduit la quantité de ressources système utilisées pour la journalisation, tout en fournissant en même temps des données de journal détaillées pour les organisations qui en ont besoin.

La journalisation binaire centralisée est une propriété de session serveur qui, lorsqu’elle est activée, configure la journalisation de tous les groupes d’URL sous la session serveur. Lorsque la journalisation binaire centralisée est activée, les données ne peuvent pas être enregistrées ou mises en forme pour des groupes d’URL individuels. Le fichier journal de journalisation binaire centralisé a une extension de nom de fichier journal binaire Internet (. IBL). Cette extension de nom de fichier garantit que les utilitaires de texte ne tentent pas d’ouvrir et de lire le fichier journal de journalisation binaire central.

## <a name="extracting-data-from-the-centralized-binary-log-file"></a>Extraction de données à partir du fichier journal binaire centralisé

Les étapes suivantes sont effectuées pour extraire des données d’un fichier journal brut :

-   Créez un outil qui localise et extrait les données que vous souhaitez à partir du fichier brut et convertit les données en texte mis en forme. Vous pouvez afficher les descriptions des formats de fichier d’en-tête et de fichier journal dans le kit de développement logiciel (SDK) IIS 6,0 sur MSDN.
-   Utilisez l’outil Analyseur de journal pour extraire les données du fichier brut. L’outil Analyseur de journal et la documentation utilisateur qui l’accompagne sont inclus dans les outils du kit de ressources IIS 6,0.

## <a name="centralized-binary-logging-file-format"></a>Format de fichier de journalisation binaire centralisé

Le fichier journal de journalisation binaire centralisée brut est constitué d’enregistrements de longueur fixe ou d’enregistrements d’index qui contiennent des identificateurs de chaîne. Les enregistrements d’index s’affichent car, dans le but d’enregistrer autant d’informations que possible, les champs de chaîne de longueur variable sont remplacés par des identificateurs numériques (index) qui mappent la chaîne de longueur variable à l’identificateur journalisé.

Le fichier journal brut n’est pas lisible par l’utilisateur et ne peut pas être lu à l’aide des analyseurs de journaux les plus disponibles. Pour extraire des données d’un fichier journal brut, vous pouvez créer un outil qui localise et extrait les données, puis les convertit en texte mis en forme.

Pour plus d’informations, consultez [journalisation centralisée des fichiers binaires](/previous-versions/windows/it-pro/windows-server-2003/cc758733(v=ws.10)) sur Microsoft TechNet.

 

 