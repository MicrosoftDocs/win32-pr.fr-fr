---
title: méthode doWipeMethod de la classe MDM_RemoteWipe
description: Déclenche le démarrage de la réinitialisation à distance par l’appareil.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- méthode doWipeMethod
- méthode doWipeMethod, classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, méthode doWipeMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464354"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a><span data-ttu-id="7ce57-106">méthode doWipeMethod de la \_ classe MDM RemoteWipe</span><span class="sxs-lookup"><span data-stu-id="7ce57-106">doWipeMethod method of the MDM\_RemoteWipe class</span></span>

<span data-ttu-id="7ce57-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="7ce57-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7ce57-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="7ce57-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7ce57-109">Déclenche le démarrage de la réinitialisation à distance par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7ce57-109">Triggers the device to start the remote wipe.</span></span> <span data-ttu-id="7ce57-110">Voir aussi : la [réinitialisation](/windows/client-management/mdm/remotewipe-csp).</span><span class="sxs-lookup"><span data-stu-id="7ce57-110">See also, [doWipe](/windows/client-management/mdm/remotewipe-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ce57-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ce57-111">Syntax</span></span>


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="7ce57-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ce57-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ce57-113">*param* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7ce57-113">*param* \[in\]</span></span>
<span data-ttu-id="7ce57-114"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7ce57-114"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7ce57-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ce57-115">Requirements</span></span>



| <span data-ttu-id="7ce57-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ce57-116">Requirement</span></span> | <span data-ttu-id="7ce57-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ce57-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ce57-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ce57-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7ce57-119">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7ce57-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ce57-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ce57-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7ce57-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ce57-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7ce57-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7ce57-122">Namespace</span></span><br/>                | <span data-ttu-id="7ce57-123">Racine DMMap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="7ce57-123">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="7ce57-124">MOF</span><span class="sxs-lookup"><span data-stu-id="7ce57-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ce57-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ce57-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ce57-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7ce57-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ce57-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ce57-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ce57-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ce57-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ce57-129">**\_REMOTEWIPE MDM**</span><span class="sxs-lookup"><span data-stu-id="7ce57-129">**MDM\_RemoteWipe**</span></span>](mdm-remotewipe.md)
</dt> <dt>

[<span data-ttu-id="7ce57-130">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="7ce57-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

