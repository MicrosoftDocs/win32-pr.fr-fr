---
description: Lors de l’utilisation du service d’événements COM+, vous pouvez prendre des mesures pour vous assurer que les informations sensibles contenues dans un événement ne sont pas compromises.
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: Considérations sur la sécurité des événements COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cfd55d901d2583a7c570dcd378ab7750e15bd03adc61ad709c76e67076efae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096899"
---
# <a name="com-events-security-considerations"></a>Considérations sur la sécurité des événements COM+

Lors de l’utilisation du service d’événements COM+, vous pouvez prendre des mesures pour vous assurer que les informations sensibles contenues dans un événement ne sont pas compromises.

Les éditeurs d’événements doivent garder à l’esprit que toute partie pouvant écrire dans votre catalogue COM+ peut s’abonner à vos événements. Par conséquent, si les informations contenues dans un objet de classe d’événements sont sensibles, vous devez utiliser l’outil d’administration Services de composants pour vérifier que les communications avec les abonnés sont chiffrées pour l’application qui contient les composants de la classe d’événements. (Sous l’onglet **sécurité** de la feuille de propriétés de l’application com+, sélectionnez **confidentialité du paquet** comme **niveau d’authentification pour les appels** .) En outre, vous devez utiliser des [filtres d’événements](filtering-events-in-com-.md) pour vous assurer que les événements sont remis uniquement aux abonnés appropriés.

Les abonnés aux événements doivent garder à l’esprit qu’un tiers malveillant disposant d’un accès à votre réseau et de la connaissance de votre objet de classe d’événements pourrait créer des événements faux. Vous devez donc utiliser la [sécurité basée sur les rôles](role-based-security-administration.md) pour vous assurer que les appelants des méthodes de votre objet de classe d’événements disposent des informations d’identification appropriées pour effectuer les actions décrites dans votre implémentation.

Pour aider à protéger les serveurs de publication et les abonnés, utilisez le service événements COM+ sur un réseau privé d’hôtes approuvés isolé d’Internet par un pare-feu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurité COM+](com--security.md)
</dt> <dt>

[Filtrage des événements dans COM+](filtering-events-in-com-.md)
</dt> <dt>

[Objet de classe d’événements COM+](the-com--event-class-object.md)
</dt> </dl>

 

 



