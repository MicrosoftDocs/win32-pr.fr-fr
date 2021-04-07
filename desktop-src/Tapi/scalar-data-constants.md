---
description: Pour les constantes de données scalaires extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs dans une plage spécifiée.
ms.assetid: 62280b71-9bec-4a9d-abd2-d3e1c2cee43f
title: Constantes de données scalaires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3187d2064501727614dfcbf0b8e11c136fea13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760798"
---
# <a name="scalar-data-constants"></a><span data-ttu-id="84f60-103">Constantes de données scalaires</span><span class="sxs-lookup"><span data-stu-id="84f60-103">Scalar Data Constants</span></span>

<span data-ttu-id="84f60-104">Pour les constantes de données scalaires extensible, un fournisseur de fournisseurs de services peut définir de nouvelles valeurs dans une plage spécifiée.</span><span class="sxs-lookup"><span data-stu-id="84f60-104">For extensible scalar data constants, a service-provider vendor can define new values in a specified range.</span></span> <span data-ttu-id="84f60-105">Étant donné que la plupart des constantes de données sont **DWORD** s, la plage comprise entre 0X00000000 et 0x7FFFFFFF est généralement réservée aux extensions futures courantes, tandis que 0X80000000 à 0xFFFFFFFF est disponible pour les extensions spécifiques au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="84f60-105">Because most data constants are **DWORD** s, the range 0x00000000 through 0x7FFFFFFF is typically reserved for common future extensions, while 0x80000000 through 0xFFFFFFFF is available for vendor-specific extensions.</span></span> <span data-ttu-id="84f60-106">L’hypothèse est qu’un fournisseur définit des valeurs qui sont des extensions naturelles des types de données définis par l’API.</span><span class="sxs-lookup"><span data-stu-id="84f60-106">The assumption is that a vendor would define values that are natural extensions of the datatypes defined by the API.</span></span>

 

 



