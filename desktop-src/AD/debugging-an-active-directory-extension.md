---
title: Débogage d’une extension de Active Directory
description: La feuille de propriétés du service Microsoft Active Directory Directory, le menu contextuel et les extensions de l’Assistant Création d’objets documentées dans cette rubrique sont implémentées en tant que serveurs COM in-proc.
ms.assetid: 8c280084-fd2f-4d34-a119-d4e925a68a5c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc8d9646f4ccc2e8c740a81ddb48422881744f5
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104031026"
---
# <a name="debugging-an-active-directory-extension"></a>Débogage d’une extension de Active Directory

La feuille de propriétés du service Microsoft Active Directory Directory, le menu contextuel et les extensions de l’Assistant Création d’objets documentées dans cette rubrique sont implémentées en tant que serveurs COM in-proc. Autrement dit, chaque extension est une DLL qui s’exécute dans le contexte du processus hôte. Pour déboguer l’extension, il est nécessaire d’associer l’extension à une application et d’exécuter l’application dans un débogueur.

## <a name="debugging-active-directory-extensions-displayed-in-the-windows-shell"></a>Débogage d’extensions de Active Directory affichées dans le shell Windows

Les extensions de Active Directory affichées dans le shell Windows sont chargées dans le contexte du processus de Explorer.exe. Ces extensions peuvent être déboguées comme une extension d’interpréteur de commandes standard. Pour plus d’informations sur le débogage des extensions d’environnement, consultez [débogage avec l’interpréteur](/previous-versions/windows/desktop/legacy/cc144064(v=vs.85))de commandes.

## <a name="debugging-active-directory-extensions-displayed-in-the-active-directory-mmc-snap-ins"></a>Débogage d’extensions de Active Directory affichées dans le Active Directory MMC Snap-Ins

Les extensions de Active Directory affichées dans les composants logiciels enfichables MMC d’administration de Active Directory sont chargées dans le contexte de la console MMC (Microsoft Management Console). Pour déboguer une extension, recherchez Mmc.exe sur le système local et définissez le débogueur pour l’utiliser en tant qu’application pour le débogage. Sur la plupart des systèmes, Mmc.exe se trouve dans le répertoire système de Windows, par exemple, C : \\ winnt \\ system32. Selon le débogueur, vous pouvez être amené à définir la DLL d’extension pour qu’elle soit également chargée par le débogueur. De nombreux débogueurs vous permettent également d’attacher le débogueur à un processus MMC en cours d’exécution. Pour plus d’informations, consultez le Guide de l’utilisateur du débogueur.

Il peut être commode de charger automatiquement MMC un composant logiciel enfichable spécifique. Pour ce faire, définissez les arguments d’application sur le chemin d’accès et le nom de fichier d’un fichier MSC. Il peut s’agir d’un fichier MSC installé par le système ou d’un fichier que vous créez. Vous pouvez créer un fichier MSC en procédant comme suit.

1.  Exécutez Mmc.exe.
2.  Chargez le composant logiciel enfichable souhaité en sélectionnant **fichier**  -  **Ajouter/supprimer un composant logiciel enfichable...** dans le menu MMC, puis sélectionnez le composant logiciel enfichable souhaité.
3.  Enregistrez le fichier MSC en sélectionnant **fichier**  -  **Enregistrer sous...** dans le menu MMC.

Si vous ne définissez pas de fichier MSC de démarrage, vous devez charger manuellement le composant logiciel enfichable souhaité lorsque vous exécutez l’application dans le débogueur.

Lorsque l’application hôte est exécutée dans le débogueur, le débogueur peut afficher un message d’avertissement indiquant que l’application en cours d’exécution ne contient pas de symboles de débogage. Cela est attendu et peut être ignoré en toute sécurité, car vous déboguez en fait la DLL, et non l’application hôte.

Dans la plupart des cas, l’extension n’est pas appelée tant que l’utilisateur n’a pas effectué une action qui entraîne le chargement et l’initialisation de l’extension. Par exemple, si vous déboguez une extension de menu contextuel affichée pour les objets utilisateur, l’extension ne se chargera pas tant que le menu contextuel d’un objet utilisateur ne sera pas affiché pour la première fois.

Vous devez maintenant être en mesure de définir des points d’arrêt et d’afficher la sortie de débogage. Si l’extension n’apparaît pas pour le chargement, définissez un point d’arrêt dans la fonction [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) de l’extension. Si **DllGetClassObject** n’est pas appelé, l’extension n’est probablement pas inscrite correctement.

Une fois le débogage terminé, quittez la console MMC et le débogueur doit se décharger normalement.

 

 