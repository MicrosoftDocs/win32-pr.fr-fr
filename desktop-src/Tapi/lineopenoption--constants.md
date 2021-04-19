---
description: Les \_ constantes LINEOPENOPTION répertorient les options disponibles pour l’ouverture d’une ligne.
ms.assetid: 361ae90c-a2cf-4107-a2da-80f561a82c56
title: Constantes LINEOPENOPTION_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dee9182ff7a28627eebd695ce5d9c0877460b15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541675"
---
# <a name="lineopenoption_-constants"></a><span data-ttu-id="da325-103">\_Constantes LINEOPENOPTION</span><span class="sxs-lookup"><span data-stu-id="da325-103">LINEOPENOPTION\_ Constants</span></span>

<span data-ttu-id="da325-104">Les **\_ constantes LINEOPENOPTION** répertorient les options disponibles pour l’ouverture d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="da325-104">The **LINEOPENOPTION\_ constants** list the available options for opening a line.</span></span>

<dl> <dt>

<span data-ttu-id="da325-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**\_proxy LINEOPENOPTION**</span><span class="sxs-lookup"><span data-stu-id="da325-105"><span id="LINEOPENOPTION_PROXY"></span><span id="lineopenoption_proxy"></span>**LINEOPENOPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da325-106">L’application est prête à gérer les demandes d’autres applications pour lesquelles la ligne est ouverte.</span><span class="sxs-lookup"><span data-stu-id="da325-106">The application is willing to handle requests from other applications that have the line open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="da325-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION \_ SINGLEADDRESS**</span><span class="sxs-lookup"><span data-stu-id="da325-107"><span id="LINEOPENOPTION_SINGLEADDRESS"></span><span id="lineopenoption_singleaddress"></span>**LINEOPENOPTION\_SINGLEADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="da325-108">L’application doit être informée des nouveaux appels créés sur le périphérique de ligne uniquement si ces appels apparaissent à l’adresse spécifiée dans le membre **dwAddressID** de la structure [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) désignée par le paramètre *lpCallParams* .</span><span class="sxs-lookup"><span data-stu-id="da325-108">The application should be informed of new calls created on the line device only if those calls appear on the address specified in the **dwAddressID** member in the [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) structure pointed to by the *lpCallParams* parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da325-109">Notes</span><span class="sxs-lookup"><span data-stu-id="da325-109">Remarks</span></span>

<span data-ttu-id="da325-110">Pour plus d’informations sur le fonctionnement de ces options, consultez [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) .</span><span class="sxs-lookup"><span data-stu-id="da325-110">See [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) for further details on the operation of these options.</span></span>

## <a name="requirements"></a><span data-ttu-id="da325-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da325-111">Requirements</span></span>



| <span data-ttu-id="da325-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da325-112">Requirement</span></span> | <span data-ttu-id="da325-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="da325-113">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="da325-114">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="da325-114">TAPI version</span></span><br/> | <span data-ttu-id="da325-115">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="da325-115">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="da325-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="da325-116">Header</span></span><br/>       | <dl> <span data-ttu-id="da325-117"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="da325-117"><dt>Tapi.h</dt></span></span> </dl> |



 

 




