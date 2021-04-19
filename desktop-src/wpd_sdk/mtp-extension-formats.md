---
description: Formats d’extension MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Formats d’extension MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524291"
---
# <a name="mtp-extension-formats"></a><span data-ttu-id="114b5-103">Formats d’extension MTP</span><span class="sxs-lookup"><span data-stu-id="114b5-103">MTP Extension Formats</span></span>

<span data-ttu-id="114b5-104">Le format d’un fichier sur un appareil peut être décrit par une valeur GUID.</span><span class="sxs-lookup"><span data-stu-id="114b5-104">The format of a file on a device can be described by a GUID value.</span></span> <span data-ttu-id="114b5-105">Cette valeur est spécifiée par la \_ propriété format de l’objet wpd \_ .</span><span class="sxs-lookup"><span data-stu-id="114b5-105">This value is specified by the WPD\_OBJECT\_FORMAT property.</span></span>

## <a name="vendor-extended-formats"></a><span data-ttu-id="114b5-106">Formats étendus par le fournisseur</span><span class="sxs-lookup"><span data-stu-id="114b5-106">Vendor-Extended Formats</span></span>

<span data-ttu-id="114b5-107">Quand un fabricant de périphériques prend en charge un format étendu de fournisseur, son pilote associe le code de format du fournisseur (UINT16) avec les 16 bits les plus élevés du **\_ format d’objet wpd \_ \_ non spécifié** .</span><span class="sxs-lookup"><span data-stu-id="114b5-107">When a device manufacturer supports a vendor-extended format, their driver combines the vendor's format code (UINT16) with the highest 16 bits of the **WPD\_OBJECT\_FORMAT\_UNSPECIFIED** GUID.</span></span>

<span data-ttu-id="114b5-108">Par exemple, si le code étendu du fournisseur est 0xB001, le GUID résultant est comme indiqué dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="114b5-108">For example, if the vendor-extended code is 0xB001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a><span data-ttu-id="114b5-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="114b5-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="114b5-110">Prise en charge des extensions MTP</span><span class="sxs-lookup"><span data-stu-id="114b5-110">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



