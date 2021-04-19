---
description: Obtient l’empreinte numérique de la clé racine de stockage pour un module donné de la partie publique de la clé racine de stockage GPC.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Win32_Tpm :: GetSrkADThumbprint, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536327"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a><span data-ttu-id="224a1-103">Win32 \_ TPM :: GetSrkADThumbprint, méthode</span><span class="sxs-lookup"><span data-stu-id="224a1-103">Win32\_Tpm::GetSrkADThumbprint method</span></span>

<span data-ttu-id="224a1-104">Obtient l’empreinte numérique de la clé racine de stockage pour un module donné de la partie publique de la clé racine de stockage GPC.</span><span class="sxs-lookup"><span data-stu-id="224a1-104">Gets the Storage root key thumbprint for a given modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="224a1-105">L’empreinte numérique est utilisée pour indexer les clés de racine de stockage sur le serveur de Active Directory si la sauvegarde Active Directory des informations d’autorisation du propriétaire du module de plateforme sécurisée est activée via le paramètre stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="224a1-105">The thumbprint is used to index the Storage Root Keys on the Active Directory server if the Active Directory backup of TPM owner authorization information is enabled through Group Policy setting.</span></span>

> [!Note]  
> <span data-ttu-id="224a1-106">À partir de Windows 10, version 1607, l’autorisation du propriétaire du module de plateforme sécurisée n’est jamais sauvegardée dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="224a1-106">Beginning with Windows 10, version 1607, the TPM owner authorization is never backed up to Active Directory.</span></span>

 

<span data-ttu-id="224a1-107">Cette méthode est accessible uniquement par les administrateurs locaux.</span><span class="sxs-lookup"><span data-stu-id="224a1-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="224a1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="224a1-108">Syntax</span></span>


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a><span data-ttu-id="224a1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="224a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="224a1-110">*SrkPublicKeyModulus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="224a1-110">*SrkPublicKeyModulus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="224a1-111">Modulo de la partie publique de la clé racine de stockage GPC.</span><span class="sxs-lookup"><span data-stu-id="224a1-111">The modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="224a1-112">Elle peut également être obtenue à l’aide de la méthode [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) de la classe [ \_ TPM Win32](win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="224a1-112">It can also be obtained using the [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) method of the [Win32\_TPM](win32-tpm.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="224a1-113">*SrkADThumbprint* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="224a1-113">*SrkADThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="224a1-114">Retourne un tableau de 20 octets contenant l’empreinte numérique de la clé racine de stockage pour le modulo donné.</span><span class="sxs-lookup"><span data-stu-id="224a1-114">Returns a 20-byte array containing the storage root key thumbprint for the given modulus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="224a1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="224a1-115">Return value</span></span>

<span data-ttu-id="224a1-116">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux [services de base TPM](../tbs/tbs-return-codes.md) , peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="224a1-116">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="224a1-117">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="224a1-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="224a1-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="224a1-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="224a1-119">Description</span><span class="sxs-lookup"><span data-stu-id="224a1-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="224a1-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="224a1-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="224a1-121">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="224a1-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="224a1-122">Notes</span><span class="sxs-lookup"><span data-stu-id="224a1-122">Remarks</span></span>

<span data-ttu-id="224a1-123">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="224a1-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="224a1-124">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="224a1-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="224a1-125">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="224a1-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="224a1-126">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="224a1-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="224a1-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="224a1-127">Requirements</span></span>



| <span data-ttu-id="224a1-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="224a1-128">Requirement</span></span> | <span data-ttu-id="224a1-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="224a1-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="224a1-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="224a1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="224a1-131">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="224a1-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="224a1-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="224a1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="224a1-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="224a1-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="224a1-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="224a1-134">Namespace</span></span><br/>                | <span data-ttu-id="224a1-135">\\\\.\\ racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="224a1-135">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="224a1-136">MOF</span><span class="sxs-lookup"><span data-stu-id="224a1-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="224a1-137"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="224a1-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="224a1-138">DLL</span><span class="sxs-lookup"><span data-stu-id="224a1-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="224a1-139"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="224a1-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="224a1-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="224a1-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="224a1-141">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="224a1-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
