---
description: Définit l’identificateur de sécurité racine pour le flux d’octets HTTP Microsoft Media Foundation.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: MFPKEY_HTTP_ByteStream_Urlmon_Security_Id, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528832"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a><span data-ttu-id="0a845-103">MFPKEY \_ http \_ ByteStream \_ urlmon \_ \_ propriété ID de sécurité</span><span class="sxs-lookup"><span data-stu-id="0a845-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Security\_Id property</span></span>

<span data-ttu-id="0a845-104">Définit l’identificateur de sécurité racine pour le flux d’octets HTTP Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0a845-104">Sets the root security identifier for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="0a845-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0a845-105">Data type</span></span>

<span data-ttu-id="0a845-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="0a845-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="0a845-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="0a845-107">PROPVARIANT member</span></span>

<span data-ttu-id="0a845-108">**CAUB**</span><span class="sxs-lookup"><span data-stu-id="0a845-108">**CAUB**</span></span>

<span data-ttu-id="0a845-109">VT \_ UI1 VT Vector \| \_</span><span class="sxs-lookup"><span data-stu-id="0a845-109">VT\_VECTOR \| VT\_UI1</span></span>

<span data-ttu-id="0a845-110">**caub**</span><span class="sxs-lookup"><span data-stu-id="0a845-110">**caub**</span></span>



## <a name="remarks"></a><span data-ttu-id="0a845-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0a845-111">Remarks</span></span>

<span data-ttu-id="0a845-112">Utilisez cette propriété pour configurer le flux d’octets HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="0a845-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="0a845-113">Pour définir la propriété, transmettez un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="0a845-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="0a845-114">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="0a845-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="0a845-115">Cette propriété s’applique uniquement lorsque la propriété [MFPKEY \_ http \_ ByteStream \_ Enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) a la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="0a845-115">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a845-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a845-116">Requirements</span></span>



| <span data-ttu-id="0a845-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a845-117">Requirement</span></span> | <span data-ttu-id="0a845-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a845-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a845-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a845-119">Header</span></span><br/> | <dl> <span data-ttu-id="0a845-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a845-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a845-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a845-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a845-122">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0a845-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
