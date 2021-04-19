---
description: Définit les indicateurs de liaison du moniker pour le flux d’octets HTTP Microsoft Media Foundation.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539574"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a><span data-ttu-id="2a769-103">MFPKEY \_ http \_ ByteStream \_ urlmon \_ - \_ propriété indicateurs de liaison</span><span class="sxs-lookup"><span data-stu-id="2a769-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Bind\_Flags property</span></span>

<span data-ttu-id="2a769-104">Définit les indicateurs de liaison du moniker pour le flux d’octets HTTP Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2a769-104">Sets the moniker binding flags for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="2a769-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2a769-105">Data type</span></span>

<span data-ttu-id="2a769-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="2a769-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2a769-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="2a769-107">PROPVARIANT member</span></span>

<span data-ttu-id="2a769-108">**CORRESPONDANTE**</span><span class="sxs-lookup"><span data-stu-id="2a769-108">**ULONG**</span></span>

<span data-ttu-id="2a769-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="2a769-109">VT\_UI4</span></span>

<span data-ttu-id="2a769-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="2a769-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2a769-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2a769-111">Remarks</span></span>

<span data-ttu-id="2a769-112">Utilisez cette propriété pour configurer le flux d’octets HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2a769-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="2a769-113">Pour définir la propriété, transmettez un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="2a769-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="2a769-114">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2a769-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="2a769-115">La valeur de cette propriété est une opération **or au niveau du** bit de l’énumération **BINDF** .</span><span class="sxs-lookup"><span data-stu-id="2a769-115">The value of this property is a bitwise **OR** of flags from the **BINDF** enumeration.</span></span> <span data-ttu-id="2a769-116">Cette propriété s’applique uniquement lorsque la propriété [MFPKEY \_ http \_ ByteStream \_ Enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) a la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="2a769-116">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a769-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a769-117">Requirements</span></span>



| <span data-ttu-id="2a769-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a769-118">Requirement</span></span> | <span data-ttu-id="2a769-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a769-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a769-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a769-120">Header</span></span><br/> | <dl> <span data-ttu-id="2a769-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a769-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a769-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a769-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a769-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a769-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
