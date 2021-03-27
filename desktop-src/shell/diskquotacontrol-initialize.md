---
description: Ouvre un volume spécifié et initialise son objet de contrôle de quota.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Iniméthode tialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971959"
---
# <a name="diskquotacontrolinitialize-method"></a><span data-ttu-id="239b3-103">DiskQuotaControl.Iniméthode tialize</span><span class="sxs-lookup"><span data-stu-id="239b3-103">DiskQuotaControl.Initialize method</span></span>

<span data-ttu-id="239b3-104">Ouvre un volume spécifié et initialise son objet de contrôle de quota.</span><span class="sxs-lookup"><span data-stu-id="239b3-104">Opens a specified volume and initializes its quota control object.</span></span>

## <a name="syntax"></a><span data-ttu-id="239b3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="239b3-105">Syntax</span></span>


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a><span data-ttu-id="239b3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="239b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="239b3-107">*sPath*</span><span class="sxs-lookup"><span data-stu-id="239b3-107">*sPath*</span></span> 
</dt> <dd>

<span data-ttu-id="239b3-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="239b3-108">Type: **String**</span></span>

<span data-ttu-id="239b3-109">Valeur de chaîne qui contient le chemin d’accès qualifié complet du volume à initialiser.</span><span class="sxs-lookup"><span data-stu-id="239b3-109">A string value that contains the fully qualified path of the volume to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="239b3-110">*bReadWrite*</span><span class="sxs-lookup"><span data-stu-id="239b3-110">*bReadWrite*</span></span> 
</dt> <dd>

<span data-ttu-id="239b3-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="239b3-111">Type: **Boolean**</span></span>

<span data-ttu-id="239b3-112">Valeur booléenne qui spécifie le mode d’ouverture du volume.</span><span class="sxs-lookup"><span data-stu-id="239b3-112">A Boolean value that specifies how the volume is to be opened.</span></span> <span data-ttu-id="239b3-113">Affectez la valeur **true** à *bReadWrite* pour l’accès en lecture/écriture ou **false** pour l’accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="239b3-113">Set *bReadWrite* to **TRUE** for read/write access or **FALSE** for read-only access.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="239b3-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="239b3-114">Return value</span></span>

<span data-ttu-id="239b3-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="239b3-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="239b3-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="239b3-116">Requirements</span></span>



| <span data-ttu-id="239b3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="239b3-117">Requirement</span></span> | <span data-ttu-id="239b3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="239b3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="239b3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="239b3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="239b3-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="239b3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="239b3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="239b3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="239b3-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="239b3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="239b3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="239b3-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="239b3-124"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="239b3-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="239b3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="239b3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="239b3-126">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="239b3-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




