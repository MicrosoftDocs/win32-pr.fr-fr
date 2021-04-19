---
description: Spécifie une stratégie de contrôle de plug-in locale.
ms.assetid: 2936F3C9-3BCB-452A-8C03-35D73A200CE2
title: Attribut MF_LOCAL_PLUGIN_CONTROL_POLICY (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd1bdaee17651cebfdc844bb5b6998907b1cd295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535703"
---
# <a name="mf_local_plugin_control_policy-attribute"></a><span data-ttu-id="51ebb-103">\_Attribut de \_ stratégie de contrôle de plug-in local MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="51ebb-103">MF\_LOCAL\_PLUGIN\_CONTROL\_POLICY attribute</span></span>

<span data-ttu-id="51ebb-104">Spécifie une stratégie de contrôle de plug-in locale.</span><span class="sxs-lookup"><span data-stu-id="51ebb-104">Specifies a local plugin control policy.</span></span>

## <a name="data-type"></a><span data-ttu-id="51ebb-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="51ebb-105">Data type</span></span>

<span data-ttu-id="51ebb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="51ebb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="51ebb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="51ebb-107">Remarks</span></span>

<span data-ttu-id="51ebb-108">Affectez à cet attribut l’une des valeurs de la [**\_ stratégie de contrôle du plug-in \_ \_ MF**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) .</span><span class="sxs-lookup"><span data-stu-id="51ebb-108">Set this attribute to one of the [**MF\_PLUGIN\_CONTROL\_POLICY**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_plugin_control_policy) values.</span></span>

<span data-ttu-id="51ebb-109">Cet attribut permet à l’application de spécifier une stratégie locale plus restrictive que la stratégie au niveau du processus configurée par [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).</span><span class="sxs-lookup"><span data-stu-id="51ebb-109">This attributes allows the app to specify a more restrictive local policy than the process-wide policy configured by [**IMFPluginControl**](/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol).</span></span>

## <a name="requirements"></a><span data-ttu-id="51ebb-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51ebb-110">Requirements</span></span>



| <span data-ttu-id="51ebb-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51ebb-111">Requirement</span></span> | <span data-ttu-id="51ebb-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="51ebb-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="51ebb-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51ebb-113">Minimum supported client</span></span><br/> | <span data-ttu-id="51ebb-114">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51ebb-114">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="51ebb-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51ebb-115">Minimum supported server</span></span><br/> | <span data-ttu-id="51ebb-116">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51ebb-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="51ebb-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="51ebb-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="51ebb-118"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="51ebb-118"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51ebb-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51ebb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51ebb-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="51ebb-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="51ebb-121">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="51ebb-121">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




