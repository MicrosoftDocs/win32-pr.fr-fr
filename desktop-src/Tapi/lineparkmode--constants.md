---
description: Les \_ constantes d’indicateur de bit LINEPARKMODE décrivent différentes façons de faire des appels de parking.
ms.assetid: 4b182c16-9d58-4244-bc5a-05c393800948
title: Constantes LINEPARKMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef27aaf35f86b02834c93992e8f427c54ffb903
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528945"
---
# <a name="lineparkmode_-constants"></a><span data-ttu-id="29482-103">\_Constantes LINEPARKMODE</span><span class="sxs-lookup"><span data-stu-id="29482-103">LINEPARKMODE\_ Constants</span></span>

<span data-ttu-id="29482-104">Les constantes d’indicateur de bit **LINEPARKMODE \_** décrivent différentes façons de faire des appels de parking.</span><span class="sxs-lookup"><span data-stu-id="29482-104">The **LINEPARKMODE\_** bit-flag constants describe different ways of parking calls.</span></span>

<dl> <dt>

<span data-ttu-id="29482-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE \_ dirigé**</span><span class="sxs-lookup"><span data-stu-id="29482-105"><span id="LINEPARKMODE_DIRECTED"></span><span id="lineparkmode_directed"></span>**LINEPARKMODE\_DIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="29482-106">Spécifie le parc d’appels dirigés.</span><span class="sxs-lookup"><span data-stu-id="29482-106">Specifies directed call park.</span></span> <span data-ttu-id="29482-107">L’adresse à laquelle l’appel doit être parqué doit être fournie au commutateur.</span><span class="sxs-lookup"><span data-stu-id="29482-107">The address where the call is to be parked must be supplied to the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="29482-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE \_ INdirect**</span><span class="sxs-lookup"><span data-stu-id="29482-108"><span id="LINEPARKMODE_NONDIRECTED"></span><span id="lineparkmode_nondirected"></span>**LINEPARKMODE\_NONDIRECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="29482-109">Spécifie un parc d’appels indirect.</span><span class="sxs-lookup"><span data-stu-id="29482-109">Specifies nondirected call park.</span></span> <span data-ttu-id="29482-110">L’adresse où l’appel est parqué est sélectionnée par le commutateur et fournie par le commutateur à l’application.</span><span class="sxs-lookup"><span data-stu-id="29482-110">The address where the call is parked is selected by the switch and provided by the switch to the application.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="29482-111">Notes</span><span class="sxs-lookup"><span data-stu-id="29482-111">Remarks</span></span>

<span data-ttu-id="29482-112">Aucune extensibilité.</span><span class="sxs-lookup"><span data-stu-id="29482-112">No extensibility.</span></span> <span data-ttu-id="29482-113">Tous les 32 bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="29482-113">All 32 bits are reserved.</span></span>

<span data-ttu-id="29482-114">Les **\_ constantes LINEPARKMODE** sont utilisées lors du stationnement d’un appel.</span><span class="sxs-lookup"><span data-stu-id="29482-114">The **LINEPARKMODE\_ constants** are used when parking a call.</span></span> <span data-ttu-id="29482-115">Consultez les fonctionnalités de l’appareil adresse d’une ligne pour savoir quel mode de parc est disponible.</span><span class="sxs-lookup"><span data-stu-id="29482-115">Consult a line's address device capabilities to find out which park mode is available.</span></span>

## <a name="requirements"></a><span data-ttu-id="29482-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29482-116">Requirements</span></span>



| <span data-ttu-id="29482-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29482-117">Requirement</span></span> | <span data-ttu-id="29482-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="29482-118">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="29482-119">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="29482-119">TAPI version</span></span><br/> | <span data-ttu-id="29482-120">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="29482-120">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="29482-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="29482-121">Header</span></span><br/>       | <dl> <span data-ttu-id="29482-122"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="29482-122"><dt>Tapi.h</dt></span></span> </dl> |



 

 




