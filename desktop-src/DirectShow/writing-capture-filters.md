---
description: Écriture de filtres de capture
ms.assetid: 7dfd1009-da09-49dc-a200-3d7a9f1c70c1
title: Écriture de filtres de capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8de1a64de2b56dbc0728432307036fc46387f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534575"
---
# <a name="writing-capture-filters"></a><span data-ttu-id="5b3f1-103">Écriture de filtres de capture</span><span class="sxs-lookup"><span data-stu-id="5b3f1-103">Writing Capture Filters</span></span>

<span data-ttu-id="5b3f1-104">L’écriture d’un filtre de capture audio ou vidéo pour DirectShow n’est pas recommandée.</span><span class="sxs-lookup"><span data-stu-id="5b3f1-104">Writing an audio or video capture filter for DirectShow is not recommended.</span></span> <span data-ttu-id="5b3f1-105">Au lieu de cela, DirectShow assure la prise en charge automatique des périphériques de capture audio et vidéo à l’aide de filtres de wrapper et de l' [énumérateur de périphérique système](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="5b3f1-105">Instead, DirectShow provides automatic support for audio and video capture devices, using wrapper filters and the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="5b3f1-106">Pour plus d’informations sur l’implémentation d’un pilote de périphérique, reportez-vous à la documentation de Windows Driver Kit (WDK).</span><span class="sxs-lookup"><span data-stu-id="5b3f1-106">For more information about implementing a device driver, refer to the Windows Driver Kit (WDK) documentation.</span></span>

<span data-ttu-id="5b3f1-107">Cette section est destinée uniquement aux développeurs qui ont besoin de capturer des données personnalisées à partir d’un périphérique matériel inhabituel.</span><span class="sxs-lookup"><span data-stu-id="5b3f1-107">This section is intended only for developers who need to capture some kind of custom data from an unusual hardware device.</span></span>

<span data-ttu-id="5b3f1-108">Cet article contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="5b3f1-108">This article contains the following sections:</span></span>

-   [<span data-ttu-id="5b3f1-109">Exigences de code confidentiel pour les filtres de capture</span><span class="sxs-lookup"><span data-stu-id="5b3f1-109">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
-   [<span data-ttu-id="5b3f1-110">Implémentation d’un pin d’aperçu (facultatif)</span><span class="sxs-lookup"><span data-stu-id="5b3f1-110">Implementing a Preview Pin (Optional)</span></span>](implementing-a-preview-pin--optional.md)
-   [<span data-ttu-id="5b3f1-111">Génération de données dans un filtre de capture</span><span class="sxs-lookup"><span data-stu-id="5b3f1-111">Producing Data in a Capture Filter</span></span>](producing-data-in-a-capture-filter.md)

## <a name="related-topics"></a><span data-ttu-id="5b3f1-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b3f1-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b3f1-113">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="5b3f1-113">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



