---
description: Les deux descripteurs (ou plus) qui font référence à un socket partagé peuvent être utilisés indépendamment en ce qui concerne les e/s.
ms.assetid: 25252552-4b62-441a-b564-e7f4a77cf68a
title: Directives de précédence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c2086b2d640e2968c56082c2d8dfff99546fc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113022"
---
# <a name="precedence-guidelines"></a>Directives de précédence

Les deux descripteurs (ou plus) qui font référence à un socket partagé peuvent être utilisés indépendamment en ce qui concerne les e/s. Toutefois, l’interface Windows Sockets n’implémente aucun type de contrôle d’accès, c’est pourquoi il revient aux processus impliqués à coordonner leurs opérations sur un socket partagé. Une utilisation courante pour les sockets partagés consiste à avoir un processus qui est responsable de la création de sockets et de l’établissement de connexions entre les sockets et les autres processus qui sont responsables de l’échange d’informations.

La règle générale pour la prise en charge de plusieurs opérations en attente sur des sockets partagés est qu’un fournisseur de services est encouragé à respecter toutes les opérations simultanées sur les sockets partagés, en particulier l’opération la plus récente sur un objet Socket. Si nécessaire, cela peut se produire au détriment d’une partie des opérations précédentes, mais toujours en attente, qui retourneront WSAEINTR dans ce cas.

 

 



