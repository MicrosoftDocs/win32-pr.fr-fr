---
description: Décrit le modèle d’authentification LSA.
ms.assetid: 0b2b868f-51a7-4f74-be4f-5f8db04d43ad
title: Modèle d’authentification LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3762595332252c22141aebdc7f3ecbe168e49a83795830a0cb03e49eb5da73ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140942"
---
# <a name="lsa-authentication-model"></a>Modèle d’authentification LSA

Le modèle d’authentification de l' [*autorité de sécurité locale*](../secgloss/l-gly.md) (LSA) présente les fonctionnalités suivantes :

-   L’authentification LSA prend en charge les [packages d’authentification](authentication-packages.md)personnalisés. Cela permet aux clients finaux et aux éditeurs de logiciels indépendants (ISV) de personnaliser ou de remplacer les routines d’authentification pour répondre aux exigences qui dépassent celles fournies par les packages d’authentification Microsoft standard. Bien que les packages d’authentification fournis par Microsoft requièrent un nom d’utilisateur et des données de connexion par mot de passe, un package d’authentification personnalisé peut prendre d’autres formes de données d’ouverture de session, telles que les informations de carte ATM et un numéro d’identification personnel (PIN). Un package d’authentification personnalisé peut également être utilisé pour implémenter un nouveau [*protocole de sécurité*](../secgloss/s-gly.md).
-   Le LSA prend en charge les packages de sécurité personnalisés, qui fonctionnent comme des fournisseurs de support de sécurité pour les applications distribuées et comme des packages d’authentification pour les applications qui requièrent des services d’authentification. La fonctionnalité d’authentification est accessible à l’aide de la même interface que celle d’un package d’authentification autonome, tandis que la fonctionnalité du fournisseur de support de sécurité est accessible à l’aide de SSPI ( [Security Support Provider Interface](sspi.md) ). L’ensemble des fonctions de prise en charge LSA disponibles pour les packages de sécurité personnalisés leur permet de fournir des fonctionnalités de sécurité avancées, telles que la création de jetons et la gestion des [*informations d’identification supplémentaires*](../secgloss/s-gly.md) .
-   L’autorité LSA prend en charge la gestion des informations d’identification hétérogènes pour interagir avec des produits non-Microsoft, tels que les réseaux et les bases de données. étant donné que ces produits ont souvent leurs propres informations d’identification de sécurité, le LSA fournit des fonctions que les packages d’authentification peuvent utiliser pour associer des informations d’identification non Microsoft à des processus de Windows. Les packages d’authentification personnalisés peuvent fournir des services pour interroger ces informations d’identification si nécessaire, par exemple lorsqu’un redirecteur réseau tente d’établir une connexion à un système distant.
-   Chaque classe d’appareil de connexion installée sur un système peut avoir son propre processus d’ouverture de session. Les classes d’appareils incluent généralement des appareils tels que les lecteurs de carte à puce. Toutefois, dans le cadre de l’authentification [*LSA*](../secgloss/l-gly.md) , les réseaux connectés sont également traités comme des appareils. par défaut, le système d’exploitation Windows fournit le processus d’ouverture de session qui prend en charge les ouvertures de session par nom d’utilisateur et mot de passe à l’aide d’un clavier. Les développeurs peuvent ajouter la prise en charge d’autres appareils, tels que les [*lecteurs*](../secgloss/r-gly.md)de [*carte à puce*](../secgloss/s-gly.md) . Pour plus d’informations sur les cartes à puce, consultez [authentification par carte à puce](smart-card-authentication.md). Pour plus d’informations sur la prise en charge des périphériques d’ouverture de session, consultez [Winlogon et Gina](winlogon-and-gina.md).

 

 
