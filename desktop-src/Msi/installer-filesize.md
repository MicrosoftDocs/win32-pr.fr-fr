---
description: La méthode FileSize de l’objet installer utilise des appels d’API Win32 pour retourner la taille du fichier spécifié dans chemin d’accès.
ms.assetid: d7119e5e-9315-4b20-a904-bc1104f3a4e4
title: Installer. FileSize, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileSize
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 593319b88e3942ae6caa1399adbe2e596bf6e737
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532729"
---
# <a name="installerfilesize-method"></a><span data-ttu-id="94223-103">Installer. FileSize, méthode</span><span class="sxs-lookup"><span data-stu-id="94223-103">Installer.FileSize method</span></span>

<span data-ttu-id="94223-104">La méthode **FileSize** de l’objet [**installer**](installer-object.md) utilise des appels d’API Win32 pour retourner la taille du fichier spécifié dans *chemin d’accès*.</span><span class="sxs-lookup"><span data-stu-id="94223-104">The **FileSize** method of the [**Installer**](installer-object.md) object uses Win32 API calls to return the size of the file specified in *Path*.</span></span>

## <a name="syntax"></a><span data-ttu-id="94223-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="94223-105">Syntax</span></span>


```JScript
Installer.FileSize(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="94223-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="94223-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94223-107">*Chemin d’accès*</span><span class="sxs-lookup"><span data-stu-id="94223-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="94223-108">Chaîne obligatoire contenant le chemin d’accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="94223-108">Required string containing the path to the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94223-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="94223-109">Return value</span></span>

<span data-ttu-id="94223-110">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="94223-110">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="94223-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94223-111">Requirements</span></span>



| <span data-ttu-id="94223-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94223-112">Requirement</span></span> | <span data-ttu-id="94223-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="94223-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94223-114">Version</span><span class="sxs-lookup"><span data-stu-id="94223-114">Version</span></span><br/> | <span data-ttu-id="94223-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="94223-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="94223-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="94223-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="94223-117">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="94223-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="94223-118">DLL</span><span class="sxs-lookup"><span data-stu-id="94223-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="94223-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94223-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="94223-120">IID</span><span class="sxs-lookup"><span data-stu-id="94223-120">IID</span></span><br/>     | <span data-ttu-id="94223-121">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="94223-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




