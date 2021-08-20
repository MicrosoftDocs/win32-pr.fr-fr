---
title: Pool de capteurs système
description: collection d’unités biométriques partageables qui fournissent l’accès aux services d’authentification Windows. Ce pool est utilisé par Winlogon, UAC et tout autre client qui associe un SID à un modèle biométrique spécifique.
ms.assetid: 308306a9-e12c-4ff6-92c3-a36667a5e548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c73a187c81812355d574b6c4fb867aad8f832c504f7ec79289879565cf73bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911612"
---
# <a name="system-sensor-pool"></a>Pool de capteurs système

le pool de capteurs système est une collection d’unités biométriques partageables qui permettent d’accéder aux services d’authentification Windows. Ce pool est utilisé par Winlogon, UAC et tout autre client qui associe un SID à un modèle biométrique spécifique. Unités biométriques dans le pool système :

-   Peut être partagé par plusieurs applications clientes.
-   Envoyer des notifications d’événements générées par l’achèvement d’opérations biométriques uniquement à l’application qui a le focus de la fenêtre active.
-   Utilisez les SID de compte pour représenter les identités de modèle. Tous les modèles associés à un compte d’utilisateur unique sont marqués avec le SID affecté à ce compte.
-   dépend du stockage de modèles dignes de confiance fourni par le Service biométrique Windows.

Une unité biométrique peut être incluse dans le pool système si elle peut être :

-   Configuré pour fonctionner en mode de base et agir uniquement comme un périphérique de capture biométrique.
-   Configuré pour fonctionner en mode avancé, mais ne possède pas de stockage de modèles intégré. Autrement dit, il doit utiliser l’adaptateur de stockage et le magasin de modèles fournis par Microsoft.
-   Configuré pour fonctionner en mode avancé, contient le stockage de modèles intégré et peut générer les hachages requis.

lorsqu’un nouveau périphérique de capteur est branché, le Service biométrique Windows crée une unité biométrique pour celui-ci et tente de configurer cette unité pour une utilisation par le pool de capteurs système. Si la configuration échoue, l’unité biométrique est placée dans le pool de capteurs non attribué.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pool de capteurs privés](private-sensor-pool.md)
</dt> <dt>

[Pools de capteurs](sensor-pools.md)
</dt> <dt>

[Comportement du pool système](system-pool-behavior.md)
</dt> </dl>

 

 




