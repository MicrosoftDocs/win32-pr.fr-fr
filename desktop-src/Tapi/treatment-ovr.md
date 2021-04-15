---
description: Le traitement fait référence à la gestion d’une session entrante qui n’a pas encore reçu de réponse ou qui a été mise en attente, telle que la musique. \_Pour obtenir la liste des traitements définis par l’interface TAPI, consultez constantes LINECALLTREATMENT.
ms.assetid: 0b8d1023-374a-4937-b39c-04043423eb47
title: Traitement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbde0e602836b543e849afb3d56c33fd6df0a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485584"
---
# <a name="treatment"></a><span data-ttu-id="c8af8-104">Traitement</span><span class="sxs-lookup"><span data-stu-id="c8af8-104">Treatment</span></span>

<span data-ttu-id="c8af8-105">Le traitement fait référence à la gestion d’une session entrante qui n’a pas encore reçu de réponse ou qui a été mise en attente, telle que la musique.</span><span class="sxs-lookup"><span data-stu-id="c8af8-105">Treatment refers to the handling of an incoming session that has not yet been answered or has been put on hold, such as music.</span></span> <span data-ttu-id="c8af8-106">Pour obtenir la liste des traitements définis par l’interface TAPI, consultez [ \_ constantes LINECALLTREATMENT](./linecalltreatment--constants.md) .</span><span class="sxs-lookup"><span data-stu-id="c8af8-106">Please see [LINECALLTREATMENT\_ Constants](./linecalltreatment--constants.md) for a list of treatments defined by TAPI.</span></span>

<span data-ttu-id="c8af8-107">Les fournisseurs de services ne prennent pas tous en charge l’utilisation de ces informations.</span><span class="sxs-lookup"><span data-stu-id="c8af8-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="c8af8-108">**TAPI 2. x : **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** membre dwCallTreatment** de *lpCallInfo*)</span><span class="sxs-lookup"><span data-stu-id="c8af8-108">**TAPI 2.x:  **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwCallTreatment** member of *lpCallInfo*)</span></span>

<span data-ttu-id="c8af8-109">**TAPI 3. x : **[**ITCallInfo :: obten \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL \_ CALLTREATMENT** membre de [**CALLINFO \_ long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span><span class="sxs-lookup"><span data-stu-id="c8af8-109">**TAPI 3.x:  **[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL\_CALLTREATMENT** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span></span>

 

 
