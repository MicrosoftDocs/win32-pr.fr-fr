---
title: Implémentation d’un système distribué
description: L’une des méthodes permettant d’implémenter des logiciels dans un système distribué consiste à utiliser la prise en charge des réseaux bruts.
ms.assetid: 46abbbec-caa1-4fee-a713-4a4a2b462051
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098263f916129115f41840e15ac689fab7e4544621989d1a4d3179e50ef17d27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020528"
---
# <a name="implementing-a-distributed-system"></a>Implémentation d’un système distribué

L’une des méthodes permettant d’implémenter des logiciels dans un système distribué consiste à utiliser la prise en charge des réseaux bruts. Cette approche comprend des sockets, des canaux nommés ou des publications HTTP, des, etc. Tous ces modèles forcent le développeur à utiliser des primitives de programmation de bas niveau, d’une manière ou d’une autre, ce qui force le développeur à gérer la représentation de données réseau (NDR), les données de Packaging, la gestion du trafic réseau et les conditions d’échec, la protection et le chiffrement de l’intégrité des données, etc.

RPC offre un modèle de programmation dans lequel le développeur conserve un contrôle granulaire de l’interaction réseau entre le client et le serveur par le biais d’une API riche, tout en évitant aux développeurs les informations et les charges qu’un système distribué a tendance à introduire.

Par exemple, considérez la charge associée à différentes approches de protection de l’intégrité et de la confidentialité des échanges de messages dans un système distribué. Lorsque vous envisagez la sécurité réseau pour les échanges de paquets, certaines protections sont plus faibles, mais plus fortes. Il n’existe pas de véritable sécurité réseau, mais uniquement les différents mécanismes de sécurité basés sur les paquets ; sécurité identifiant l’appelant (qui a tendance à être faible, car le contenu des paquets peut souvent être modifié en transit), sécurité protégeant l’intégrité du paquet sans protéger la confidentialité (plusieurs signatures et hachages) et sécurité protégeant la confidentialité de l’échange de messages (divers mécanismes de chiffrement).

Une autre charge liée à l’implémentation d’un système distribué sécurisé est l’algorithme nécessaire pour implémenter des primitives de sécurité telles que le chiffrement, la signature, l’authentification, etc. Un développeur peut implémenter ces algorithmes, mais cela est difficile, sujet aux erreurs et même risqué, car les algorithmes résultants présentent souvent des failles de sécurité subtiles. Un développeur peut également utiliser un fournisseur de sécurité disponible pour implémenter la protection des interactions réseau au sein d’un système distribué.

À l’aide de RPC, ces deux charges sont très faciles à résoudre. Un développeur doit simplement indiquer à RPC le package de sécurité à utiliser, ainsi que la protection de sécurité à appliquer à l’échange de messages (en termes d’authentification, de chiffrement, d’authentification mutuelle, de suivi de l’identité de l’appelant, etc.). RPC s’occupe de tous les détails en coulisses de manière efficace, tout en offrant au développeur un contrôle total sur la façon dont les données sont protégées.

 

 




