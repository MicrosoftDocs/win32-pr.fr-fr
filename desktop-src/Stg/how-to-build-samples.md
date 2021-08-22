---
title: Comment générer des exemples
description: Pour générer un exemple COM, l’environnement de l’ordinateur doit être configuré pour générer des applications Microsoft Win32 C++.
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- Comment générer des exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782a75bb54127191757a515244d439bbff9570c96f4e0bb2ac603477bedb96a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663119"
---
# <a name="how-to-build-samples"></a>Comment générer des exemples

Pour générer un exemple COM, l’environnement de l’ordinateur doit être configuré pour générer des applications Microsoft Win32 C++.

## <a name="preparing-a-computer-to-create-com-samples"></a>Préparation d’un ordinateur pour créer des exemples COM

l’environnement de l’ordinateur doit être configuré avec un compilateur C++ 32 bits, un éditeur de liens et un compilateur de ressources correctement installés et compatibles avec Microsoft Visual C++ 4. x ou version ultérieure, et un SDK Windows correctement installé. il est préférable d’installer le SDK Windows dernier. le SDK Windows fournit des fichiers de bibliothèque et. lib requis pour la fonctionnalité COM codée dans les exemples.

pour exécuter avec succès les exemples Remclien, Freserve et Freclien nécessite des fonctionnalités système disponibles dans les systèmes d’exploitation Windows : Windows Server 2003, Windows XP, Windows 2000 ou Windows NT 4,0. les exemples Remclien, Freserve et Freclien seront générés, mais ils ne s’exécuteront pas sur les systèmes d’exploitation Windows i, Windows 98 ou Windows 95, sauf si DCOM (Distributed com) et com free thread font partie du système d’exploitation. cette prise en charge est disponible pour les systèmes d’exploitation Windows i, Windows 98 et Windows 95 dans le module complémentaire DCOM95. DCOM95 peut actuellement être obtenu par [téléchargement à partir de Microsoft](https://www.microsoft.com/download/details.aspx?id=31661).

Chaque répertoire d’exemple contient les fichiers sources nécessaires pour générer et exécuter l’exemple. Le répertoire de l’exemple parent contient un fichier Makeall.bat, que vous pouvez exécuter à partir de l’invite de commandes pour rendre tous les exemples de code dans la branche ci-dessous. Pour plus d’informations, consultez le fichier Makeall.bat. Si votre environnement est configuré pour générer des applications C++ Win32, vous pouvez simplement exécuter Makeall.bat à partir du répertoire où il réside pour générer tous les exemples de code dans la branche ci-dessous. Makeall garantit l’ordre correct de la build afin que toutes les dépendances de l’exemple de code soient satisfaites.

Le répertoire principal possède également un Makefile qui génère tous les exemples de code du didacticiel à l’aide d’options similaires à celles prises en charge par Makeall.bat. Pour plus d’informations, consultez ce Makefile. ce makefile suppose que l’intégralité de la branche samples code est installée dans le cadre de la SDK Windows. À l’heure actuelle, cet emplacement a un chemin d’accès similaire à *D : \\ MSSDK \\ Samples \\ com \\ TUTSAMP*, où D : représente le lecteur d’installation. si vous avez extrait l’exemple de branche de code du didacticiel (par exemple, le répertoire com com et ses sous-répertoires) vers un autre emplacement en dehors du SDK Windows (ou si vous avez obtenu l’exemple défini en tant que téléchargement distinct à partir du site web de Microsoft), utilisez Makeall.bat pour compiler tous les exemples de la branche. En général, Makeall.bat est recommandé. Un fichier de Logmall.bat est également fourni. Il est identique au fichier de commandes makeall, sauf qu’il journalise toute la sortie de compilation dans un fichier Errorlog.txt dans le répertoire principal du didacticiel.

Deux fichiers de commandes, Regall.bat et Unregall.bat, sont également fournis dans le répertoire principal pour inscrire et annuler l’inscription de tous les serveurs COM dans la série d’exemples de code du didacticiel. Pour inscrire tous les serveurs, exécutez Regall.bat fichier à partir du répertoire principal. Pour annuler l’inscription de tous les serveurs, exécutez Unregall.bat de la même manière. Ces fichiers de commandes requièrent une génération antérieure des exemples de code REGISTER, MARSHAL, DLLSERVE, LICSERVE, LOCSERVE, APTSERVE, FRESERVE et conserved. Si vous effectuez une génération normale des exemples de code, les Makefiles serveur inscriront automatiquement les serveurs. Dans ce cas, il n’est pas nécessaire d’exécuter le fichier de commandes Regall.

Exécutez le fichier de commandes Cleanall.bat pour effectuer une cleanall exhaustive de tous les exemples de didacticiels COM.

> [!WARNING]
> ce fichier de commandes supprime tous les fichiers de Visual Studio projet et d’autres fichiers de travail temporaires créés par Visual C++ dans les exemples. Tous les serveurs COM générés dans les exemples de code du didacticiel sont désinscrits du Registre. Tous les fichiers exe et .dll exécutables sont supprimés. Tous les fichiers de symboles de débogage sont supprimés. Les fichiers générés dans divers environnements de génération sont également supprimés.

 

Exécutez « makeall Clean » pour effectuer un nettoyage plus rapide, mais plus modeste, de tous les exemples de code. Cette opération de nettoyage ne tente pas d’être aussi complète que celle exécutée par Cleanall.bat. Les fichiers. obj sont supprimés, mais les binaires de sortie sont conservés. Les serveurs COM ne sont pas désinscrits du Registre.

cette série d’exemples provient d’une partie intégrante de la SDK Windows. par conséquent, la narration du didacticiel part du principe qu’un environnement avec le SDK Windows correctement installé.

toutefois, les versions de Microsoft Visual C++ version 4,0 et ultérieure peuvent également fournir les fichiers de bibliothèque include et. lib requis pour la compilation. dans ce cas, l’installation du SDK Windows peut ne pas être nécessaire pour compiler les exemples.

Pour plus d’informations et pour obtenir des exemples détaillés de génération, consultez :

[Configuration de l’environnement](environment-setup.md)

[Makefiles](makefiles.md)

[Utilisation de Visual Studio](using-visual-studio.md)

[Extraction des exemples de code](extracting-the-code-samples.md)

[Conventions de style de codage](coding-style-conventions.md)

 

 




