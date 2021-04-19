---
description: Ajoute une chaîne et des données supplémentaires à une table.
ms.assetid: e6f29cb0-4468-435d-9ae3-217d4f69e87e
title: pSetupStringTableAddStringEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableAddStringEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 22de3bcc2ad21b82e1fd8306a0c668f83c723b9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532237"
---
# <a name="psetupstringtableaddstringex-function"></a><span data-ttu-id="9d06a-103">pSetupStringTableAddStringEx fonction)</span><span class="sxs-lookup"><span data-stu-id="9d06a-103">pSetupStringTableAddStringEx function</span></span>

<span data-ttu-id="9d06a-104">\[Cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="9d06a-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="9d06a-105">Ajoute une chaîne et des données supplémentaires à une table.</span><span class="sxs-lookup"><span data-stu-id="9d06a-105">Adds a string and extra data to a table.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d06a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d06a-106">Syntax</span></span>


```C++
LONG pSetupStringTableAddStringEx(
  _In_     PVOID StringTable,
  _In_     PTSTR String,
  _In_     DWORD Flags,
  _In_opt_ PVOID ExtraData,
  _In_opt_ UINT  ExtraDataSize
);
```



## <a name="parameters"></a><span data-ttu-id="9d06a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d06a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d06a-108">*STRINGTABLE* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d06a-108">*StringTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d06a-109">Pointeur vers la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="9d06a-109">A pointer to the string table.</span></span>

</dd> <dt>

<span data-ttu-id="9d06a-110">*Chaîne* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d06a-110">*String* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d06a-111">Pointeur vers une chaîne à ajouter à la table.</span><span class="sxs-lookup"><span data-stu-id="9d06a-111">A pointer to string to be added to the table.</span></span>

</dd> <dt>

<span data-ttu-id="9d06a-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9d06a-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d06a-113">La valeur de ce paramètre peut être `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA` .</span><span class="sxs-lookup"><span data-stu-id="9d06a-113">The value of this parameter can be `STRTAB_CASE_SENSITIVE | STRTAB_NEW_EXTRADATA`.</span></span>



| <span data-ttu-id="9d06a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d06a-114">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="9d06a-115">Signification</span><span class="sxs-lookup"><span data-stu-id="9d06a-115">Meaning</span></span>                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="STRTAB_CASE_SENSITIVE"></span><span id="strtab_case_sensitive"></span><dl> <span data-ttu-id="9d06a-116"><dt>**STRTAB \_ 0x001 \_ sensibles**</dt> à la casse <dt></dt></span><span class="sxs-lookup"><span data-stu-id="9d06a-116"><dt>**STRTAB\_CASE\_SENSITIVE**</dt> <dt>0x001</dt></span></span> </dl> | <span data-ttu-id="9d06a-117">La chaîne respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="9d06a-117">String is case sensitive.</span></span><br/> |
| <span id="STRTAB_NEW_EXTRADATA"></span><span id="strtab_new_extradata"></span><dl> <span data-ttu-id="9d06a-118"><dt>**STRTAB \_ NOUVEAU \_ EXTRADATA**</dt> <dt>0x004</dt></span><span class="sxs-lookup"><span data-stu-id="9d06a-118"><dt>**STRTAB\_NEW\_EXTRADATA**</dt> <dt>0x004</dt></span></span> </dl>    | <span data-ttu-id="9d06a-119">Il y a des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9d06a-119">There is extra data.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="9d06a-120">*ExtraData* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9d06a-120">*ExtraData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d06a-121">Pointeur facultatif vers un objet de données supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="9d06a-121">A optional pointer to an extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="9d06a-122">*ExtraDataSize* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9d06a-122">*ExtraDataSize* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9d06a-123">Taille des données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="9d06a-123">The size of the extra data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9d06a-124">Notes</span><span class="sxs-lookup"><span data-stu-id="9d06a-124">Remarks</span></span>

<span data-ttu-id="9d06a-125">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9d06a-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d06a-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d06a-126">Requirements</span></span>



| <span data-ttu-id="9d06a-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d06a-127">Requirement</span></span> | <span data-ttu-id="9d06a-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d06a-128">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d06a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9d06a-129">DLL</span></span><br/> | <dl> <span data-ttu-id="9d06a-130"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d06a-130"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
