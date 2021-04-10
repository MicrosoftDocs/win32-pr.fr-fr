---
title: Méthode GetIcon de la classe Win32_TSGetIcon
description: Retourne le contenu de l’icône spécifiée.
ms.assetid: 9448181c-27b8-40eb-9369-8abe1422243b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetIcon
- Services Bureau à distance de la méthode GetIcon, classe Win32_TSGetIcon
- Win32_TSGetIcon de la classe Services Bureau à distance, méthode GetIcon
topic_type:
- apiref
api_name:
- Win32_TSGetIcon.GetIcon
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92cd20cad668b0e3a6bba191c83ecdca2934ca17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941755"
---
# <a name="geticon-method-of-the-win32_tsgeticon-class"></a><span data-ttu-id="f697a-106">Méthode GetIcon de la \_ classe Win32 TSGetIcon</span><span class="sxs-lookup"><span data-stu-id="f697a-106">GetIcon method of the Win32\_TSGetIcon class</span></span>

<span data-ttu-id="f697a-107">Retourne le contenu de l’icône spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f697a-107">Returns the contents of the specified icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="f697a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f697a-108">Syntax</span></span>


```mof
uint32 GetIcon(
  [in]  string FilePath,
  [in]  sint32 Index,
  [out] uint8  IconContents[]
);
```



## <a name="parameters"></a><span data-ttu-id="f697a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f697a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f697a-110">*FilePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f697a-110">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f697a-111">Spécifie le chemin d’accès au fichier qui contient l’icône</span><span class="sxs-lookup"><span data-stu-id="f697a-111">Specifies the path to the file that contains the icon</span></span>

</dd> <dt>

<span data-ttu-id="f697a-112">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f697a-112">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f697a-113">Spécifie l’index de l’icône dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="f697a-113">Specifies the index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="f697a-114">*IconContents* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f697a-114">*IconContents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f697a-115">En cas de réussite, contient le contenu de l’icône.</span><span class="sxs-lookup"><span data-stu-id="f697a-115">On successful completion contains the contents of the icon.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f697a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f697a-116">Requirements</span></span>



| <span data-ttu-id="f697a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f697a-117">Requirement</span></span> | <span data-ttu-id="f697a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f697a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f697a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f697a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f697a-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f697a-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f697a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f697a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f697a-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f697a-122">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="f697a-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f697a-123">Namespace</span></span><br/>                | <span data-ttu-id="f697a-124">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="f697a-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f697a-125">MOF</span><span class="sxs-lookup"><span data-stu-id="f697a-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f697a-126"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f697a-126"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="f697a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f697a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f697a-128"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f697a-128"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f697a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f697a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f697a-130">**\_TSGetIcon Win32**</span><span class="sxs-lookup"><span data-stu-id="f697a-130">**Win32\_TSGetIcon**</span></span>](win32-tsgeticon.md)
</dt> </dl>

 

 





