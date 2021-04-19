---
description: Récupère le titre du fichier pour le chemin d’accès au fichier spécifié.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: pSetupGetFileTitle fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539523"
---
# <a name="psetupgetfiletitle-function"></a><span data-ttu-id="1ac83-103">pSetupGetFileTitle fonction)</span><span class="sxs-lookup"><span data-stu-id="1ac83-103">pSetupGetFileTitle function</span></span>

<span data-ttu-id="1ac83-104">\[Cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="1ac83-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="1ac83-105">Récupère le titre du fichier pour le chemin d’accès au fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="1ac83-105">Retrieves the file title for the specified file path.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac83-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ac83-106">Syntax</span></span>


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a><span data-ttu-id="1ac83-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ac83-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ac83-108">*FilePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ac83-108">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ac83-109">Chemin d'accès au fichier.</span><span class="sxs-lookup"><span data-stu-id="1ac83-109">The file path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ac83-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ac83-110">Return value</span></span>

<span data-ttu-id="1ac83-111">Pointeur vers une chaîne qui reçoit le titre du fichier.</span><span class="sxs-lookup"><span data-stu-id="1ac83-111">A pointer to string that receives the file title.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ac83-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1ac83-112">Remarks</span></span>

<span data-ttu-id="1ac83-113">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1ac83-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ac83-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ac83-114">Requirements</span></span>



| <span data-ttu-id="1ac83-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ac83-115">Requirement</span></span> | <span data-ttu-id="1ac83-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ac83-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ac83-117">DLL</span><span class="sxs-lookup"><span data-stu-id="1ac83-117">DLL</span></span><br/> | <dl> <span data-ttu-id="1ac83-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ac83-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
