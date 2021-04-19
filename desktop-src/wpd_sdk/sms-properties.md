---
description: Appareils mobiles Windows prend en charge les propriétés SMS suivantes.
ms.assetid: d821f378-522f-4f0a-825b-6b15295e7b12
title: Propriétés de SMS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: c43917c8c26027713b4e5076e8eb3789b95f08e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528461"
---
# <a name="sms-properties"></a><span data-ttu-id="ac56b-103">Propriétés SMS</span><span class="sxs-lookup"><span data-stu-id="ac56b-103">SMS Properties</span></span>

<span data-ttu-id="ac56b-104">Appareils mobiles Windows prend en charge les propriétés SMS suivantes.</span><span class="sxs-lookup"><span data-stu-id="ac56b-104">Windows Portable Devices supports the following SMS properties.</span></span>



| <span data-ttu-id="ac56b-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="ac56b-105">Property</span></span>                   | <span data-ttu-id="ac56b-106">VarType</span><span class="sxs-lookup"><span data-stu-id="ac56b-106">VarType</span></span>        | <span data-ttu-id="ac56b-107">Description</span><span class="sxs-lookup"><span data-stu-id="ac56b-107">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac56b-108">**\_encodage SMS wpd \_**</span><span class="sxs-lookup"><span data-stu-id="ac56b-108">**WPD\_SMS\_ENCODING**</span></span>     | <span data-ttu-id="ac56b-109">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="ac56b-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ac56b-110">Valeur qui spécifie la façon dont le pilote codera le message texte envoyé par le client.</span><span class="sxs-lookup"><span data-stu-id="ac56b-110">A value that specifies how the driver will encode the text message sent by the client.</span></span> <span data-ttu-id="ac56b-111">Il s’agit d’une propriété en lecture seule ; le client ne peut pas spécifier le type de codage utilisé par un appareil pour envoyer des messages.</span><span class="sxs-lookup"><span data-stu-id="ac56b-111">This is a read-only property; the client cannot specify what encoding type a device uses to send messages.</span></span> <span data-ttu-id="ac56b-112">Ces valeurs dupliquent les valeurs énumérées des [**\_ \_ \_ types d’encodage SMS wpd**](wpd-sms-encoding-types.md) .</span><span class="sxs-lookup"><span data-stu-id="ac56b-112">These values duplicate the [**WPD\_SMS\_ENCODING\_TYPES**](wpd-sms-encoding-types.md) enumerated values.</span></span> |
| <span data-ttu-id="ac56b-113">**\_ \_ charge utile max SMS pour wpd \_**</span><span class="sxs-lookup"><span data-stu-id="ac56b-113">**WPD\_SMS\_MAX\_PAYLOAD**</span></span> | <span data-ttu-id="ac56b-114">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="ac56b-114">**VT\_UI4**</span></span>    | <span data-ttu-id="ac56b-115">Nombre maximal d’octets qui peuvent être contenus dans un message.</span><span class="sxs-lookup"><span data-stu-id="ac56b-115">The maximum number of bytes that can be contained in a message.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="ac56b-116">**\_fournisseur SMS \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="ac56b-116">**WPD\_SMS\_PROVIDER**</span></span>     | <span data-ttu-id="ac56b-117">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="ac56b-117">**VT\_LPWSTR**</span></span> | <span data-ttu-id="ac56b-118">Nom du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="ac56b-118">The service provider's name.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ac56b-119">**\_ \_ délai d’expiration du SMS wpd**</span><span class="sxs-lookup"><span data-stu-id="ac56b-119">**WPD\_SMS\_TIMEOUT**</span></span>      | <span data-ttu-id="ac56b-120">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="ac56b-120">**VT\_UI4**</span></span>    | <span data-ttu-id="ac56b-121">Nombre de millisecondes jusqu’à ce qu’un délai d’attente soit retourné.</span><span class="sxs-lookup"><span data-stu-id="ac56b-121">The number of milliseconds until a timeout is returned.</span></span>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="ac56b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac56b-122">Requirements</span></span>



| <span data-ttu-id="ac56b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac56b-123">Requirement</span></span> | <span data-ttu-id="ac56b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac56b-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac56b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac56b-125">Header</span></span><br/> | <dl> <span data-ttu-id="ac56b-126"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac56b-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac56b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac56b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac56b-128">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="ac56b-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




