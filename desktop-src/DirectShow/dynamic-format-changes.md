---
description: Modifications de format dynamique
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Modifications de format dynamique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516748"
---
# <a name="dynamic-format-changes"></a><span data-ttu-id="f65c2-103">Modifications de format dynamique</span><span class="sxs-lookup"><span data-stu-id="f65c2-103">Dynamic Format Changes</span></span>

<span data-ttu-id="f65c2-104">Lorsque deux filtres se connectent, ils s’accordent sur un type de média, qui décrit le format des données que le filtre en amont va distribuer.</span><span class="sxs-lookup"><span data-stu-id="f65c2-104">When two filters connect, they agree on a media type, which describes the format of the data that the upstream filter will deliver.</span></span> <span data-ttu-id="f65c2-105">Dans la plupart des cas, le type de média est fixe pour la durée de la connexion.</span><span class="sxs-lookup"><span data-stu-id="f65c2-105">In most cases, the media type is fixed for the duration of the connection.</span></span> <span data-ttu-id="f65c2-106">Toutefois, DirectShow offre une prise en charge limitée des filtres pour modifier le type de média.</span><span class="sxs-lookup"><span data-stu-id="f65c2-106">However, DirectShow does offer limited support for filters to change the media type.</span></span> <span data-ttu-id="f65c2-107">Lorsqu’un filtre change de type de média, il est appelé une *modification de format dynamique*.</span><span class="sxs-lookup"><span data-stu-id="f65c2-107">When a filter switches media types, it is called a *dynamic format change*.</span></span> <span data-ttu-id="f65c2-108">Si vous écrivez un filtre DirectShow, vous devez être conscient des mécanismes pour les modifications de format dynamique.</span><span class="sxs-lookup"><span data-stu-id="f65c2-108">If you are writing a DirectShow filter, you should be aware of the mechanisms for dynamic format changes.</span></span> <span data-ttu-id="f65c2-109">Même si votre filtre ne prend pas en charge ces modifications, il doit répondre correctement si un autre filtre demande un nouveau format.</span><span class="sxs-lookup"><span data-stu-id="f65c2-109">Even if your filter does not support such changes, it should respond correctly if another filter requests a new format.</span></span>

<span data-ttu-id="f65c2-110">DirectShow définit plusieurs mécanismes distincts pour les modifications de format dynamiques, en fonction de l’état du graphique de filtre et du type de modification requis.</span><span class="sxs-lookup"><span data-stu-id="f65c2-110">DirectShow defines several distinct mechanisms for dynamic format changes, depending on the state of filter graph and the type of change that is required.</span></span>

-   <span data-ttu-id="f65c2-111">Si le graphique est arrêté, les broches peuvent se reconnecter et renégocier le type de média.</span><span class="sxs-lookup"><span data-stu-id="f65c2-111">If the graph is stopped, the pins can reconnect and renegotiate the media type.</span></span> <span data-ttu-id="f65c2-112">Pour plus d’informations, consultez [reconnexion des codes confidentiels](reconnecting-pins.md).</span><span class="sxs-lookup"><span data-stu-id="f65c2-112">For more information, see [Reconnecting Pins](reconnecting-pins.md).</span></span>
-   <span data-ttu-id="f65c2-113">Certains filtres peuvent reconnecter des broches même si le graphique est actif (en cours d’exécution ou en pause).</span><span class="sxs-lookup"><span data-stu-id="f65c2-113">Some filters can reconnect pins even while the graph is active (running or paused).</span></span> <span data-ttu-id="f65c2-114">Pour plus d’informations sur ce mécanisme, consultez [reconnexion dynamique](dynamic-reconnection.md).</span><span class="sxs-lookup"><span data-stu-id="f65c2-114">For more information about this mechanism, see [Dynamic Reconnection](dynamic-reconnection.md).</span></span>

<span data-ttu-id="f65c2-115">Sinon, si le graphique est actif, mais que les filtres en question ne prennent pas en charge les reconnexions de code confidentiel dynamique, il existe trois mécanismes possibles pour modifier le format :</span><span class="sxs-lookup"><span data-stu-id="f65c2-115">Otherwise, if the graph is active, but the filters in question do not support dynamic pin reconnections, there are three possible mechanisms for changing the format:</span></span>

-   <span data-ttu-id="f65c2-116">[QueryAccept (en aval)](queryaccept--downstream.md) est utilisé quand une broche de sortie propose une modification de format à son homologue en aval, mais uniquement si le nouveau format ne requiert pas une mémoire tampon plus grande.</span><span class="sxs-lookup"><span data-stu-id="f65c2-116">[QueryAccept (Downstream)](queryaccept--downstream.md) is used when If an output pin proposes a format change to its downstream peer, but only if the new format does not require a larger buffer.</span></span>
-   <span data-ttu-id="f65c2-117">[QueryAccept (en amont)](queryaccept--upstream.md) est utilisé lorsqu’une broche d’entrée propose une modification de format à son homologue en amont.</span><span class="sxs-lookup"><span data-stu-id="f65c2-117">[QueryAccept (Upstream)](queryaccept--upstream.md) is used when an input pin proposes a format change to its upstream peer.</span></span> <span data-ttu-id="f65c2-118">Le nouveau format peut être de la même taille, ou il peut être plus grand.</span><span class="sxs-lookup"><span data-stu-id="f65c2-118">The new format can be the same size, or it can be larger.</span></span>
-   <span data-ttu-id="f65c2-119">[ReceiveConnection](receiveconnection.md) est utilisé lorsqu’une broche de sortie propose une modification de format à son homologue en aval, et que le nouveau format requiert une mémoire tampon plus grande.</span><span class="sxs-lookup"><span data-stu-id="f65c2-119">[ReceiveConnection](receiveconnection.md) is used when an output pin proposes a format change to its downstream peer, and the new format requires a larger buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f65c2-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f65c2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f65c2-121">Gestion des modifications de format à partir du convertisseur vidéo</span><span class="sxs-lookup"><span data-stu-id="f65c2-121">Handling Format Changes from the Video Renderer</span></span>](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



