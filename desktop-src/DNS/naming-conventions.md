---
title: Conventions d'affectation de noms
description: Les conventions d’affectation de noms partagent un objectif commun pour résoudre sans ambiguïté un nom en une adresse réseau, généralement une adresse IP. La différence entre les conventions d’attribution de noms se situe dans l’approche distincte de chaque convention pour la résolution de noms.
ms.assetid: 1ec96d2d-bb5a-4938-88c2-4d2802a326cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2091123ed2bf1022910231cd08cb0e6cccae51a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029495"
---
# <a name="naming-conventions"></a>Conventions d'affectation de noms

Les conventions d’affectation de noms partagent un objectif commun : pour résoudre sans ambiguïté un nom en une adresse réseau, généralement une adresse IP. La différence entre les conventions d’attribution de noms se situe dans l’approche distincte de chaque convention pour la résolution de noms.

Les conventions d’affectation de noms suivantes sont utilisées pour identifier les ordinateurs dans diverses méthodes de résolution de noms système, y compris la méthode 2000 de Windows :

-   [Nom de l’ordinateur](#computer-name)
-   [Nom d’hôte](#host-name)
-   [Nom de domaine complet (FQDN)](#fully-qualified-domain-name)
-   [Nom unique relatif](#relative-distinguished-name)

## <a name="computer-name"></a>Nom d’ordinateur

Dans l’espace de noms NetBIOS plat, un nom unique résout sans ambiguïté un nom d’ordinateur en adresse réseau. Il s’agit du nom que les versions précédentes de Windows ont stockées dans le navigateur et le navigateur principal, ce qui permet aux réseaux Windows homologues de parcourir les ressources sur les ordinateurs Windows en réseau. Dans ce scénario, le terme associé à l’ordinateur est le nom de l' *ordinateur*. L’inscription du nom de l’ordinateur dépend des diffusions réseau (et d’un explorateur principal, déterminé par les élections remportées par des numéros de version Windows ultérieures ou l’utilisation de Windows NT, ou d’une combinaison). Cela était utile pour les réseaux Windows de petite taille, mais les réseaux se sont bientôt dépassés au-delà de ce que l’utilisation des diffusions et des listes simples de navigateurs principaux de fichiers plats pouvaient être servies.

## <a name="host-name"></a>Nom d’hôte

Ensuite, le service WINS (Windows Internet Service de nommage), qui permettait un référentiel dynamique et centralisé de noms d’ordinateur NetBIOS stockés sur des serveurs WINS. Ces dépôts peuvent traiter un réseau plus grand. Avec ce développement, les requêtes de résolution de noms peuvent être dirigées vers un serveur WINS (au lieu d’être diffusées) et les conflits peuvent être arbitrés de manière centralisée. Avec WINS, le terme nom d’ordinateur a été conservé, mais le terme *nom d’hôte* est également apparu et utilisé de façon interchangeable avec le nom de l’ordinateur. À l’époque, WINS était le programme de résolution de nom par défaut pour les plates-formes Windows, mais DNS s’est retrouvé avec la popularité et la prolifération des réseaux plus grands et plus grands.

Les réseaux ont augmenté et WINS est devenu moins apte à gérer le volume croissant de noms. La possibilité de décroître de WINS pour gérer la charge de résolution de nom n’était pas due à la puissance de traitement requise pour la résolution, mais plutôt au fait que la génération de noms uniques pour un grand nombre d’ordinateurs est devenue une charge de gestion croissante.

## <a name="fully-qualified-domain-name"></a>Nom de domaine complet

DNS est une meilleure solution ; avec son espace de noms hiérarchique, le besoin de noms d’ordinateur uniques est isolé pour un domaine donné, ce qui permet à un nom d’ordinateur tel que *Server1* d’exister dans différents emplacements de domaine dans la même hiérarchie. Avec la possibilité d’avoir le même nom d’hôte dans des domaines différents, il est nécessaire d’avoir un nom qui corrigeait correctement la hiérarchie DNS. Le nom devait inclure non seulement le nom de l’ordinateur ou le nom d’hôte, mais également un nom qui pourrait identifier sans ambiguïté, ou qualifier entièrement cet ordinateur dans l’ensemble de la hiérarchie DNS. Ce nom est le [*nom de domaine*](f-gly.md) complet (FQDN), par exemple, server1.widgets.Microsoft.com.

Toutefois, dans certaines situations, la partie de la hiérarchie de domaine du nom de domaine complet est lourde et un nom local pour un ordinateur donné (ou tout autre hôte DNS) relatif au domaine DNS dans lequel réside l’hôte est nécessaire. Ce nom est le [*nom unique relatif*](r-gly.md). Le nom unique relatif est simplement le nom d’hôte unique à gauche du point le plus à gauche dans le nom de domaine complet, de telle sorte qu’un nom de domaine complet de server1.widgets.microsoft.com a Serveur1 comme nom unique relatif.

## <a name="relative-distinguished-name"></a>Nom unique relatif

Plutôt que d’imposer de nouveaux noms ou de nouvelles conventions d’affectation de noms aux utilisateurs de noms NetBIOS, DNS utilise simplement le nom d’ordinateur (nom d’hôte) comme nom unique relatif et ajoute la hiérarchie de domaine DNS à ce nom pour créer le nom de domaine complet. L’illustration suivante montre comment identifier la partie nom d’ordinateur (ou nom d’hôte, ou nom unique relatif) du nom de domaine complet :

![combinaison de la hiérarchie de domaines RDN et DNS pour créer un nom de domaine complet](images/fqdn.png)

 

 




