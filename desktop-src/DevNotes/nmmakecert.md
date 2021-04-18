---
description: Crée un certificat utilisateur à utiliser avec la Conférence NetMeeting.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: NmMakeCert fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543231"
---
# <a name="nmmakecert-function"></a><span data-ttu-id="55418-103">NmMakeCert fonction)</span><span class="sxs-lookup"><span data-stu-id="55418-103">NmMakeCert function</span></span>

<span data-ttu-id="55418-104">Crée un certificat utilisateur à utiliser avec la Conférence NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="55418-104">Creates a user certificate for use with NetMeeting conferencing.</span></span>

## <a name="syntax"></a><span data-ttu-id="55418-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="55418-105">Syntax</span></span>


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="55418-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="55418-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55418-107">*szFirstName*</span><span class="sxs-lookup"><span data-stu-id="55418-107">*szFirstName*</span></span> 
</dt> <dd>

<span data-ttu-id="55418-108">Prénom de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55418-108">The user's first name.</span></span>

</dd> <dt>

<span data-ttu-id="55418-109">*szLastName*</span><span class="sxs-lookup"><span data-stu-id="55418-109">*szLastName*</span></span> 
</dt> <dd>

<span data-ttu-id="55418-110">Nom de famille de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55418-110">The user's last name.</span></span>

</dd> <dt>

<span data-ttu-id="55418-111">*szEmailName*</span><span class="sxs-lookup"><span data-stu-id="55418-111">*szEmailName*</span></span> 
</dt> <dd>

<span data-ttu-id="55418-112">Nom de l’adresse de messagerie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55418-112">The user's email name.</span></span>

</dd> <dt>

<span data-ttu-id="55418-113">*szCity*</span><span class="sxs-lookup"><span data-stu-id="55418-113">*szCity*</span></span> 
</dt> <dd>

<span data-ttu-id="55418-114">ville de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55418-114">The user's city.</span></span>

</dd> <dt>

<span data-ttu-id="55418-115">*szCountry*</span><span class="sxs-lookup"><span data-stu-id="55418-115">*szCountry*</span></span> 
</dt> <dd>

<span data-ttu-id="55418-116">Pays/région de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55418-116">The user's country/region.</span></span>

</dd> <dt>

<span data-ttu-id="55418-117">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="55418-117">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="55418-118">Valeur qui indique comment le certificat doit être créé.</span><span class="sxs-lookup"><span data-stu-id="55418-118">A value that indicates how the certificate should be created.</span></span> <span data-ttu-id="55418-119">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="55418-119">Values can be any of the following.</span></span>



| <span data-ttu-id="55418-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="55418-120">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="55418-121">Signification</span><span class="sxs-lookup"><span data-stu-id="55418-121">Meaning</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <span data-ttu-id="55418-122"><dt>**Nmmkcert \_ F \_ Cleanup \_ uniquement**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="55418-122"><dt>**NMMKCERT\_F\_CLEANUP\_ONLY**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="55418-123">Supprimez l’ancien certificat sans en créer un nouveau.</span><span class="sxs-lookup"><span data-stu-id="55418-123">Delete the old certificate without creating a new one.</span></span> <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <span data-ttu-id="55418-124"><dt>**Nmmkcert \_ F \_ DELETEOLDCERT**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="55418-124"><dt>**NMMKCERT\_F\_DELETEOLDCERT**</dt> <dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="55418-125">Supprimez l’ancien certificat créé précédemment avec cette fonction.</span><span class="sxs-lookup"><span data-stu-id="55418-125">Delete the old certificate previously created with this function.</span></span> <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <span data-ttu-id="55418-126"><dt>**Nmmkcert \_ F \_ \_ ordinateur local**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="55418-126"><dt>**NMMKCERT\_F\_LOCAL\_MACHINE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="55418-127">Créez le certificat dans le magasin de certificats de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="55418-127">Create the certificate in the local machine certificate store.</span></span> <br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55418-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="55418-128">Return value</span></span>

<span data-ttu-id="55418-129">Retourne 1 si la fonction réussit et-1 si la fonction échoue.</span><span class="sxs-lookup"><span data-stu-id="55418-129">Returns 1 if the function succeeds and –1 if the function fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="55418-130">Notes</span><span class="sxs-lookup"><span data-stu-id="55418-130">Remarks</span></span>

<span data-ttu-id="55418-131">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="55418-131">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="55418-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55418-132">Requirements</span></span>



| <span data-ttu-id="55418-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55418-133">Requirement</span></span> | <span data-ttu-id="55418-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="55418-134">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55418-135">DLL</span><span class="sxs-lookup"><span data-stu-id="55418-135">DLL</span></span><br/> | <dl> <span data-ttu-id="55418-136"><dt>Nmmkcert.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55418-136"><dt>Nmmkcert.dll</dt></span></span> </dl> |



 

 
