---
title: Méthode CreateUserDiskTemplate de la classe Win32_TSSessionDirectory
description: Crée un modèle de disque utilisateur.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode CreateUserDiskTemplate
- Services Bureau à distance de la méthode CreateUserDiskTemplate, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode CreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103097"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="7264b-106">Méthode CreateUserDiskTemplate de la \_ classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="7264b-106">CreateUserDiskTemplate method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="7264b-107">Crée un modèle de disque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7264b-107">Creates a user disk template.</span></span>

## <a name="syntax"></a><span data-ttu-id="7264b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7264b-108">Syntax</span></span>


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="7264b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7264b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7264b-110">*UserDisksStorageUrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7264b-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7264b-111">Emplacement du partage où sont stockés tous les disques utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7264b-111">The location of the share where all user disks are stored.</span></span>

</dd> <dt>

<span data-ttu-id="7264b-112">*UserDiskMaxSizeInGB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7264b-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7264b-113">Taille maximale en gigaoctets pour tous les disques utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7264b-113">The maximum size in gigabytes, for all user disks.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7264b-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7264b-114">Requirements</span></span>



| <span data-ttu-id="7264b-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7264b-115">Requirement</span></span> | <span data-ttu-id="7264b-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="7264b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7264b-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7264b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7264b-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7264b-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7264b-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7264b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7264b-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7264b-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="7264b-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7264b-121">Namespace</span></span><br/>                | <span data-ttu-id="7264b-122">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="7264b-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7264b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="7264b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7264b-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7264b-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7264b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7264b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7264b-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7264b-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7264b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7264b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7264b-128">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="7264b-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





