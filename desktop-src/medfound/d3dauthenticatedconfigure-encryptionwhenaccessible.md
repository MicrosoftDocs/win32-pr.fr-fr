---
description: Définit le niveau de chiffrement effectué avant que le contenu protégé soit accessible au processeur ou au bus.
ms.assetid: 6de6c4a3-705a-4420-b9f4-8d4d442b23bf
title: D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_ENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8b624c26c81549372e0e09b4a08ce73f6cd3dd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524591"
---
# <a name="d3dauthenticatedconfigure_encryptionwhenaccessible"></a><span data-ttu-id="991dc-103">D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE</span><span class="sxs-lookup"><span data-stu-id="991dc-103">D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="991dc-104">Définit le niveau de chiffrement effectué avant que le contenu protégé soit accessible au processeur ou au bus.</span><span class="sxs-lookup"><span data-stu-id="991dc-104">Sets the level of encryption that is performed before protected content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="991dc-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="991dc-105">Requirement</span></span> | <span data-ttu-id="991dc-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="991dc-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="991dc-107">GUID de la commande</span><span class="sxs-lookup"><span data-stu-id="991dc-107">Command GUID</span></span> | <span data-ttu-id="991dc-108">**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**</span><span class="sxs-lookup"><span data-stu-id="991dc-108">**D3DAUTHENTICATEDCONFIGURE\_ENCRYPTIONWHENACCESSIBLE**</span></span>                                                                     |
| <span data-ttu-id="991dc-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="991dc-109">Input data</span></span>   | [<span data-ttu-id="991dc-110">**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**</span><span class="sxs-lookup"><span data-stu-id="991dc-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREUNCOMPRESSEDENCRYPTION**</span></span>](d3dauthenticatedchannel-configureuncompressedencryption.md) |



 

## <a name="remarks"></a><span data-ttu-id="991dc-111">Notes</span><span class="sxs-lookup"><span data-stu-id="991dc-111">Remarks</span></span>

<span data-ttu-id="991dc-112">Les types de canaux suivants prennent en charge cette requête :</span><span class="sxs-lookup"><span data-stu-id="991dc-112">The following channel types support this query:</span></span>

-   <span data-ttu-id="991dc-113">**\_Matériel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="991dc-113">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="991dc-114">**\_Logiciel du pilote D3DAUTHENTICATEDCHANNEL \_**</span><span class="sxs-lookup"><span data-stu-id="991dc-114">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="991dc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="991dc-115">Requirements</span></span>



| <span data-ttu-id="991dc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="991dc-116">Requirement</span></span> | <span data-ttu-id="991dc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="991dc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="991dc-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="991dc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="991dc-119">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="991dc-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="991dc-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="991dc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="991dc-121">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="991dc-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="991dc-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="991dc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="991dc-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="991dc-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="991dc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="991dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="991dc-125">Commandes protection du contenu</span><span class="sxs-lookup"><span data-stu-id="991dc-125">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="991dc-126">protection du contenu basé sur GPU</span><span class="sxs-lookup"><span data-stu-id="991dc-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="991dc-127">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="991dc-127">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




