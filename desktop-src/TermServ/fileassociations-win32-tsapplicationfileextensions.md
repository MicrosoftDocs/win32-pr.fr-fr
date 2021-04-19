---
title: Méthode FileAssociations de la classe Win32_TSApplicationFileExtensions
description: Analyse le registre pour obtenir les associations de fichiers actuelles pour une application.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode FileAssociations
- Services Bureau à distance de la méthode FileAssociations, classe Win32_TSApplicationFileExtensions
- Win32_TSApplicationFileExtensions de la classe Services Bureau à distance, méthode FileAssociations
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536921"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="833db-106">Méthode FileAssociations de la \_ classe Win32 TSApplicationFileExtensions</span><span class="sxs-lookup"><span data-stu-id="833db-106">FileAssociations method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="833db-107">Analyse le registre pour obtenir les associations de fichiers actuelles pour une application.</span><span class="sxs-lookup"><span data-stu-id="833db-107">Scans the registry to get the current file associations for an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="833db-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="833db-108">Syntax</span></span>


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a><span data-ttu-id="833db-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="833db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="833db-110">*Chemin* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="833db-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="833db-111">Spécifie le chemin d’accès à l’application.</span><span class="sxs-lookup"><span data-stu-id="833db-111">Specifies the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="833db-112">*FileAssociations* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="833db-112">*FileAssociations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="833db-113">En cas de réussite, contient les associations de fichiers pour cette application.</span><span class="sxs-lookup"><span data-stu-id="833db-113">On successful completion contains the file associations for this application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="833db-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="833db-114">Requirements</span></span>



| <span data-ttu-id="833db-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="833db-115">Requirement</span></span> | <span data-ttu-id="833db-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="833db-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="833db-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="833db-117">Minimum supported client</span></span><br/> | <span data-ttu-id="833db-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="833db-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="833db-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="833db-119">Minimum supported server</span></span><br/> | <span data-ttu-id="833db-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="833db-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="833db-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="833db-121">Namespace</span></span><br/>                | <span data-ttu-id="833db-122">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="833db-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="833db-123">MOF</span><span class="sxs-lookup"><span data-stu-id="833db-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="833db-124"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="833db-124"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="833db-125">DLL</span><span class="sxs-lookup"><span data-stu-id="833db-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="833db-126"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="833db-126"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="833db-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="833db-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833db-128">**\_TSApplicationFileExtensions Win32**</span><span class="sxs-lookup"><span data-stu-id="833db-128">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> <dt>

[<span data-ttu-id="833db-129">**\_RDFileAssociation Win32**</span><span class="sxs-lookup"><span data-stu-id="833db-129">**Win32\_RDFileAssociation**</span></span>](win32-rdfileassociation.md)
</dt> </dl>

 

 





