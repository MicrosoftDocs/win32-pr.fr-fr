---
title: Méthode FileExtensions de la classe Win32_TSApplicationFileExtensions
description: Fournit une liste des extensions de nom de fichier qui sont gérées par une application.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FileExtensions
- Services Bureau à distance de la méthode FileExtensions, classe Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions de la classe Services Bureau à distance, méthode FileExtensions
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942726"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="f3573-106">Méthode FileExtensions de la \_ classe Win32 TSApplicationFileExtensions</span><span class="sxs-lookup"><span data-stu-id="f3573-106">FileExtensions method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="f3573-107">Fournit une liste des extensions de nom de fichier qui sont gérées par une application.</span><span class="sxs-lookup"><span data-stu-id="f3573-107">Provides a list of the file name extensions that are handled by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3573-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3573-108">Syntax</span></span>


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a><span data-ttu-id="f3573-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3573-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3573-110">*Chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3573-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3573-111">Chemin d'accès de l'application.</span><span class="sxs-lookup"><span data-stu-id="f3573-111">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="f3573-112">*Extensions* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f3573-112">*Extensions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3573-113">Extensions de nom de fichier gérées par l’application.</span><span class="sxs-lookup"><span data-stu-id="f3573-113">The file name extensions that are handled by the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f3573-114">Notes</span><span class="sxs-lookup"><span data-stu-id="f3573-114">Remarks</span></span>

<span data-ttu-id="f3573-115">Vous devez être membre du groupe administrateurs pour appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f3573-115">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="f3573-116">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f3573-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f3573-117">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f3573-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f3573-118">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f3573-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f3573-119">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f3573-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f3573-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3573-120">Requirements</span></span>



| <span data-ttu-id="f3573-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3573-121">Requirement</span></span> | <span data-ttu-id="f3573-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3573-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3573-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3573-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f3573-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3573-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f3573-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3573-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f3573-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3573-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3573-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f3573-127">Namespace</span></span><br/>                | <span data-ttu-id="f3573-128">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="f3573-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f3573-129">MOF</span><span class="sxs-lookup"><span data-stu-id="f3573-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3573-130"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3573-130"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="f3573-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f3573-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3573-132"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3573-132"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3573-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3573-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3573-134">**\_TSApplicationFileExtensions Win32**</span><span class="sxs-lookup"><span data-stu-id="f3573-134">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

