---
title: avantages des Stockage structurées
description: COM fournit un ensemble de services, collectivement appelé stockage structuré.
ms.assetid: d05d2dbc-d1d2-4ef8-a773-5337e2746da3
keywords:
- structured Stockage Strctd Stg, avantages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a52159f37b3bf443419beaadbcf9f76aa9c5d7209e04b25506eea850c4d3d98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663561"
---
# <a name="benefits-of-structured-storage"></a>avantages des Stockage structurées

COM fournit un ensemble de services, collectivement appelé stockage structuré. Parmi les avantages de ces services, citons la réduction des pénalités de performances et de la surcharge associée au stockage d’objets distincts dans un fichier plat. Au lieu d’un fichier plat, COM stocke les objets séparés dans un seul fichier structuré composé de deux éléments principaux : les objets de stockage et les objets de flux. Ensemble, ils fonctionnent comme un système de fichiers dans un fichier.

Le stockage structuré résout les problèmes de performances en éliminant la nécessité de réécrire entièrement un fichier dans le stockage chaque fois qu’un nouvel objet est ajouté à un fichier composé, ou lorsque la taille d’un objet existant augmente. Les nouvelles données sont écrites à l’emplacement suivant disponible dans le stockage permanent, et l’objet de stockage met à jour la table des pointeurs qu’elle gère pour suivre les emplacements de ses objets de stockage et de flux. En même temps, le stockage structuré permet aux utilisateurs finaux d’interagir et de gérer un fichier composé comme s’il s’agissait d’un fichier unique plutôt que d’une hiérarchie imbriquée d’objets distincts.

Le stockage structuré présente également d’autres avantages :

-   **Accès incrémentiel**. Si un utilisateur a besoin d’accéder à un objet dans un fichier composé, il peut charger et enregistrer uniquement cet objet, plutôt que le fichier entier.
-   **Utilisation multiple**. Plusieurs utilisateurs finaux ou applications peuvent lire et écrire simultanément des informations dans le même fichier composé.
-   **Traitement des transactions**. Les utilisateurs peuvent lire ou écrire dans les fichiers composés COM en mode transactionnel, où les modifications apportées au fichier sont mises en mémoire tampon et peuvent ensuite être validées dans le fichier ou inversées.
-   **Enregistrements de mémoire insuffisante**. Le stockage structuré fournit des fonctionnalités permettant d’enregistrer des fichiers dans des situations de mémoire insuffisante.

 

 




