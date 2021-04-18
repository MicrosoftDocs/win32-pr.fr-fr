---
description: Définit une fenêtre pour le flux d’octets HTTP Microsoft Media Foundation.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: MFPKEY_HTTP_ByteStream_Urlmon_Window, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526656"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a><span data-ttu-id="20a5c-103">MFPKEY \_ http \_ ByteStream \_ urlmon, propriété de la \_ fenêtre</span><span class="sxs-lookup"><span data-stu-id="20a5c-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Window property</span></span>

<span data-ttu-id="20a5c-104">Définit une fenêtre pour le flux d’octets HTTP Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="20a5c-104">Sets a window for the Microsoft Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="20a5c-105">La fenêtre est utilisée pour présenter des informations dans l’interface utilisateur pendant une opération de liaison.</span><span class="sxs-lookup"><span data-stu-id="20a5c-105">The window is used to present information in the user interface during a bind operation.</span></span>



<span data-ttu-id="20a5c-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="20a5c-106">Data type</span></span>

<span data-ttu-id="20a5c-107">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="20a5c-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="20a5c-108">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="20a5c-108">PROPVARIANT member</span></span>

<span data-ttu-id="20a5c-109">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="20a5c-109">**IUnknown\***</span></span>

<span data-ttu-id="20a5c-110">VT \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="20a5c-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="20a5c-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="20a5c-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="20a5c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="20a5c-112">Remarks</span></span>

<span data-ttu-id="20a5c-113">Utilisez cette propriété pour configurer le flux d’octets HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="20a5c-113">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="20a5c-114">Pour définir la propriété, transmettez un pointeur [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) au programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="20a5c-114">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="20a5c-115">Pour plus d’informations, consultez [configuration d’une source de média](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="20a5c-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="20a5c-116">La valeur de cette propriété est un pointeur vers l’interface **IWindowForBindingUI** .</span><span class="sxs-lookup"><span data-stu-id="20a5c-116">The value of this property is a pointer to the **IWindowForBindingUI** interface.</span></span> <span data-ttu-id="20a5c-117">Cette propriété s’applique uniquement lorsque la propriété [MFPKEY \_ http \_ ByteStream \_ Enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) a la valeur **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="20a5c-117">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="20a5c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20a5c-118">Requirements</span></span>



| <span data-ttu-id="20a5c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20a5c-119">Requirement</span></span> | <span data-ttu-id="20a5c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="20a5c-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="20a5c-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="20a5c-121">Header</span></span><br/> | <dl> <span data-ttu-id="20a5c-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="20a5c-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20a5c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20a5c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a5c-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20a5c-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
