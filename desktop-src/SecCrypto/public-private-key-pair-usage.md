---
description: Toutes les opérations normales de RSA/SChannel et de Diffie-Hellman/Schannel utilisent la \_ paire de clés publique/privée à KeyExchange.
ms.assetid: e12afdbb-7ba8-444e-a43f-e262b481a353
title: Utilisation de la paire de clés publique/privée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38dba78c487c433875ed23ce3f2f3c87a86b07c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530650"
---
# <a name="publicprivate-key-pair-usage"></a>Utilisation de la paire de clés publique/privée

Toutes les opérations normales de [*RSA*](../secgloss/r-gly.md)/Schannel et [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel utilisent la \_ paire de [*clés publique/privée*](../secgloss/p-gly.md)à KeyExchange. Pour permettre l' [*authentification*](../secgloss/a-gly.md)du serveur, le côté serveur des opérations Schannel doit avoir accès à son certificat [*X. 509*](../secgloss/x-gly.md) contenant sa clé publique et à l’accès à la [*clé privée*](../secgloss/p-gly.md)correspondante. Le côté client de [*Schannel*](../secgloss/s-gly.md) a besoin de son certificat avec sa clé publique et d’un accès à sa clé privée si l’authentification du client est implémentée.

Étant donné que les moteurs de protocole Schannel n’utilisent jamais la \_ paire de clés publique/privée at signature, cette paire de clés n’a pas besoin d’être prise en charge par un nouveau fournisseur de services de chiffrement prenant uniquement en charge RSA/SChannel ou Diffie-Hellman/Schannel.

Si un moteur de protocole utilise une suite de chiffrement d’exportation SSL 3,0 avec une \_ paire de clés at KeyExchange supérieure à 512 bits, le serveur doit utiliser une paire de clés RSA supplémentaire. Cette paire de clés supplémentaire est toujours exactement de 512 bits et peut être éphémère. La paire est stockée en tant qu' \_ élément at KeyExchange dans un conteneur de clé détenu par le moteur de protocole. Un descripteur de ce conteneur de clé est généralement acquis au démarrage du moteur de protocole.

Diffie-Hellman prend en charge uniquement [*CALG \_ DH \_ EPHEM*](../secgloss/c-gly.md) et utilise des clés publiques RSA ou DSS normales.

 

 
