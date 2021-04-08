---
title: Extension de programmation
description: Les extensions de programmation ont plusieurs avantages, toutefois, une application est opaque ; l’administrateur doit faire confiance à la documentation fournie avec l’application d’installation.
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- Extension de programmation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671254"
---
# <a name="programmatic-extension"></a>Extension de programmation

L’avantage d’un fichier LDIF est que l’administrateur peut examiner sa fonction. Toutefois, le schéma peut également être étendu par programmation. Les extensions de programmation ont plusieurs avantages, mais une application est opaque ; l’administrateur doit faire confiance à la documentation fournie avec l’application d’installation. L’utilisation d’extensions de schéma de programmation peut être un obstacle au déploiement pour les applications qui les utilisent. Une extension de programmation est indifférente ; Il s’agit d’un fichier exécutable Windows NT. Le binaire ne peut pas être falsifié, contrairement à un fichier LDIF ou. csv, qui peut être modifié par inadvertance ou par malveillance.

Les avantages d’un fichier LDIF sont les suivants :

-   Les applications peuvent détecter et récupérer des erreurs et fournir des commentaires à l’utilisateur.
-   Les applications peuvent gérer Unicode sans avoir recours à l’encodage Base64.
-   Les applications peuvent tirer parti des API d’installation Windows Installer.
-   Les applications peuvent être signées pour établir l’authenticité.

 

 




