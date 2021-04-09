---
title: Méthode RdvCreateUserDiskTemplate de la classe Win32_RdvhManagement
description: Crée un modèle de disque utilisateur, avec la taille maximale spécifiée, à l’emplacement spécifié.
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RdvCreateUserDiskTemplate
- Services Bureau à distance de la méthode RdvCreateUserDiskTemplate, classe Win32_RdvhManagement
- Win32_RdvhManagement de la classe Services Bureau à distance, méthode RdvCreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743285"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="a4f58-106">Méthode RdvCreateUserDiskTemplate de la \_ classe Win32 RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="a4f58-106">RdvCreateUserDiskTemplate method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="a4f58-107">Crée un modèle de disque utilisateur, avec la taille maximale spécifiée, à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="a4f58-107">Creates a user disk template, with the specified maximum size, at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f58-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a4f58-108">Syntax</span></span>


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="a4f58-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a4f58-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f58-110">*UserDisksStorageUrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4f58-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f58-111">Emplacement du stockage sur disque de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a4f58-111">Location of the user disk storage.</span></span>

</dd> <dt>

<span data-ttu-id="a4f58-112">*UserDiskMaxSizeInGB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a4f58-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f58-113">Taille maximale du disque de l’utilisateur, en Go.</span><span class="sxs-lookup"><span data-stu-id="a4f58-113">Maximum size of the user disk, in GB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f58-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a4f58-114">Return value</span></span>

<span data-ttu-id="a4f58-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="a4f58-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a4f58-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a4f58-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4f58-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a4f58-117">Remarks</span></span>

<span data-ttu-id="a4f58-118">Tous les disques utilisateur créés à l’aide de ce modèle auront la même taille maximale que le modèle.</span><span class="sxs-lookup"><span data-stu-id="a4f58-118">All user disks created using this template will have the same maximum size as the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4f58-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4f58-119">Requirements</span></span>



| <span data-ttu-id="a4f58-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4f58-120">Requirement</span></span> | <span data-ttu-id="a4f58-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4f58-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f58-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4f58-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f58-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4f58-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="a4f58-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4f58-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f58-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a4f58-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="a4f58-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="a4f58-126">Namespace</span></span><br/>                | <span data-ttu-id="a4f58-127">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="a4f58-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="a4f58-128">MOF</span><span class="sxs-lookup"><span data-stu-id="a4f58-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4f58-129"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4f58-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="a4f58-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a4f58-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4f58-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4f58-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4f58-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4f58-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f58-133">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="a4f58-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





