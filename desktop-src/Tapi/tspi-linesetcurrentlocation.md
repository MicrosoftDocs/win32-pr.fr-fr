---
description: Cette \_ fonction TSPI lineSetCurrentLocation est obsolète. L’interface TAPI a appelé cette fonction lorsque l’utilisateur (à l’aide de la boîte de dialogue Propriétés de la numérotation) ou une application (à l’aide de la fonction lineSetCurrentLocation) a modifié l’emplacement de traduction des adresses.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2361135770ac2d3900a902e0b7fa4fecad511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757005"
---
# <a name="tspi_linesetcurrentlocation"></a><span data-ttu-id="240d3-104">TSPI \_ lineSetCurrentLocation</span><span class="sxs-lookup"><span data-stu-id="240d3-104">TSPI\_lineSetCurrentLocation</span></span>

<span data-ttu-id="240d3-105">Cette \_ fonction TSPI lineSetCurrentLocation est obsolète.</span><span class="sxs-lookup"><span data-stu-id="240d3-105">This TSPI\_lineSetCurrentLocation function is obsolete.</span></span> <span data-ttu-id="240d3-106">L’interface TAPI a appelé cette fonction lorsque l’utilisateur (à l’aide de la boîte de dialogue Propriétés de la **numérotation** ) ou une application (à l’aide de la fonction [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) ) a modifié l’emplacement de traduction des adresses.</span><span class="sxs-lookup"><span data-stu-id="240d3-106">TAPI called this function when the user (using the **Dialing Properties** dialog box) or an application (using the [**lineSetCurrentLocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) function) changed the address translation location.</span></span>

<span data-ttu-id="240d3-107">À l’heure actuelle, une modification de l’emplacement de traduction aboutit à un \_ message DEVSTATE de ligne avec *dwParam1* défini sur LINEDEVSTATE \_ TRANSLATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="240d3-107">Currently, a change in translation location results in a LINE\_DEVSTATE message with *dwParam1* set to LINEDEVSTATE\_TRANSLATECHANGE.</span></span>

 

 
