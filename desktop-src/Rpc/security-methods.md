---
title: Méthodes de sécurité
description: Microsoft RPC prend en charge deux méthodes différentes pour l’ajout de la sécurité à votre application distribuée.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac09f29c4912228207e5c09d4551f408a76788d3d3ecf999aae2fcc1c63ded6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018037"
---
# <a name="security-methods"></a>Méthodes de sécurité

Microsoft RPC prend en charge deux méthodes différentes pour l’ajout de la sécurité à votre application distribuée. La première méthode consiste à utiliser l’interface SSPI (Security Support Provider Interface), accessible à l’aide des fonctions RPC. En général, il est préférable d’utiliser cette méthode. L’interface SSPI fournit les fonctionnalités d’authentification les plus flexibles et indépendantes du réseau.

La deuxième méthode consiste à utiliser les fonctionnalités de sécurité intégrées aux protocoles de transport système. La méthode de sécurité au niveau du transport n’est pas la méthode recommandée. L’utilisation de l’interface SSPI est recommandée car elle fonctionne sur tous les transports, sur plusieurs plateformes, et fournit des niveaux élevés de sécurité, notamment la confidentialité.

Cette section fournit des vues d’ensemble de la sécurité SSPI et de la sécurité au niveau du transport dans les rubriques suivantes :

-   [interface du fournisseur de la prise en charge de la sécurité (Security Support Provider Interface ou SSPI)](security-support-provider-interface-sspi-.md)
-   [Sécurité de transport](transport-security.md)

 

 




