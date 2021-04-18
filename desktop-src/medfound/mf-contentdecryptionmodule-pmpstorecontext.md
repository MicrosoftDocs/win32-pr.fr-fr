---
description: Spécifie une chaîne de contexte utilisée par les implémentations du module de déchiffrement de contenu (CDM) qui utilisent MediaProtectionPMPServer.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543106"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a><span data-ttu-id="e3c93-103">MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT, propriété</span><span class="sxs-lookup"><span data-stu-id="e3c93-103">MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT property</span></span>

<span data-ttu-id="e3c93-104">Spécifie une chaîne de contexte utilisée par les implémentations du module de déchiffrement de contenu (CDM) qui utilisent [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span><span class="sxs-lookup"><span data-stu-id="e3c93-104">Specifies a context string used by Content Decryption Module (CDM) implementations that use [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span></span>


## <a name="data-type"></a><span data-ttu-id="e3c93-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e3c93-105">Data type</span></span>

<span data-ttu-id="e3c93-106">**LPWStr** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="e3c93-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="e3c93-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="e3c93-107">Property GUID</span></span>

<span data-ttu-id="e3c93-108">**\_PMPSTORECONTEXT CONTENTDECRYPTIONMODULE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="e3c93-108">**MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT**</span></span>

## <a name="property-value"></a><span data-ttu-id="e3c93-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e3c93-109">Property value</span></span>

<span data-ttu-id="e3c93-110">Chaîne de contexte utilisée par les implémentations du module de déchiffrement de contenu (CDM).</span><span class="sxs-lookup"><span data-stu-id="e3c93-110">A  a context string used by Content Decryption Module (CDM) implementations.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c93-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e3c93-111">Remarks</span></span>

<span data-ttu-id="e3c93-112">L’implémenteur CDM doit rechercher cette valeur et transmettre la valeur au [constructeur MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) à l’aide du nom de propriété « Windows. Media. protection. PMPStoreContext ».</span><span class="sxs-lookup"><span data-stu-id="e3c93-112">The CDM implementer should look for this value and pass the value to the [MediaProtectionPMPServer constructor](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) using the property name "Windows.Media.Protection.PMPStoreContext".</span></span>


<span data-ttu-id="e3c93-113">Les applications ne doivent pas créer cette propriété lors de l’appel de [IMFContentDecryptionModuleAccess :: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="e3c93-113">Apps should not create this property when calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3c93-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3c93-114">Requirements</span></span>



| <span data-ttu-id="e3c93-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3c93-115">Requirement</span></span> | <span data-ttu-id="e3c93-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3c93-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c93-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3c93-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3c93-118">Mise à jour 2020 de Windows 10 avril</span><span class="sxs-lookup"><span data-stu-id="e3c93-118">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="e3c93-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3c93-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3c93-120"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c93-120"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3c93-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3c93-121">See also</span></span>

- [<span data-ttu-id="e3c93-122">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e3c93-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="e3c93-123">MediaProtectionPMPServer</span><span class="sxs-lookup"><span data-stu-id="e3c93-123">MediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




