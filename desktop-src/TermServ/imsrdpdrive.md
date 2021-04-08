---
title: Interface IMsRdpDrive
description: Contient des informations sur un objet lecteur.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpDrive
- Services Bureau à distance de l’interface IMsRdpDrive, Description
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739989"
---
# <a name="imsrdpdrive-interface"></a><span data-ttu-id="d1a52-105">Interface IMsRdpDrive</span><span class="sxs-lookup"><span data-stu-id="d1a52-105">IMsRdpDrive interface</span></span>

<span data-ttu-id="d1a52-106">Contient des informations sur un objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="d1a52-106">Contains information about a drive object.</span></span>

## <a name="members"></a><span data-ttu-id="d1a52-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d1a52-107">Members</span></span>

<span data-ttu-id="d1a52-108">L’interface **IMsRdpDrive** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="d1a52-108">The **IMsRdpDrive** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="d1a52-109">**IMsRdpDrive** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d1a52-109">**IMsRdpDrive** also has these types of members:</span></span>

-   [<span data-ttu-id="d1a52-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1a52-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1a52-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1a52-111">Properties</span></span>

<span data-ttu-id="d1a52-112">L’interface **IMsRdpDrive** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d1a52-112">The **IMsRdpDrive** interface has these properties.</span></span>



| <span data-ttu-id="d1a52-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="d1a52-113">Property</span></span>                                                            | <span data-ttu-id="d1a52-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d1a52-114">Access type</span></span>           | <span data-ttu-id="d1a52-115">Description</span><span class="sxs-lookup"><span data-stu-id="d1a52-115">Description</span></span>                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [<span data-ttu-id="d1a52-116">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d1a52-116">**Name**</span></span>](imsrdpdrive-name.md)<br/>                         | <span data-ttu-id="d1a52-117">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1a52-117">Read-only</span></span><br/>  | <span data-ttu-id="d1a52-118">Récupère le nom du lecteur.</span><span class="sxs-lookup"><span data-stu-id="d1a52-118">Retrieves the name of the drive.</span></span><br/>              |
| [<span data-ttu-id="d1a52-119">**RedirectionState**</span><span class="sxs-lookup"><span data-stu-id="d1a52-119">**RedirectionState**</span></span>](imsrdpdrive-redirectionstate.md)<br/> | <span data-ttu-id="d1a52-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d1a52-120">Read/write</span></span><br/> | <span data-ttu-id="d1a52-121">Indique l’état de redirection du lecteur.</span><span class="sxs-lookup"><span data-stu-id="d1a52-121">Indicates the redirection state of the drive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d1a52-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1a52-122">Requirements</span></span>



| <span data-ttu-id="d1a52-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1a52-123">Requirement</span></span> | <span data-ttu-id="d1a52-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1a52-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a52-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1a52-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a52-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1a52-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d1a52-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1a52-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a52-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1a52-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d1a52-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d1a52-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1a52-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1a52-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1a52-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d1a52-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1a52-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1a52-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d1a52-133">IID</span><span class="sxs-lookup"><span data-stu-id="d1a52-133">IID</span></span><br/>                      | <span data-ttu-id="d1a52-134">IID \_ IMsRdpDrive est défini en tant que d28b5458-f694-47a8-8e61-40356a767e46</span><span class="sxs-lookup"><span data-stu-id="d1a52-134">IID\_IMsRdpDrive is defined as d28b5458-f694-47a8-8e61-40356a767e46</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="d1a52-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1a52-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a52-136">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="d1a52-136">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="d1a52-137">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="d1a52-137">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

