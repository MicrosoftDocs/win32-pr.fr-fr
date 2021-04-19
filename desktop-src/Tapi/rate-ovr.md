---
description: La fréquence ou la bande passante d’un appel spécifie la vitesse de transmission des données. Trois points de données identifient la fréquence actuelle du taux maximal pour un mode de support spécifié et le taux minimal pour le mode porteur.
ms.assetid: bc373ac5-a986-483f-a136-60cdc2e2c6b0
title: Tarif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40747c26a98d8eb69e8161fb04302c5187121dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538921"
---
# <a name="rate"></a><span data-ttu-id="f1c40-104">Tarif</span><span class="sxs-lookup"><span data-stu-id="f1c40-104">Rate</span></span>

<span data-ttu-id="f1c40-105">Le taux (ou la bande passante) d’un appel spécifie la vitesse de transmission des données.</span><span class="sxs-lookup"><span data-stu-id="f1c40-105">The rate (or bandwidth) of a call specifies the speed of data transmission.</span></span> <span data-ttu-id="f1c40-106">Taux d’identification de trois points de données : taux actuel, taux maximal pour un mode de support spécifié et taux minimal pour le mode porteur.</span><span class="sxs-lookup"><span data-stu-id="f1c40-106">Three data points identify rate: the current rate, the maximum rate for a specified bearer mode, and the minimum rate for the bearer mode.</span></span>

<span data-ttu-id="f1c40-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="f1c40-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="f1c40-108">\* \* TAPI 2. x : \* \*[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **DwMinRate** ou **dwMaxRate** membre de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span><span class="sxs-lookup"><span data-stu-id="f1c40-108">\*\*TAPI 2.x:  \*\*[**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwMinRate** or **dwMaxRate** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)</span></span>

<span data-ttu-id="f1c40-109">\* \* TAPI 3. x : \* \*[**ITCallInfo :: obten \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo ::p ut \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ MAXRATE**, **CIL \_ MINRATE** ou **CIL \_ rate** Member of [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span><span class="sxs-lookup"><span data-stu-id="f1c40-109">\*\*TAPI 3.x:  \*\*[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_MAXRATE**, **CIL\_MINRATE**, or **CIL\_RATE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)</span></span>

<span data-ttu-id="f1c40-110">\* \* TSPI : \* \* message de [**ligne \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) , avec *dwParam1* défini sur le taux de LINECALLINFOSTATE \_</span><span class="sxs-lookup"><span data-stu-id="f1c40-110">\*\*TSPI:  \*\*[**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_RATE</span></span>

 

 
