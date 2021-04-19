---
description: Effectue un test automatique du module de plateforme sécurisée et retourne le résultat.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Méthode SelfTest de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515626"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a><span data-ttu-id="b397b-103">Méthode SelfTest de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="b397b-103">SelfTest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="b397b-104">La méthode **SelfTest** de la [**classe \_ TPM Win32**](win32-tpm.md) effectue un test automatique du module de plateforme sécurisée et retourne le résultat.</span><span class="sxs-lookup"><span data-stu-id="b397b-104">The **SelfTest** method of the [**Win32\_Tpm**](win32-tpm.md) class performs a self-test of the TPM and returns the result.</span></span>

<span data-ttu-id="b397b-105">Un auto-test TPM s’exécute automatiquement au démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b397b-105">A TPM self-test runs automatically when the computer starts.</span></span>

## <a name="syntax"></a><span data-ttu-id="b397b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b397b-106">Syntax</span></span>


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="b397b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b397b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b397b-108">*SelfTestResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b397b-108">*SelfTestResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b397b-109">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="b397b-109">Type: **uint8\[\]**</span></span>

<span data-ttu-id="b397b-110">Tableau d’octets qui contient le résultat de l’auto-test.</span><span class="sxs-lookup"><span data-stu-id="b397b-110">An array of bytes that contains the self-test result.</span></span> <span data-ttu-id="b397b-111">Le format de ce paramètre est spécifique au fabricant.</span><span class="sxs-lookup"><span data-stu-id="b397b-111">The format of this parameter is manufacturer-specific.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b397b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b397b-112">Return value</span></span>

<span data-ttu-id="b397b-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b397b-113">Type: **uint32**</span></span>

<span data-ttu-id="b397b-114">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="b397b-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="b397b-115">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="b397b-115">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="b397b-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b397b-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="b397b-117">Description</span><span class="sxs-lookup"><span data-stu-id="b397b-117">Description</span></span>                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="b397b-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b397b-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="b397b-119">La méthode a été exécutée avec succès.</span><span class="sxs-lookup"><span data-stu-id="b397b-119">The method ran successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b397b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b397b-120">Remarks</span></span>

<span data-ttu-id="b397b-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="b397b-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b397b-122">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="b397b-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b397b-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="b397b-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b397b-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b397b-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b397b-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b397b-125">Requirements</span></span>



| <span data-ttu-id="b397b-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b397b-126">Requirement</span></span> | <span data-ttu-id="b397b-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b397b-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b397b-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b397b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b397b-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b397b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b397b-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b397b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b397b-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b397b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b397b-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b397b-132">Namespace</span></span><br/>                | <span data-ttu-id="b397b-133">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="b397b-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="b397b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="b397b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b397b-135"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="b397b-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="b397b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b397b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b397b-137"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="b397b-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b397b-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b397b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b397b-139">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="b397b-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
