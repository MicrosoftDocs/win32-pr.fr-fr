---
description: Les GUID suivants prennent en charge les implémentations de module de déchiffrement de contenu (CDM).
title: GUID du module de déchiffrement du contenu (CDM)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525241"
---
# <a name="content-decryption-module-cdm-guids"></a><span data-ttu-id="603ff-103">GUID du module de déchiffrement du contenu (CDM)</span><span class="sxs-lookup"><span data-stu-id="603ff-103">Content Decryption Module (CDM) GUIDs</span></span>

<span data-ttu-id="603ff-104">Les GUID suivants prennent en charge les implémentations de module de déchiffrement de contenu (CDM).</span><span class="sxs-lookup"><span data-stu-id="603ff-104">The following GUIDs support Content Decryption Module (CDM) implementations.</span></span>

<span data-ttu-id="603ff-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span><span class="sxs-lookup"><span data-stu-id="603ff-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span></span>

<span data-ttu-id="603ff-106">GUID de service utilisé pour obtenir des interfaces à partir d’une implémentation de [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , telle que l’interface [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) WinRT.</span><span class="sxs-lookup"><span data-stu-id="603ff-106">Service GUID used to obtain interfaces from an [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) implementation,such as the WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) interface.</span></span> <span data-ttu-id="603ff-107">Une implémentation de **IMFContentDecryptionModule** doit implémenter [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) et prendre en charge ce GUID de service.</span><span class="sxs-lookup"><span data-stu-id="603ff-107">An implementation of **IMFContentDecryptionModule** should implement [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) and support this service GUID.</span></span>


## <a name="requirements"></a><span data-ttu-id="603ff-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="603ff-108">Requirements</span></span>



| <span data-ttu-id="603ff-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="603ff-109">Requirement</span></span> | <span data-ttu-id="603ff-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="603ff-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="603ff-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="603ff-111">Header</span></span><br/> | <dl> <span data-ttu-id="603ff-112"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="603ff-112"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="603ff-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="603ff-113">See also</span></span>



- [<span data-ttu-id="603ff-114">Constantes Media Foundation</span><span class="sxs-lookup"><span data-stu-id="603ff-114">Media Foundation Constants</span></span>](media-foundation-constants.md)
- <span data-ttu-id="603ff-115">[IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span><span class="sxs-lookup"><span data-stu-id="603ff-115">[IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span></span>
- [<span data-ttu-id="603ff-116">IMediaProtectionPMPServer</span><span class="sxs-lookup"><span data-stu-id="603ff-116">IMediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [<span data-ttu-id="603ff-117">IMFGetService</span><span class="sxs-lookup"><span data-stu-id="603ff-117">IMFGetService</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




