---
description: Un nom de périphérique MS-DOS est une jonction qui pointe vers le chemin d’accès d’un périphérique MS-DOS. Ces jonctions composent l’espace de noms du périphérique MS-DOS.
ms.assetid: 7d802e9f-dc09-4e3d-b064-e9b57af396e2
title: Définition d’un nom de périphérique MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ed89e1d9938e320ecce3ff0b35b8ae0792fe219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538871"
---
# <a name="defining-an-ms-dos-device-name"></a>Définition d’un nom de périphérique MS-DOS

Un nom de périphérique MS-DOS est une jonction qui pointe vers le chemin d’accès d’un périphérique MS-DOS. Ces jonctions composent l’espace de noms du périphérique MS-DOS. Appelez les fonctions [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) et [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) pour créer et modifier ces jonctions. [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) supprime une jonction créée par **SetVolumeMountPoint**, et **DefineDosDevice** supprime les jonctions qu’elle crée.

Une fois qu’un nom de périphérique MS-DOS est défini, il reste visible pour tous les processus.

-   Tous les périphériques MS-DOS sont identifiés par Windows via un ID d’authentification. Un ID d’authentification est le LUID (identificateur unique local) associé à chaque session de connexion au moment de sa création.
-   La visibilité d’un nom de périphérique MS-DOS est classée comme globale ou locale, et est définie comme telle par son inclusion dans les espaces de noms de périphérique MS-DOS global et de périphérique MS-DOS local. Le contenu des périphériques MS-DOS de l’espace de noms global est accessible par tous les utilisateurs, et le contenu des périphériques MS-DOS de l’espace de noms local est accessible uniquement par l’utilisateur dont le jeton d’accès contient le AuthenticationID associé à cet espace de noms d’appareil MS-DOS local.

Plusieurs espaces de noms d’appareils MS-DOS locaux et un seul espace de noms de périphérique MS-DOS global peuvent exister simultanément et sur un ordinateur.

Notez que seuls les processus qui s’exécutent dans le contexte LocalSystem peuvent appeler [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) pour créer un périphérique MS-DOS dans l’espace de noms de périphérique MS-DOS global. En outre, l’espace de noms de l’appareil MS-DOS local correspondant à un AuthenticationID spécifique est supprimé lorsque la dernière référence à ce AuthenticationID est supprimée.

Lorsque votre code interroge un nom de périphérique MS-DOS existant en appelant [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew), il commence par Rechercher l’espace de noms de l’appareil ms-dos local. Si ce n’est pas le cas, la fonction recherchera ensuite l’espace de noms de l’appareil MS-DOS global. Lorsque votre code interroge tous les noms de périphériques MS-DOS existants à l’aide de cette fonction, la liste des noms retournés dépend de s’il s’exécute dans le contexte LocalSystem. Dans ce cas, seuls les noms des périphériques MS-DOS inclus dans l’espace de noms du périphérique MS-DOS global sont renvoyés. Si ce n’est pas le cas, une concaténation des noms des appareils dans les espaces de noms des périphériques MS-DOS globaux et locaux est retournée. Si un nom de périphérique existe dans les deux espaces de noms, **QueryDosDevice** retourne l’entrée dans l’espace de noms de l’appareil ms-dos local. Cela s’applique également à la liste de tous les noms de périphériques MS-DOS retournés par [**GetLogicalDrives**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrives) et [**GetLogicalDriveStrings**](/windows/desktop/api/FileAPI/nf-fileapi-getlogicaldrivestringsw).

Notez que le scénario suivant peut se produire :

1.  L’utilisateur A, qui ne s’exécute pas dans le contexte LocalSystem, crée un nom de périphérique dans l’espace de noms de l’appareil MS-DOS local correspondant, et ce nom d’appareil n’existe pas dans l’espace de noms du périphérique MS-DOS global.
2.  L’utilisateur B, qui s’exécute dans le contexte LocalSystem, crée le même nom de périphérique dans l’espace de noms de périphérique MS-DOS global.

Dans ce scénario, l’utilisateur A n’a pas accès au nom de l’appareil dans l’espace de noms de l’appareil MS-DOS global tant qu’il n’a pas supprimé ou renommé le nom de l’appareil dans son espace de noms de périphérique MS-DOS local. Pour réduire la probabilité d’apparition de ce scénario, les lettres de lecteur MS-DOS doivent être allouées dans l’espace de noms d’appareil MS-DOS global à partir de C : et se terminant par et z :. Cette séquence doit être inversée pour l’allocation des lettres de lecteur MS-DOS dans l’espace de noms de l’appareil MS-DOS local.

Si vous n’êtes pas en cours d’exécution dans le contexte LocalSystem, [**DefineDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-definedosdevicew) ne vous permet pas de définir un nom de périphérique dans l’espace de noms de l’appareil ms-dos local si ce nom de périphérique existe déjà dans vos espaces de noms de périphérique MS-DOS local ou global. Appelez [**QueryDosDevice**](/windows/desktop/api/FileAPI/nf-fileapi-querydosdevicew) avant d’appeler **DefineDosDevice** pour déterminer si le nom de l’appareil que vous avez l’intention de définir existe dans vos espaces de noms de périphérique MS-DOS.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nommage des fichiers, chemins d’accès et espaces de noms](naming-a-file.md)
</dt> </dl>

 

 



