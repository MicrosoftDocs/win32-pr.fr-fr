---
description: Contient le CLSID d’un chargeur de topologie pour la session multimédia.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: Attribut MF_SESSION_TOPOLOADER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536627"
---
# <a name="mf_session_topoloader-attribute"></a><span data-ttu-id="a9298-103">\_Attribut TOPOLOADER de session MF \_</span><span class="sxs-lookup"><span data-stu-id="a9298-103">MF\_SESSION\_TOPOLOADER attribute</span></span>

<span data-ttu-id="a9298-104">Contient le CLSID d’un chargeur de topologie pour la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="a9298-104">Contains the CLSID of a topology loader for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="a9298-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="a9298-105">Data type</span></span>

<span data-ttu-id="a9298-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a9298-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a9298-107">Notes</span><span class="sxs-lookup"><span data-stu-id="a9298-107">Remarks</span></span>

<span data-ttu-id="a9298-108">Vous pouvez utiliser cet attribut pour fournir un chargeur de topologie personnalisé pour la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="a9298-108">You can use this attribute to provide a custom topology loader for the Media Session.</span></span>

<span data-ttu-id="a9298-109">Définissez cet attribut à l’aide du paramètre *pConfiguration* de la fonction [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou de la fonction [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="a9298-109">Set this attribute using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function or the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="a9298-110">Si cet attribut est défini, la session multimédia appelle **CoCreateInstance** avec le CLSID spécifié lors de la création du chargeur de topologie.</span><span class="sxs-lookup"><span data-stu-id="a9298-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID when it creates the topology loader.</span></span> <span data-ttu-id="a9298-111">L’objet créé par ce CLSID doit exposer l’interface [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .</span><span class="sxs-lookup"><span data-stu-id="a9298-111">The object created by this CLSID must expose the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="a9298-112">Si cet attribut n’est pas défini, la session multimédia crée le chargeur de topologie par défaut fourni dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a9298-112">If this attribute is not set, the Media Session creates the default topology loader provided in Media Foundation.</span></span>

<span data-ttu-id="a9298-113">Un chargeur de topologie doit prendre en charge les cloisonnements multithread.</span><span class="sxs-lookup"><span data-stu-id="a9298-113">A topology loader must support multithreaded apartments.</span></span> <span data-ttu-id="a9298-114">Vous devez enregistrer le chargeur de topologie en tant que ThreadingModel = « both ».</span><span class="sxs-lookup"><span data-stu-id="a9298-114">You should register the topology loader as ThreadingModel="Both".</span></span> <span data-ttu-id="a9298-115">En outre, si vous utilisez le chargeur de topologie à l’intérieur du chemin d’accès de média protégé (PMP), le chargeur de topologie doit être un composant approuvé.</span><span class="sxs-lookup"><span data-stu-id="a9298-115">Also, if you are using the topology loader inside the protected media path (PMP), the topology loader must be a trusted component.</span></span> <span data-ttu-id="a9298-116">Pour plus d’informations, consultez [chemin d’accès au média protégé](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="a9298-116">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

<span data-ttu-id="a9298-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="a9298-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9298-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a9298-118">Requirements</span></span>



| <span data-ttu-id="a9298-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a9298-119">Requirement</span></span> | <span data-ttu-id="a9298-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a9298-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a9298-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9298-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a9298-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9298-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a9298-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a9298-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a9298-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a9298-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a9298-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a9298-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9298-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9298-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9298-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a9298-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9298-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9298-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a9298-129">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="a9298-129">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="a9298-130">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="a9298-130">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="a9298-131">Attributs de session multimédia</span><span class="sxs-lookup"><span data-stu-id="a9298-131">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="a9298-132">Chargeurs de topologie personnalisés</span><span class="sxs-lookup"><span data-stu-id="a9298-132">Custom Topology Loaders</span></span>](custom-topology-loaders.md)
</dt> </dl>

 

 




