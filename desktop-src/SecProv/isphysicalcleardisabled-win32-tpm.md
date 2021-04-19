---
description: La méthode IsPhysicalClearDisabled de la \_ classe TPM Win32 indique si seul le propriétaire de l’appareil peut être en mesure d’effacer l’appareil.
ms.assetid: b87f1c4f-8735-45c5-9256-53dbb9579f95
title: Méthode IsPhysicalClearDisabled de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9179aae2f4902ce29e2bab98b4c9c0b793804de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520650"
---
# <a name="isphysicalcleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="c822f-103">Méthode IsPhysicalClearDisabled de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="c822f-103">IsPhysicalClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="c822f-104">La méthode **IsPhysicalClearDisabled** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si seul le propriétaire de l’appareil peut être en mesure d’effacer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c822f-104">The **IsPhysicalClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether only the device owner may be able to clear the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="c822f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c822f-105">Syntax</span></span>


```mof
uint32 IsPhysicalClearDisabled(
  [out] boolean IsPhysicalClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="c822f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c822f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c822f-107">*IsPhysicalClearDisabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c822f-107">*IsPhysicalClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c822f-108">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="c822f-108">Type: **boolean**</span></span>

<span data-ttu-id="c822f-109">Si la **valeur est true**, seul le propriétaire de l’appareil peut effacer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c822f-109">If **true**, only the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c822f-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c822f-110">Return value</span></span>

<span data-ttu-id="c822f-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c822f-111">Type: **uint32**</span></span>

<span data-ttu-id="c822f-112">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="c822f-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="c822f-113">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c822f-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="c822f-114">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c822f-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="c822f-115">Description</span><span class="sxs-lookup"><span data-stu-id="c822f-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c822f-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c822f-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c822f-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="c822f-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c822f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c822f-118">Remarks</span></span>

<span data-ttu-id="c822f-119">Cette valeur est réinitialisée à **false** au début de chaque cycle de démarrage.</span><span class="sxs-lookup"><span data-stu-id="c822f-119">This value is reset to **false** at the beginning of each startup cycle.</span></span>

<span data-ttu-id="c822f-120">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c822f-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c822f-121">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c822f-121">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c822f-122">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c822f-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c822f-123">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c822f-123">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c822f-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c822f-124">Requirements</span></span>



| <span data-ttu-id="c822f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c822f-125">Requirement</span></span> | <span data-ttu-id="c822f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c822f-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c822f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c822f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c822f-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c822f-128">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c822f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c822f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c822f-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c822f-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c822f-131">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c822f-131">Namespace</span></span><br/>                | <span data-ttu-id="c822f-132">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="c822f-132">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="c822f-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c822f-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c822f-134"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="c822f-134"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="c822f-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c822f-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c822f-136"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="c822f-136"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c822f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c822f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c822f-138">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="c822f-138">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
