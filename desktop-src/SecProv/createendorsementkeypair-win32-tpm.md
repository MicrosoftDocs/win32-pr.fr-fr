---
description: Crée une paire de clés de type EK 2048 bits sur le module de plateforme sécurisée.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Méthode CreateEndorsementKeyPair de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525690"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a><span data-ttu-id="a5abc-103">Méthode CreateEndorsementKeyPair de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="a5abc-103">CreateEndorsementKeyPair method of the Win32\_Tpm class</span></span>

<span data-ttu-id="a5abc-104">La méthode **CreateEndorsementKeyPair** de la [**classe \_ TPM Win32**](win32-tpm.md) crée une paire de clés de type EK 2048 bits sur le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="a5abc-104">The **CreateEndorsementKeyPair** method of the [**Win32\_Tpm**](win32-tpm.md) class creates an 2048-bit endorsement key pair on the TPM.</span></span> <span data-ttu-id="a5abc-105">La paire de clés de type EK doit être disponible pour que la méthode [**TakeOwnership**](takeownership-win32-tpm.md) s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="a5abc-105">The endorsement key pair must be available for the [**TakeOwnership**](takeownership-win32-tpm.md) method to run successfully.</span></span> <span data-ttu-id="a5abc-106">Vous pouvez utiliser la méthode [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) pour détecter si la clé de type EK existe déjà sur le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="a5abc-106">You can use the [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) method to detect whether the endorsement key already exists on the TPM.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5abc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5abc-107">Syntax</span></span>


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a><span data-ttu-id="a5abc-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5abc-108">Parameters</span></span>

<span data-ttu-id="a5abc-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="a5abc-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5abc-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a5abc-110">Return value</span></span>

<span data-ttu-id="a5abc-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a5abc-111">Type: **uint32**</span></span>

<span data-ttu-id="a5abc-112">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="a5abc-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="a5abc-113">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="a5abc-113">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="a5abc-114">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a5abc-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="a5abc-115">Description</span><span class="sxs-lookup"><span data-stu-id="a5abc-115">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="a5abc-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="a5abc-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="a5abc-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a5abc-117">The method was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="a5abc-118"><dt> **TPM \_ E \_ désactivé \_ cmd**</dt> <dt>2150105096 (0x80280008)</dt></span><span class="sxs-lookup"><span data-stu-id="a5abc-118"><dt>**TPM\_E\_DISABLED\_CMD** </dt> <dt>2150105096 (0x80280008)</dt></span></span> </dl> | <span data-ttu-id="a5abc-119">Une paire de clés de type EK existe déjà sur ce module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="a5abc-119">An endorsement key pair already exists on this TPM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5abc-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a5abc-120">Remarks</span></span>

<span data-ttu-id="a5abc-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="a5abc-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a5abc-122">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="a5abc-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="a5abc-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="a5abc-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a5abc-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="a5abc-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a5abc-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5abc-125">Requirements</span></span>



| <span data-ttu-id="a5abc-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5abc-126">Requirement</span></span> | <span data-ttu-id="a5abc-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5abc-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5abc-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5abc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a5abc-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5abc-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a5abc-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5abc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a5abc-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5abc-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a5abc-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a5abc-132">Namespace</span></span><br/>                | <span data-ttu-id="a5abc-133">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="a5abc-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="a5abc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="a5abc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a5abc-135"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="a5abc-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="a5abc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a5abc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5abc-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="a5abc-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5abc-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5abc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5abc-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="a5abc-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
