---
description: Spécifie une liste de chaînes Unicode représentant les fonctionnalités de l’appareil requises par la transformation du capteur.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: Attribut MF_DEVICESTREAM_REQUIRED_CAPABILITIES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113674"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a><span data-ttu-id="5f1ee-103">\_Attribut des \_ fonctionnalités requises DEVICESTREAM \_ MF</span><span class="sxs-lookup"><span data-stu-id="5f1ee-103">MF\_DEVICESTREAM\_REQUIRED\_CAPABILITIES attribute</span></span>

<span data-ttu-id="5f1ee-104">Spécifie une liste de chaînes Unicode représentant les fonctionnalités de l’appareil requises par la transformation du capteur.</span><span class="sxs-lookup"><span data-stu-id="5f1ee-104">Specifies a list of unicode strings representing the device capabilities required by the sensor transform.</span></span>

## <a name="data-type"></a><span data-ttu-id="5f1ee-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5f1ee-105">Data type</span></span>

<span data-ttu-id="5f1ee-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="5f1ee-106">\**WCHAR\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="5f1ee-107">Notes</span><span class="sxs-lookup"><span data-stu-id="5f1ee-107">Remarks</span></span>

<span data-ttu-id="5f1ee-108">Cet attribut est facultatif et n’est requis que si la transformation du capteur accède à une ressource protégée.</span><span class="sxs-lookup"><span data-stu-id="5f1ee-108">This attribute is optional and only required if the sensor transform accesses a protected resource.</span></span> <span data-ttu-id="5f1ee-109">La valeur doit être une liste délimitée par des points-virgules de jetons de chaîne définis dans [_ *DeviceCapability* \*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span><span class="sxs-lookup"><span data-stu-id="5f1ee-109">The value must be a semicolon delimited list of string tokens defined in [_ *DeviceCapability*\*](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f1ee-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f1ee-110">Requirements</span></span>



| <span data-ttu-id="5f1ee-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f1ee-111">Requirement</span></span> | <span data-ttu-id="5f1ee-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f1ee-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f1ee-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f1ee-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5f1ee-114">Applications de bureau Windows 10, version 1703 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f1ee-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5f1ee-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f1ee-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5f1ee-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f1ee-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="5f1ee-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f1ee-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f1ee-118"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f1ee-118"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
