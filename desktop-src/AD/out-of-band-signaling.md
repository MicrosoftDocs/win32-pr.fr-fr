---
title: Signalisation hors bande
description: Les applications qui coopèrent qui partagent des données communes à l’aide de l’annuaire peuvent utiliser la signalisation hors bande pour éviter la distorsion de version et les mises à jour partielles.
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028599"
---
# <a name="out-of-band-signaling"></a>Signalisation hors bande

Les applications qui coopèrent qui partagent des données communes à l’aide de l’annuaire peuvent utiliser la signalisation hors bande pour éviter la distorsion de version et les mises à jour partielles. En bref, les applications qui coopèrent utilisent un mécanisme distinct de la réplication d’annuaire pour s’informer mutuellement des modifications apportées aux données communes partagées. La signalisation hors bande est plus efficace lorsqu’elle est utilisée en association avec un mécanisme de contrôle de version, ce qui permet au partenaire de détecter la modification pour informer les partenaires distants de la version des données partagées à attendre.

En revenant à l’exemple RPC fourni dans la section « décalage de version » du [comportement de réplication dans Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md), le serveur RPC peut rappeler aux clients connectés pour les informer de la migration vers un nouveau serveur : «je vais le déplacer. Veillez à ce que la réplication vous apporte bientôt la nouvelle adresse. le client peut ainsi gérer la période de transition.

Les applications qui requièrent des stratégies identiques pour être en mesure de communiquer entre elles peuvent utiliser la signalisation hors bande pour s’assurer qu’une nouvelle stratégie n’est pas utilisée tant que toutes les parties concernées ne l’ont pas reçue. Par exemple, si la stratégie de sécurité du protocole Internet (IPsec) entre deux ordinateurs est modifiée, un agent sur la machine source peut contacter un agent sur l’ordinateur de destination pour négocier l’application de la stratégie modifiée, avec la machine source qui retarde l’application jusqu’à ce que l’ordinateur de destination ait reçu également la nouvelle stratégie.

 

 




