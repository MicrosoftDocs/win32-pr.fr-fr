---
description: Contient le CLSID d’un gestionnaire de qualité pour la session multimédia.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: Attribut MF_SESSION_QUALITY_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319638"
---
# <a name="mf_session_quality_manager-attribute"></a><span data-ttu-id="2d14f-103">\_Attribut de \_ Gestionnaire de qualité de session MF \_</span><span class="sxs-lookup"><span data-stu-id="2d14f-103">MF\_SESSION\_QUALITY\_MANAGER attribute</span></span>

<span data-ttu-id="2d14f-104">Contient le CLSID d’un gestionnaire de qualité pour la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="2d14f-104">Contains the CLSID of a quality manager for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="2d14f-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="2d14f-105">Data type</span></span>

<span data-ttu-id="2d14f-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="2d14f-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="2d14f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="2d14f-107">Remarks</span></span>

<span data-ttu-id="2d14f-108">Vous pouvez utiliser cet attribut pour fournir un gestionnaire de qualité personnalisé pour la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="2d14f-108">You can use this attribute to provide a custom quality manager for the Media Session.</span></span>

<span data-ttu-id="2d14f-109">Définissez cet attribut à l’aide du paramètre *pConfiguration* de la fonction [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) ou [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="2d14f-109">Set this attribute by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="2d14f-110">Si cet attribut est défini, la session multimédia appelle **CoCreateInstance** avec le CLSID spécifié pour créer le gestionnaire de qualité.</span><span class="sxs-lookup"><span data-stu-id="2d14f-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID to create the quality manager.</span></span> <span data-ttu-id="2d14f-111">L’objet créé par ce CLSID doit exposer l’interface [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) .</span><span class="sxs-lookup"><span data-stu-id="2d14f-111">The object created by this CLSID must expose the [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) interface.</span></span>

<span data-ttu-id="2d14f-112">Si cet attribut n’est pas défini, la session multimédia crée le gestionnaire de qualité par défaut fourni dans Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="2d14f-112">If this attribute is not set, the Media Session creates the default quality manager provided in Media Foundation.</span></span>

<span data-ttu-id="2d14f-113">Si vous souhaitez exécuter la session multimédia sans le gestionnaire de qualité, définissez cet attribut sur **GUID \_ null**.</span><span class="sxs-lookup"><span data-stu-id="2d14f-113">If you want to run the Media Session with no quality manager at all, set this attribute to **GUID\_NULL**.</span></span>

<span data-ttu-id="2d14f-114">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2d14f-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d14f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d14f-115">Requirements</span></span>



| <span data-ttu-id="2d14f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d14f-116">Requirement</span></span> | <span data-ttu-id="2d14f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d14f-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2d14f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d14f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2d14f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d14f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2d14f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2d14f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2d14f-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2d14f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2d14f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d14f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d14f-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d14f-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d14f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d14f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d14f-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2d14f-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2d14f-126">**IMFAttributes :: GetGUID**</span><span class="sxs-lookup"><span data-stu-id="2d14f-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="2d14f-127">**IMFAttributes :: SetGUID**</span><span class="sxs-lookup"><span data-stu-id="2d14f-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="2d14f-128">Attributs de session multimédia</span><span class="sxs-lookup"><span data-stu-id="2d14f-128">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




