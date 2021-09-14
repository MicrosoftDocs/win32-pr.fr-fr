---
description: Pour mapper les données d’un fichier à la mémoire virtuelle d’un processus, vous devez créer une vue du fichier.
ms.assetid: b1ebd9a4-cde4-4c0c-80d2-5ccb655cd3a4
title: Création d’un affichage des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498f7ba132efd9ecf82f9ec087492c9622824b51
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094193"
---
# <a name="creating-a-file-view"></a>Création d’un affichage des fichiers

Pour mapper les données d’un fichier à la mémoire virtuelle d’un processus, vous devez créer une vue du fichier. Les fonctions [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) et [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) utilisent le descripteur d’objet de mappage de fichier retourné par [**CreateFileMapping**](/windows/desktop/api/WinBase/nf-winbase-createfilemappinga) pour créer une vue du fichier ou une partie du fichier dans l’espace d’adressage virtuel du processus. Ces fonctions échouent si les indicateurs d’accès sont en conflit avec ceux spécifiés lorsque **CreateFileMapping** a créé l’objet de mappage de fichier.

La fonction [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) retourne un pointeur vers l’affichage des fichiers. En déréférençant un pointeur dans la plage d’adresses spécifiée dans **MapViewOfFile**, une application peut lire des données à partir du fichier et écrire des données dans le fichier. L’écriture dans l’affichage des fichiers entraîne des modifications de l’objet de mappage de fichier. L’écriture réelle dans le fichier sur le disque est gérée par le système. Les données ne sont pas réellement transférées au moment où l’objet de mappage de fichier est écrit. Au lieu de cela, une grande partie de l’entrée et de la sortie du fichier (e/s) est mise en cache pour améliorer les performances générales du système. Les applications peuvent remplacer ce comportement en appelant la fonction [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) pour forcer le système à effectuer immédiatement des transactions sur disque.

La fonction [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) fonctionne exactement comme la fonction [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) , à ceci près qu’elle permet à un processus de spécifier l’adresse de base de la vue du fichier dans l’espace d’adressage virtuel du processus dans le paramètre *lpvBase* . S’il n’y a pas assez d’espace à l’adresse spécifiée, l’appel échoue. Par conséquent, si vous devez mapper un fichier à la même adresse dans plusieurs processus, les processus doivent négocier une adresse appropriée : le paramètre *lpvBase* doit être un multiple entier de la granularité d’allocation de mémoire système ou l’appel échoue. Pour obtenir la granularité d’allocation de mémoire du système, utilisez la fonction [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) , qui remplit les membres d’une structure d' [**\_ informations système**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .

Une application peut créer plusieurs vues de fichiers à partir du même objet de mappage de fichier. Une vue de fichier peut avoir une taille différente de celle de l’objet de mappage de fichier dont elle est dérivée, mais elle doit être inférieure à l’objet de mappage de fichier. Le décalage spécifié par les paramètres *dwOffsetHigh* et *dwOffsetLow* de [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) doit être un multiple de la granularité d’allocation du système.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une vue dans un fichier](creating-a-view-within-a-file.md)
</dt> </dl>

 

 
