---
description: Spécifie un chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour les données spécifiques au contenu.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526901"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a><span data-ttu-id="f44ad-103">MF \_ CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH, propriété</span><span class="sxs-lookup"><span data-stu-id="f44ad-103">MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH property</span></span>

<span data-ttu-id="f44ad-104">Spécifie un chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour les données spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="f44ad-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>


## <a name="data-type"></a><span data-ttu-id="f44ad-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f44ad-105">Data type</span></span>

<span data-ttu-id="f44ad-106">**LPWStr** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="f44ad-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f44ad-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="f44ad-107">Property GUID</span></span>

<span data-ttu-id="f44ad-108">**\_INPRIVATESTOREPATH CONTENTDECRYPTIONMODULE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="f44ad-108">**MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="f44ad-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f44ad-109">Property value</span></span>

<span data-ttu-id="f44ad-110">Chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour les données spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="f44ad-110">A file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>

## <a name="remarks"></a><span data-ttu-id="f44ad-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f44ad-111">Remarks</span></span>

<span data-ttu-id="f44ad-112">L’application doit supprimer l’emplacement du magasin après la libération de l’objet CDM.</span><span class="sxs-lookup"><span data-stu-id="f44ad-112">The app should delete the store location after the CDM object has been released.</span></span>

<span data-ttu-id="f44ad-113">Si cette propriété n’est pas définie, le système utilise le chemin d’accès spécifié avec la propriété [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) pour les données spécifiques au contenu.</span><span class="sxs-lookup"><span data-stu-id="f44ad-113">If this property isn't set, the system will use the path specified with the [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) property for content-specific data.</span></span>

<span data-ttu-id="f44ad-114">Définissez cette propriété lorsque vous créez un CDM en appelant [IMFContentDecryptionModuleAccess :: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="f44ad-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="f44ad-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f44ad-115">Requirements</span></span>



| <span data-ttu-id="f44ad-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f44ad-116">Requirement</span></span> | <span data-ttu-id="f44ad-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f44ad-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f44ad-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f44ad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f44ad-119">Mise à jour 2020 de Windows 10 avril</span><span class="sxs-lookup"><span data-stu-id="f44ad-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="f44ad-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f44ad-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f44ad-121"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="f44ad-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f44ad-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f44ad-122">See also</span></span>

- [<span data-ttu-id="f44ad-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f44ad-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="f44ad-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span><span class="sxs-lookup"><span data-stu-id="f44ad-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




