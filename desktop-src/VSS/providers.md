---
description: Les fournisseurs gèrent les volumes en cours d’exécution et créent des clichés instantanés à la demande.
ms.assetid: 4e6b46b0-df9e-4458-b0ac-e237d7656337
title: Fournisseurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9e098981c6246392fef75f717b1d7676df1aa134e4faef3e436ee8b3eb537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591326"
---
# <a name="providers"></a>Fournisseurs

Les [*fournisseurs*](vssgloss-p.md) gèrent les volumes en cours d’exécution et créent des clichés instantanés à la demande.

En réponse à une demande d’un demandeur, un fournisseur génère des événements COM pour signaler les applications d’un cliché instantané à venir, puis crée et gère cette copie jusqu’à ce qu’elle ne soit plus nécessaire.

Lorsqu’un cliché instantané est en cours d’existence, le fournisseur crée un environnement où il existe effectivement deux copies indépendantes de tout volume qui a fait l’objet de clichés instantanés : un disque en cours d’exécution utilisé et mis à jour normalement, l’autre copie qui est fixe et stable pour la sauvegarde.

bien qu’un fournisseur par défaut soit fourni dans le cadre de Windows, d’autres fournisseurs sont libres de fournir leurs propres implémentations optimisées pour leur propre matériel de stockage et leurs propres offres logicielles.

Du point de vue d’un développeur d’applications de sauvegarde/restauration ou de l’utilisateur final, tous les fournisseurs disposent de la même interface (consultez [sélection des fournisseurs](selecting-providers.md)).

Tous les fournisseurs doivent être en mesure d’effectuer les opérations suivantes :

-   Interceptez les demandes d’e/s entre le système de fichiers et le système de stockage de masse sous-jacent.
-   Capturez et récupérez l’état d’un volume au moment du cliché instantané, en conservant une vue « limite dans le temps » des fichiers sur le disque sans que les opérations d’e/s partielles soient reflétées dans leur état.
-   Utilisez cette vue « ponctuelle » pour exposer (au minimum les applications compatibles VSS) un volume virtuel contenant les données des clichés instantanés.

Selon la procédure à suivre, un fournisseur peut être de l’un des trois types suivants :

-   [Fournisseur système](#system-provider)
-   [Fournisseurs de logiciels](#software-providers)
-   [Fournisseurs de matériel](#hardware-providers)

## <a name="system-provider"></a>Fournisseur système

un fournisseur de clichés instantanés, le [*fournisseur système*](vssgloss-s.md), est fourni par défaut dans une installation de système d’exploitation Windows. Actuellement, le fournisseur système est une instance particulière d’un fournisseur de logiciels. Toutefois, cela peut changer à l’avenir.

Pour conserver une vue « limite dans le temps » d’un volume contenu dans le cliché instantané, le fournisseur système utilise une technique de copie sur écriture. Les copies des secteurs sur le disque qui ont été modifiés (appelées « différences ») depuis le début de la création de clichés instantanés sont stockées dans une zone de stockage de clichés instantanés.

Par conséquent, le fournisseur système peut exposer le volume actif, qui peut être écrit et lu normalement, et appliquer les « différences » aux données du volume actif pour exposer efficacement les données figées du cliché instantané.

Pour le fournisseur système, la zone de stockage de cliché instantané doit se trouver sur un volume NTFS. Le volume qui fait l’objet du cliché instantané n’a pas besoin d’être un volume NTFS, mais au moins un volume monté sur le système doit en être un.

## <a name="software-providers"></a>Fournisseurs de logiciels

Les fournisseurs de clichés instantanés logiciels interceptent et traitent les demandes d’e/s dans une couche logicielle entre le système de fichiers et le logiciel du gestionnaire de volume. Ces fournisseurs sont implémentés en tant que composant DLL en mode utilisateur et au moins un pilote de périphérique en mode noyau, généralement (mais pas nécessairement) un pilote de filtre de stockage. Le travail de création de ces clichés instantanés s’effectue dans le logiciel.

Un fournisseur de clichés instantanés logiciel doit conserver une vue « ponctuelle » d’un volume en ayant accès à un ensemble de fichiers qui peuvent être utilisés pour recréer avec précision l’état du volume avant le cliché instantané. Par exemple, il s’agit de la technique de copie sur écriture du fournisseur système.

Toutefois, VSS n’impose aucune restriction quant à la technique utilisée par les fournisseurs de logiciels pour créer et gérer des clichés instantanés, et les fournisseurs tiers sont libres de mettre en œuvre leurs fournisseurs de logiciels tels qu’ils s’affichent.

En outre, VSS prend en charge la plupart des fonctionnalités des fournisseurs de clichés instantanés logiciels, telles que la définition du point dans le temps, la synchronisation et le vidage des données, la fourniture d’une interface commune pour les applications de sauvegarde et la gestion du cliché instantané.

Un fournisseur de logiciels, par définition, s’applique à un plus grand nombre de plates-formes de stockage qu’un fournisseur de matériel, et doit être en mesure d’utiliser les disques de base ou les volumes logiques également. Cette généralisation sacrifie les performances qui peuvent être disponibles en implémentant des clichés instantanés sur le matériel et n’utilise pas les fonctionnalités de capture de volume ou de mise en miroir de fichiers spécifiques au fournisseur.

## <a name="hardware-providers"></a>Fournisseurs de matériel

Les fournisseurs de clichés instantanés matériels interceptent les demandes d’e/s du système de fichiers au niveau du matériel en travaillant conjointement avec un adaptateur de stockage matériel ou un contrôleur. La tâche de création du cliché instantané est effectuée par un adaptateur hôte, un dispositif de stockage ou un contrôleur RAID en dehors du système d’exploitation.

Ces fournisseurs sont implémentés en tant que composant DLL en mode utilisateur communiquant avec le matériel qui expose les données de cliché instantané : par conséquent, les fournisseurs de clichés instantanés de matériel peuvent avoir besoin d’appeler ou de créer d’autres composants en mode noyau.

Les fournisseurs de matériel exposent aux clichés instantanés VSS de disques complets ou d’unités logiques (LUN). Les demandeurs gèrent toujours les clichés instantanés de volumes ; tout le mappage de volume à disque est géré en interne par VSS. Les clichés instantanés créés par les fournisseurs de matériel des volumes qui résident sur des disques dynamiques ont une exigence spécifique : ils ne peuvent pas être importés sur le même système. Ils doivent être créés et transportables et importés sur un deuxième système.

Bien qu’un fournisseur de clichés instantanés matériel utilise des fonctionnalités VSS qui définissent le point dans le temps, permet la synchronisation des données, gère le cliché instantané et fournit une interface commune avec les applications de sauvegarde, VSS ne spécifie pas le mécanisme sous-jacent par lequel le fournisseur de matériel produit et gère les clichés instantanés.

 

 



