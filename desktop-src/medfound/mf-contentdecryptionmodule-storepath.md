---
description: Spécifie un chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour l’initialisation.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485217"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a><span data-ttu-id="f9feb-103">MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH, propriété</span><span class="sxs-lookup"><span data-stu-id="f9feb-103">MF\_CONTENTDECRYPTIONMODULE\_STOREPATH property</span></span>

<span data-ttu-id="f9feb-104">Spécifie un chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="f9feb-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>


## <a name="data-type"></a><span data-ttu-id="f9feb-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f9feb-105">Data type</span></span>

<span data-ttu-id="f9feb-106">**LPWStr** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="f9feb-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f9feb-107">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="f9feb-107">Property GUID</span></span>

<span data-ttu-id="f9feb-108">**\_STOREPATH CONTENTDECRYPTIONMODULE \_ MF**</span><span class="sxs-lookup"><span data-stu-id="f9feb-108">**MF\_CONTENTDECRYPTIONMODULE\_STOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="f9feb-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f9feb-109">Property value</span></span>

<span data-ttu-id="f9feb-110">Chemin de fichier représentant un emplacement de stockage que le module de déchiffrement de contenu (CDM) peut utiliser pour l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="f9feb-110">A file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9feb-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f9feb-111">Remarks</span></span>

<span data-ttu-id="f9feb-112">Le chemin d’accès spécifié avec cette propriété sera également utilisé pour les données spécifiques au contenu si la propriété [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="f9feb-112">The path specified with this property will also be used for content-specific data if the [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) property isn't set.</span></span>

<span data-ttu-id="f9feb-113">Pour améliorer les performances de COM, l’application ne doit pas supprimer l’emplacement du magasin après la publication de l’objet CDM.</span><span class="sxs-lookup"><span data-stu-id="f9feb-113">To improve COM performance, the app should not delete the store location after the CDM object has been released.</span></span>



<span data-ttu-id="f9feb-114">Définissez cette propriété lorsque vous créez un CDM en appelant [IMFContentDecryptionModuleAccess :: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="f9feb-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9feb-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9feb-115">Requirements</span></span>



| <span data-ttu-id="f9feb-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9feb-116">Requirement</span></span> | <span data-ttu-id="f9feb-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9feb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9feb-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9feb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f9feb-119">Mise à jour 2020 de Windows 10 avril</span><span class="sxs-lookup"><span data-stu-id="f9feb-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="f9feb-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9feb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9feb-121"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9feb-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9feb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9feb-122">See also</span></span>

- [<span data-ttu-id="f9feb-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f9feb-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="f9feb-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span><span class="sxs-lookup"><span data-stu-id="f9feb-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




