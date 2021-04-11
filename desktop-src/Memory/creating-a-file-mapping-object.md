---
description: La première étape du mappage d’un fichier consiste à ouvrir le fichier en appelant la fonction CreateFile.
ms.assetid: e00d8742-b717-419c-902c-9a286d75d8aa
title: Création d’un objet de mappage de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65badc2af8aed5211c2f5c590fc0998019dae264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319122"
---
# <a name="creating-a-file-mapping-object"></a>Création d’un objet de mappage de fichier

La première étape du mappage d’un fichier consiste à ouvrir le fichier en appelant la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) . Pour vous assurer que les autres processus ne peuvent pas écrire dans la partie du fichier qui est mappée, vous devez ouvrir le fichier avec un accès exclusif. En outre, le descripteur de fichier doit rester ouvert jusqu’à ce que le processus n’ait plus besoin de l’objet de mappage de fichier. Un moyen simple d’obtenir un accès exclusif consiste à spécifier zéro dans le paramètre *fdwShareMode* de **CreateFile**. Le handle retourné par **CreateFile** est utilisé par la fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) pour créer un objet de mappage de fichier.

La fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) retourne un handle vers l’objet de mappage de fichier. Ce descripteur sera utilisé lors [de la création d’une vue de fichier](creating-a-file-view.md) afin que vous puissiez accéder à la mémoire partagée. Quand vous appelez **CreateFileMapping**, vous spécifiez un nom d’objet, le nombre d’octets à mapper à partir du fichier et l’autorisation de lecture/écriture pour la mémoire mappée. Le premier processus qui appelle **CreateFileMapping** crée l’objet de mappage de fichier. Les processus qui appellent **CreateFileMapping** pour un objet existant reçoivent un handle vers l’objet existant. Vous pouvez savoir si un appel réussi à **CreateFileMapping** a créé ou ouvert l’objet de mappage de fichier en appelant la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) . **GetLastError** **ne retourne aucune \_ erreur** au processus de création et l' **erreur \_ \_ existe déjà** pour les processus suivants.

La fonction [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) échoue si les indicateurs d’accès sont en conflit avec ceux spécifiés lors de l’ouverture du fichier par la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) . Par exemple, pour lire et écrire dans le fichier :

-   Spécifiez les valeurs d' **\_ écriture** génériques **\_ en lecture** et générique dans le paramètre *fdwAccess* de [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea).
-   Spécifiez la valeur **\_ ReadWrite de page** dans le paramètre *fdwProtect* de [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga).

La création d’un objet de mappage de fichier ne valide pas la mémoire physique, il la réserve uniquement.

## <a name="file-mapping-size"></a>Taille du mappage de fichier

La taille de l’objet de mappage de fichier est indépendante de la taille du fichier mappé. Toutefois, si l’objet de mappage de fichier est plus grand que le fichier, le système développe le fichier avant que [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) ne retourne. Si l’objet de mappage de fichier est plus petit que le fichier, le système mappe uniquement le nombre spécifié d’octets à partir du fichier.

Les paramètres *dwMaximumSizeHigh* et *dwMaximumSizeLow* de [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) vous permettent de spécifier le nombre d’octets à mapper à partir du fichier :

-   Si vous ne souhaitez pas que la taille du fichier change (par exemple, lors du mappage de fichiers en lecture seule), appelez [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) et spécifiez zéro pour *dwMaximumSizeHigh* et *dwMaximumSizeLow*. Cela crée un objet de mappage de fichier qui a exactement la même taille que le fichier. Dans le cas contraire, vous devez calculer ou estimer la taille du fichier fini, car la taille des objets de mappage de fichier est statique. une fois créé, leur taille ne peut pas être augmentée ou diminuée. Une tentative de mappage d’un fichier avec une longueur de zéro de cette manière échoue avec un code d’erreur de **fichier d’erreur \_ \_ non valide**. Les programmes doivent tester les fichiers dont la longueur est égale à zéro et rejeter ces fichiers.

-   La taille d’un objet de mappage de fichier qui est stocké par un fichier nommé est limitée par l’espace disque. La taille d’une vue de fichier est limitée au plus grand bloc contigu disponible de mémoire virtuelle non réservée. Il se trouve au maximum de 2 Go moins la mémoire virtuelle déjà réservée par le processus.

La taille de l’objet de mappage de fichier que vous sélectionnez contrôle à quelle distance dans le fichier vous pouvez « voir » le mappage de mémoire. Si vous créez un objet de mappage de fichier dont la taille est de 500 Ko, vous avez accès uniquement aux 500 premiers Ko du fichier, quelle que soit la taille du fichier. Étant donné qu’il ne coûte aucune ressource système pour créer un objet de mappage de fichier plus volumineux, créez un objet de mappage de fichier qui correspond à la taille du fichier (définissez les paramètres *dwMaximumSizeHigh* et *dwMaximumSizeLow* de [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) à la fois sur zéro) même si vous ne prévoyez pas d’afficher l’intégralité du fichier. Le coût des ressources système est lié à la création des vues et à leur accès.

Si vous souhaitez afficher une partie du fichier qui ne commence pas au début du fichier, vous devez créer un objet de mappage de fichier. Cet objet correspond à la taille de la partie du fichier que vous souhaitez afficher plus l’offset dans le fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une vue dans un fichier](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
