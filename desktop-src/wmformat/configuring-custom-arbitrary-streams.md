---
title: Configuration de flux arbitraires personnalisés
description: Configuration de flux arbitraires personnalisés
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- flux, configuration de flux arbitraires personnalisés
- codecs, configuration de flux arbitraires personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672974"
---
# <a name="configuring-custom-arbitrary-streams"></a><span data-ttu-id="02f36-105">Configuration de flux arbitraires personnalisés</span><span class="sxs-lookup"><span data-stu-id="02f36-105">Configuring Custom Arbitrary Streams</span></span>

<span data-ttu-id="02f36-106">Lorsque vous utilisez votre propre type de données arbitraire, vous devez créer une valeur GUID qui servira d’identificateur de type de média majeur.</span><span class="sxs-lookup"><span data-stu-id="02f36-106">When using your own arbitrary data type, you must create a GUID value to serve as the major media type identifier for it.</span></span> <span data-ttu-id="02f36-107">Lorsque l’enregistreur rencontre un flux dans un profil avec un type majeur qu’il ne reconnaît pas, il suppose que le flux de données est une donnée arbitraire personnalisée.</span><span class="sxs-lookup"><span data-stu-id="02f36-107">When the writer encounters a stream in a profile with a major type it does not recognize, it assumes that the stream is custom arbitrary data.</span></span> <span data-ttu-id="02f36-108">Il acceptera vos exemples, les paquets de paquets et les combinera avec des échantillons des autres flux du fichier sans vérifier les données de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="02f36-108">It will accept your samples, packetize them, and combine them with samples from the other streams in the file without verifying the data in any way.</span></span>

<span data-ttu-id="02f36-109">Vous pouvez également créer vos propres identificateurs GUID de sous-type pour définir des sous-catégories de vos données personnalisées.</span><span class="sxs-lookup"><span data-stu-id="02f36-109">You can also create your own subtype GUID identifiers to define subcategories of your custom data.</span></span> <span data-ttu-id="02f36-110">L’enregistreur ignore complètement ces sous-types, mais ils sont conservés dans la section d’en-tête du fichier ASF, de sorte que votre application de lecture peut les récupérer et prendre des décisions en fonction de celles-ci.</span><span class="sxs-lookup"><span data-stu-id="02f36-110">The writer will ignore these subtypes completely, but they will be preserved in the header section of the ASF file, so your reading application can retrieve them and make decisions based on them.</span></span>

<span data-ttu-id="02f36-111">Un flux arbitraire requiert une vitesse de transmission et une fenêtre de mémoire tampon, et doit avoir une structure de [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) dont les valeurs sont effacées, à l’exception du type de média et du sous-type (si vous en utilisez un).</span><span class="sxs-lookup"><span data-stu-id="02f36-111">An arbitrary stream requires a bit rate and buffer window, and must have a [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure with the values cleared except for the major media type and subtype(if using one).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02f36-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="02f36-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02f36-113">**Configuration commune à tous les flux**</span><span class="sxs-lookup"><span data-stu-id="02f36-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="02f36-114">**Configuration de types de flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="02f36-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="02f36-115">**Flux de données arbitraires personnalisés**</span><span class="sxs-lookup"><span data-stu-id="02f36-115">**Custom Arbitrary Data Streams**</span></span>](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




