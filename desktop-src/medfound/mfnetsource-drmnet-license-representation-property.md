---
description: Stocke un tableau d’octets qui représente la licence DRM associée au flux d’octets.
ms.assetid: 866a9706-0b0a-4675-af61-5f55a5a69014
title: MFNETSOURCE_DRMNET_LICENSE_REPRESENTATION, propriété (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92af9a17779381aaed2d2226e17023ca40bc9c1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753125"
---
# <a name="mfnetsource_drmnet_license_representation-property"></a><span data-ttu-id="73124-103">\_Propriété de \_ représentation de licence MFNETSOURCE DRMNET \_</span><span class="sxs-lookup"><span data-stu-id="73124-103">MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION property</span></span>

<span data-ttu-id="73124-104">Stocke un tableau d’octets qui représente la licence DRM associée au flux d’octets.</span><span class="sxs-lookup"><span data-stu-id="73124-104">Stores an array of bytes that represents the DRM license associated with the byte stream.</span></span>



<span data-ttu-id="73124-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="73124-105">Data type</span></span>

<span data-ttu-id="73124-106">Type de PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="73124-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="73124-107">Membre PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="73124-107">PROPVARIANT member</span></span>

<span data-ttu-id="73124-108">Tableau d’octets (**BLOB**)</span><span class="sxs-lookup"><span data-stu-id="73124-108">Byte array (**BLOB**)</span></span>

<span data-ttu-id="73124-109">\_objet BLOB VT</span><span class="sxs-lookup"><span data-stu-id="73124-109">VT\_BLOB</span></span>

<span data-ttu-id="73124-110">**objet BLOB**</span><span class="sxs-lookup"><span data-stu-id="73124-110">**blob**</span></span>



## <a name="remarks"></a><span data-ttu-id="73124-111">Notes</span><span class="sxs-lookup"><span data-stu-id="73124-111">Remarks</span></span>

<span data-ttu-id="73124-112">La **représentation de \_ \_ licence MFNETSOURCE \_ DRMNET** constante définit le GUID de cette clé de propriété.</span><span class="sxs-lookup"><span data-stu-id="73124-112">The constant **MFNETSOURCE\_DRMNET\_LICENSE\_REPRESENTATION** defines the GUID for this property key.</span></span> <span data-ttu-id="73124-113">L’identificateur de propriété (PID) est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="73124-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="73124-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="73124-114">This property is read-only.</span></span> <span data-ttu-id="73124-115">Pour récupérer la valeur de la propriété à partir du flux d’octets réseau, appelez **IPropertyStore :: GetValue** et transmettez la structure **PROPERTYKEY** dans le paramètre *Key* .</span><span class="sxs-lookup"><span data-stu-id="73124-115">To get the property value from the network byte stream, call **IPropertyStore::GetValue** and pass the **PROPERTYKEY** structure in the *key* parameter.</span></span> <span data-ttu-id="73124-116">Le membre **fmtid** de **PROPERTYKEY** doit avoir la valeur GUID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="73124-116">The **fmtid** member of **PROPERTYKEY** must be set to the property GUID.</span></span>

## <a name="requirements"></a><span data-ttu-id="73124-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73124-117">Requirements</span></span>



| <span data-ttu-id="73124-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73124-118">Requirement</span></span> | <span data-ttu-id="73124-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="73124-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73124-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73124-120">Minimum supported client</span></span><br/> | <span data-ttu-id="73124-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73124-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="73124-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="73124-122">Minimum supported server</span></span><br/> | <span data-ttu-id="73124-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="73124-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="73124-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="73124-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="73124-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="73124-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73124-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73124-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73124-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="73124-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="73124-128">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="73124-128">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




