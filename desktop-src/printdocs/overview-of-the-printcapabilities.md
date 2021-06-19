---
description: Le PrintCapabilities décrit les configurations ou les États disponibles sur un appareil, qui peuvent souvent être placés dans plusieurs configurations différentes.
ms.assetid: 094472fc-28ca-4d7a-a8be-cc4623d02ff2
title: Vue d’ensemble du PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8f61d1ee4125a9a1ac5f9ddb07cf226cd7094e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408522"
---
# <a name="overview-of-the-printcapabilities"></a><span data-ttu-id="57a2e-103">Vue d’ensemble du PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="57a2e-103">Overview of the PrintCapabilities</span></span>

<span data-ttu-id="57a2e-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="57a2e-104">This topic is not current.</span></span> <span data-ttu-id="57a2e-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="57a2e-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="57a2e-106">Le PrintCapabilities décrit les configurations ou les États disponibles sur un appareil.</span><span class="sxs-lookup"><span data-stu-id="57a2e-106">The PrintCapabilities describe the configurations or states available on a device.</span></span> <span data-ttu-id="57a2e-107">Un appareil qui est décrit par PrintCapabilities peut souvent être placé dans plusieurs configurations différentes.</span><span class="sxs-lookup"><span data-stu-id="57a2e-107">A device that is described by PrintCapabilities can often be placed in a number of different configurations.</span></span> <span data-ttu-id="57a2e-108">Dans le cas d’un périphérique d’impression, les attributs d’impression typiques incluent l’impression recto-verso, la résolution et la taille du média.</span><span class="sxs-lookup"><span data-stu-id="57a2e-108">In the case of a printing device, typical printing attributes include duplex printing, resolution, and media size.</span></span> <span data-ttu-id="57a2e-109">Si l’appareil prend en charge ces attributs, ils font partie de la configuration de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="57a2e-109">If the device supports these attributes, they are part of the configuration for that device.</span></span> <span data-ttu-id="57a2e-110">L’utilisateur sélectionne une configuration particulière en affectant une valeur spécifique à chacun des attributs disponibles. par exemple, duplex : OneSided, résolution : 600 ppp et MediaSize : Legal.</span><span class="sxs-lookup"><span data-stu-id="57a2e-110">The user selects a particular configuration by assigning a specific value to each of the available attributes; for example, Duplex: OneSided, Resolution: 600 dpi, and MediaSize: Legal.</span></span>

<span data-ttu-id="57a2e-111">Le PrintCapabilities est basé sur l’infrastructure du schéma d’impression, qui définit les éléments qui peuvent être utilisés dans le PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="57a2e-111">The PrintCapabilities are built on the Print Schema Framework, which defines the elements that can be used in the PrintCapabilities.</span></span> <span data-ttu-id="57a2e-112">Les mots clés du schéma d’impression définissent des hiérarchies d’éléments communément utilisées, ou Mots clés, afin de promouvoir la portabilité des informations et de l’intention entre les clients individuels.</span><span class="sxs-lookup"><span data-stu-id="57a2e-112">The Print Schema Keywords define commonly-used element hierarchies, or keywords, for the purpose of promoting portability of the information and intent between individual clients.</span></span> <span data-ttu-id="57a2e-113">Toutefois, les mots clés du schéma d’impression autorisent également les extensions privées afin que PrintCapabilities puisse être adapté pour répondre à des besoins spécifiques.</span><span class="sxs-lookup"><span data-stu-id="57a2e-113">However, the Print Schema Keywords also allow private extensions so that PrintCapabilities can be tailored to meet specific needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="57a2e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="57a2e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57a2e-115">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="57a2e-115">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



