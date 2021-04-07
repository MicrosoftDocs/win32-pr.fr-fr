---
title: Ne pas faire confiance à votre homologue
description: '\ 0034 ; ne faites pas confiance à votre homologue \ 0034 ; est une règle de sécurité de base, mais elle est souvent négligée.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4c5c7ba3760e14a66fb4765000c7a6698599b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672842"
---
# <a name="do-not-trust-your-peer"></a>Ne pas faire confiance à votre homologue

« Ne pas approuver votre homologue » est une règle de sécurité de base, mais elle est souvent négligée. Ne partez pas du principe que l’autre partie d’une communication se comporte correctement et ne supposez pas que votre homologue transmettra les données attendues. MIDL et RPC effectuent des vérifications en votre nom, mais pas toutes les vérifications.

Savoir quel aspect des paramètres sont vérifiés par MIDL ou RPC, et quels aspects vous devez vérifier vous-même. Par exemple, pour les handles de contexte in/out, RPC vérifie que le handle de contexte n’est pas une valeur non null valide. Elle autorise les valeurs NULL et les valeurs valides, mais de nombreux développeurs ne savent pas que les valeurs NULL sont autorisées. Il s’agit d’un point à vérifier.

Même si vous faites généralement confiance à votre homologue, veillez à ne pas introduire de nouveaux chemins d’accès par lesquels un ordinateur compromis ou un compte principal peut attaquer d’autres ordinateurs. Imaginez qu’un utilisateur choisit son mot de passe anniversaire et qu’il est deviné par un pirate. Même après l’authentification des demandes de l’utilisateur et l’accès à ses données est autorisé, assurez-vous qu’il n’existe pas de vulnérabilités exploitables, telles que des dépassements de pile qui peuvent permettre à une personne malveillante de prendre le contrôle de votre serveur et d’étendre la violation de la sécurité.

 

 




