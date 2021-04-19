---
description: Les \_ constantes d’indicateur de bit LINEADDRESSMODE décrivent les différentes façons d’identifier une adresse sur un appareil de ligne.
ms.assetid: f0f132a0-2e8e-478f-909b-c100aa360daa
title: Constantes LINEADDRESSMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5e926772c82a36865c7f3b95c1ca1321db5682
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523620"
---
# <a name="lineaddressmode_-constants"></a><span data-ttu-id="b8ef9-103">\_Constantes LINEADDRESSMODE</span><span class="sxs-lookup"><span data-stu-id="b8ef9-103">LINEADDRESSMODE\_ Constants</span></span>

<span data-ttu-id="b8ef9-104">Les constantes d’indicateur de bit **LINEADDRESSMODE \_** décrivent les différentes façons d’identifier une adresse sur un appareil de ligne.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-104">The **LINEADDRESSMODE\_** bit-flag constants describe various ways of identifying an address on a line device.</span></span>

<dl> <dt>

<span data-ttu-id="b8ef9-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE \_ ADDRESSID**</span><span class="sxs-lookup"><span data-stu-id="b8ef9-105"><span id="LINEADDRESSMODE_ADDRESSID"></span><span id="lineaddressmode_addressid"></span>**LINEADDRESSMODE\_ADDRESSID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8ef9-106">L’adresse est spécifiée avec un petit entier compris entre 0 et *dwNumAddresses* moins un, où *dwNumAddresses* est la valeur dans les capacités de l’appareil de la ligne.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-106">The address is specified with a small integer in the range 0 to *dwNumAddresses* minus one, where *dwNumAddresses* is the value in the line's device capabilities.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b8ef9-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE \_ DIALABLEADDR**</span><span class="sxs-lookup"><span data-stu-id="b8ef9-107"><span id="LINEADDRESSMODE_DIALABLEADDR"></span><span id="lineaddressmode_dialableaddr"></span>**LINEADDRESSMODE\_DIALABLEADDR**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b8ef9-108">L’adresse est spécifiée par son numéro de téléphone.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-108">The address is specified through its phone number.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b8ef9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b8ef9-109">Remarks</span></span>

<span data-ttu-id="b8ef9-110">Les 16 bits de poids fort peuvent être affectés pour les extensions spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-110">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="b8ef9-111">Les 16 bits de poids faible sont réservés.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-111">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="b8ef9-112">Cette constante est utilisée pour sélectionner une adresse sur une ligne sur laquelle un appel doit être généré.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-112">This constant is used to select an address on a line on which to originate a call.</span></span> <span data-ttu-id="b8ef9-113">Le modèle habituel sélectionne l’adresse à l’aide de son identificateur d’adresse.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-113">The usual model would select the address by means of its address identifier.</span></span> <span data-ttu-id="b8ef9-114">Les identificateurs d’adresse sont le mécanisme utilisé pour identifier les adresses dans l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-114">Address identifiers are the mechanism used to identify addresses throughout TAPI.</span></span> <span data-ttu-id="b8ef9-115">Toutefois, dans certains environnements, lors de la création d’un appel, il est souvent plus pratique d’identifier l’adresse d’origine d’un appel par numéro de téléphone plutôt que par identificateur d’adresse.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-115">However, in some environments, when making a call, it is often more practical to identify a call's originating address by phone number rather than by address identifier.</span></span> <span data-ttu-id="b8ef9-116">Par exemple, la modélisation possible d’un grand nombre de stations (tierces) sur le commutateur à l’aide d’un périphérique de ligne avec de nombreuses adresses.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-116">One example is in the possible modeling of large numbers of stations (third party) on the switch by means of one line device with many addresses.</span></span> <span data-ttu-id="b8ef9-117">La ligne représente l’ensemble de toutes les stations, et chaque station est mappée à une adresse avec son propre numéro de téléphone principal et son identificateur d’adresse.</span><span class="sxs-lookup"><span data-stu-id="b8ef9-117">The line represents the set of all stations, and each station is mapped to an address with its own primary phone number and address identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8ef9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8ef9-118">Requirements</span></span>



| <span data-ttu-id="b8ef9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8ef9-119">Requirement</span></span> | <span data-ttu-id="b8ef9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8ef9-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b8ef9-121">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b8ef9-121">TAPI version</span></span><br/> | <span data-ttu-id="b8ef9-122">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b8ef9-122">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b8ef9-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8ef9-123">Header</span></span><br/>       | <dl> <span data-ttu-id="b8ef9-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ef9-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




