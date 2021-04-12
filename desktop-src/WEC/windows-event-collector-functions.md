---
title: Fonctions du collecteur d’événements Windows
description: La liste suivante décrit brièvement les fonctions utilisées dans le collecteur d’événements Windows.
ms.assetid: 48155df6-ba9c-4abe-ba84-6190cee95878
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c20e3bbee6226d385681c7471bb7fd3f337dfa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309190"
---
# <a name="windows-event-collector-functions"></a>Fonctions du collecteur d’événements Windows

La liste suivante décrit brièvement les fonctions utilisées dans le collecteur d’événements Windows.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**EcClose**](/windows/desktop/api/Evcoll/nf-evcoll-ecclose)
</dt> <dd>

Ferme un handle reçu à partir d’autres fonctions du collecteur d’événements.

</dd> <dt>

[**EcDeleteSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecdeletesubscription)
</dt> <dd>

Supprime un abonnement existant.

</dd> <dt>

[**EcEnumNextSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecenumnextsubscription)
</dt> <dd>

Continue l’énumération des abonnements inscrits sur l’ordinateur local.

</dd> <dt>

[**EcGetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarrayproperty)
</dt> <dd>

Récupère les valeurs de propriété pour les sources d’événements d’un abonnement.

</dd> <dt>

[**EcGetObjectArraySize**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetobjectarraysize)
</dt> <dd>

Récupère le nombre d’index du tableau de valeurs de propriété pour les sources d’événements d’un abonnement.

</dd> <dt>

[**EcGetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionproperty)
</dt> <dd>

Récupère une valeur de propriété à partir d’un objet d’abonnement.

</dd> <dt>

[**EcGetSubscriptionRunTimeStatus**](/windows/desktop/api/Evcoll/nf-evcoll-ecgetsubscriptionruntimestatus)
</dt> <dd>

Récupère les informations d’état d’exécution pour une source d’événement d’un abonnement ou de l’abonnement lui-même.

</dd> <dt>

[**EcInsertObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecinsertobjectarrayelement)
</dt> <dd>

Insère un objet vide dans un tableau de valeurs de propriété pour les sources d’événements d’un abonnement.

</dd> <dt>

[**EcOpenSubscriptionEnum**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscriptionenum)
</dt> <dd>

Crée un énumérateur d’abonnement pour énumérer tous les abonnements inscrits sur l’ordinateur local.

</dd> <dt>

[**EcOpenSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecopensubscription)
</dt> <dd>

Ouvre un abonnement existant ou crée un nouvel abonnement.

</dd> <dt>

[**EcSaveSubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecsavesubscription)
</dt> <dd>

Enregistre les informations de configuration de l’abonnement.

</dd> <dt>

[**EcSetObjectArrayProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetobjectarrayproperty)
</dt> <dd>

Définit une valeur de propriété dans un tableau de valeurs de propriété pour les sources d’événements d’un abonnement.

</dd> <dt>

[**EcSetSubscriptionProperty**](/windows/desktop/api/Evcoll/nf-evcoll-ecsetsubscriptionproperty)
</dt> <dd>

Définit de nouvelles valeurs ou met à jour les valeurs existantes d’un abonnement.

</dd> <dt>

[**EcRemoveObjectArrayElement**](/windows/desktop/api/Evcoll/nf-evcoll-ecremoveobjectarrayelement)
</dt> <dd>

Supprime un élément d’un tableau d’objets qui contiennent des valeurs de propriété pour les sources d’événements d’un abonnement.

</dd> <dt>

[**EcRetrySubscription**](/windows/desktop/api/Evcoll/nf-evcoll-ecretrysubscription)
</dt> <dd>

Effectue une nouvelle tentative de connexion à la source d’événement d’un abonnement qui n’est pas connecté.

</dd> </dl>

 

 




