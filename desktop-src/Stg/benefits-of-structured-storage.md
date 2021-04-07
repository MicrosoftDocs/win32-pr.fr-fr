---
title: Avantages du stockage structuré
description: COM fournit un ensemble de services, collectivement appelé stockage structuré.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- Stockage structuré Strctd STG, avantages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68b954fda33e18f654ccc0360f58ddb14e5d110
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671673"
---
# <a name="benefits-of-structured-storage"></a>Avantages du stockage structuré

COM fournit un ensemble de services, collectivement appelé stockage structuré. Parmi les avantages de ces services, citons la réduction des pénalités de performances et de la surcharge associée au stockage d’objets distincts dans un fichier plat. Au lieu d’un fichier plat, COM stocke les objets séparés dans un seul fichier structuré composé de deux éléments principaux : les objets de stockage et les objets de flux. Ensemble, ils fonctionnent comme un système de fichiers dans un fichier.

Le stockage structuré résout les problèmes de performances en éliminant la nécessité de réécrire entièrement un fichier dans le stockage chaque fois qu’un nouvel objet est ajouté à un fichier composé, ou lorsque la taille d’un objet existant augmente. Les nouvelles données sont écrites à l’emplacement suivant disponible dans le stockage permanent, et l’objet de stockage met à jour la table des pointeurs qu’elle gère pour suivre les emplacements de ses objets de stockage et de flux. En même temps, le stockage structuré permet aux utilisateurs finaux d’interagir et de gérer un fichier composé comme s’il s’agissait d’un fichier unique plutôt que d’une hiérarchie imbriquée d’objets distincts.

Le stockage structuré présente également d’autres avantages :

-   **Accès incrémentiel**. Si un utilisateur a besoin d’accéder à un objet dans un fichier composé, il peut charger et enregistrer uniquement cet objet, plutôt que le fichier entier.
-   **Utilisation multiple**. Plusieurs utilisateurs finaux ou applications peuvent lire et écrire simultanément des informations dans le même fichier composé.
-   **Traitement des transactions**. Les utilisateurs peuvent lire ou écrire dans les fichiers composés COM en mode transactionnel, où les modifications apportées au fichier sont mises en mémoire tampon et peuvent ensuite être validées dans le fichier ou inversées.
-   **Enregistrements de mémoire insuffisante**. Le stockage structuré fournit des fonctionnalités permettant d’enregistrer des fichiers dans des situations de mémoire insuffisante.

 

 




