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
# <a name="mpeg-sample-properties"></a><span data-ttu-id="78959-103">Exemples de propriétés MPEG</span><span class="sxs-lookup"><span data-stu-id="78959-103">MPEG Sample Properties</span></span>

<span data-ttu-id="78959-104">Les exemples MPEG présentent les caractéristiques suivantes.</span><span class="sxs-lookup"><span data-stu-id="78959-104">MPEG samples have the following characteristics.</span></span>

<span data-ttu-id="78959-105">**Horodatages**</span><span class="sxs-lookup"><span data-stu-id="78959-105">**Time Stamps**</span></span>

<span data-ttu-id="78959-106">Tous les exemples n’ont pas d’heure de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="78959-106">Not all samples have start and stop times.</span></span> <span data-ttu-id="78959-107">L’exemple de temps d’arrêt du paquet et des données de charge utile n’est pas utile. Il est généralement défini sur l’heure de début plus un.</span><span class="sxs-lookup"><span data-stu-id="78959-107">The sample stop time for packet and payload data is not useful; it is usually set to the start time plus one.</span></span> <span data-ttu-id="78959-108">Les exemples de données de paquets MPEG ou de charge utile auront une heure de début et de fin définie si le paquet de la couche système à partir duquel ils sont générés comportait une PTS valide.</span><span class="sxs-lookup"><span data-stu-id="78959-108">MPEG packet or payload data samples will have a start and stop time set if the system layer packet they are generated from had a valid PTS.</span></span>

<span data-ttu-id="78959-109">Pour plus d’informations sur les horodatages, consultez la section 2.4.1 de ISO1-11172 : « l’en-tête de paquet peut contenir des horodatages de décodage et/ou de présentation (DTS et PTS) qui font référence à la première unité d’accès dans le paquet. »</span><span class="sxs-lookup"><span data-stu-id="78959-109">For more information about time stamps, see section 2.4.1 of ISO1-11172: "The packet header may contain decoding and/or presentation time stamps (DTS and PTS) that refer to the first access unit in the packet."</span></span>

<span data-ttu-id="78959-110">Pour les \_ principaux types de flux MPEG, l’heure de début est la position d’octet du premier octet, évaluée à 1 octet par seconde.</span><span class="sxs-lookup"><span data-stu-id="78959-110">For MPEG\_Stream major types, the start time is the byte position of the first byte, rated at 1 byte per second.</span></span> <span data-ttu-id="78959-111">L’heure de fin est la position d’octet du dernier octet.</span><span class="sxs-lookup"><span data-stu-id="78959-111">The stop time is the byte position of the last byte.</span></span> <span data-ttu-id="78959-112">Ainsi, les échantillons consécutifs doivent avoir l’heure d’arrêt du premier paquet égale à l’heure de début du paquet suivant.</span><span class="sxs-lookup"><span data-stu-id="78959-112">Thus, consecutive samples should have the stop time of the first packet equal to the start time of the next packet.</span></span> <span data-ttu-id="78959-113">Pour les données de CD vidéo, l’origine du support doit correspondre au format d’un fichier vidéo-CD exposé par CDFS avec le bloc RIFF standard au début.</span><span class="sxs-lookup"><span data-stu-id="78959-113">For Video CD data, the origin of the medium must match the format of a video-CD file exposed by CDFS with the standard RIFF chunk at the start.</span></span>

<span data-ttu-id="78959-114">Pour les types de paquets vidéo et de charge utile MPEG, l’horodatage est l’heure de présentation de la première image vidéo dont le code de démarrage de l’image commence dans l’échantillon.</span><span class="sxs-lookup"><span data-stu-id="78959-114">For MPEG video packet and payload types, the time stamp is the presentation time for the first video frame whose picture start code begins in the sample.</span></span>

<span data-ttu-id="78959-115">Pour les types de paquets audio et de charge utile MPEG, l’horodatage est l’heure de présentation de la première image audio dont le code de synchronisation commence dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="78959-115">For MPEG audio packet and payload types, the time stamp is the presentation time for the first audio frame whose sync code starts in the sample.</span></span>

<span data-ttu-id="78959-116">Il est supposé que les données de paquet et de charge utile sans horodatage peuvent être préinscrites avec succès par les filtres de gestion.</span><span class="sxs-lookup"><span data-stu-id="78959-116">It is assumed that packet and payload data without time stamps can be successfully prerolled by the handling filters.</span></span>

<span data-ttu-id="78959-117">**Discontinuités**</span><span class="sxs-lookup"><span data-stu-id="78959-117">**Discontinuities**</span></span>

<span data-ttu-id="78959-118">En cas de rupture dans le flux (par exemple, un écart dans les données en temps réel, ou une erreur dans les données ou après une recherche), la propriété discontinu est définie sur l’exemple de support suivant.</span><span class="sxs-lookup"><span data-stu-id="78959-118">If there is a break in the stream (for example, a gap in the real-time data, or an error in the data or after a seek), the discontinuity property is set on the next media sample.</span></span> <span data-ttu-id="78959-119">Cela permet également une discontinuisation des horodateurs.</span><span class="sxs-lookup"><span data-stu-id="78959-119">This also allows for a time-stamp discontinuity.</span></span>

<span data-ttu-id="78959-120">**Notifications de fin de flux**</span><span class="sxs-lookup"><span data-stu-id="78959-120">**End-of-Stream Notifications**</span></span>

<span data-ttu-id="78959-121">Quand le décodeur reçoit cette notification, il doit traiter toutes les données mises en mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="78959-121">When the decoder receives this notification, it must process any buffered data.</span></span> <span data-ttu-id="78959-122">Toutes les nouvelles données doivent ensuite démarrer avec la propriété discontinu.</span><span class="sxs-lookup"><span data-stu-id="78959-122">Any new data must then start with the discontinuity property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78959-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="78959-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78959-124">Prise en charge MPEG-2 dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="78959-124">MPEG-2 Support in DirectShow</span></span>](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



