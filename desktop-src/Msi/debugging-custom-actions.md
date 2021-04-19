---
description: Vous pouvez déboguer des actions personnalisées basées sur des bibliothèques de liens dynamiques à l’aide des outils de débogage pour Windows. Il n’est pas possible d’utiliser le débogage dynamique avec des actions personnalisées basées sur des scripts ou des fichiers exécutables.
ms.assetid: 4241a27a-c127-4c65-96a2-1d655b343eba
title: Débogage des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ddfbc9952f0dd7fc1b85b5c64fa6a23381ceafe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544950"
---
# <a name="debugging-custom-actions"></a>Débogage des actions personnalisées

Vous pouvez déboguer des actions personnalisées basées sur des [bibliothèques de liens dynamiques](dynamic-link-libraries.md) à l’aide [des outils de débogage pour Windows](https://www.microsoft.com/?ref=go). Il n’est pas possible d’utiliser le débogage dynamique avec des actions personnalisées basées sur des [scripts](scripts.md)ou des [fichiers exécutables](executable-files.md) .

Les techniques décrites dans cette section peuvent vous aider à déboguer Windows Installer actions personnalisées. Pour plus d’informations sur les [outils de débogage pour Windows](https://www.microsoft.com/?ref=go), consultez la section outils de développement de pilotes de Windows Driver Kit (WDK).

Windows Installer utilise la variable d’environnement MsiBreak pour déterminer l’action personnalisée à déboguer. Si vous avez accès au code source de l’action personnalisée, vous pouvez être en mesure d’utiliser le débogage sans MsiBreak. Pour démarrer le débogage sans MsiBreak, placez une boîte de message temporaire au début du code de l’action. Quand la boîte de message s’affiche pendant l’installation, attachez le débogueur au processus qui possède la boîte de message. Vous pouvez ensuite définir les points d’arrêt nécessaires et ignorer la boîte de message pour reprendre l’exécution. Cette méthode ne permet pas de déboguer les parties précédentes de l’action personnalisée.

Pour utiliser la variable d’environnement MsiBreak pour déboguer l’action personnalisée, définissez MsiBreak sur le nom de l’action personnalisée dans la [table CustomAction](customaction-table.md). MsiBreak peut être une variable d’environnement système ou utilisateur. Si la variable est définie en tant que variable système, un redémarrage du système peut être nécessaire lorsque la valeur est modifiée pour détecter la nouvelle valeur.

Pour utiliser la variable d’environnement MsiBreak pour déboguer une interface utilisateur incorporée, définissez la valeur de MsiBreak sur MsiEmbeddedUI.

Windows Installer vérifie uniquement la variable d’environnement MsiBreak si l’utilisateur est un administrateur. Le programme d’installation ignore la valeur de MsiBreak si l’utilisateur n’est pas un administrateur, même s’il s’agit d’une [*application gérée*](m-gly.md).

Si vous déboguez une action personnalisée qui s’exécute avec des privilèges élevés (système) dans la séquence d’exécution, attachez le débogueur au service Windows Installer. Lors du débogage d’une action personnalisée qui s’exécute avec des privilèges empruntés dans la séquence d’exécution, le système affiche une boîte de dialogue qui indique le processus à déboguer. L’utilisateur est invité par une boîte de dialogue indiquant le processus à déboguer. Pour plus d’informations sur les actions personnalisées avec élévation de privilèges, consultez sécurité des actions [personnalisées](custom-action-security.md).

Une fois que le débogueur a été attaché au processus approprié, le programme d’installation déclenche un point d’arrêt du débogueur immédiatement avant d’appeler le point d’entrée de la DLL. Au point d’arrêt, votre DLL est déjà chargée dans le processus et l’adresse du point d’entrée est déterminée. Si votre DLL d’action personnalisée n’a pas pu être chargée ou si le point d’entrée de l’action personnalisée n’existait pas, aucun point d’arrêt n’est déclenché. Étant donné que le point d’arrêt est déclenché avant l’appel de la fonction DLL, une fois le point d’arrêt déclenché, vous devez utiliser votre débogueur pour effectuer un pas à pas détaillé jusqu’à ce que votre point d’entrée d’action personnalisé soit appelé. Vous pouvez également définir un point d’arrêt n’importe où dans votre action personnalisée et reprendre l’exécution normale.

Le Windows Installer exécute les dll qui ne sont pas stockées dans la [table binaire](binary-table.md) directement à partir de l’emplacement de la dll. Le programme d’installation ne connaît pas le nom d’origine d’une DLL stockée dans la table binaire et exécute l’action personnalisée DLL sous un nom de fichier temporaire. La forme du nom de fichier temporaire est MSI ?????. TMP. Sur Windows XP, ce fichier temporaire est stocké dans un emplacement sécurisé, généralement le <WindowFolder> \\ programme d’installation.

Notez que de nombreuses dll créées pour le débogage contiennent le nom et le chemin d’accès du fichier PDB correspondant dans le cadre de la DLL proprement dite. Lors du débogage de ce type de DLL sur un système où le fichier PDB se trouve à l’emplacement stocké dans la DLL, les symboles peuvent être chargés automatiquement par l’outil débogueur. Dans les situations où le fichier PDB est introuvable à l’emplacement stocké, où le débogueur ne prend pas en charge le chargement de symboles à partir de l’emplacement stocké, ou où la DLL n’a pas été générée avec des informations de débogage, vous devrez peut-être placer vos fichiers de symboles dans le dossier avec le fichier DLL temporaire.

Le programme d’installation ajoute des informations de débogage pour les scripts d’action personnalisés dans le fichier journal d’installation.

``` syntax
There is a problem with this Windows Installer package. A script 
required for this install to complete could not be run. Contact your 
support personnel or package vendor.  {Custom action [2] script error 
[3], [4]: [5] Line [6], Column [7], [8] }
```

 

 



