---
description: Fournit une interface de rappel permettant à l’application de recevoir un objet d’activateur de contenu à partir de la session de chemin d’accès multimédia protégée (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: Attribut MF_SESSION_CONTENT_PROTECTION_MANAGER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520636"
---
# <a name="mf_session_content_protection_manager-attribute"></a><span data-ttu-id="34820-103">\_Attribut de \_ Content \_ protection \_ Manager de session MF</span><span class="sxs-lookup"><span data-stu-id="34820-103">MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="34820-104">Fournit une interface de rappel permettant à l’application de recevoir un objet d’activateur de contenu à partir de la session de chemin d’accès multimédia protégée (PMP).</span><span class="sxs-lookup"><span data-stu-id="34820-104">Provides a callback interface for the application to receive a content enabler object from the protected media path (PMP) session.</span></span>

## <a name="data-type"></a><span data-ttu-id="34820-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="34820-105">Data type</span></span>

<span data-ttu-id="34820-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="34820-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="34820-107">Notes</span><span class="sxs-lookup"><span data-stu-id="34820-107">Remarks</span></span>

<span data-ttu-id="34820-108">La valeur de cet attribut est un pointeur vers l’interface [_ *IMFContentProtectionManager* \*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) de l’application.</span><span class="sxs-lookup"><span data-stu-id="34820-108">The value of this attribute is a pointer to the application's [_ *IMFContentProtectionManager*\*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="34820-109">Définissez cet attribut sur la session PMP à l’aide du paramètre *pConfiguration* de la fonction [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="34820-109">Set this attribute on the PMP session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="34820-110">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="34820-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="34820-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34820-111">Requirements</span></span>



| <span data-ttu-id="34820-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34820-112">Requirement</span></span> | <span data-ttu-id="34820-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="34820-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="34820-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34820-114">Minimum supported client</span></span><br/> | <span data-ttu-id="34820-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34820-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="34820-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34820-116">Minimum supported server</span></span><br/> | <span data-ttu-id="34820-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34820-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="34820-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="34820-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="34820-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="34820-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34820-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34820-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34820-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="34820-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="34820-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="34820-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="34820-123">**IMFAttributes :: Setunknown,**</span><span class="sxs-lookup"><span data-stu-id="34820-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="34820-124">Attributs de session multimédia</span><span class="sxs-lookup"><span data-stu-id="34820-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="34820-125">Comment lire des fichiers multimédias protégés</span><span class="sxs-lookup"><span data-stu-id="34820-125">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




