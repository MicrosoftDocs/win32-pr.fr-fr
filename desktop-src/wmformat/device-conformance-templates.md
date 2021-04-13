---
title: Modèles de conformité des appareils
description: Modèles de conformité des appareils
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- Windows Media Format SDK, modèles de conformité des appareils
- codecs, modèles de conformité des appareils
- modèles de conformité des appareils, à propos de
- modèles, modèles de conformité des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311275"
---
# <a name="device-conformance-templates"></a><span data-ttu-id="2753e-107">Modèles de conformité des appareils</span><span class="sxs-lookup"><span data-stu-id="2753e-107">Device Conformance Templates</span></span>

<span data-ttu-id="2753e-108">Les codecs de la série Windows Media 9 prennent en charge les modèles de conformité des appareils, qui sont des plages définies de paramètres de configuration de flux et d’algorithmes de codec.</span><span class="sxs-lookup"><span data-stu-id="2753e-108">The Windows Media 9 Series codecs support device conformance templates, which are defined ranges of stream configuration settings and codec algorithms.</span></span> <span data-ttu-id="2753e-109">Chaque modèle définit les plages de valeurs appropriées pour certains périphériques.</span><span class="sxs-lookup"><span data-stu-id="2753e-109">Each template defines the ranges of values appropriate for certain devices.</span></span>

<span data-ttu-id="2753e-110">Par le passé, les fabricants de matériel qui rendaient des appareils aptes à émettre des fichiers ASF fonctionnaient tous avec leurs propres normes.</span><span class="sxs-lookup"><span data-stu-id="2753e-110">In the past, the hardware manufacturers that made devices capable of playing ASF files were all working to their own standards.</span></span> <span data-ttu-id="2753e-111">Cela a abouti à une large gamme de fonctionnalités sur des appareils similaires qui se poursuivent aujourd’hui.</span><span class="sxs-lookup"><span data-stu-id="2753e-111">This resulted in the widely disparate range of capabilities on similar devices that continues today.</span></span>

<span data-ttu-id="2753e-112">Avec les modèles de conformité des appareils, les codecs Windows Media établissent un motif commun pour les appareils similaires.</span><span class="sxs-lookup"><span data-stu-id="2753e-112">With device conformance templates, the Windows Media codecs establish common ground for similar devices.</span></span> <span data-ttu-id="2753e-113">Les fabricants de matériel peuvent indiquer les modèles auxquels leurs appareils sont conformes, ce qui permet aux créateurs de contenu de cibler plus en toute confiance leurs fichiers pour la lecture des appareils.</span><span class="sxs-lookup"><span data-stu-id="2753e-113">Hardware manufacturers can state which templates their devices conform to, enabling content creators to more confidently target their files to reading devices.</span></span> <span data-ttu-id="2753e-114">Il est également plus facile pour les applications de lecteur de déterminer si un fichier est inapproprié pour l’appareil avant de tenter de le lire.</span><span class="sxs-lookup"><span data-stu-id="2753e-114">It is also easier for player applications to determine whether a file is inappropriate for the device before attempting to play it.</span></span>

<span data-ttu-id="2753e-115">Un modèle de conformité de périphérique est identifié par une chaîne, qui est stockée sous la forme d’un attribut de métadonnées associé au flux auquel le modèle s’applique.</span><span class="sxs-lookup"><span data-stu-id="2753e-115">A device conformance template is identified by a string, which is stored as a metadata attribute associated with the stream to which the template applies.</span></span> <span data-ttu-id="2753e-116">Pour obtenir la liste des modèles et leurs chaînes et paramètres, consultez [paramètres de modèle de conformité des appareils](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2753e-116">For a list of the templates and their strings and parameters, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="2753e-117">Les modèles de conformité des appareils sont pris en charge pour tous les codecs Windows Media 9 et versions ultérieures, à l’exception du codec d’écran Windows Media Video 9 et du codec Windows Media Audio 9 Lossless.</span><span class="sxs-lookup"><span data-stu-id="2753e-117">Device conformance templates are supported for all of the Windows Media 9 Series and later codecs except the Windows Media Video 9 Screen codec and the Windows Media Audio 9 Lossless codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2753e-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2753e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2753e-119">**Fonctionnalités du codec**</span><span class="sxs-lookup"><span data-stu-id="2753e-119">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="2753e-120">**Utilisation des modèles de conformité des appareils**</span><span class="sxs-lookup"><span data-stu-id="2753e-120">**Working with Device Conformance Templates**</span></span>](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




