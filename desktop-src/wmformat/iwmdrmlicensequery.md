---
title: Interface IWMDRMLicenseQuery
description: L’interface IWMDRMLicenseQuery permet aux applications d’interroger les droits et l’état de licence d’un fichier protégé.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Format Windows Media de l’interface IWMDRMLicenseQuery
- Interface IWMDRMLicenseQuery format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728716"
---
# <a name="iwmdrmlicensequery-interface"></a><span data-ttu-id="4f137-105">Interface IWMDRMLicenseQuery</span><span class="sxs-lookup"><span data-stu-id="4f137-105">IWMDRMLicenseQuery interface</span></span>

<span data-ttu-id="4f137-106">L’interface **IWMDRMLicenseQuery** permet aux applications d’interroger les droits et l’état de licence d’un fichier protégé.</span><span class="sxs-lookup"><span data-stu-id="4f137-106">The **IWMDRMLicenseQuery** interface enables applications to query the rights and license state for a protected file.</span></span> <span data-ttu-id="4f137-107">Cette interface utilise l’ID de clé pour exécuter des requêtes sur le magasin de licences local.</span><span class="sxs-lookup"><span data-stu-id="4f137-107">This interface uses the Key ID to perform queries on the local license store.</span></span>

<span data-ttu-id="4f137-108">Pour obtenir une instance de cette interface, appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md).</span><span class="sxs-lookup"><span data-stu-id="4f137-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="4f137-109">Transmettez **IID \_ IWMDRMLicenseQuery** comme paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="4f137-109">Pass **IID\_IWMDRMLicenseQuery** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="4f137-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4f137-110">Members</span></span>

<span data-ttu-id="4f137-111">L’interface **IWMDRMLicenseQuery** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4f137-111">The **IWMDRMLicenseQuery** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4f137-112">**IWMDRMLicenseQuery** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4f137-112">**IWMDRMLicenseQuery** also has these types of members:</span></span>

-   [<span data-ttu-id="4f137-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4f137-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4f137-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4f137-114">Methods</span></span>

<span data-ttu-id="4f137-115">L’interface **IWMDRMLicenseQuery** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4f137-115">The **IWMDRMLicenseQuery** interface has these methods.</span></span>



| <span data-ttu-id="4f137-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="4f137-116">Method</span></span>                                                                                | <span data-ttu-id="4f137-117">Description</span><span class="sxs-lookup"><span data-stu-id="4f137-117">Description</span></span>                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4f137-118">**QueryActionAllowed**</span><span class="sxs-lookup"><span data-stu-id="4f137-118">**QueryActionAllowed**</span></span>](iwmdrmlicensequery-queryactionallowed.md)                   | <span data-ttu-id="4f137-119">Interroge le magasin de licences local pour obtenir les autorisations nécessaires pour effectuer des actions par ID de clé.</span><span class="sxs-lookup"><span data-stu-id="4f137-119">Queries the local license store for permissions to perform actions by Key ID.</span></span><br/>         |
| [<span data-ttu-id="4f137-120">**QueryLicenseState**</span><span class="sxs-lookup"><span data-stu-id="4f137-120">**QueryLicenseState**</span></span>](iwmdrmlicensequery-querylicensestate.md)                     | <span data-ttu-id="4f137-121">Interroge le magasin de licences local pour obtenir les données d’état de licence par ID de clé et les droits spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4f137-121">Queries the local license store for license state data by Key ID and specific rights.</span></span><br/> |
| [<span data-ttu-id="4f137-122">**SetActionAllowedQueryParams**</span><span class="sxs-lookup"><span data-stu-id="4f137-122">**SetActionAllowedQueryParams**</span></span>](iwmdrmlicensequery-setactionallowedqueryparams.md) | <span data-ttu-id="4f137-123">Définit des paramètres environnementaux pour améliorer la précision des requêtes de licence.</span><span class="sxs-lookup"><span data-stu-id="4f137-123">Sets environmental parameters to improve the accuracy of license queries.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="4f137-124">Notes</span><span class="sxs-lookup"><span data-stu-id="4f137-124">Remarks</span></span>

<span data-ttu-id="4f137-125">Les méthodes de **IWMDRMLicenseQuery** ne fournissent pas d’informations sur les licences individuelles.</span><span class="sxs-lookup"><span data-stu-id="4f137-125">The methods of **IWMDRMLicenseQuery** do not provide information about individual licenses.</span></span> <span data-ttu-id="4f137-126">Au lieu de cela, les données de licence sont agrégées par le sous-système DRM avant le renvoi des résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="4f137-126">Instead, the license data is aggregated by the DRM subsystem before the query results are returned.</span></span>

## <a name="see-also"></a><span data-ttu-id="4f137-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f137-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f137-128">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="4f137-128">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

