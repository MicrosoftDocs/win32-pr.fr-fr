---
description: L’exemple suivant décrit comment organiser votre application en composants Windows Installer.
ms.assetid: 981a3def-1e59-4703-ad97-c8cd5431375d
title: Définition des composants du programme d’installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ade4476fa1bf54a0ab4f64d0d43d72265ac1eb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534613"
---
# <a name="defining-installer-components"></a>Définition des composants du programme d’installation

L’exemple suivant décrit comment organiser votre application en composants Windows Installer.

**Pour organiser une application en composants**

1.  Commencez par obtenir un répertoire et une arborescence de fichiers pour tous les fichiers et autres ressources utilisés dans votre application.
2.  Identifiez les fichiers, les clés de Registre, les raccourcis ou les autres ressources qui sont partagés entre les applications et qui peuvent être fournis par les composants existants disponibles sous forme de [modules de fusion](merge-modules.md). Vous ne devez pas inclure ces ressources dans les composants que vous créez. Au lieu de cela, vous devez obtenir ces composants en fusionnant les modules de fusion dans votre package d’installation. Les étapes suivantes décrivent comment organiser les ressources restantes de l’application en composants.
3.  Définissez un nouveau composant pour chaque fichier. exe,. dll et. ocx. Désignez ces fichiers comme fichiers de chemin d’accès de clé de leurs composants. Assignez à chaque composant un GUID de code de composant.
4.  Définissez un nouveau composant pour chaque fichier d’aide. hlp ou. chm. Désignez ces fichiers comme fichiers de chemin d’accès de clé de leurs composants. Ajoutez les fichiers. CNT ou. Chi aux composants contenant les fichiers. hlp et. chm associés. Assignez à chaque composant un GUID de code de composant.
5.  Définissez un nouveau composant pour chaque fichier qui sert de cible de raccourci. Désignez ces fichiers comme fichiers de chemin d’accès de clé de leurs composants. Assignez à chaque composant un GUID de code de composant.
6.  Regroupez toutes les ressources restantes dans des dossiers. Toutes les ressources de chaque dossier doivent être fournies ensemble. S’il est possible qu’une paire de ressources soit livrée séparément, placez-les dans des dossiers distincts. Définissez un nouveau composant pour chaque dossier. Essayez de réduire le nombre total de composants pour améliorer les performances. Divisez l’application en plusieurs composants lorsqu’il est nécessaire que le programme d’installation vérifie complètement la validité de l’installation. Désignez n’importe quel fichier du composant comme fichier de chemin d’accès de clé. Assignez à chaque composant un GUID de code de composant.
7.  Ajoutez des clés de Registre aux composants. Toutes les clés de Registre qui pointent vers un fichier doivent être incluses dans le composant de ce fichier. Les autres clés de Registre doivent être regroupées logiquement avec les fichiers qui en ont besoin.

 

 



