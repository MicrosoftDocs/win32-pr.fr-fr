---
title: Configuration de flux de texte
description: Configuration de flux de texte
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- flux, configuration de flux de texte
- codecs, configuration des flux de texte
- flux de texte, configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462238"
---
# <a name="configuring-text-streams"></a><span data-ttu-id="cbdb2-106">Configuration de flux de texte</span><span class="sxs-lookup"><span data-stu-id="cbdb2-106">Configuring Text Streams</span></span>

<span data-ttu-id="cbdb2-107">Les flux de texte sont essentiellement les mêmes que les flux arbitraires personnalisés.</span><span class="sxs-lookup"><span data-stu-id="cbdb2-107">Text streams are essentially the same as custom arbitrary streams.</span></span> <span data-ttu-id="cbdb2-108">Il n’y a pas d’informations de configuration associées à un flux de texte pour identifier le type d’encodage de texte, de sorte que l’objet Writer ne peut pas vérifier les exemples.</span><span class="sxs-lookup"><span data-stu-id="cbdb2-108">There is no configuration information associated with a text stream to identify the type of text encoding, so the writer object cannot verify samples.</span></span>

<span data-ttu-id="cbdb2-109">Pour configurer un flux de texte, vous devez vous assurer que la structure de [**\_ \_ type de média WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contient un type de média majeur de \_ texte WMMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="cbdb2-109">To configure a text stream, you must ensure that the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure contains a major media type of WMMEDIATYPE\_TEXT.</span></span> <span data-ttu-id="cbdb2-110">Vous devez également définir une vitesse de transmission et une fenêtre de mémoire tampon pour le flux.</span><span class="sxs-lookup"><span data-stu-id="cbdb2-110">You must also set a bit rate and buffer window for the stream.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbdb2-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cbdb2-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cbdb2-112">**Calcul de la vitesse de transmission et des valeurs de fenêtre de mémoire tampon pour les flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="cbdb2-112">**Calculating Bit Rate and Buffer Window Values for Arbitrary Streams**</span></span>](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[<span data-ttu-id="cbdb2-113">**Configuration commune à tous les flux**</span><span class="sxs-lookup"><span data-stu-id="cbdb2-113">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="cbdb2-114">**Configuration de types de flux arbitraires**</span><span class="sxs-lookup"><span data-stu-id="cbdb2-114">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="cbdb2-115">**Flux de texte**</span><span class="sxs-lookup"><span data-stu-id="cbdb2-115">**Text Streams**</span></span>](text-streams.md)
</dt> </dl>

 

 




