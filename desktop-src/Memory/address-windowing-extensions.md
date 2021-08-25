---
description: AWE (Address Windowing Extensions) est un ensemble d’extensions qui permet à une application de manipuler rapidement la mémoire physique supérieure à 4 Go.
ms.assetid: 48a29922-8130-4540-86b0-0faa120566a6
title: Address Windowing Extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5f0c68e9609834a9065a919d12c23c40521e99ede94feb96889050b6873654
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764409"
---
# <a name="address-windowing-extensions"></a>Address Windowing Extensions

AWE (Address Windowing Extensions) est un ensemble d’extensions qui permet à une application de manipuler rapidement la mémoire physique supérieure à 4 Go. Certaines applications gourmandes en données, telles que les systèmes de gestion de base de données et les logiciels scientifiques et d’ingénierie, ont besoin d’accéder à des caches de données très volumineux. Dans le cas de jeux de données très volumineux, la restriction du cache pour qu’il s’adapte aux 2 Go d’espace d’adressage utilisateur d’une application est une restriction grave. Dans ce cas, le cache est trop petit pour prendre en charge correctement l’application.

AWE résout ce problème en permettant aux applications de traiter directement de grandes quantités de mémoire tout en continuant à utiliser des pointeurs 32 bits. AWE permet aux applications d’avoir des caches de données supérieurs à 4 Go (lorsque la mémoire physique est suffisante). AWE utilise la mémoire physique non paginée et les vues de fenêtre de différentes parties de cette mémoire physique dans un espace d’adressage virtuel 32 bits.

AWE impose quelques restrictions sur la façon dont cette mémoire peut être utilisée, principalement parce que ces restrictions autorisent un mappage, un remappage et une libération extrêmement rapides. La gestion de mémoire rapide est importante pour ces espaces d’adressage potentiellement énormes.

-   Les plages d’adresses virtuelles allouées pour AWE ne sont pas partageables avec d’autres processus (et ne peuvent donc pas être héritées). En fait, deux adresses virtuelles AWE différentes au sein du même processus ne sont pas autorisées à mapper la même page physique. Ces restrictions fournissent un remappage et un nettoyage rapides lorsque la mémoire est libérée.
-   Les pages physiques qui peuvent être allouées pour une région AWE sont limitées par le nombre de pages physiques présentes dans l’ordinateur, car cette mémoire n’est jamais paginée – elle est verrouillée jusqu’à ce que l’application la libère ou la ferme explicitement. Les pages physiques allouées pour un processus donné peuvent être mappées à n’importe quelle région virtuelle AWE au sein du même processus. Les applications qui utilisent AWE doivent veiller à ne pas prendre trop de mémoire physique, car elles provoquent la pagination excessive d’autres applications ou empêchent la création de nouveaux processus ou threads en raison d’un manque de ressources. Utilisez la fonction [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) pour surveiller l’utilisation de la mémoire physique.
-   Les adresses virtuelles AWE sont toujours en lecture/écriture et ne peuvent pas être protégées par le biais d’appels à [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) (autrement dit, aucune mémoire en lecture seule, mémoire NoAccess, pages de garde et like ne peut être spécifiée).
-   Les plages d’adresses AWE ne peuvent pas être utilisées pour mettre en mémoire tampon des données pour des appels graphiques ou vidéo.
-   Une plage de mémoire AWE ne peut pas être fractionnée et elle ne peut pas être supprimée. Au lieu de cela, vous devez supprimer l’intégralité de la plage d’adresses virtuelles en tant qu’unité lorsque la suppression est requise. Cela signifie que vous devez spécifier la **\_ libération** de la mémoire lors de l’appel de [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree).
-   Les applications peuvent mapper plusieurs régions simultanément, à condition qu’elles ne se chevauchent pas.
-   Les applications qui utilisent AWE ne sont pas prises en charge en mode émulation. Autrement dit, une application x86 qui utilise des fonctions AWE doit être recompilée pour s’exécuter sur un autre processeur, alors que la plupart des applications peuvent s’exécuter sans recompilation sous un émulateur sur d’autres plateformes.

Cette solution résout les problèmes de mémoire physique de manière très générale et applicable. Voici quelques-uns des avantages des extensions AWE :

-   Un petit groupe de nouvelles fonctions est défini pour manipuler la mémoire AWE.
-   AWE offre une fonctionnalité de remappage très rapide. Le remappage est effectué en manipulant les tables de mémoire virtuelle, et non en déplaçant les données dans la mémoire physique.
-   AWE offre une granularité de taille de page adaptée au processeur (par exemple, 4 Ko sur x86), ce qui est plus utile pour les applications que les grandes pages (par exemple, 2 Mo ou 4 Mo sur x86).

Une application doit disposer du privilège verrouiller les pages en mémoire pour utiliser AWE. Pour obtenir ce privilège, un administrateur doit ajouter **des pages de verrouillage en mémoire** aux **attributions des droits utilisateur** de l’utilisateur. Pour plus d’informations sur la façon de procéder, consultez la rubrique « droits d’utilisateur » dans l’aide du système d’exploitation.

Les fonctions suivantes composent l’API AWE (Address Windowing Extensions).



| Fonction                                                                          | Description                                                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) et [ **VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Réserver une partie de l’espace d’adressage virtuel à utiliser pour AWE, en utilisant le **MEM \_ physique**.                                                                                                                                                                       |
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages)                    | Allouez de la mémoire physique pour une utilisation avec AWE.                                                                                                                                                                                                                |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages)                              | Mapper (ou invalider) des adresses virtuelles AWE sur un ensemble de pages physiques obtenues avec [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages).                                                                                                    |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter)                | Mapper (ou invalider) des adresses virtuelles AWE sur tout ensemble de pages physiques obtenues avec [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages), mais avec un contrôle plus précis que celui fourni par [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages). |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages)                            | Mémoire physique libre utilisée pour AWE.                                                                                                                                                                                                               |



 

 

 
