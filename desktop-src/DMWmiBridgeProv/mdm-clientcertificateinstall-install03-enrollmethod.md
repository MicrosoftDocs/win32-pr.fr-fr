---
title: Méthode EnrollMethod de la classe MDM_ClientCertificateInstall_Install03
description: Déclenche le démarrage de l’inscription de certificat par l’appareil.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Méthode EnrollMethod
- Méthode EnrollMethod, classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, méthode EnrollMethod
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742637"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a><span data-ttu-id="ca473-106">Méthode EnrollMethod de la \_ \_ classe Install03 MDM ClientCertificateInstall</span><span class="sxs-lookup"><span data-stu-id="ca473-106">EnrollMethod method of the MDM\_ClientCertificateInstall\_Install03 class</span></span>

<span data-ttu-id="ca473-107">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="ca473-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="ca473-108">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="ca473-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="ca473-109">Déclenche le démarrage de l’inscription de certificat par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ca473-109">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="ca473-110">L’appareil n’enverra pas de notification au serveur MDM une fois l’inscription du certificat terminée.</span><span class="sxs-lookup"><span data-stu-id="ca473-110">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="ca473-111">Le serveur MDM peut interroger ultérieurement l’appareil pour savoir si un nouveau certificat est ajouté.</span><span class="sxs-lookup"><span data-stu-id="ca473-111">The MDM server could later query the device to find out whether new certificate is added.</span></span> <span data-ttu-id="ca473-112">Voir aussi [**inscrire**](/windows/client-management/mdm/clientcertificateinstall-csp).</span><span class="sxs-lookup"><span data-stu-id="ca473-112">See also, [**Enroll**](/windows/client-management/mdm/clientcertificateinstall-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="ca473-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca473-113">Syntax</span></span>


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a><span data-ttu-id="ca473-114">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca473-114">Parameters</span></span>

<span data-ttu-id="ca473-115">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="ca473-115">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca473-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ca473-116">Return value</span></span>

<span data-ttu-id="ca473-117">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="ca473-117">Required.</span></span> <span data-ttu-id="ca473-118">Déclenche le démarrage de l’inscription de certificat par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ca473-118">Triggers the device to start the certificate enrollment.</span></span> <span data-ttu-id="ca473-119">L’appareil n’enverra pas de notification au serveur MDM une fois l’inscription du certificat terminée.</span><span class="sxs-lookup"><span data-stu-id="ca473-119">The device will not notify MDM server after certificate enrollment is done.</span></span> <span data-ttu-id="ca473-120">Le serveur MDM peut interroger ultérieurement l’appareil pour savoir si un nouveau certificat est ajouté.</span><span class="sxs-lookup"><span data-stu-id="ca473-120">The MDM server could later query the device to find out whether new certificate is added.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca473-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca473-121">Requirements</span></span>



| <span data-ttu-id="ca473-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca473-122">Requirement</span></span> | <span data-ttu-id="ca473-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca473-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca473-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca473-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ca473-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ca473-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca473-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca473-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ca473-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca473-127">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="ca473-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ca473-128">Namespace</span></span><br/>                | <span data-ttu-id="ca473-129">Racine dmmap de gestion des appareils mobiles \\ \\ \\</span><span class="sxs-lookup"><span data-stu-id="ca473-129">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="ca473-130">MOF</span><span class="sxs-lookup"><span data-stu-id="ca473-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca473-131"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca473-131"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca473-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ca473-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca473-133"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca473-133"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca473-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca473-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca473-135">**MDM \_ ClientCertificateInstall \_ Install03**</span><span class="sxs-lookup"><span data-stu-id="ca473-135">**MDM\_ClientCertificateInstall\_Install03**</span></span>](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[<span data-ttu-id="ca473-136">Utilisation de scripts PowerShell avec le fournisseur de pont WMI</span><span class="sxs-lookup"><span data-stu-id="ca473-136">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

