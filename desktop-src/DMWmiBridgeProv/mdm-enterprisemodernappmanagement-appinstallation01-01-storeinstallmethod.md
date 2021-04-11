---
title: Méthode StoreInstallMethod de la classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Méthode permettant d’effectuer l’installation d’une application et d’une licence à partir du Windows Store. Voir aussi StoreInstall.
ms.assetid: 4f8aff47-ad16-4fe5-85be-7ddb55ddff24
keywords:
- Méthode StoreInstallMethod
- Méthode StoreInstallMethod, classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, méthode StoreInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.StoreInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4ae34e8502b7d408a7fb4d96fb9c2c4fadb509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942525"
---
# <a name="storeinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="d0cc4-107">Méthode StoreInstallMethod de la \_ classe EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="d0cc4-107">StoreInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="d0cc4-108">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d0cc4-109">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d0cc4-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d0cc4-110">Méthode permettant d’effectuer l’installation d’une application et d’une licence à partir du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="d0cc4-110">Method to perform an install of an app and a license from the Windows Store.</span></span> <span data-ttu-id="d0cc4-111">Voir aussi [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="d0cc4-111">See also, [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="d0cc4-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0cc4-112">Syntax</span></span>


```mof
uint32 StoreInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="d0cc4-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0cc4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0cc4-114">*param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d0cc4-114">*param* \[in\]</span></span>
<span data-ttu-id="d0cc4-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d0cc4-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d0cc4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0cc4-116">Requirements</span></span>



| <span data-ttu-id="d0cc4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0cc4-117">Requirement</span></span> | <span data-ttu-id="d0cc4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0cc4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0cc4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0cc4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d0cc4-120">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0cc4-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d0cc4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0cc4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d0cc4-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0cc4-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="d0cc4-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d0cc4-123">Namespace</span></span><br/>                | <span data-ttu-id="d0cc4-124">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="d0cc4-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="d0cc4-125">MOF</span><span class="sxs-lookup"><span data-stu-id="d0cc4-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0cc4-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0cc4-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0cc4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="d0cc4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0cc4-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0cc4-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0cc4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0cc4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0cc4-130">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="d0cc4-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="d0cc4-131">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="d0cc4-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

