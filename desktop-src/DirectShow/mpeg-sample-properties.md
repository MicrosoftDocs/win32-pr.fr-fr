---
description: Exemples de propriétés MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Exemples de propriétés MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515749"
---
# <a name="mpeg-sample-properties"></a>Exemples de propriétés MPEG

Les exemples MPEG présentent les caractéristiques suivantes.

**Horodatages**

Tous les exemples n’ont pas d’heure de début et de fin. L’exemple de temps d’arrêt du paquet et des données de charge utile n’est pas utile. Il est généralement défini sur l’heure de début plus un. Les exemples de données de paquets MPEG ou de charge utile auront une heure de début et de fin définie si le paquet de la couche système à partir duquel ils sont générés comportait une PTS valide.

Pour plus d’informations sur les horodatages, consultez la section 2.4.1 de ISO1-11172 : « l’en-tête de paquet peut contenir des horodatages de décodage et/ou de présentation (DTS et PTS) qui font référence à la première unité d’accès dans le paquet. »

Pour les \_ principaux types de flux MPEG, l’heure de début est la position d’octet du premier octet, évaluée à 1 octet par seconde. L’heure de fin est la position d’octet du dernier octet. Ainsi, les échantillons consécutifs doivent avoir l’heure d’arrêt du premier paquet égale à l’heure de début du paquet suivant. Pour les données de CD vidéo, l’origine du support doit correspondre au format d’un fichier vidéo-CD exposé par CDFS avec le bloc RIFF standard au début.

Pour les types de paquets vidéo et de charge utile MPEG, l’horodatage est l’heure de présentation de la première image vidéo dont le code de démarrage de l’image commence dans l’échantillon.

Pour les types de paquets audio et de charge utile MPEG, l’horodatage est l’heure de présentation de la première image audio dont le code de synchronisation commence dans l’exemple.

Il est supposé que les données de paquet et de charge utile sans horodatage peuvent être préinscrites avec succès par les filtres de gestion.

**Discontinuités**

En cas de rupture dans le flux (par exemple, un écart dans les données en temps réel, ou une erreur dans les données ou après une recherche), la propriété discontinu est définie sur l’exemple de support suivant. Cela permet également une discontinuisation des horodateurs.

**Notifications de fin de flux**

Quand le décodeur reçoit cette notification, il doit traiter toutes les données mises en mémoire tampon. Toutes les nouvelles données doivent ensuite démarrer avec la propriété discontinu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge MPEG-2 dans DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



