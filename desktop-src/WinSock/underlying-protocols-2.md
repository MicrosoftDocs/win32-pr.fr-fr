---
description: Certains protocoles dont votre application dépend pour certains services, tels que l’appel de procédure distante (RPC), peuvent avoir des fonctions et des structures dépendantes de la version IP qui nécessitent que vous modifiiez votre application en termes d’utilisation.
ms.assetid: b1eac461-10c9-4077-b531-28b7c65a2e31
title: Protocoles sous-jacents pour les applications Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88789a5f4cd557111c6e1aee8c51ba00eed25e82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127296626"
---
# <a name="underlying-protocols-for-ipv6-winsock-applications"></a>Protocoles sous-jacents pour les applications Winsock IPv6

Certains protocoles dont votre application dépend pour certains services, tels que l’appel de procédure distante (RPC), peuvent avoir des fonctions et des structures dépendantes de la version IP qui nécessitent que vous modifiiez votre application en termes d’utilisation.

Une partie du processus de modification de votre code pour prendre en charge IPv6 doit inclure la détermination de l’utilisation des protocoles sous-jacents (du point de vue de la pile, ces protocoles sont considérés comme des protocoles de couche supérieure) nécessitent une modification pour pouvoir utiliser correctement IPv6.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide IPv6 pour les Applications Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modification des structures de données pour IPv6 Winsock appications](changing-data-structures-2.md)
</dt> <dt>

[Sockets à double pile pour les applications Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Appels de fonction pour les applications Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Utilisation d’adresses IPv4 codées en dur](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problèmes d’interface utilisateur pour les applications Winsock IPv6](user-interface-issues-2.md)
</dt> </dl>

 

 



