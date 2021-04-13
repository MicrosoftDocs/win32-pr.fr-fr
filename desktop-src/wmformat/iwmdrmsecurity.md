---
title: Interface IWMDRMSecurity
description: L’interface IWMDRMSecurity gère diverses informations relatives à la sécurité pour l’ordinateur client et le sous-système de gestion des droits numériques (DRM). Pour obtenir une instance de cette interface, appelez IWMDRMProvider CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Format Windows Media de l’interface IWMDRMSecurity
- Interface IWMDRMSecurity format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d8b18e56c24fd0f3d3f86f217f547d626b74ded0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312754"
---
# <a name="iwmdrmsecurity-interface"></a><span data-ttu-id="7adc0-105">Interface IWMDRMSecurity</span><span class="sxs-lookup"><span data-stu-id="7adc0-105">IWMDRMSecurity interface</span></span>

<span data-ttu-id="7adc0-106">L’interface **IWMDRMSecurity** gère diverses informations relatives à la sécurité pour l’ordinateur client et le sous-système de gestion des droits numériques (DRM).</span><span class="sxs-lookup"><span data-stu-id="7adc0-106">The **IWMDRMSecurity** interface manages a variety of security-related information for the client computer and digital rights management (DRM) subsystem.</span></span>

<span data-ttu-id="7adc0-107">Pour obtenir une instance de cette interface, appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="7adc0-107">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="7adc0-108">Transmettez **IID \_ IWMDRMSecurity** comme paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="7adc0-108">Pass **IID\_IWMDRMSecurity** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="7adc0-109">Membres</span><span class="sxs-lookup"><span data-stu-id="7adc0-109">Members</span></span>

<span data-ttu-id="7adc0-110">L’interface **IWMDRMSecurity** hérite de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="7adc0-110">The **IWMDRMSecurity** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="7adc0-111">**IWMDRMSecurity** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7adc0-111">**IWMDRMSecurity** also has these types of members:</span></span>

-   [<span data-ttu-id="7adc0-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7adc0-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7adc0-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7adc0-113">Methods</span></span>

<span data-ttu-id="7adc0-114">L’interface **IWMDRMSecurity** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7adc0-114">The **IWMDRMSecurity** interface has these methods.</span></span>



| <span data-ttu-id="7adc0-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="7adc0-115">Method</span></span>                                                                                      | <span data-ttu-id="7adc0-116">Description</span><span class="sxs-lookup"><span data-stu-id="7adc0-116">Description</span></span>                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7adc0-117">**CheckCertForRevocation**</span><span class="sxs-lookup"><span data-stu-id="7adc0-117">**CheckCertForRevocation**</span></span>](iwmdrmsecurity-checkcertforrevocation.md)                     | <span data-ttu-id="7adc0-118">Détermine si un certificat a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="7adc0-118">Determines whether a certificate has been revoked.</span></span><br/>                                                    |
| [<span data-ttu-id="7adc0-119">**GetContentEnablersForRevocations**</span><span class="sxs-lookup"><span data-stu-id="7adc0-119">**GetContentEnablersForRevocations**</span></span>](iwmdrmsecurity-getcontentenablersforrevocations.md) | <span data-ttu-id="7adc0-120">Récupère les interfaces d’activation du contenu qui permettent le renouvellement des composants en fonction de certificats révoqués.</span><span class="sxs-lookup"><span data-stu-id="7adc0-120">Retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span><br/> |
| [<span data-ttu-id="7adc0-121">**GetContentEnablersFromHashes**</span><span class="sxs-lookup"><span data-stu-id="7adc0-121">**GetContentEnablersFromHashes**</span></span>](iwmdrmsecurity-getcontentenablersfromhashes.md)         | <span data-ttu-id="7adc0-122">Récupère les interfaces d’activation du contenu qui permettent le renouvellement des composants en fonction de certificats hachés.</span><span class="sxs-lookup"><span data-stu-id="7adc0-122">Retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span><br/>  |
| [<span data-ttu-id="7adc0-123">**GetMachineCertificate**</span><span class="sxs-lookup"><span data-stu-id="7adc0-123">**GetMachineCertificate**</span></span>](iwmdrmsecurity-getmachinecertificate.md)                       | <span data-ttu-id="7adc0-124">Récupère le certificat de l’ordinateur du sous-système DRM sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="7adc0-124">Retrieves the machine certificate of the DRM subsystem on the client computer.</span></span><br/>                        |
| [<span data-ttu-id="7adc0-125">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="7adc0-125">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)                               | <span data-ttu-id="7adc0-126">Récupère une liste de révocation de certificats à partir du magasin local.</span><span class="sxs-lookup"><span data-stu-id="7adc0-126">Retrieves a certificate revocation list from the local store.</span></span><br/>                                         |
| [<span data-ttu-id="7adc0-127">**GetRevocationDataVersion**</span><span class="sxs-lookup"><span data-stu-id="7adc0-127">**GetRevocationDataVersion**</span></span>](iwmdrmsecurity-getrevocationdataversion.md)                 | <span data-ttu-id="7adc0-128">Récupère le numéro de version d’une liste de révocation de certificats dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="7adc0-128">Retrieves the version number of a certificate revocation list in the local store.</span></span><br/>                     |
| [<span data-ttu-id="7adc0-129">**GetSecurityVersion**</span><span class="sxs-lookup"><span data-stu-id="7adc0-129">**GetSecurityVersion**</span></span>](iwmdrmsecurity-getsecurityversion.md)                             | <span data-ttu-id="7adc0-130">Récupère la version du sous-système DRM sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="7adc0-130">Retrieves the version of the DRM subsystem on the client computer.</span></span><br/>                                    |
| [<span data-ttu-id="7adc0-131">**PerformSecurityUpdate**</span><span class="sxs-lookup"><span data-stu-id="7adc0-131">**PerformSecurityUpdate**</span></span>](iwmdrmsecurity-performsecurityupdate.md)                       | <span data-ttu-id="7adc0-132">Lance une mise à jour de sécurité pour le sous-système DRM sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="7adc0-132">Initiates a security update to the DRM subsystem on the client computer.</span></span><br/>                              |
| [<span data-ttu-id="7adc0-133">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="7adc0-133">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)                               | <span data-ttu-id="7adc0-134">Définit une liste de révocation de certificats dans le magasin local.</span><span class="sxs-lookup"><span data-stu-id="7adc0-134">Sets a certificate revocation list in the local store.</span></span><br/>                                                |



 

## <a name="see-also"></a><span data-ttu-id="7adc0-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7adc0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adc0-136">**Exemple d’individualisation DRM**</span><span class="sxs-lookup"><span data-stu-id="7adc0-136">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="7adc0-137">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="7adc0-137">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="7adc0-138">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="7adc0-138">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





