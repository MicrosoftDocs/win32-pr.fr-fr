---
title: Méthode ChangeProductKeyMethod de la classe MDM_WindowsLicensing
description: Cette méthode installe une clé de produit pour les appareils Windows 10 Desktop. Point ne pas redémarrer. Voir aussi ChangeProductKey.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Méthode ChangeProductKeyMethod
- Méthode ChangeProductKeyMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, méthode ChangeProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e00345fb0e23655b457e0540c70289a169c54ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466194"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="a41be-108">Méthode ChangeProductKeyMethod de la \_ classe MDM WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="a41be-108">ChangeProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="a41be-109">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a41be-109">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a41be-110">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a41be-110">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a41be-111">Cette méthode installe une clé de produit pour les appareils Windows 10 Desktop.</span><span class="sxs-lookup"><span data-stu-id="a41be-111">This method installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="a41be-112">Point ne pas redémarrer.</span><span class="sxs-lookup"><span data-stu-id="a41be-112">Dot not reboot.</span></span> <span data-ttu-id="a41be-113">Voir aussi [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)</span><span class="sxs-lookup"><span data-stu-id="a41be-113">See also [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)</span></span>

## <a name="syntax"></a><span data-ttu-id="a41be-114">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a41be-114">Syntax</span></span>


```mof
uint32 ChangeProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="a41be-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a41be-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a41be-116">*param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a41be-116">*param* \[in\]</span></span>
<span data-ttu-id="a41be-117"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a41be-117"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a41be-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a41be-118">Requirements</span></span>



| <span data-ttu-id="a41be-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a41be-119">Requirement</span></span> | <span data-ttu-id="a41be-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a41be-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a41be-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a41be-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a41be-122">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a41be-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a41be-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a41be-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a41be-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a41be-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a41be-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a41be-125">Namespace</span></span><br/>                | <span data-ttu-id="a41be-126">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="a41be-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a41be-127">MOF</span><span class="sxs-lookup"><span data-stu-id="a41be-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a41be-128"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a41be-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a41be-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a41be-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a41be-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a41be-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a41be-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a41be-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a41be-132">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="a41be-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> </dl>

 

