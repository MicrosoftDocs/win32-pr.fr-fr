---
description: Supprime une source réseau ou URL.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Méthode patch. SourceListClearSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532555"
---
# <a name="patchsourcelistclearsource-method"></a><span data-ttu-id="9a0a1-103">Méthode patch. SourceListClearSource</span><span class="sxs-lookup"><span data-stu-id="9a0a1-103">Patch.SourceListClearSource method</span></span>

<span data-ttu-id="9a0a1-104">La méthode **SourceListClearSource** supprime une source réseau ou URL.</span><span class="sxs-lookup"><span data-stu-id="9a0a1-104">The **SourceListClearSource** method removes a network or URL source.</span></span> <span data-ttu-id="9a0a1-105">Cette méthode appelle [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span><span class="sxs-lookup"><span data-stu-id="9a0a1-105">This method calls [**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea).</span></span>

## <a name="syntax"></a><span data-ttu-id="9a0a1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a0a1-106">Syntax</span></span>


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a><span data-ttu-id="9a0a1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a0a1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a0a1-108">*Type*</span><span class="sxs-lookup"><span data-stu-id="9a0a1-108">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="9a0a1-109">Type de source à supprimer.</span><span class="sxs-lookup"><span data-stu-id="9a0a1-109">Type of source to be removed.</span></span>

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

<span data-ttu-id="9a0a1-110">**\_réseau MSISOURCETYPE**</span><span class="sxs-lookup"><span data-stu-id="9a0a1-110">**MSISOURCETYPE\_NETWORK**</span></span>
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

<span data-ttu-id="9a0a1-111">**\_URL MSISOURCETYPE**</span><span class="sxs-lookup"><span data-stu-id="9a0a1-111">**MSISOURCETYPE\_URL**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="9a0a1-112">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="9a0a1-112">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="9a0a1-113">Chemin d’accès à la source à supprimer.</span><span class="sxs-lookup"><span data-stu-id="9a0a1-113">Path to the source to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a0a1-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a0a1-114">Return value</span></span>

<span data-ttu-id="9a0a1-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9a0a1-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0a1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a0a1-116">Requirements</span></span>



| <span data-ttu-id="9a0a1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a0a1-117">Requirement</span></span> | <span data-ttu-id="9a0a1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a0a1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0a1-119">Version</span><span class="sxs-lookup"><span data-stu-id="9a0a1-119">Version</span></span><br/> | <span data-ttu-id="9a0a1-120">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9a0a1-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9a0a1-121">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9a0a1-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9a0a1-122">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9a0a1-122">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="9a0a1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9a0a1-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="9a0a1-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a0a1-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="9a0a1-125">IID</span><span class="sxs-lookup"><span data-stu-id="9a0a1-125">IID</span></span><br/>     | <span data-ttu-id="9a0a1-126">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9a0a1-126">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="9a0a1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a0a1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0a1-128">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="9a0a1-128">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="9a0a1-129">**MsiSourceListClearSource**</span><span class="sxs-lookup"><span data-stu-id="9a0a1-129">**MsiSourceListClearSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[<span data-ttu-id="9a0a1-130">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="9a0a1-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




