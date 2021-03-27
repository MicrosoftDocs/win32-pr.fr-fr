---
description: Cette rubrique fournit des informations sur les considérations relatives à la sécurité de GDI. Cette rubrique ne fournit pas tout ce dont vous avez besoin pour connaître les problèmes de sécurité. Au lieu de cela, utilisez-le comme point de départ et référence pour ce domaine technologique.
ms.assetid: 374e3ac7-f635-47f1-a72a-14e1be85c795
title: 'Considérations relatives à la sécurité : GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71644da7d313e2efe0f287002c3e41a3a813a733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952443"
---
# <a name="security-considerations-gdi"></a><span data-ttu-id="e63aa-105">Considérations relatives à la sécurité : GDI</span><span class="sxs-lookup"><span data-stu-id="e63aa-105">Security Considerations: GDI</span></span>

<span data-ttu-id="e63aa-106">Cette rubrique fournit des informations sur les considérations relatives à la sécurité de GDI.</span><span class="sxs-lookup"><span data-stu-id="e63aa-106">This topic provides information about security considerations related to GDI.</span></span> <span data-ttu-id="e63aa-107">Cette rubrique ne fournit pas tout ce dont vous avez besoin pour connaître les problèmes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e63aa-107">This topic does not provide all you need to know about security issues.</span></span> <span data-ttu-id="e63aa-108">Au lieu de cela, utilisez-le comme point de départ et référence pour ce domaine technologique.</span><span class="sxs-lookup"><span data-stu-id="e63aa-108">Instead, use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="e63aa-109">GDI rencontre généralement des problèmes de sécurité, car il gère l’affichage plutôt que l’entrée.</span><span class="sxs-lookup"><span data-stu-id="e63aa-109">GDI generally has few security concerns because it deals with display rather than input.</span></span> <span data-ttu-id="e63aa-110">Toutefois, voici quelques-uns des problèmes que vous devez prendre en compte.</span><span class="sxs-lookup"><span data-stu-id="e63aa-110">However, here are a few issues that you should consider.</span></span>

<span data-ttu-id="e63aa-111">Les bitmaps, les sous-fichiers et les polices sont des structures complexes qui pourraient être endommagées.</span><span class="sxs-lookup"><span data-stu-id="e63aa-111">Bitmaps, metafiles, and fonts are complex structures that could become corrupted.</span></span> <span data-ttu-id="e63aa-112">Il est conseillé d’essayer de s’assurer que ces éléments ne sont pas endommagés et qu’ils proviennent d’une source digne de confiance.</span><span class="sxs-lookup"><span data-stu-id="e63aa-112">It is good practice to try to ensure that these items are uncorrupted and from a trustworthy source.</span></span>

<span data-ttu-id="e63aa-113">Une application peut spécifier le descripteur de sécurité pour certaines des API d’impression et de mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="e63aa-113">An application can specify the security descriptor for some of the printing and spooling APIs.</span></span> <span data-ttu-id="e63aa-114">Vous devez veiller à définir le descripteur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="e63aa-114">You should take care when setting the security descriptor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e63aa-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e63aa-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e63aa-116">Centre de sécurité Microsoft</span><span class="sxs-lookup"><span data-stu-id="e63aa-116">Microsoft Security Central</span></span>](https://www.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="e63aa-117">Centre de développement Sécurité</span><span class="sxs-lookup"><span data-stu-id="e63aa-117">Security Developer Center</span></span>](https://technet.microsoft.com/security/)
</dt> <dt>

[<span data-ttu-id="e63aa-118">Centre de Sécurité TechNet</span><span class="sxs-lookup"><span data-stu-id="e63aa-118">Security TechCenter</span></span>](https://technet.microsoft.com/security/default.aspx)
</dt> </dl>

 

 



