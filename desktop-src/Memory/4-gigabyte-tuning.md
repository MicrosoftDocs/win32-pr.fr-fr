---
description: 'Réglage à 4 gigaoctets : BCDEdit et Boot.ini'
ms.assetid: 991eb86f-9e6f-4084-8b6f-f979e42104b5
title: 'Réglage à 4 gigaoctets : BCDEdit et Boot.ini'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f997ae09748370d5ec8ec246da80b6440d7aaf45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094233"
---
# <a name="4-gigabyte-tuning-bcdedit-and-bootini"></a>Réglage à 4 gigaoctets : BCDEdit et Boot.ini

sur les éditions 32 bits de Windows, les applications disposent de 4 gigaoctets (go) d’espace d’adressage virtuel disponible. L’espace d’adressage virtuel est divisé de manière à ce que 2 Go soient disponibles pour l’application et les 2 Go sont uniquement disponibles pour le système. La fonctionnalité de réglage à 4 gigaoctets (réglage de RAM 4GT ou 4GT), activée avec la commande *bcdedit/set increaseuserva* , augmente l’espace d’adressage virtuel disponible pour l’application jusqu’à 3 Go, et réduit la quantité disponible sur le système entre 1 et 2 Go.

Pour les applications gourmandes en mémoire, telles que les systèmes de gestion de base de données (SGBD), l’utilisation d’un espace d’adressage virtuel plus important peut offrir des avantages considérables en matière de performances et d’évolutivité. Toutefois, le cache de fichiers, le pool paginé et la réserve non paginée sont plus petits, ce qui peut nuire aux applications avec une mise en réseau lourde ou des e/s. Par conséquent, vous pouvez tester votre application sous charge et examiner les compteurs de performance pour déterminer si votre application tire parti de l’espace d’adressage plus grand.

Pour activer 4GT, utilisez la commande [bcdedit/set](/windows-hardware/drivers/devtest/bcdedit--set) pour définir l’option d’entrée de démarrage **increaseuserva** sur une valeur comprise entre 2048 (2 Go) et 3072 (3 Go).

**Windows Server 2003 et versions antérieures :** Pour activer 4GT, ajoutez le commutateur **/3GB** au fichier Boot.ini. Le commutateur **/3GB** est pris en charge sur les systèmes suivants :

-   Windows Server 2003
-   Windows XP Professionnel

Le commutateur **/3GB** permet aux applications d’accéder à 3 Go d’espace d’adressage virtuel complet et réduit la quantité de mémoire disponible pour le système à 1 Go. sur Windows Server 2003, la quantité d’espace d’adressage disponible pour les applications peut être ajustée en définissant le commutateur **/userva** dans Boot.ini sur une valeur comprise entre 2048 et 3072, ce qui augmente la quantité d’espace d’adressage disponible pour le système. Cela peut aider à maintenir les performances globales du système lorsque l’application nécessite plus de 2 Go mais moins de 3 Go d’espace d’adressage.

Pour permettre à une application d’utiliser l’espace d’adressage le plus grand, définissez l’indicateur de prise en [**\_ \_ \_ \_ charge d’adresses volumineuses du fichier image**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) dans l’en-tête d’image. l’éditeur de liens inclus avec Microsoft Visual C++ prend en charge le commutateur **/largeaddressaware** pour définir cet indicateur. La définition de cet indicateur, puis l’exécution de l’application sur un système qui ne dispose pas de la prise en charge de 4GT, ne doit pas affecter l’application.

sur les éditions 64 bits de Windows, les applications 32 bits marquées avec l’indicateur de [**\_ \_ \_ \_ reconnaissance d’adresse volumineux du fichier IMAGE**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) disposent de 4 go d’espace d’adressage disponibles.

**éditions Itanium du Windows Server 2003 :** Avant SP1, les processus 32 bits ne disposent que de 2 Go d’espace d’adressage disponibles.

Utilisez les instructions suivantes pour prendre en charge 4GT dans les applications :

-   Les adresses proches de la limite de 2 Go sont généralement utilisées par différentes DLL système. Par conséquent, un processus 32 bits ne peut pas allouer plus de 2 Go de mémoire contiguë, même si la totalité de l’espace d’adressage de 4 Go est disponible.
-   Pour récupérer la quantité d’espace virtuel utilisateur total, utilisez la fonction [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) . Pour récupérer l’adresse utilisateur la plus élevée possible, utilisez la fonction [**GetSystemInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) . Détectez toujours la valeur réelle au moment de l’exécution et évitez d’utiliser des définitions constantes câblées telles que : `#define HIGHEST_USER_ADDRESS 0xC0000000` .
-   Évitez les comparaisons signées avec des pointeurs, car ils peuvent provoquer le blocage des applications sur un système compatible 4GT. Une condition telle que la suivante est false pour un pointeur qui est au-dessus de 2 Go : `if (pointer > 40000000)` .
-   Le code qui utilise le bit le plus élevé d’un pointeur pour une fonction définie par l’application échouera quand 4GT sera activé. Par exemple, un mot de 32 bits peut être considéré comme une adresse en mode utilisateur s’il est inférieur à 0x80000000 et un code d’erreur s’il est indiqué ci-dessus. Ce n’est pas le cas avec 4GT.

[**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) retourne généralement des adresses faibles avant les adresses haute. Par conséquent, votre processus peut ne pas utiliser des adresses très élevées, sauf s’il alloue beaucoup de mémoire ou a un espace d’adressage virtuel fragmenté. Pour forcer les allocations à allouer à partir d’adresses supérieures avant des adresses plus basses à des fins de test, spécifiez mem de haut en bas lors de l’appel de **VirtualAlloc** ou définissez la valeur de Registre suivante sur **\_ \_ la** valeur égale à égale à

**HKEY \_ Gestion \_** de la \\  \\  \\  \\ mémoire du gestionnaire de session du **Gestionnaire de session** \\  \\  du système d’ordinateur local AllocationPreference

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[limites de mémoire pour les versions de Windows](memory-limits-for-windows-releases.md)
</dt> <dt>

[Extension d’adresse physique](physical-address-extension.md)
</dt> <dt>

[informations techniques de référence sur 4GT](/previous-versions/windows/it-pro/windows-server-2003/cc778496(v=ws.10))
</dt> </dl>

 

 
