---
description: La fonction InetGetAutodial retourne les paramètres de numérotation automatique à partir du Registre.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: InetGetAutodial fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541430"
---
# <a name="inetgetautodial-function"></a><span data-ttu-id="daa5d-103">InetGetAutodial fonction)</span><span class="sxs-lookup"><span data-stu-id="daa5d-103">InetGetAutodial function</span></span>

<span data-ttu-id="daa5d-104">\[Cette fonction n’est pas prise en charge et peut être modifiée ou non disponible dans les futures versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="daa5d-104">\[This function is unsupported and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="daa5d-105">\]</span><span class="sxs-lookup"><span data-stu-id="daa5d-105">\]</span></span>

<span data-ttu-id="daa5d-106">La fonction **InetGetAutodial** retourne les paramètres de numérotation automatique à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="daa5d-106">The **InetGetAutodial** function returns the autodial settings from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="daa5d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="daa5d-107">Syntax</span></span>


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a><span data-ttu-id="daa5d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="daa5d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="daa5d-109">*lpfEnable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="daa5d-109">*lpfEnable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="daa5d-110">Indique si la numérotation automatique est activée.</span><span class="sxs-lookup"><span data-stu-id="daa5d-110">Indicates whether autodial is enabled.</span></span> <span data-ttu-id="daa5d-111">La valeur **true** lors du retour indique que la numérotation automatique est activée.</span><span class="sxs-lookup"><span data-stu-id="daa5d-111">A value of **TRUE** upon return indicates autodial is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="daa5d-112">*lpszEntryName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="daa5d-112">*lpszEntryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="daa5d-113">Au retour, contient le nom de l’entrée d’annuaire téléphonique définie pour la numérotation automatique.</span><span class="sxs-lookup"><span data-stu-id="daa5d-113">On return, contains the name of the phone book entry that is set for autodial.</span></span>

</dd> <dt>

<span data-ttu-id="daa5d-114">*cbEntryNameSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="daa5d-114">*cbEntryNameSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="daa5d-115">Taille de la mémoire tampon allouée par l’appelant pour le nom de l’entrée de l’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="daa5d-115">Size of the buffer allocated by the caller for the phone book entry name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="daa5d-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="daa5d-116">Return value</span></span>

<span data-ttu-id="daa5d-117">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="daa5d-117">This function can return one of these values.</span></span>



| <span data-ttu-id="daa5d-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="daa5d-118">Return code</span></span>                                                                                                | <span data-ttu-id="daa5d-119">Description</span><span class="sxs-lookup"><span data-stu-id="daa5d-119">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="daa5d-120"><dt>**ERREUR de \_ réussite**</dt></span><span class="sxs-lookup"><span data-stu-id="daa5d-120"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="daa5d-121">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="daa5d-121">The call was successful.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="daa5d-122"><dt>**ERREUR d' \_ arguments incorrects \_**</dt></span><span class="sxs-lookup"><span data-stu-id="daa5d-122"><dt>**ERROR\_BAD\_ARGUMENTS**</dt></span></span> </dl>       | <span data-ttu-id="daa5d-123">*lpfEnable* ou *lpszEntryName* contient un pointeur **null** , ou la valeur de *cbEntryNameSize* est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="daa5d-123">*lpfEnable* or *lpszEntryName* contains a **NULL** pointer, or the value of *cbEntryNameSize* is zero.</span></span><br/>                                         |
| <dl> <span data-ttu-id="daa5d-124"><dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="daa5d-124"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>  | <span data-ttu-id="daa5d-125">La mémoire est insuffisante pour allouer les tampons internes.</span><span class="sxs-lookup"><span data-stu-id="daa5d-125">There was insufficient memory to allocate internal buffers.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="daa5d-126"><dt>**ERREUR \_ de \_ mémoire tampon insuffisante**</dt></span><span class="sxs-lookup"><span data-stu-id="daa5d-126"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="daa5d-127">*cbEntryNameSize* n’indique pas que la mémoire tampon vers laquelle pointe *lpszEntryName* est suffisamment grande pour recevoir le nom de l’entrée de l’annuaire téléphonique.</span><span class="sxs-lookup"><span data-stu-id="daa5d-127">*cbEntryNameSize* does not indicate that the buffer pointed to by *lpszEntryName* is large enough to receive the name of the phone book entry.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="daa5d-128">Notes</span><span class="sxs-lookup"><span data-stu-id="daa5d-128">Remarks</span></span>

<span data-ttu-id="daa5d-129">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="daa5d-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="daa5d-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="daa5d-130">Requirements</span></span>



| <span data-ttu-id="daa5d-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="daa5d-131">Requirement</span></span> | <span data-ttu-id="daa5d-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="daa5d-132">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="daa5d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="daa5d-133">DLL</span></span><br/> | <dl> <span data-ttu-id="daa5d-134"><dt>Inetcfg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="daa5d-134"><dt>Inetcfg.dll</dt></span></span> </dl> |



 

 
