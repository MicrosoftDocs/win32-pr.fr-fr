---
title: Méthode VerifyHealthMethod de la classe MDM_HealthAttestation
description: Méthode pour informer l’appareil de la préparation d’une demande de vérification du certificat d’intégrité. Voir aussi VerifyHealth.
ms.assetid: f5b11081-c664-4525-8f36-5f17c21e7f22
keywords:
- Méthode VerifyHealthMethod
- Méthode VerifyHealthMethod, classe MDM_HealthAttestation
- Classe MDM_HealthAttestation, méthode VerifyHealthMethod
topic_type:
- apiref
api_name:
- MDM_HealthAttestation.VerifyHealthMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d71d3758059706d4ea598e7012433220feb27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511754"
---
# <a name="verifyhealthmethod-method-of-the-mdm_healthattestation-class"></a><span data-ttu-id="49c6b-107">Méthode VerifyHealthMethod de la \_ classe MDM HealthAttestation</span><span class="sxs-lookup"><span data-stu-id="49c6b-107">VerifyHealthMethod method of the MDM\_HealthAttestation class</span></span>

<span data-ttu-id="49c6b-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="49c6b-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="49c6b-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="49c6b-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="49c6b-110">Méthode pour informer l’appareil de la préparation d’une demande de vérification du certificat d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="49c6b-110">Method to notify the device to prepare a health certificate verification request.</span></span> <span data-ttu-id="49c6b-111">Voir aussi [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span><span class="sxs-lookup"><span data-stu-id="49c6b-111">See also, [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="49c6b-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49c6b-112">Syntax</span></span>


```mof
uint32 VerifyHealthMethod();
```



## <a name="parameters"></a><span data-ttu-id="49c6b-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49c6b-113">Parameters</span></span>

<span data-ttu-id="49c6b-114">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="49c6b-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c6b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49c6b-115">Requirements</span></span>



| <span data-ttu-id="49c6b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49c6b-116">Requirement</span></span> | <span data-ttu-id="49c6b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="49c6b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49c6b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49c6b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="49c6b-119">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="49c6b-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49c6b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="49c6b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="49c6b-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="49c6b-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="49c6b-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="49c6b-122">Namespace</span></span><br/>                | <span data-ttu-id="49c6b-123">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="49c6b-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="49c6b-124">MOF</span><span class="sxs-lookup"><span data-stu-id="49c6b-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49c6b-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49c6b-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="49c6b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="49c6b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49c6b-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49c6b-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49c6b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49c6b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c6b-129">**\_HEALTHATTESTATION MDM**</span><span class="sxs-lookup"><span data-stu-id="49c6b-129">**MDM\_HealthAttestation**</span></span>](mdm-healthattestation.md)
</dt> <dt>

[<span data-ttu-id="49c6b-130">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="49c6b-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

