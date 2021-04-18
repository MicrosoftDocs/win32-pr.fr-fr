---
description: La méthode ExtractPatchXMLData de l’objet installer extrait des informations d’un correctif sous forme de chaîne XML. Les informations peuvent être utilisées pour déterminer si le correctif s’applique sur un système cible. Cette méthode appelle MsiExtractPatchXMLData.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Installer. ExtractPatchXMLData, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525947"
---
# <a name="installerextractpatchxmldata-method"></a><span data-ttu-id="3538c-105">Installer. ExtractPatchXMLData, méthode</span><span class="sxs-lookup"><span data-stu-id="3538c-105">Installer.ExtractPatchXMLData method</span></span>

<span data-ttu-id="3538c-106">La méthode **ExtractPatchXMLData** de l’objet [**installer**](installer-object.md) extrait des informations d’un correctif sous forme de chaîne XML.</span><span class="sxs-lookup"><span data-stu-id="3538c-106">The **ExtractPatchXMLData** method of the [**Installer**](installer-object.md) object extracts information from a patch as an XML string.</span></span> <span data-ttu-id="3538c-107">Les informations peuvent être utilisées pour déterminer si le correctif s’applique sur un système cible.</span><span class="sxs-lookup"><span data-stu-id="3538c-107">The information can be used to determine whether the patch applies on a target system.</span></span> <span data-ttu-id="3538c-108">Cette méthode appelle [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span><span class="sxs-lookup"><span data-stu-id="3538c-108">This method calls [**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa).</span></span>

## <a name="syntax"></a><span data-ttu-id="3538c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3538c-109">Syntax</span></span>


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a><span data-ttu-id="3538c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3538c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3538c-111">*PatchPath*</span><span class="sxs-lookup"><span data-stu-id="3538c-111">*PatchPath*</span></span> 
</dt> <dd>

<span data-ttu-id="3538c-112">Chemin d’accès complet au correctif à partir duquel les informations de mise en application doivent être extraites.</span><span class="sxs-lookup"><span data-stu-id="3538c-112">Full path to the patch from which the applicability information is to be extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3538c-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3538c-113">Return value</span></span>

<span data-ttu-id="3538c-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3538c-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3538c-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3538c-115">Requirements</span></span>



| <span data-ttu-id="3538c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3538c-116">Requirement</span></span> | <span data-ttu-id="3538c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3538c-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3538c-118">Version</span><span class="sxs-lookup"><span data-stu-id="3538c-118">Version</span></span><br/> | <span data-ttu-id="3538c-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3538c-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3538c-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3538c-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3538c-121">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3538c-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="3538c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3538c-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="3538c-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3538c-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="3538c-124">IID</span><span class="sxs-lookup"><span data-stu-id="3538c-124">IID</span></span><br/>     | <span data-ttu-id="3538c-125">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3538c-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="3538c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3538c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3538c-127">**MsiExtractPatchXMLData**</span><span class="sxs-lookup"><span data-stu-id="3538c-127">**MsiExtractPatchXMLData**</span></span>](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[<span data-ttu-id="3538c-128">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="3538c-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




