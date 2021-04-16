---
title: Interface IWMDRMLicense
description: L’interface IWMDRMLicense représente une liste d’une ou de plusieurs licences.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Format Windows Media de l’interface IWMDRMLicense
- Interface IWMDRMLicense format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463375"
---
# <a name="iwmdrmlicense-interface"></a><span data-ttu-id="34ffb-105">Interface IWMDRMLicense</span><span class="sxs-lookup"><span data-stu-id="34ffb-105">IWMDRMLicense interface</span></span>

<span data-ttu-id="34ffb-106">L’interface **IWMDRMLicense** représente une liste d’une ou de plusieurs licences.</span><span class="sxs-lookup"><span data-stu-id="34ffb-106">The **IWMDRMLicense** interface represents a list of one or more licenses.</span></span>

## <a name="members"></a><span data-ttu-id="34ffb-107">Membres</span><span class="sxs-lookup"><span data-stu-id="34ffb-107">Members</span></span>

<span data-ttu-id="34ffb-108">L’interface **IWMDRMLicense** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="34ffb-108">The **IWMDRMLicense** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="34ffb-109">**IWMDRMLicense** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="34ffb-109">**IWMDRMLicense** also has these types of members:</span></span>

-   [<span data-ttu-id="34ffb-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="34ffb-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="34ffb-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="34ffb-111">Methods</span></span>

<span data-ttu-id="34ffb-112">L’interface **IWMDRMLicense** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="34ffb-112">The **IWMDRMLicense** interface has these methods.</span></span>



| <span data-ttu-id="34ffb-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="34ffb-113">Method</span></span>                                                                                   | <span data-ttu-id="34ffb-114">Description</span><span class="sxs-lookup"><span data-stu-id="34ffb-114">Description</span></span>                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34ffb-115">**CanPersist**</span><span class="sxs-lookup"><span data-stu-id="34ffb-115">**CanPersist**</span></span>](iwmdrmlicense-canpersist.md)                                           | <span data-ttu-id="34ffb-116">Interroge si la licence peut être rendue persistante dans un magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="34ffb-116">Queries whether the license can be persisted on in a local license store.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="34ffb-117">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="34ffb-117">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)                                 | <span data-ttu-id="34ffb-118">Crée un objet déchiffreur à l’aide des paramètres de la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="34ffb-118">Creates a decryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="34ffb-119">**CreateEncryptor**</span><span class="sxs-lookup"><span data-stu-id="34ffb-119">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)                                 | <span data-ttu-id="34ffb-120">Crée un objet chiffreur à l’aide des paramètres de la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="34ffb-120">Creates an encryptor object using the settings of the current license.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="34ffb-121">**CreateSecureDecryptor**</span><span class="sxs-lookup"><span data-stu-id="34ffb-121">**CreateSecureDecryptor**</span></span>](iwmdrmlicense-createsecuredecryptor.md)                     | <span data-ttu-id="34ffb-122">Crée un objet déchiffreur sécurisé.</span><span class="sxs-lookup"><span data-stu-id="34ffb-122">Creates a secure decryptor object.</span></span> <span data-ttu-id="34ffb-123">Le déchiffreur sécurisé diffère du déchiffreur normal en ce sens qu’il déchiffre le contenu, puis le chiffre à nouveau en fonction des paramètres spécifiés dans les paramètres de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="34ffb-123">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span><br/> |
| [<span data-ttu-id="34ffb-124">**GetAnalogVideoRestrictionLevels**</span><span class="sxs-lookup"><span data-stu-id="34ffb-124">**GetAnalogVideoRestrictionLevels**</span></span>](iwmdrmlicense-getanalogvideorestrictionlevels.md) | <span data-ttu-id="34ffb-125">Récupère toutes les restrictions vidéo analogiques définies sur la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="34ffb-125">Retrieves all analog video restrictions set on the current license.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="34ffb-126">**GetInclusionList**</span><span class="sxs-lookup"><span data-stu-id="34ffb-126">**GetInclusionList**</span></span>](iwmdrmlicense-getinclusionlist.md)                               | <span data-ttu-id="34ffb-127">Récupère la liste d’inclusion entière pour la licence ou la chaîne de licences actuelle.</span><span class="sxs-lookup"><span data-stu-id="34ffb-127">Retrieves the entire inclusion list for the current license or license chain.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="34ffb-128">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="34ffb-128">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)                                           | <span data-ttu-id="34ffb-129">Récupère les données de licence en tant que Extensible Markup Language (XML) ou XMR (extensible Media Rights).</span><span class="sxs-lookup"><span data-stu-id="34ffb-129">Retrieves the license as Extensible Markup Language (XML) or Extensible Media Rights (XMR) data.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="34ffb-130">**GetLicenseProperty**</span><span class="sxs-lookup"><span data-stu-id="34ffb-130">**GetLicenseProperty**</span></span>](iwmdrmlicense-getlicenseproperty.md)                           | <span data-ttu-id="34ffb-131">Récupère une propriété de la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="34ffb-131">Retrieves a property from the current license.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="34ffb-132">**GetNext**</span><span class="sxs-lookup"><span data-stu-id="34ffb-132">**GetNext**</span></span>](iwmdrmlicense-getnext.md)                                                 | <span data-ttu-id="34ffb-133">Charge les informations relatives à la licence suivante dans la liste.</span><span class="sxs-lookup"><span data-stu-id="34ffb-133">Loads the information about the next license in the list.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="34ffb-134">**GetOutputProtectionLevels**</span><span class="sxs-lookup"><span data-stu-id="34ffb-134">**GetOutputProtectionLevels**</span></span>](iwmdrmlicense-getoutputprotectionlevels.md)             | <span data-ttu-id="34ffb-135">Récupère des informations sur tous les niveaux de protection de sortie (OPLs) attribués à la licence.</span><span class="sxs-lookup"><span data-stu-id="34ffb-135">Retrieves information about all output protection levels (OPLs) assigned to the license.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="34ffb-136">**PersistLicense**</span><span class="sxs-lookup"><span data-stu-id="34ffb-136">**PersistLicense**</span></span>](iwmdrmlicense-persistlicense.md)                                   | <span data-ttu-id="34ffb-137">Enregistre la licence actuelle à partir du magasin temporaire dans le magasin de licences local permanent.</span><span class="sxs-lookup"><span data-stu-id="34ffb-137">Saves the current license from the temporary store into the permanent local license store.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="34ffb-138">**ResetEnumeration**</span><span class="sxs-lookup"><span data-stu-id="34ffb-138">**ResetEnumeration**</span></span>](iwmdrmlicense-resetenumeration.md)                               | <span data-ttu-id="34ffb-139">Réinitialise la liste de licences à son état d’origine.</span><span class="sxs-lookup"><span data-stu-id="34ffb-139">Resets the license list to its original state.</span></span><br/>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="34ffb-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34ffb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34ffb-141">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="34ffb-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

