---
title: Ne pas faire confiance à votre homologue
description: '\ 0034 ; ne faites pas confiance à votre homologue \ 0034 ; est une règle de sécurité de base, mais elle est souvent négligée.'
ms.assetid: 776c1c99-feb1-415c-9a18-e9bf581bc3ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf9235e8b01b6c7b10be96b1d34ed989b27421420d15489441aea948445cfde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021759"
---
# <a name="do-not-trust-your-peer"></a>Ne pas faire confiance à votre homologue

« Ne pas approuver votre homologue » est une règle de sécurité de base, mais elle est souvent négligée. Ne partez pas du principe que l’autre partie d’une communication se comporte correctement et ne supposez pas que votre homologue transmettra les données attendues. MIDL et RPC effectuent des vérifications en votre nom, mais pas toutes les vérifications.

Savoir quel aspect des paramètres sont vérifiés par MIDL ou RPC, et quels aspects vous devez vérifier vous-même. Par exemple, pour les handles de contexte in/out, RPC vérifie que le handle de contexte n’est pas une valeur non null valide. Elle autorise les valeurs NULL et les valeurs valides, mais de nombreux développeurs ne savent pas que les valeurs NULL sont autorisées. Il s’agit d’un point à vérifier.

Même si vous faites généralement confiance à votre homologue, veillez à ne pas introduire de nouveaux chemins d’accès par lesquels un ordinateur compromis ou un compte principal peut attaquer d’autres ordinateurs. Imagine qu’un utilisateur choisisse son anniversaire comme mot de passe et qu’il est deviné par une personne malveillante. Même après l’authentification des demandes de l’utilisateur et l’accès à ses données est autorisé, assurez-vous qu’il n’existe pas de vulnérabilités exploitables, telles que des dépassements de pile qui peuvent permettre à une personne malveillante de prendre le contrôle de votre serveur et d’étendre la violation de la sécurité.

 

 




