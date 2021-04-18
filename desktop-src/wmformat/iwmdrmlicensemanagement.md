---
title: Interface IWMDRMLicenseManagement
description: L’interface IWMDRMLicenseManagement fournit des méthodes qui effectuent des opérations générales liées au magasin de licences local. Pour obtenir une instance de cette interface, appelez IWMDRMProvider CreateObject. Transmettez IID \_ IWMDRMLicenseManagement comme paramètre riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Format Windows Media de l’interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312481"
---
# <a name="iwmdrmlicensemanagement-interface"></a><span data-ttu-id="2f50e-106">Interface IWMDRMLicenseManagement</span><span class="sxs-lookup"><span data-stu-id="2f50e-106">IWMDRMLicenseManagement interface</span></span>

<span data-ttu-id="2f50e-107">L’interface **IWMDRMLicenseManagement** fournit des méthodes qui effectuent des opérations générales liées au magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="2f50e-107">The **IWMDRMLicenseManagement** interface provides methods that perform general operations related to the local license store.</span></span>

<span data-ttu-id="2f50e-108">Pour obtenir une instance de cette interface, appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="2f50e-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="2f50e-109">Transmettez **IID \_ IWMDRMLicenseManagement** comme paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="2f50e-109">Pass **IID\_IWMDRMLicenseManagement** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="2f50e-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2f50e-110">Members</span></span>

<span data-ttu-id="2f50e-111">L’interface **IWMDRMLicenseManagement** hérite de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span><span class="sxs-lookup"><span data-stu-id="2f50e-111">The **IWMDRMLicenseManagement** interface inherits from [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md).</span></span> <span data-ttu-id="2f50e-112">**IWMDRMLicenseManagement** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2f50e-112">**IWMDRMLicenseManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="2f50e-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f50e-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2f50e-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f50e-114">Methods</span></span>

<span data-ttu-id="2f50e-115">L’interface **IWMDRMLicenseManagement** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2f50e-115">The **IWMDRMLicenseManagement** interface has these methods.</span></span>



| <span data-ttu-id="2f50e-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="2f50e-116">Method</span></span>                                                                                               | <span data-ttu-id="2f50e-117">Description</span><span class="sxs-lookup"><span data-stu-id="2f50e-117">Description</span></span>                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2f50e-118">**AcquireLicense**</span><span class="sxs-lookup"><span data-stu-id="2f50e-118">**AcquireLicense**</span></span>](iwmdrmlicensemanagement-acquirelicense.md)                                     | <span data-ttu-id="2f50e-119">Acquiert de manière asynchrone une licence à partir d’une URL spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2f50e-119">Asynchronously acquires a license from a specified URL.</span></span><br/>                                                      |
| [<span data-ttu-id="2f50e-120">**BackupLicenses**</span><span class="sxs-lookup"><span data-stu-id="2f50e-120">**BackupLicenses**</span></span>](iwmdrmlicensemanagement-backuplicenses.md)                                     | <span data-ttu-id="2f50e-121">Crée une sauvegarde des licences dans le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="2f50e-121">Creates a backup of the licenses in the local license store.</span></span><br/>                                                 |
| [<span data-ttu-id="2f50e-122">**CleanLicenseStore**</span><span class="sxs-lookup"><span data-stu-id="2f50e-122">**CleanLicenseStore**</span></span>](iwmdrmlicensemanagement-cleanlicensestore.md)                               | <span data-ttu-id="2f50e-123">Supprime les licences marquées du magasin de licences et défragmente le magasin pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="2f50e-123">Removes marked licenses from the license store and defragments the store to improve performance.</span></span><br/>             |
| [<span data-ttu-id="2f50e-124">**CreateLicenseEnumeration**</span><span class="sxs-lookup"><span data-stu-id="2f50e-124">**CreateLicenseEnumeration**</span></span>](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | <span data-ttu-id="2f50e-125">Crée un objet d’énumérateur de licence rempli avec les informations de licence en fonction des valeurs de paramètre.</span><span class="sxs-lookup"><span data-stu-id="2f50e-125">Creates a license enumerator object populated with license information based on parameter values.</span></span><br/>            |
| [<span data-ttu-id="2f50e-126">**CreateLicenseRevocationChallenge**</span><span class="sxs-lookup"><span data-stu-id="2f50e-126">**CreateLicenseRevocationChallenge**</span></span>](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | <span data-ttu-id="2f50e-127">Génère une demande de révocation de licence.</span><span class="sxs-lookup"><span data-stu-id="2f50e-127">Generates a license revocation challenge.</span></span><br/>                                                                    |
| [<span data-ttu-id="2f50e-128">**DeleteLicense**</span><span class="sxs-lookup"><span data-stu-id="2f50e-128">**DeleteLicense**</span></span>](iwmdrmlicensemanagement-deletelicense.md)                                       | <span data-ttu-id="2f50e-129">Supprime une licence du magasin de licences local temporaire.</span><span class="sxs-lookup"><span data-stu-id="2f50e-129">Deletes a license from the temporary local license store.</span></span><br/>                                                    |
| [<span data-ttu-id="2f50e-130">**MonitorLicenseAcquisition**</span><span class="sxs-lookup"><span data-stu-id="2f50e-130">**MonitorLicenseAcquisition**</span></span>](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | <span data-ttu-id="2f50e-131">Lance l’analyse pour un processus d’acquisition de licence.</span><span class="sxs-lookup"><span data-stu-id="2f50e-131">Initiates monitoring for a license acquisition process.</span></span><br/>                                                      |
| [<span data-ttu-id="2f50e-132">**ProcessLicenseDeletionMessage**</span><span class="sxs-lookup"><span data-stu-id="2f50e-132">**ProcessLicenseDeletionMessage**</span></span>](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | <span data-ttu-id="2f50e-133">Supprime une licence importée pour le contenu initialement protégé par un autre système de protection du contenu.</span><span class="sxs-lookup"><span data-stu-id="2f50e-133">Deletes a license that was imported for content originally protected with another content protection system.</span></span><br/> |
| [<span data-ttu-id="2f50e-134">**ProcessLicenseRevocationResponse**</span><span class="sxs-lookup"><span data-stu-id="2f50e-134">**ProcessLicenseRevocationResponse**</span></span>](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | <span data-ttu-id="2f50e-135">Révoque les licences du magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="2f50e-135">Revokes licenses from the local license store.</span></span><br/>                                                               |
| [<span data-ttu-id="2f50e-136">**RestoreLicenses**</span><span class="sxs-lookup"><span data-stu-id="2f50e-136">**RestoreLicenses**</span></span>](iwmdrmlicensemanagement-restorelicenses.md)                                   | <span data-ttu-id="2f50e-137">Restaure les licences précédemment sauvegardées.</span><span class="sxs-lookup"><span data-stu-id="2f50e-137">Restores previously backed up licenses.</span></span><br/>                                                                      |
| [<span data-ttu-id="2f50e-138">**StoreLicense**</span><span class="sxs-lookup"><span data-stu-id="2f50e-138">**StoreLicense**</span></span>](iwmdrmlicensemanagement-storelicense.md)                                         | <span data-ttu-id="2f50e-139">Ajoute une licence au magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="2f50e-139">Adds a license to the local license store.</span></span><br/>                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="2f50e-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f50e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f50e-141">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="2f50e-141">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="2f50e-142">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="2f50e-142">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





