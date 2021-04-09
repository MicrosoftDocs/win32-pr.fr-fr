---
description: Un fournisseur de services peut indiquer des numéros de téléphone générés de manière externe en définissant les membres de la structure LINECALLINFO lors du traitement de la \_ fonction TSPI lineGetCallInfo.
ms.assetid: 10c83199-de7d-4a9b-84c4-ef8f5ea5055a
title: Numéros de téléphone générés de manière externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e7039023ecec987a16c39367a569925c20ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751613"
---
# <a name="externally-generated-phone-numbers"></a><span data-ttu-id="59fdb-103">Numéros de téléphone générés de manière externe</span><span class="sxs-lookup"><span data-stu-id="59fdb-103">Externally Generated Phone Numbers</span></span>

<span data-ttu-id="59fdb-104">Un fournisseur de services peut indiquer des numéros de téléphone générés de manière externe (autrement dit, des chiffres pour les appels sortants générés en externe sur l’ordinateur) en définissant les membres **DisplayableAddress**, **CalledParty** ou [comments](./comment-ovr.md) dans la structure [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) lors du traitement de la fonction [**\_ lineGetCallInfo TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="59fdb-104">A service provider can indicate externally generated phone numbers (that is, numbers for outbound calls generated externally to the computer) by setting the **DisplayableAddress**, **CalledParty**, or [Comment](./comment-ovr.md) members in the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure when processing the [**TSPI\_lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) function.</span></span> <span data-ttu-id="59fdb-105">Si TAPI n’a pas enregistré ses propres données pour ces membres, il laisse les données définies par le fournisseur de services inchangées.</span><span class="sxs-lookup"><span data-stu-id="59fdb-105">If TAPI has not saved its own data for these members, it leaves the data set by the service provider unchanged.</span></span> <span data-ttu-id="59fdb-106">Si l’interface TAPI n’a pas de données mises en cache pour ces membres, TAPI ajoute son texte à la fin de la partie variable de la structure **LINECALLINFO** et remplace la taille et l’offset que le fournisseur de services a placé dans la partie fixe.</span><span class="sxs-lookup"><span data-stu-id="59fdb-106">If TAPI does have cached data for these members, TAPI adds its text to the end of the variable portion of the **LINECALLINFO** structure and overwrites the size and offset the service provider has put into the fixed portion.</span></span>

<span data-ttu-id="59fdb-107">Un fournisseur de services peut également copier un nombre sortant dans le membre **CalledID** .</span><span class="sxs-lookup"><span data-stu-id="59fdb-107">A service provider can also copy an outbound number into the **CalledID** member.</span></span> <span data-ttu-id="59fdb-108">Par conséquent, les applications de journalisation doivent vérifier le membre **CalledID** sur les appels sortants si les membres **DisplayableAddress** et **CalledParty** sont vides.</span><span class="sxs-lookup"><span data-stu-id="59fdb-108">Therefore, logging applications should check the **CalledID** member on outbound calls if the **DisplayableAddress** and **CalledParty** members are empty.</span></span>

 

 
