---
description: La propriété FileAttributes de l’objet installer retourne un nombre qui représente les attributs de fichier combinés pour le chemin d’accès désigné à un fichier ou un dossier.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Installer. FileAttributes, propriété (Windows. Storage. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532512"
---
# <a name="installerfileattributes-property"></a><span data-ttu-id="64fd0-103">Installer. FileAttributes, propriété</span><span class="sxs-lookup"><span data-stu-id="64fd0-103">Installer.FileAttributes property</span></span>

<span data-ttu-id="64fd0-104">La propriété **FileAttributes** de l’objet [**installer**](installer-object.md) retourne un nombre qui représente les attributs de fichier combinés pour le chemin d’accès désigné à un fichier ou un dossier.</span><span class="sxs-lookup"><span data-stu-id="64fd0-104">The **FileAttributes** property of the [**Installer**](installer-object.md) object returns a number representing the combined file attributes for the designated path to a file or folder.</span></span>

<span data-ttu-id="64fd0-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="64fd0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="64fd0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64fd0-106">Syntax</span></span>


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a><span data-ttu-id="64fd0-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="64fd0-107">Property value</span></span>

<span data-ttu-id="64fd0-108">Chemin d’accès au fichier ou dossier requis.</span><span class="sxs-lookup"><span data-stu-id="64fd0-108">The required path to the file or folder.</span></span> <span data-ttu-id="64fd0-109">Un chemin d’accès partiel suppose le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="64fd0-109">A partial path assumes the current directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="64fd0-110">Notes</span><span class="sxs-lookup"><span data-stu-id="64fd0-110">Remarks</span></span>

<span data-ttu-id="64fd0-111">La propriété **FileAttributes** retourne les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="64fd0-111">The **FileAttributes** property returns the following values.</span></span>



| <span data-ttu-id="64fd0-112">Attribut de fichier</span><span class="sxs-lookup"><span data-stu-id="64fd0-112">File attribute</span></span>              | <span data-ttu-id="64fd0-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="64fd0-113">Value</span></span>      | <span data-ttu-id="64fd0-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="64fd0-114">Value</span></span> |
|-----------------------------|------------|-------|
| <span data-ttu-id="64fd0-115">FILE\_ATTRIBUTE\_READONLY</span><span class="sxs-lookup"><span data-stu-id="64fd0-115">FILE\_ATTRIBUTE\_READONLY</span></span>   | <span data-ttu-id="64fd0-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="64fd0-116">0x00000001</span></span> | <span data-ttu-id="64fd0-117">1</span><span class="sxs-lookup"><span data-stu-id="64fd0-117">1</span></span>     |
| <span data-ttu-id="64fd0-118">FILE\_ATTRIBUTE\_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="64fd0-118">FILE\_ATTRIBUTE\_HIDDEN</span></span>     | <span data-ttu-id="64fd0-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="64fd0-119">0x00000002</span></span> | <span data-ttu-id="64fd0-120">2</span><span class="sxs-lookup"><span data-stu-id="64fd0-120">2</span></span>     |
| <span data-ttu-id="64fd0-121">FILE\_ATTRIBUTE\_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="64fd0-121">FILE\_ATTRIBUTE\_SYSTEM</span></span>     | <span data-ttu-id="64fd0-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="64fd0-122">0x00000004</span></span> | <span data-ttu-id="64fd0-123">4</span><span class="sxs-lookup"><span data-stu-id="64fd0-123">4</span></span>     |
| <span data-ttu-id="64fd0-124">FILE\_ATTRIBUTE\_DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="64fd0-124">FILE\_ATTRIBUTE\_DIRECTORY</span></span>  | <span data-ttu-id="64fd0-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="64fd0-125">0x00000010</span></span> | <span data-ttu-id="64fd0-126">16</span><span class="sxs-lookup"><span data-stu-id="64fd0-126">16</span></span>    |
| <span data-ttu-id="64fd0-127">attribut de fichier \_ \_ temporaire</span><span class="sxs-lookup"><span data-stu-id="64fd0-127">FILE\_ATTRIBUTE\_TEMPORARY</span></span>  | <span data-ttu-id="64fd0-128">0x00000100</span><span class="sxs-lookup"><span data-stu-id="64fd0-128">0x00000100</span></span> | <span data-ttu-id="64fd0-129">256</span><span class="sxs-lookup"><span data-stu-id="64fd0-129">256</span></span>   |
| <span data-ttu-id="64fd0-130">FILE\_ATTRIBUTE\_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="64fd0-130">FILE\_ATTRIBUTE\_COMPRESSED</span></span> | <span data-ttu-id="64fd0-131">0x00000800</span><span class="sxs-lookup"><span data-stu-id="64fd0-131">0x00000800</span></span> | <span data-ttu-id="64fd0-132">2 048</span><span class="sxs-lookup"><span data-stu-id="64fd0-132">2048</span></span>  |
| <span data-ttu-id="64fd0-133">FILE\_ATTRIBUTE\_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="64fd0-133">FILE\_ATTRIBUTE\_OFFLINE</span></span>    | <span data-ttu-id="64fd0-134">0x00001000</span><span class="sxs-lookup"><span data-stu-id="64fd0-134">0x00001000</span></span> | <span data-ttu-id="64fd0-135">4096</span><span class="sxs-lookup"><span data-stu-id="64fd0-135">4096</span></span>  |



 

<span data-ttu-id="64fd0-136">Retourne – 1 si le fichier ou le dossier n’existe pas ou n’est pas accessible.</span><span class="sxs-lookup"><span data-stu-id="64fd0-136">Returns –1 if the file or folder does not exist or is not accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="64fd0-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="64fd0-137">Requirements</span></span>



| <span data-ttu-id="64fd0-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64fd0-138">Requirement</span></span> | <span data-ttu-id="64fd0-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="64fd0-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64fd0-140">Version</span><span class="sxs-lookup"><span data-stu-id="64fd0-140">Version</span></span><br/> | <span data-ttu-id="64fd0-141">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="64fd0-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="64fd0-142">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="64fd0-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="64fd0-143">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="64fd0-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="64fd0-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="64fd0-144">Header</span></span><br/>  | <dl> <span data-ttu-id="64fd0-145"><dt>Windows. Storage. h</dt></span><span class="sxs-lookup"><span data-stu-id="64fd0-145"><dt>Windows.storage.h</dt></span></span> </dl>                                                                                                                                                            |
| <span data-ttu-id="64fd0-146">DLL</span><span class="sxs-lookup"><span data-stu-id="64fd0-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="64fd0-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64fd0-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="64fd0-148">IID</span><span class="sxs-lookup"><span data-stu-id="64fd0-148">IID</span></span><br/>     | <span data-ttu-id="64fd0-149">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="64fd0-149">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




