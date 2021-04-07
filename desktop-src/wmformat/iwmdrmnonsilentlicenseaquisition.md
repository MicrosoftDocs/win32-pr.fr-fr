---
title: Interface IWMDRMNonSilentLicenseAquisition
description: L’interface IWMDRMNonSilentLicenseAquisition fournit des méthodes qui permettent d’acquérir une licence nécessitant l’intervention de l’utilisateur. Cette interface peut être obtenue en effectuant une acquisition de licence non silencieuse.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Format Windows Media de l’interface IWMDRMNonSilentLicenseAquisition
- Interface IWMDRMNonSilentLicenseAquisition format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728709"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a><span data-ttu-id="a7c23-105">Interface IWMDRMNonSilentLicenseAquisition</span><span class="sxs-lookup"><span data-stu-id="a7c23-105">IWMDRMNonSilentLicenseAquisition interface</span></span>

<span data-ttu-id="a7c23-106">L’interface **IWMDRMNonSilentLicenseAquisition** fournit des méthodes qui permettent d’acquérir une licence nécessitant l’intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a7c23-106">The **IWMDRMNonSilentLicenseAquisition** interface provides methods that enable license acquisition requiring user intervention.</span></span>

<span data-ttu-id="a7c23-107">Cette interface peut être obtenue en effectuant une acquisition de licence non silencieuse.</span><span class="sxs-lookup"><span data-stu-id="a7c23-107">This interface can be obtained by performing non-silent license acquisition.</span></span> <span data-ttu-id="a7c23-108">Une fois que vous avez appelé [**IWMDRMLicenseManagement :: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , un événement **MEWMDRMLicenseAcquisitionCompleted** est généré.</span><span class="sxs-lookup"><span data-stu-id="a7c23-108">After you call [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) an **MEWMDRMLicenseAcquisitionCompleted** event will be generated.</span></span> <span data-ttu-id="a7c23-109">Appelez la méthode **IMFMediaEvent :: GetValue** de l’événement pour obtenir un pointeur vers une interface **IUnknown** qui peut être interrogée pour obtenir un pointeur vers une instance de cette interface.</span><span class="sxs-lookup"><span data-stu-id="a7c23-109">Call the **IMFMediaEvent::GetValue** method of the event to get a pointer to an **IUnknown** interface that can be queried for a pointer to an instance of this interface.</span></span>

## <a name="members"></a><span data-ttu-id="a7c23-110">Membres</span><span class="sxs-lookup"><span data-stu-id="a7c23-110">Members</span></span>

<span data-ttu-id="a7c23-111">L’interface **IWMDRMNonSilentLicenseAquisition** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a7c23-111">The **IWMDRMNonSilentLicenseAquisition** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a7c23-112">**IWMDRMNonSilentLicenseAquisition** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a7c23-112">**IWMDRMNonSilentLicenseAquisition** also has these types of members:</span></span>

-   [<span data-ttu-id="a7c23-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a7c23-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a7c23-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a7c23-114">Methods</span></span>

<span data-ttu-id="a7c23-115">L’interface **IWMDRMNonSilentLicenseAquisition** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a7c23-115">The **IWMDRMNonSilentLicenseAquisition** interface has these methods.</span></span>



| <span data-ttu-id="a7c23-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="a7c23-116">Method</span></span>                                                                | <span data-ttu-id="a7c23-117">Description</span><span class="sxs-lookup"><span data-stu-id="a7c23-117">Description</span></span>                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7c23-118">**GetChallenge**</span><span class="sxs-lookup"><span data-stu-id="a7c23-118">**GetChallenge**</span></span>](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | <span data-ttu-id="a7c23-119">Récupère le problème de licence qui doit être publié sur le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="a7c23-119">Retrieves the license challenge that should be posted to the license server.</span></span><br/> |
| [<span data-ttu-id="a7c23-120">**GetURL**</span><span class="sxs-lookup"><span data-stu-id="a7c23-120">**GetURL**</span></span>](iwmdrmnonsilentlicenseaquisition-geturl.md)             | <span data-ttu-id="a7c23-121">Récupère l’URL vers laquelle la demande de licence doit être publiée.</span><span class="sxs-lookup"><span data-stu-id="a7c23-121">Retrieves the URL to which the license challenge should be posted.</span></span><br/>           |



 

## <a name="see-also"></a><span data-ttu-id="a7c23-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7c23-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c23-123">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="a7c23-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a7c23-124">**Acquisition de licence non silencieuse**</span><span class="sxs-lookup"><span data-stu-id="a7c23-124">**Non-Silent License Acquisition**</span></span>](non-silent-license-acquisition.md)
</dt> </dl>

 

