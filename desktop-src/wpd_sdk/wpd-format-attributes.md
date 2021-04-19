---
description: 'Pour Windows 7, Windows Mobile Devices prend en charge les attributs suivants pour les formats sur un service d’appareil. Ces attributs sont retournés par la méthode IPortableDeviceServiceCapabilities :: GetFormatAttributes.'
ms.assetid: 53282e01-54da-4adf-8a09-2086d6398275
title: Attributs de format (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Format
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 559f731ec7d61007b05e4625ff67488b5ef482fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538119"
---
# <a name="format-attributes"></a><span data-ttu-id="b2206-104">Attributs de format</span><span class="sxs-lookup"><span data-stu-id="b2206-104">Format Attributes</span></span>

<span data-ttu-id="b2206-105">Pour Windows 7, Windows Mobile Devices prend en charge les attributs suivants pour les formats sur un service d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b2206-105">For Windows 7, Windows Portable Devices supports the following attributes for formats on a device service.</span></span> <span data-ttu-id="b2206-106">Ces attributs sont retournés par la méthode [**IPortableDeviceServiceCapabilities :: GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) .</span><span class="sxs-lookup"><span data-stu-id="b2206-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetFormatAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getformatattributes) method.</span></span>




| <span data-ttu-id="b2206-107">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b2206-107">**Attribute**</span></span>                        | <span data-ttu-id="b2206-108">**VarType**</span><span class="sxs-lookup"><span data-stu-id="b2206-108">**VarType**</span></span>    | <span data-ttu-id="b2206-109">**Description**</span><span class="sxs-lookup"><span data-stu-id="b2206-109">**Description**</span></span>                                                                                                           |
|--------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2206-110">**\_attribut de format wpd \_ \_ MimeType**</span><span class="sxs-lookup"><span data-stu-id="b2206-110">**WPD\_FORMAT\_ATTRIBUTE\_MIMETYPE**</span></span> | <span data-ttu-id="b2206-111">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="b2206-111">**VT\_LPWSTR**</span></span> | <span data-ttu-id="b2206-112">Type MIME de format.</span><span class="sxs-lookup"><span data-stu-id="b2206-112">The format MIME type.</span></span>                                                                                                     |
| <span data-ttu-id="b2206-113">**nom de l' \_ attribut de format wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b2206-113">**WPD\_FORMAT\_ATTRIBUTE\_NAME**</span></span>     | <span data-ttu-id="b2206-114">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="b2206-114">**VT\_LPWSTR**</span></span> | <span data-ttu-id="b2206-115">Chaîne qui spécifie le nom convivial du format du script.</span><span class="sxs-lookup"><span data-stu-id="b2206-115">A string that specifies the script-friendly name of the format.</span></span> <span data-ttu-id="b2206-116">Les caractères valides sont alphanumériques \[ a-zA-z0-9 \] et' \_ '.</span><span class="sxs-lookup"><span data-stu-id="b2206-116">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="b2206-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2206-117">Requirements</span></span>



| <span data-ttu-id="b2206-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2206-118">Requirement</span></span> | <span data-ttu-id="b2206-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2206-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2206-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2206-120">Header</span></span><br/> | <dl> <span data-ttu-id="b2206-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2206-121"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2206-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2206-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2206-123">**Propriétés et attributs**</span><span class="sxs-lookup"><span data-stu-id="b2206-123">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




