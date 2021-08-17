---
description: Cette annexe illustre une version réécrite des exemples d’applications Simplec. c et simple. c qui gère correctement le code du serveur CodeIPv6-Enabled du client IPv4 ou IPv6.
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 'Annexe B : code source agnostique de la version IP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37daf34b4a7d46a2fb8fc3cbaf5aed6cf7e054a3fb0147de8d86a643a9e4f59f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741606"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a>Annexe B : code source agnostique de la version IP

Cette annexe illustre une version réécrite des exemples d’applications Simplec. c et simple. c qui gère en douceur IPv4 ou IPv6.

-   [Code client compatible IPv6](ipv6-enabled-client-code-2.md)
-   [Code serveur compatible IPv6](ipv6-enabled-server-code-2.md)

Ce code illustre les instructions énoncées dans ce guide IPv6 et est inclus pour fournir le code source qui a été correctement modifié pour ajouter la prise en charge d’IPv6. Cet exemple est volontairement simple, mais il fournit un exemple pratique pour l’utilisation et la révision de. Une version IPv4 uniquement de ce code source est fournie dans [annexe A : code source IPv4 uniquement](appendix-a-ipv4-only-source-code-2.md).

en comparant le code source de l’annexe A (IPv4 uniquement) et de l’annexe B (IP-version agnostique), vous avez une idée des modifications nécessaires à la modification de votre application Windows sockets afin d’ajouter la prise en charge d’IPv6.

 

 



