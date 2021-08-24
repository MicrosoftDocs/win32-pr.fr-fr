---
description: résolution de noms et modèle d’inscription pour l’indexeur de Windows sockets (Winsock).
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Modèle de résolution de noms pour le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f012a5c14a6dae9045b303ecb7c4e39f1d93d264285138d98c0e93274ef921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132112"
---
# <a name="name-resolution-model-for-the-spi"></a>Modèle de résolution de noms pour le SPI

Lors du développement d’une application client/serveur indépendante du protocole, deux exigences de base existent en ce qui concerne la résolution de noms et l’inscription :

-   La capacité du serveur à la moitié de l’application (ci-après le terme de service) d’inscrire son existence dans (ou de devenir accessible à) un ou plusieurs espaces de noms.
-   Capacité de l’application cliente à rechercher le service dans un espace de noms et à obtenir le protocole de transport et les informations d’adressage requis.

Pour ceux habitués au développement d’applications basées sur TCP/IP, cela peut impliquer un peu plus que la recherche d’une adresse d’hôte, puis l’utilisation d’un numéro de port convenu. Toutefois, d’autres schémas de mise en réseau autorisent l’emplacement du service, le protocole utilisé pour le service et d’autres attributs à découvrir au moment de l’exécution. pour prendre en charge l’ensemble des fonctionnalités disponibles dans les services de noms existants, l’interface Windows sockets 2 adopte le modèle décrit ci-dessous.

Un *espace de noms* fait référence à une capacité à associer (au minimum) les attributs de protocole et d’adressage d’un service réseau avec un ou plusieurs noms conviviaux. De nombreux espaces de noms sont actuellement utilisés en grande partie, y compris le système DNS (Domain Name System), le Services d’annuaire NetWare (NDS) (NDS), le système de noms de domaine (NDS) d’Internet, etc. Ces espaces de noms varient considérablement dans la façon dont ils sont organisés et implémentés. certaines de leurs propriétés sont particulièrement importantes pour comprendre le point de vue de la résolution de noms de Windows sockets.

 

 



