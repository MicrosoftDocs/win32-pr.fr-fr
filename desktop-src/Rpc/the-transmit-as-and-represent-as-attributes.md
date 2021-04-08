---
title: Attributs transmit_as et represent_as
description: Cette section décrit l’implémentation de la conversion de type de données de programmeur à l’aide de MIDL \ transmettre \_ en tant que \ et \ représente \_ As \ Attributes.
ms.assetid: 2e1af786-f507-453f-bb10-74805ef6b1a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16760091479a306b9dc9c815c7f3a41b25012ca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842402"
---
# <a name="the-transmit_as-and-represent_as-attributes"></a><span data-ttu-id="bd565-103">Les \_ attributs transmit As et dereprésente \_ As</span><span class="sxs-lookup"><span data-stu-id="bd565-103">The transmit\_as and represent\_as Attributes</span></span>

<span data-ttu-id="bd565-104">Cette section décrit l’implémentation de la conversion de type de données de programmeur à l’aide de la fonction MIDL **\[** [**transmit \_ As**](/windows/desktop/Midl/transmit-as) **\]** et **\[** [**représente \_ en tant qu'**](/windows/desktop/Midl/represent-as) **\]** attributs.</span><span class="sxs-lookup"><span data-stu-id="bd565-104">This section discusses the implementation of programmer data type conversion using the MIDL **\[**[**transmit\_as**](/windows/desktop/Midl/transmit-as)**\]** and **\[**[**represent\_as**](/windows/desktop/Midl/represent-as)**\]** attributes.</span></span> <span data-ttu-id="bd565-105">La discussion est présentée dans les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd565-105">The discussion is presented in the following sections:</span></span>

-   [<span data-ttu-id="bd565-106">L’attribut **transmit \_ As**</span><span class="sxs-lookup"><span data-stu-id="bd565-106">The **transmit\_as** Attribute</span></span>](the-transmit-as-attribute.md)
-   [<span data-ttu-id="bd565-107">**Type \_ vers \_** la fonction de transmission</span><span class="sxs-lookup"><span data-stu-id="bd565-107">The **type\_to\_xmit** Function</span></span>](the-type-to-xmit-function.md)
-   [<span data-ttu-id="bd565-108">Le **type \_ de \_** la fonction de transmission</span><span class="sxs-lookup"><span data-stu-id="bd565-108">The **type\_from\_xmit** Function</span></span>](the-type-from-xmit-function.md)
-   [<span data-ttu-id="bd565-109">Fonction de transmission **\_ \_ libre du type**</span><span class="sxs-lookup"><span data-stu-id="bd565-109">The **type\_free\_xmit** Function</span></span>](the-type-free-xmit-function.md)
-   [<span data-ttu-id="bd565-110">**Type \_ Free \_ inst** , fonction</span><span class="sxs-lookup"><span data-stu-id="bd565-110">The **type\_free\_inst** Function</span></span>](the-type-free-inst-function.md)
-   [<span data-ttu-id="bd565-111">L’attribut **représente \_ en tant que**</span><span class="sxs-lookup"><span data-stu-id="bd565-111">The **represent\_as** Attribute</span></span>](the-represent-as-attribute.md)
-   [<span data-ttu-id="bd565-112">**Type nommé \_ \_ à partir de \_** la fonction locale</span><span class="sxs-lookup"><span data-stu-id="bd565-112">The **named\_type\_from\_local** Function</span></span>](the-named-type-from-local-function.md)
-   [<span data-ttu-id="bd565-113">Le **\_ type nommé \_ vers \_** la fonction locale</span><span class="sxs-lookup"><span data-stu-id="bd565-113">The **named\_type\_to\_local** Function</span></span>](the-named-type-to-local-function.md)
-   [<span data-ttu-id="bd565-114">Fonction **\_ \_ \_ locale Free de type nommé**</span><span class="sxs-lookup"><span data-stu-id="bd565-114">The **named\_type\_free\_local** Function</span></span>](the-named-type-free-local-function.md)
-   [<span data-ttu-id="bd565-115">Le **\_ type nommé \_ Free \_ inst** , fonction</span><span class="sxs-lookup"><span data-stu-id="bd565-115">The **named\_type\_free\_inst** Function</span></span>](the-named-type-free-inst-function.md)

 

 