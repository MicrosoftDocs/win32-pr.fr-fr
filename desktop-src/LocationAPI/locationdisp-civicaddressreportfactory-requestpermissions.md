---
description: Ouvre une boîte de dialogue système pour demander l’autorisation de l’utilisateur pour les périphériques avec emplacement.
ms.assetid: b213591a-2830-4979-b532-e71cdef1b994
title: Méthode LocationDisp. CivicAddressReportFactory. RequestPermissions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d027687302c544974d13b1ba50194e8d6003a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320886"
---
# <a name="locationdispcivicaddressreportfactoryrequestpermissions-method"></a><span data-ttu-id="c2c72-103">Méthode LocationDisp. CivicAddressReportFactory. RequestPermissions</span><span class="sxs-lookup"><span data-stu-id="c2c72-103">LocationDisp.CivicAddressReportFactory.RequestPermissions method</span></span>

<span data-ttu-id="c2c72-104">\[Le modèle d’objet d’API emplacement peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="c2c72-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c2c72-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="c2c72-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="c2c72-106">Au lieu de cela, pour accéder à l’emplacement à partir d’un site Web, utilisez l' [API de géolocalisation W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c2c72-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="c2c72-107">Pour accéder à l’emplacement à partir d’une application de bureau, utilisez l’API [**Windows. Devices. géolocalisation**](/uwp/api/Windows.Devices.Geolocation) .\]</span><span class="sxs-lookup"><span data-stu-id="c2c72-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="c2c72-108">Ouvre une boîte de dialogue système pour demander l’autorisation de l’utilisateur pour les périphériques avec emplacement.</span><span class="sxs-lookup"><span data-stu-id="c2c72-108">Opens a system dialog box to request user permission for location-enabled devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2c72-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2c72-109">Syntax</span></span>


```JScript
LocationDisp.CivicAddressReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a><span data-ttu-id="c2c72-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c2c72-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2c72-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="c2c72-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c2c72-112">Ce paramètre n’est pas utilisé et doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="c2c72-112">This parameter is not used and should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2c72-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c2c72-113">Return value</span></span>

<span data-ttu-id="c2c72-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="c2c72-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2c72-115">Notes</span><span class="sxs-lookup"><span data-stu-id="c2c72-115">Remarks</span></span>

<span data-ttu-id="c2c72-116">L’appel est synchrone et l’appelant attend la fermeture de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c2c72-116">The call is synchronous and the caller waits for the dialog box to be closed.</span></span>

> [!Note]  
> <span data-ttu-id="c2c72-117">Si une application s’exécutant en mode protégé, telle qu’un objet d’assistance du navigateur (BHO) pour Internet Explorer, appelle **RequestPermissions** et que l’utilisateur choisit l’option **ne pas activer ce capteur d’emplacement** dans la boîte de dialogue, le fournisseur de localisation n’est pas activé, mais Windows affiche à nouveau la boîte de dialogue si **RequestPermissions** est appelé de nouveau par le même utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c2c72-117">If an application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls **RequestPermissions**, and the user chooses the **Don't enable this location sensor** option in the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if **RequestPermissions** is called again by the same user.</span></span> <span data-ttu-id="c2c72-118">Les applications qui s’exécutent en mode protégé peuvent choisir de ne pas appeler [**RequestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) au démarrage, de sorte que l’utilisateur ne voit pas une boîte de dialogue éventuellement indésirable à chaque démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="c2c72-118">Applications that run in protected mode may choose to not call [**RequestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) on startup so that the user does not see a possibly unwanted dialog box each time the application starts.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c2c72-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="c2c72-119">Examples</span></span>

<span data-ttu-id="c2c72-120">Pour obtenir un exemple d’utilisation de cette méthode, consultez [écoute des événements de rapport d’adresse postale](/uwp/api/Windows.Devices.Geolocation).</span><span class="sxs-lookup"><span data-stu-id="c2c72-120">For an example of how to use this method, see [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="c2c72-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2c72-121">Requirements</span></span>



| <span data-ttu-id="c2c72-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2c72-122">Requirement</span></span> | <span data-ttu-id="c2c72-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2c72-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="c2c72-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2c72-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c2c72-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c2c72-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c2c72-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2c72-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c2c72-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c2c72-127">None supported</span></span><br/>                  |



 

