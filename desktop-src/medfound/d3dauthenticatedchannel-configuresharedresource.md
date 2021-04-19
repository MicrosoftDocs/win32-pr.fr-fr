---
description: Contient des données d’entrée pour une \_ commande D3DAUTHENTICATEDCONFIGURE SHAREDRESOURCE.
ms.assetid: bdeb0cc4-90f0-4174-a859-4b3fecb17bab
title: Structure D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 7cbbb1645b232195e1cdb12e859234339ddda287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515389"
---
# <a name="d3dauthenticatedchannel_configuresharedresource-structure"></a><span data-ttu-id="c4d5a-103">D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE, structure</span><span class="sxs-lookup"><span data-stu-id="c4d5a-103">D3DAUTHENTICATEDCHANNEL\_CONFIGURESHAREDRESOURCE structure</span></span>

<span data-ttu-id="c4d5a-104">Contient des données d’entrée pour une commande [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="c4d5a-104">Contains input data for a [**D3DAUTHENTICATEDCONFIGURE\_SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) command.</span></span>

<span data-ttu-id="c4d5a-105">Pour envoyer cette requête, appelez [**IDirect3DAuthenticatedChannel9 :: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span><span class="sxs-lookup"><span data-stu-id="c4d5a-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure).</span></span>

## <a name="syntax"></a><span data-ttu-id="c4d5a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4d5a-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE {
  D3DAUTHENTICATEDCHANNEL_CONFIGURE_INPUT       Parameters;
  D3DAUTHENTICATEDCHANNEL_PROCESSIDENTIFIERTYPE ProcessIdentiferType;
  HANDLE                                        ProcessHandle;
  BOOL                                          AllowAccess;
} D3DAUTHENTICATEDCHANNEL_CONFIGURESHAREDRESOURCE;
```



## <a name="members"></a><span data-ttu-id="c4d5a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c4d5a-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="c4d5a-108">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="c4d5a-108">**Parameters**</span></span>
</dt> <dd>

<span data-ttu-id="c4d5a-109">Un [**D3DAUTHENTICATEDCHANNEL \_ configure une structure \_ d’entrée**](d3dauthenticatedchannel-configure-input.md) qui contient le GUID de la commande et d’autres données.</span><span class="sxs-lookup"><span data-stu-id="c4d5a-109">A [**D3DAUTHENTICATEDCHANNEL\_CONFIGURE\_INPUT**](d3dauthenticatedchannel-configure-input.md) structure that contains the command GUID and other data.</span></span>

</dd> <dt>

<span data-ttu-id="c4d5a-110">**ProcessIdentiferType**</span><span class="sxs-lookup"><span data-stu-id="c4d5a-110">**ProcessIdentiferType**</span></span>
</dt> <dd>

<span data-ttu-id="c4d5a-111">Valeur [**D3DAUTHENTICATEDCHANNEL \_ PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) qui spécifie le type de processus.</span><span class="sxs-lookup"><span data-stu-id="c4d5a-111">A [**D3DAUTHENTICATEDCHANNEL\_PROCESSIDENTIFIERTYPE**](d3dauthenticatedchannel-processidentifiertype.md) value that specifies the type of process.</span></span> <span data-ttu-id="c4d5a-112">Pour spécifier le processus de Gestionnaire de fenêtrage (DWM), affectez la valeur **PROCESSIDTYPE \_ DWM** à ce membre.</span><span class="sxs-lookup"><span data-stu-id="c4d5a-112">To specify the Desktop Window Manager (DWM) process, set this member to **PROCESSIDTYPE\_DWM**.</span></span> <span data-ttu-id="c4d5a-113">Sinon, définissez ce membre sur **\_ handle PROCESSIDTYPE** et définissez le membre **ProcessHandle** sur un handle valide.</span><span class="sxs-lookup"><span data-stu-id="c4d5a-113">Otherwise, set this member to **PROCESSIDTYPE\_HANDLE** and set the **ProcessHandle** member to a valid handle.</span></span>

</dd> <dt>

<span data-ttu-id="c4d5a-114">**ProcessHandle**</span><span class="sxs-lookup"><span data-stu-id="c4d5a-114">**ProcessHandle**</span></span>
</dt> <dd>

<span data-ttu-id="c4d5a-115">Handle de processus.</span><span class="sxs-lookup"><span data-stu-id="c4d5a-115">A process handle.</span></span> <span data-ttu-id="c4d5a-116">Si le membre **ProcessIdentifier** est égal **au \_ descripteur PROCESSTIDTYPE**, le membre **ProcessHandle** spécifie un handle vers un processus.</span><span class="sxs-lookup"><span data-stu-id="c4d5a-116">If the **ProcessIdentifier** member equals **PROCESSTIDTYPE\_HANDLE**, the **ProcessHandle** member specifies a handle to a process.</span></span> <span data-ttu-id="c4d5a-117">Dans le cas contraire, la valeur est ignorée.</span><span class="sxs-lookup"><span data-stu-id="c4d5a-117">Otherwise, the value is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c4d5a-118">**AllowAccess**</span><span class="sxs-lookup"><span data-stu-id="c4d5a-118">**AllowAccess**</span></span>
</dt> <dd>

<span data-ttu-id="c4d5a-119">Si la **valeur est true**, le processus spécifié a accès aux ressources partagées restreintes.</span><span class="sxs-lookup"><span data-stu-id="c4d5a-119">If **TRUE**, the specified process has access to restricted shared resources.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c4d5a-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4d5a-120">Requirements</span></span>



| <span data-ttu-id="c4d5a-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4d5a-121">Requirement</span></span> | <span data-ttu-id="c4d5a-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4d5a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d5a-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4d5a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="c4d5a-124">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4d5a-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c4d5a-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4d5a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="c4d5a-126">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4d5a-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c4d5a-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4d5a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4d5a-128"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4d5a-128"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4d5a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4d5a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d5a-130">Structures vidéo Direct3D</span><span class="sxs-lookup"><span data-stu-id="c4d5a-130">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="c4d5a-131">**IDirect3DAuthenticatedChannel9 :: configure**</span><span class="sxs-lookup"><span data-stu-id="c4d5a-131">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




