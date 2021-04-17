---
description: 'Contient la réponse à un appel à la méthode IDirect3DAuthenticatedChannel9 :: configure.'
ms.assetid: 6f33d3f7-a883-4aca-a058-b656d745f2b1
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 6c7a029bd73069795b83b0b2a330835782192683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317990"
---
# <a name="d3dauthenticatedchannel_configure_output-structure"></a><span data-ttu-id="c3902-103">D3DAUTHENTICATEDCHANNEL \_ configurer la \_ structure de sortie</span><span class="sxs-lookup"><span data-stu-id="c3902-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_OUTPUT structure</span></span>

<span data-ttu-id="c3902-104">Contient la réponse à un appel à la méthode [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="c3902-104">Contains the response to a call to the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3902-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3902-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
  HRESULT  ReturnCode;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="c3902-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c3902-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3902-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="c3902-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="c3902-108">Structure [**D3D \_ OMAC**](d3d-omac.md) qui contient un code d’Authentification de message (Mac) des données.</span><span class="sxs-lookup"><span data-stu-id="c3902-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="c3902-109">Le pilote utilise l’algorithme CBC MAC (OMAC) basé sur AES pour calculer cette valeur pour le bloc de données qui s’affiche après ce membre de la structure.</span><span class="sxs-lookup"><span data-stu-id="c3902-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="c3902-110">**ConfigureType**</span><span class="sxs-lookup"><span data-stu-id="c3902-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="c3902-111">GUID qui spécifie la commande.</span><span class="sxs-lookup"><span data-stu-id="c3902-111">A GUID that specifies the command.</span></span> <span data-ttu-id="c3902-112">Pour obtenir la liste des valeurs, consultez [protection du contenu des commandes](content-protection-commands.md).</span><span class="sxs-lookup"><span data-stu-id="c3902-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="c3902-113">**hChannel**</span><span class="sxs-lookup"><span data-stu-id="c3902-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="c3902-114">Handle vers le canal authentifié.</span><span class="sxs-lookup"><span data-stu-id="c3902-114">A handle to the authenticated channel.</span></span>

</dd> <dt>

<span data-ttu-id="c3902-115">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="c3902-115">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="c3902-116">Numéro de séquence de la commande.</span><span class="sxs-lookup"><span data-stu-id="c3902-116">The command sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="c3902-117">**ReturnCode**</span><span class="sxs-lookup"><span data-stu-id="c3902-117">**ReturnCode**</span></span>
</dt> <dd>

<span data-ttu-id="c3902-118">Code de résultat de la commande.</span><span class="sxs-lookup"><span data-stu-id="c3902-118">The result code for the command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3902-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c3902-119">Remarks</span></span>

<span data-ttu-id="c3902-120">Pour **les membres** ConfigureType **, hChannel** et , le pilote utilise les mêmes valeurs que celles fournies par l’application dans [**D3DAUTHENTICATEDCHANNEL configurer la structure \_ \_ d’entrée**](d3dauthenticatedchannel-configure-input.md) .</span><span class="sxs-lookup"><span data-stu-id="c3902-120">For the **ConfigureType**, **hChannel**, and **SequenceNumber** members, the driver uses the same values that the application provided in the [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure.</span></span> <span data-ttu-id="c3902-121">L’application doit vérifier que ces valeurs correspondent.</span><span class="sxs-lookup"><span data-stu-id="c3902-121">The application should verify that these values match.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3902-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3902-122">Requirements</span></span>



| <span data-ttu-id="c3902-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3902-123">Requirement</span></span> | <span data-ttu-id="c3902-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3902-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c3902-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3902-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c3902-126">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3902-126">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c3902-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3902-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c3902-128">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3902-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c3902-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3902-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3902-130"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c3902-130"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3902-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3902-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3902-132">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="c3902-132">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="c3902-133">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="c3902-133">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




