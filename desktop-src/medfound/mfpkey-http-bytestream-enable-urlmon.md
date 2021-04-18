---
description: Permet à l’Microsoft Media Foundation flux d’octets HTTP d’utiliser des monikers d’URL (également appelé urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: MFPKEY_HTTP_ByteStream_Enable_Urlmon, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525984"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a><span data-ttu-id="2ca17-103">MFPKEY \_ http \_ ByteStream \_ Enable \_ urlmon, propriété</span><span class="sxs-lookup"><span data-stu-id="2ca17-103">MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon property</span></span>

<span data-ttu-id="2ca17-104">Permet à l’Microsoft Media Foundation flux d’octets HTTP d’utiliser des monikers d’URL (également appelé *urlmon*).</span><span class="sxs-lookup"><span data-stu-id="2ca17-104">Enables the Microsoft Media Foundation HTTP byte stream to use URL monikers (also called *Urlmon*).</span></span>



<span data-ttu-id="2ca17-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2ca17-105">Data type</span></span>

<span data-ttu-id="2ca17-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="2ca17-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="2ca17-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="2ca17-107">PROPVARIANT member</span></span>

<span data-ttu-id="2ca17-108">**VARIANT \_ booléen**</span><span class="sxs-lookup"><span data-stu-id="2ca17-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="2ca17-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="2ca17-109">VT\_BOOL</span></span>

<span data-ttu-id="2ca17-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="2ca17-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="2ca17-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2ca17-111">Remarks</span></span>

<span data-ttu-id="2ca17-112">Utilisez cette propriété pour configurer le flux d’octets HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2ca17-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="2ca17-113">Pour définir la propriété, transmettez un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="2ca17-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="2ca17-114">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="2ca17-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="2ca17-115">Si la valeur est **\_ true**, le flux d’octets http utilise urlmon pour le transport http.</span><span class="sxs-lookup"><span data-stu-id="2ca17-115">If the value is **VARIANT\_TRUE**, the HTTP byte stream uses Urlmon for HTTP transport.</span></span> <span data-ttu-id="2ca17-116">Dans le cas contraire, si la valeur est **\_ false**, le flux d’octets utilise WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="2ca17-116">Otherwise, if the value is **VARIANT\_FALSE**, the byte stream uses WinHTTP.</span></span>

<span data-ttu-id="2ca17-117">La valeur par défaut **est \_ true** pour les applications du Windows Store et la **variante \_ false** pour l’application de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="2ca17-117">The default value is **VARIANT\_TRUE** for Windows Store apps and **VARIANT\_FALSE** for Windows desktop application.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ca17-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ca17-118">Requirements</span></span>



| <span data-ttu-id="2ca17-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ca17-119">Requirement</span></span> | <span data-ttu-id="2ca17-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ca17-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2ca17-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="2ca17-121">Header</span></span><br/> | <dl> <span data-ttu-id="2ca17-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ca17-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ca17-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ca17-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ca17-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2ca17-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
