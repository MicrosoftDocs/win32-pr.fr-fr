---
description: Récupère les attributs de base pour l’objet fichier spécifié.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: NtQueryAttributesFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533738"
---
# <a name="ntqueryattributesfile-function"></a><span data-ttu-id="25454-103">NtQueryAttributesFile fonction)</span><span class="sxs-lookup"><span data-stu-id="25454-103">NtQueryAttributesFile function</span></span>

<span data-ttu-id="25454-104">\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]</span><span class="sxs-lookup"><span data-stu-id="25454-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="25454-105">Récupère les attributs de base pour l’objet fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="25454-105">Retrieves basic attributes for the specified file object.</span></span>

## <a name="syntax"></a><span data-ttu-id="25454-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25454-106">Syntax</span></span>


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a><span data-ttu-id="25454-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25454-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25454-108">*ObjectAttributes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="25454-108">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25454-109">Pointeur vers une structure [d' \_ attributs d’objet](https://msdn.microsoft.com/library/aa491657.aspx) qui fournit les attributs à utiliser pour l’objet fichier.</span><span class="sxs-lookup"><span data-stu-id="25454-109">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure that supplies the attributes to be used for the file object.</span></span>

</dd> <dt>

<span data-ttu-id="25454-110">*FileInformation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="25454-110">*FileInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25454-111">Pointeur vers une structure [d' \_ \_ informations de base de fichier](https://msdn.microsoft.com/library/aa491634.aspx) pour recevoir les informations d’attribut de fichier retournées.</span><span class="sxs-lookup"><span data-stu-id="25454-111">A pointer to a [FILE\_BASIC\_INFORMATION](https://msdn.microsoft.com/library/aa491634.aspx) structure to receive the returned file attribute information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25454-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25454-112">Return value</span></span>

<span data-ttu-id="25454-113">Retourne un code NTSTATUS ou d’erreur.</span><span class="sxs-lookup"><span data-stu-id="25454-113">Returns an NTSTATUS or error code.</span></span>

<span data-ttu-id="25454-114">Les formulaires et la signification des codes d’erreur de NTSTATUS sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le kit WDK et sont décrits dans la documentation WDK.</span><span class="sxs-lookup"><span data-stu-id="25454-114">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="25454-115">Notes</span><span class="sxs-lookup"><span data-stu-id="25454-115">Remarks</span></span>

<span data-ttu-id="25454-116">Cette fonction n’a aucun fichier d’en-tête associé.</span><span class="sxs-lookup"><span data-stu-id="25454-116">This function has no associated header file.</span></span> <span data-ttu-id="25454-117">La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK.</span><span class="sxs-lookup"><span data-stu-id="25454-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="25454-118">Vous pouvez également utiliser les fonctions [**LoadLibrary**](-loadlibrary.md) et [**GetProcAddress**](-getprocaddress-.md) pour établir une liaison dynamique à Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="25454-118">You can also use the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="25454-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25454-119">Requirements</span></span>



| <span data-ttu-id="25454-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25454-120">Requirement</span></span> | <span data-ttu-id="25454-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="25454-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="25454-122">DLL</span><span class="sxs-lookup"><span data-stu-id="25454-122">DLL</span></span><br/> | <dl> <span data-ttu-id="25454-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25454-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




