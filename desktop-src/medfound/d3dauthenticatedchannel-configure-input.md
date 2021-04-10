---
description: 'Contient des données d’entrée pour la méthode IDirect3DAuthenticatedChannel9 :: configure.'
ms.assetid: 7646100e-f768-4935-9e71-1d9db0d69c52
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 82cd60dbb65517beb65a3a7cb413e1d93ac72062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201166"
---
# <a name="d3dauthenticatedchannel_configure_input-structure"></a><span data-ttu-id="3248e-103">D3DAUTHENTICATEDCHANNEL \_ configurer la \_ structure d’entrée</span><span class="sxs-lookup"><span data-stu-id="3248e-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT structure</span></span>

<span data-ttu-id="3248e-104">Contient des données d’entrée pour la méthode [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .</span><span class="sxs-lookup"><span data-stu-id="3248e-104">Contains input data for the [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3248e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3248e-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT {
  D3D_OMAC omac;
  GUID     ConfigureType;
  HANDLE   hChannel;
  UINT     SequenceNumber;
} D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT;
```



## <a name="members"></a><span data-ttu-id="3248e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="3248e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3248e-107">**omac**</span><span class="sxs-lookup"><span data-stu-id="3248e-107">**omac**</span></span>
</dt> <dd>

<span data-ttu-id="3248e-108">Structure [**D3D \_ OMAC**](d3d-omac.md) qui contient un code d’Authentification de message (Mac) des données.</span><span class="sxs-lookup"><span data-stu-id="3248e-108">A [**D3D\_OMAC**](d3d-omac.md) structure that contains a Message Authentication Code (MAC) of the data.</span></span> <span data-ttu-id="3248e-109">Le pilote utilise l’algorithme CBC MAC (OMAC) basé sur AES pour calculer cette valeur pour le bloc de données qui s’affiche après ce membre de la structure.</span><span class="sxs-lookup"><span data-stu-id="3248e-109">The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.</span></span>

</dd> <dt>

<span data-ttu-id="3248e-110">**ConfigureType**</span><span class="sxs-lookup"><span data-stu-id="3248e-110">**ConfigureType**</span></span>
</dt> <dd>

<span data-ttu-id="3248e-111">GUID qui spécifie la commande.</span><span class="sxs-lookup"><span data-stu-id="3248e-111">A GUID that specifies the command.</span></span> <span data-ttu-id="3248e-112">Pour obtenir la liste des valeurs, consultez [protection du contenu des commandes](content-protection-commands.md).</span><span class="sxs-lookup"><span data-stu-id="3248e-112">For a list of values, see [Content Protection Commands](content-protection-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="3248e-113">**hChannel**</span><span class="sxs-lookup"><span data-stu-id="3248e-113">**hChannel**</span></span>
</dt> <dd>

<span data-ttu-id="3248e-114">Handle vers le canal authentifié.</span><span class="sxs-lookup"><span data-stu-id="3248e-114">A handle to the authenticated channel.</span></span> <span data-ttu-id="3248e-115">Pour récupérer le handle, appelez [**IDirect3DDevice9Video :: CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span><span class="sxs-lookup"><span data-stu-id="3248e-115">To get the handle, call [**IDirect3DDevice9Video::CreateAuthenticatedChannel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9video-createauthenticatedchannel).</span></span>

</dd> <dt>

<span data-ttu-id="3248e-116">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="3248e-116">**SequenceNumber**</span></span>
</dt> <dd>

<span data-ttu-id="3248e-117">Numéro de séquence de la requête.</span><span class="sxs-lookup"><span data-stu-id="3248e-117">The query sequence number.</span></span> <span data-ttu-id="3248e-118">Au début de la session, générez un nombre aléatoire 32 bits sécurisé par chiffrement à utiliser comme numéro de séquence de départ.</span><span class="sxs-lookup"><span data-stu-id="3248e-118">At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number.</span></span> <span data-ttu-id="3248e-119">Pour chaque commande, incrémentez le numéro de séquence de 1.</span><span class="sxs-lookup"><span data-stu-id="3248e-119">For each command, increment the sequence number by 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3248e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3248e-120">Requirements</span></span>



| <span data-ttu-id="3248e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3248e-121">Requirement</span></span> | <span data-ttu-id="3248e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="3248e-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3248e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3248e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3248e-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3248e-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3248e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3248e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3248e-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3248e-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3248e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="3248e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3248e-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="3248e-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3248e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3248e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3248e-130">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="3248e-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="3248e-131">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="3248e-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




