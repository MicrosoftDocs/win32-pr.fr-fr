---
description: La méthode SourceListClearAll de l’objet patch efface la liste source complète de toutes les sources du type spécifié pour un correctif. Accepte le type en tant que paramètre. Cette méthode appelle MsiSourceListClearAllEx.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Méthode patch. SourceListClearAll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 31d7bceac706715099778cf84af2c3b2ec323880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540536"
---
# <a name="patchsourcelistclearall-method"></a><span data-ttu-id="1569d-105">Méthode patch. SourceListClearAll</span><span class="sxs-lookup"><span data-stu-id="1569d-105">Patch.SourceListClearAll method</span></span>

<span data-ttu-id="1569d-106">La méthode **SourceListClearAll** de l’objet [**patch**](patch-object.md) efface la liste source complète de toutes les sources du type spécifié pour un correctif.</span><span class="sxs-lookup"><span data-stu-id="1569d-106">The **SourceListClearAll** method of the [**Patch**](patch-object.md) object clears the complete source list of all sources of the specified type for a patch.</span></span> <span data-ttu-id="1569d-107">Accepte le *type* en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="1569d-107">Accepts *Type* as a parameter.</span></span> <span data-ttu-id="1569d-108">Cette méthode appelle [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span><span class="sxs-lookup"><span data-stu-id="1569d-108">This method calls [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="1569d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1569d-109">Syntax</span></span>


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a><span data-ttu-id="1569d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1569d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1569d-111">*Type*</span><span class="sxs-lookup"><span data-stu-id="1569d-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="1569d-112">Type de source, par exemple, réseau, URL ou média.</span><span class="sxs-lookup"><span data-stu-id="1569d-112">The type of source type, such as network, URL or media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1569d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1569d-113">Return value</span></span>

<span data-ttu-id="1569d-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1569d-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1569d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1569d-115">Requirements</span></span>



| <span data-ttu-id="1569d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1569d-116">Requirement</span></span> | <span data-ttu-id="1569d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1569d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1569d-118">Version</span><span class="sxs-lookup"><span data-stu-id="1569d-118">Version</span></span><br/> | <span data-ttu-id="1569d-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1569d-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="1569d-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="1569d-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="1569d-121">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="1569d-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="1569d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1569d-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="1569d-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1569d-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="1569d-124">IID</span><span class="sxs-lookup"><span data-stu-id="1569d-124">IID</span></span><br/>     | <span data-ttu-id="1569d-125">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="1569d-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="1569d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1569d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1569d-127">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="1569d-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="1569d-128">**MsiSourceListClearAllEx**</span><span class="sxs-lookup"><span data-stu-id="1569d-128">**MsiSourceListClearAllEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[<span data-ttu-id="1569d-129">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="1569d-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




