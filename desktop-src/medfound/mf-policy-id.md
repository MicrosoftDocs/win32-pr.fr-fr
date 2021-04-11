---
description: Identificateur qui peut être défini sur un IMFOutputPolicy.
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: MF_POLICY_ID (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787195b20980164d7534bccc267781cdbb7510e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042746"
---
# <a name="mf_policy_id-attribute"></a><span data-ttu-id="1915f-103">Attribut d’ID de \_ stratégie MF \_</span><span class="sxs-lookup"><span data-stu-id="1915f-103">MF\_POLICY\_ID attribute</span></span>

<span data-ttu-id="1915f-104">Identificateur qui peut être défini sur un [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy).</span><span class="sxs-lookup"><span data-stu-id="1915f-104">An identifier that can be set on an [IMFOutputPolicy](/windows/win32/api/mfidl/nn-mfidl-imfoutputpolicy).</span></span>

## <a name="data-type"></a><span data-ttu-id="1915f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1915f-105">Data type</span></span>

<span data-ttu-id="1915f-106">**UInt32** (traité comme **bool**)</span><span class="sxs-lookup"><span data-stu-id="1915f-106">**UINT32** (treated as **BOOL**)</span></span>

## <a name="remarks"></a><span data-ttu-id="1915f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1915f-107">Remarks</span></span>

<span data-ttu-id="1915f-108">La valeur peut être reçue à partir de l’événement de média [MEPolicySet](./mepolicyset.md) .</span><span class="sxs-lookup"><span data-stu-id="1915f-108">The value can be recieved from the [MEPolicySet](./mepolicyset.md) media event.</span></span> <span data-ttu-id="1915f-109">Elle est stockée sous la forme d’une charge utile de type **VT_UI4** dans l’événement **MEPolicySet** .</span><span class="sxs-lookup"><span data-stu-id="1915f-109">It is stored as a **VT_UI4** type payload in the **MEPolicySet** event.</span></span>


## <a name="requirements"></a><span data-ttu-id="1915f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1915f-110">Requirements</span></span>



| <span data-ttu-id="1915f-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1915f-111">Requirement</span></span> | <span data-ttu-id="1915f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="1915f-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1915f-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1915f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1915f-114">Mise à jour 2020 de Windows 10 avril</span><span class="sxs-lookup"><span data-stu-id="1915f-114">Windows 10 April 2020 Update</span></span>   <br/>                                      |
| <span data-ttu-id="1915f-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1915f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1915f-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1915f-116">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1915f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="1915f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1915f-118"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1915f-118"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1915f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1915f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1915f-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1915f-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>



 

 
