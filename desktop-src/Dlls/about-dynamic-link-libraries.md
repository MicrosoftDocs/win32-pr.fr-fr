---
description: La liaison dynamique permet à un module d’inclure uniquement les informations nécessaires pour localiser une fonction DLL exportée au moment du chargement ou de l’exécution.
ms.assetid: df2a8e4c-7ad0-46ea-9643-1528a9ea1503
title: À propos des bibliothèques Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a62e6a6a23315e915bd4a5a7fe6e2dcb54a9a2ebfbd66bf5d4ba7a2519a04576
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815908"
---
# <a name="about-dynamic-link-libraries"></a>À propos des bibliothèques Dynamic-Link

La liaison dynamique permet à un module d’inclure uniquement les informations nécessaires pour localiser une fonction DLL exportée au moment du chargement ou de l’exécution. La liaison dynamique diffère de la liaison statique plus familière, dans laquelle l’éditeur de liens copie le code d’une fonction de bibliothèque dans chaque module qui l’appelle.

## <a name="types-of-dynamic-linking"></a>Types de liaison dynamique

Il existe deux méthodes pour appeler une fonction dans une DLL :

-   Dans la *liaison dynamique au moment du chargement*, un module effectue des appels explicites aux fonctions dll exportées comme s’il s’agissait de fonctions locales. Pour ce faire, vous devez lier le module à la bibliothèque d’importation pour la DLL qui contient les fonctions. Une bibliothèque d’importation fournit le système avec les informations nécessaires pour charger la DLL et rechercher les fonctions DLL exportées lorsque l’application est chargée.
-   Dans la *liaison dynamique au moment* de l’exécution, un module utilise la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) pour charger la dll au moment de l’exécution. Une fois la DLL chargée, le module appelle la fonction [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour récupérer les adresses des fonctions dll exportées. Le module appelle les fonctions DLL exportées à l’aide des pointeurs de fonction retournés par **GetProcAddress**. Cela élimine la nécessité d’une bibliothèque d’importation.

## <a name="dlls-and-memory-management"></a>Gestion des dll et de la mémoire

Chaque processus qui charge la DLL le mappe dans son espace d’adressage virtuel. Une fois que le processus a chargé la DLL dans son adresse virtuelle, elle peut appeler les fonctions DLL exportées.

Le système gère un nombre de références par processus pour chaque DLL. Quand un thread charge la DLL, le nombre de références est incrémenté d’une unité. Lorsque le processus se termine, ou lorsque le nombre de références devient zéro (liaison dynamique au moment de l’exécution uniquement), la DLL est déchargée de l’espace d’adressage virtuel du processus.

À l’instar de toute autre fonction, une fonction DLL exportée s’exécute dans le contexte du thread qui l’appelle. Par conséquent, les conditions suivantes s’appliquent :

-   Les threads du processus qui a appelé la DLL peuvent utiliser des handles ouverts par une fonction DLL. De même, les handles ouverts par n’importe quel thread du processus appelant peuvent être utilisés dans la fonction DLL.
-   La DLL utilise la pile du thread appelant et l’espace d’adressage virtuel du processus appelant.
-   La DLL alloue de la mémoire à partir de l’espace d’adressage virtuel du processus appelant.

Pour plus d’informations sur les dll, consultez les rubriques suivantes :

-   [Avantages de la liaison dynamique](advantages-of-dynamic-linking.md)
-   [Création de bibliothèque de liens dynamiques](dynamic-link-library-creation.md)
-   [Fonction de Entry-Point de bibliothèque de liens dynamiques](dynamic-link-library-entry-point-function.md)
-   [Liaison dynamique au moment du chargement](load-time-dynamic-linking.md)
-   [Liaison dynamique au moment de l’exécution](run-time-dynamic-linking.md)
-   [Ordre de recherche de la bibliothèque de liens dynamiques](dynamic-link-library-search-order.md)
-   [Données de bibliothèque de liens dynamiques](dynamic-link-library-data.md)
-   [Redirection de bibliothèque de liens dynamiques](dynamic-link-library-redirection.md)
-   [Mises à jour de la bibliothèque de liens dynamiques](dynamic-link-library-updates.md)
-   [Sécurité de la bibliothèque de liens dynamiques](dynamic-link-library-security.md)
-   [DLL AppInit et démarrage sécurisé](secure-boot-and-appinit-dlls.md)

 

 
