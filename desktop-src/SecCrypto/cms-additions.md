---
description: La syntaxe de message de chiffrement (CMS), dérivée de la \# version 1,5 de PKCS 7, est la syntaxe utilisée pour hacher, signer numériquement, authentifier et chiffrer des messages arbitraires.
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: Ajouts CMS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce7c54867c1ee2a603e37751bf43a0abc65cee670c4a1fc994c9ace3f3404bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876959"
---
# <a name="cms-additions"></a>Ajouts CMS

La syntaxe de message de chiffrement (CMS), dérivée de la \# version 1,5 de PKCS 7, est la syntaxe utilisée pour [*hacher*](../secgloss/h-gly.md), [*signer numériquement*](../secgloss/d-gly.md), authentifier et chiffrer des messages arbitraires. Dans la mesure du possible, la compatibilité descendante est préservée. Toutefois, des modifications ont été apportées pour prendre en charge le transfert de certificat d’attribut et les techniques d’accord de clé pour la gestion des clés. CMS autorise l’encapsulation multiple afin qu’une enveloppe d’encapsulation puisse être imbriquée dans une autre. En outre, une partie peut signer numériquement des données précédemment encapsulées ; des attributs arbitraires, tels que l’heure de signature, peuvent être signés avec le contenu du message ; les attributs et, tels que les contre- [*signatures*](../secgloss/c-gly.md), peuvent être associés à une signature. CMS peut prendre en charge diverses architectures pour la gestion des clés basée sur les certificats.

Pour prendre en charge des fonctionnalités CMS supplémentaires, de nouveaux champs ont été attribués aux structures de données sous-jacentes. De nouveaux indicateurs et valeurs de paramètre ont également été ajoutés. Toutes les structures de données et toutes les API utilisant CMS sont à compatibilité descendante de 100% avec la \# version 1,5 de PKCS 7.

Les ajouts incluent les ajouts de [données enveloppés](enveloped-data-additions.md) et les [ajouts de données signés](signed-data-additions.md).

 

 
