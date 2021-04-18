---
title: Méthode EnableUserVhd de la classe Win32_TSSessionDirectory
description: Active un disque dur virtuel de profil utilisateur sur un serveur hôte hôte.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode EnableUserVhd
- Services Bureau à distance de la méthode EnableUserVhd, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode EnableUserVhd
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464e105d2f8f0c80126e6b9ca5e5a383b2d17628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106533574"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="63998-106">Méthode EnableUserVhd de la \_ classe Win32 TSSessionDirectory</span><span class="sxs-lookup"><span data-stu-id="63998-106">EnableUserVhd method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="63998-107">Active un disque dur virtuel de profil utilisateur sur un serveur hôte hôte.</span><span class="sxs-lookup"><span data-stu-id="63998-107">Enables a user profile VHD on an RDSH server.</span></span>

## <a name="syntax"></a><span data-ttu-id="63998-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63998-108">Syntax</span></span>


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a><span data-ttu-id="63998-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63998-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63998-110">*UvhdShareUrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63998-110">*UvhdShareUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63998-111">Emplacement du partage où sont stockés tous les disques durs virtuels de profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63998-111">The location of the share where all user profile VHDs are stored.</span></span>

</dd> <dt>

<span data-ttu-id="63998-112">*UvhdRoamingPolicyXml* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="63998-112">*UvhdRoamingPolicyXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63998-113">Stratégie d’itinérance pour le disque dur virtuel du profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63998-113">The roaming policy for the user profile VHD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63998-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63998-114">Requirements</span></span>



| <span data-ttu-id="63998-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63998-115">Requirement</span></span> | <span data-ttu-id="63998-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="63998-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63998-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63998-117">Minimum supported client</span></span><br/> | <span data-ttu-id="63998-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="63998-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="63998-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63998-119">Minimum supported server</span></span><br/> | <span data-ttu-id="63998-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="63998-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="63998-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="63998-121">Namespace</span></span><br/>                | <span data-ttu-id="63998-122">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="63998-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="63998-123">MOF</span><span class="sxs-lookup"><span data-stu-id="63998-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63998-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63998-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="63998-125">DLL</span><span class="sxs-lookup"><span data-stu-id="63998-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63998-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63998-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63998-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63998-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63998-128">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="63998-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





