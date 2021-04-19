---
description: Le programme d’installation définit les propriétés selon l’ordre de priorité suivant. Une valeur de propriété dans cette liste peut remplacer une valeur qui vient après celle-ci et être remplacée par une valeur antérieure à celle-ci dans la liste.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Ordre de priorité des propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522446"
---
# <a name="order-of-property-precedence"></a><span data-ttu-id="847a6-104">Ordre de priorité des propriétés</span><span class="sxs-lookup"><span data-stu-id="847a6-104">Order of Property Precedence</span></span>

<span data-ttu-id="847a6-105">Le programme d’installation définit les propriétés selon l’ordre de priorité suivant.</span><span class="sxs-lookup"><span data-stu-id="847a6-105">The installer sets properties using the following order of precedence.</span></span> <span data-ttu-id="847a6-106">Une valeur de propriété dans cette liste peut remplacer une valeur qui vient après celle-ci et être remplacée par une valeur antérieure à celle-ci dans la liste.</span><span class="sxs-lookup"><span data-stu-id="847a6-106">A property value in this list can override a value that comes after it and be overridden by a value coming before it in the list.</span></span>

1.  <span data-ttu-id="847a6-107">Propriétés spécifiées par l’environnement d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="847a6-107">Properties specified by the operating environment.</span></span>
2.  <span data-ttu-id="847a6-108">[Propriétés publiques](public-properties.md) définies sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="847a6-108">[Public properties](public-properties.md) set on the command line.</span></span>
3.  <span data-ttu-id="847a6-109">Propriétés publiques listées par [**AdminProperties**](adminproperties.md) PropertySet pendant une [installation administrative](administrative-installation.md) .</span><span class="sxs-lookup"><span data-stu-id="847a6-109">Public properties listed by the [**AdminProperties**](adminproperties.md) propertyset during an [administrative installation](administrative-installation.md) .</span></span>
4.  <span data-ttu-id="847a6-110">Propriétés publiques ou privées définies lors de l’application d’une [*transformation*](t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="847a6-110">Public or private properties set during the application of a [*transform*](t-gly.md).</span></span>
5.  <span data-ttu-id="847a6-111">Propriété publique ou privée définie par la création de la [table de propriétés](property-table.md) du fichier. msi.</span><span class="sxs-lookup"><span data-stu-id="847a6-111">Public or private property that set by authoring the [Property table](property-table.md) of the .msi file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="847a6-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="847a6-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="847a6-113">À propos des propriétés</span><span class="sxs-lookup"><span data-stu-id="847a6-113">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



