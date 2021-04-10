---
title: Méthodes de sécurité
description: Microsoft RPC prend en charge deux méthodes différentes pour l’ajout de la sécurité à votre application distribuée.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029663"
---
# <a name="security-methods"></a>Méthodes de sécurité

Microsoft RPC prend en charge deux méthodes différentes pour l’ajout de la sécurité à votre application distribuée. La première méthode consiste à utiliser l’interface SSPI (Security Support Provider Interface), accessible à l’aide des fonctions RPC. En général, il est préférable d’utiliser cette méthode. L’interface SSPI fournit les fonctionnalités d’authentification les plus flexibles et indépendantes du réseau.

La deuxième méthode consiste à utiliser les fonctionnalités de sécurité intégrées aux protocoles de transport système. La méthode de sécurité au niveau du transport n’est pas la méthode recommandée. L’utilisation de l’interface SSPI est recommandée car elle fonctionne sur tous les transports, sur plusieurs plateformes, et fournit des niveaux élevés de sécurité, notamment la confidentialité.

Cette section fournit des vues d’ensemble de la sécurité SSPI et de la sécurité au niveau du transport dans les rubriques suivantes :

-   [interface du fournisseur de la prise en charge de la sécurité (Security Support Provider Interface ou SSPI)](security-support-provider-interface-sspi-.md)
-   [Sécurité de transport](transport-security.md)

 

 




