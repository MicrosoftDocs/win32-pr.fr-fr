---
title: LSLicense, structure
description: Contient des informations sur une licence de Services Bureau à distance spécifique.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la structure LSLicense
- Services Bureau à distance pointeur de structure LPLSLicense
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dcb8551c1d1edfd9486d42df63de9a76fab38433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465123"
---
# <a name="lslicense-structure"></a><span data-ttu-id="20373-105">LSLicense, structure</span><span class="sxs-lookup"><span data-stu-id="20373-105">LSLicense structure</span></span>

<span data-ttu-id="20373-106">Contient des informations sur une licence de Services Bureau à distance spécifique.</span><span class="sxs-lookup"><span data-stu-id="20373-106">Contains information about a specific Remote Desktop Services license.</span></span>

> [!Note]  
> <span data-ttu-id="20373-107">Cette structure n’est définie dans aucun fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="20373-107">This structure is not defined in any header file.</span></span> <span data-ttu-id="20373-108">Pour utiliser cette structure, vous devez la définir vous-même comme indiqué dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="20373-108">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="20373-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20373-109">Syntax</span></span>


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a><span data-ttu-id="20373-110">Membres</span><span class="sxs-lookup"><span data-stu-id="20373-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="20373-111">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="20373-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="20373-112">Version de la licence.</span><span class="sxs-lookup"><span data-stu-id="20373-112">Version of the license.</span></span>

</dd> <dt>

<span data-ttu-id="20373-113">**dwLicenseId**</span><span class="sxs-lookup"><span data-stu-id="20373-113">**dwLicenseId**</span></span>
</dt> <dd>

<span data-ttu-id="20373-114">ID de la licence.</span><span class="sxs-lookup"><span data-stu-id="20373-114">ID of the license.</span></span>

</dd> <dt>

<span data-ttu-id="20373-115">**dwKeyPackId**</span><span class="sxs-lookup"><span data-stu-id="20373-115">**dwKeyPackId**</span></span>
</dt> <dd>

<span data-ttu-id="20373-116">ID du [**LSKeyPack**](lskeypack.md) qui contient la licence.</span><span class="sxs-lookup"><span data-stu-id="20373-116">ID of the [**LSKeyPack**](lskeypack.md) that contains the license.</span></span>

</dd> <dt>

<span data-ttu-id="20373-117">**szHWID**</span><span class="sxs-lookup"><span data-stu-id="20373-117">**szHWID**</span></span>
</dt> <dd>

<span data-ttu-id="20373-118">ID matériel du client Connexion Bureau à distance (RDC) qui a émis la licence.</span><span class="sxs-lookup"><span data-stu-id="20373-118">Hardware ID of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="20373-119">**szMachineName**</span><span class="sxs-lookup"><span data-stu-id="20373-119">**szMachineName**</span></span>
</dt> <dd>

<span data-ttu-id="20373-120">Nom du client Connexion Bureau à distance (RDC) qui a émis la licence.</span><span class="sxs-lookup"><span data-stu-id="20373-120">Name of the Remote Desktop Connection (RDC) client that was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="20373-121">**szUserName**</span><span class="sxs-lookup"><span data-stu-id="20373-121">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="20373-122">Nom de l’utilisateur qui a émis la licence.</span><span class="sxs-lookup"><span data-stu-id="20373-122">Name of the user who was issued the license.</span></span>

</dd> <dt>

<span data-ttu-id="20373-123">**dwCertSerialLicense**</span><span class="sxs-lookup"><span data-stu-id="20373-123">**dwCertSerialLicense**</span></span>
</dt> <dd>

<span data-ttu-id="20373-124">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="20373-124">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="20373-125">**dwLicenseSerialNumber**</span><span class="sxs-lookup"><span data-stu-id="20373-125">**dwLicenseSerialNumber**</span></span>
</dt> <dd>

<span data-ttu-id="20373-126">Numéro de série de la licence.</span><span class="sxs-lookup"><span data-stu-id="20373-126">Serial number of the license.</span></span>

</dd> <dt>

<span data-ttu-id="20373-127">**ftIssueDate**</span><span class="sxs-lookup"><span data-stu-id="20373-127">**ftIssueDate**</span></span>
</dt> <dd>

<span data-ttu-id="20373-128">Date à laquelle la licence a été émise.</span><span class="sxs-lookup"><span data-stu-id="20373-128">Date that the license was issued.</span></span>

</dd> <dt>

<span data-ttu-id="20373-129">**ftExpireDate**</span><span class="sxs-lookup"><span data-stu-id="20373-129">**ftExpireDate**</span></span>
</dt> <dd>

<span data-ttu-id="20373-130">Date d’expiration de la licence.</span><span class="sxs-lookup"><span data-stu-id="20373-130">Date that the license will expire.</span></span>

</dd> <dt>

<span data-ttu-id="20373-131">**ucLicenseStatus**</span><span class="sxs-lookup"><span data-stu-id="20373-131">**ucLicenseStatus**</span></span>
</dt> <dd>

<span data-ttu-id="20373-132">État actuel de la licence.</span><span class="sxs-lookup"><span data-stu-id="20373-132">Current status of the license.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="20373-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="20373-133">Requirements</span></span>



| <span data-ttu-id="20373-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="20373-134">Requirement</span></span> | <span data-ttu-id="20373-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="20373-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="20373-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20373-136">Minimum supported client</span></span><br/> | <span data-ttu-id="20373-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="20373-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="20373-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="20373-138">Minimum supported server</span></span><br/> | <span data-ttu-id="20373-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="20373-139">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="20373-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="20373-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20373-141">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="20373-141">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="20373-142">**TLSLicenseEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="20373-142">**TLSLicenseEnumBegin**</span></span>](tlslicenseenumbegin.md)
</dt> <dt>

[<span data-ttu-id="20373-143">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="20373-143">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="20373-144">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="20373-144">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

 





