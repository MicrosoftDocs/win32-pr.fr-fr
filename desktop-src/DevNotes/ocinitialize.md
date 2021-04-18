---
description: Initialise le gestionnaire de composants facultatif.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: OcInitialize fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540220"
---
# <a name="ocinitialize-function"></a><span data-ttu-id="9b4b6-103">OcInitialize fonction)</span><span class="sxs-lookup"><span data-stu-id="9b4b6-103">OcInitialize function</span></span>

<span data-ttu-id="9b4b6-104">Initialise le gestionnaire de composants facultatif.</span><span class="sxs-lookup"><span data-stu-id="9b4b6-104">Initializes the optional component manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b4b6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9b4b6-105">Syntax</span></span>


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a><span data-ttu-id="9b4b6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9b4b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b4b6-107">*Rappels* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b4b6-107">*Callbacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4b6-108">Pointeur vers une structure [**de \_ \_ rappels de client OCM**](ocm-client-callbacks.md) qui spécifie les fonctions de rappel que le gestionnaire OC doit utiliser pour effectuer diverses tâches.</span><span class="sxs-lookup"><span data-stu-id="9b4b6-108">A pointer to an [**OCM\_CLIENT\_CALLBACKS**](ocm-client-callbacks.md) structure that specifies the callback functions to be used by the OC manager to perform various tasks.</span></span>

</dd> <dt>

<span data-ttu-id="9b4b6-109">*MasterOcInfName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b4b6-109">*MasterOcInfName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4b6-110">Chemin d’accès du fichier. inf OC maître.</span><span class="sxs-lookup"><span data-stu-id="9b4b6-110">The path of the master OC .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="9b4b6-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9b4b6-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4b6-112">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9b4b6-112">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9b4b6-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_ FORCENEWINF** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9b4b6-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT\_FORCENEWINF** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="9b4b6-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_ KILLSUBCOMPS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="9b4b6-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT\_KILLSUBCOMPS** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="9b4b6-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_ RUNQUIET** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="9b4b6-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT\_RUNQUIET** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="9b4b6-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_ LANGUAGEAWARE** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="9b4b6-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT\_LANGUAGEAWARE** (0x00000008)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="9b4b6-117">*ShowError* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9b4b6-117">*ShowError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4b6-118">Si la fonction échoue, ce paramètre indique s’il faut afficher un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="9b4b6-118">If the function fails, this parameter indicates whether to display an error message.</span></span>

</dd> <dt>

<span data-ttu-id="9b4b6-119">*Journal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9b4b6-119">*Log* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9b4b6-120">Handle du journal.</span><span class="sxs-lookup"><span data-stu-id="9b4b6-120">A handle to the log.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b4b6-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9b4b6-121">Return value</span></span>

<span data-ttu-id="9b4b6-122">La fonction retourne la valeur de contexte du gestionnaire OC.</span><span class="sxs-lookup"><span data-stu-id="9b4b6-122">The function returns the OC manager context value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b4b6-123">Notes</span><span class="sxs-lookup"><span data-stu-id="9b4b6-123">Remarks</span></span>

<span data-ttu-id="9b4b6-124">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9b4b6-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b4b6-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9b4b6-125">Requirements</span></span>



| <span data-ttu-id="9b4b6-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9b4b6-126">Requirement</span></span> | <span data-ttu-id="9b4b6-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9b4b6-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b4b6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="9b4b6-128">DLL</span></span><br/> | <dl> <span data-ttu-id="9b4b6-129"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b4b6-129"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b4b6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9b4b6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b4b6-131">**\_rappels de client OCM \_**</span><span class="sxs-lookup"><span data-stu-id="9b4b6-131">**OCM\_CLIENT\_CALLBACKS**</span></span>](ocm-client-callbacks.md)
</dt> <dt>

[<span data-ttu-id="9b4b6-132">**OcTerminate**</span><span class="sxs-lookup"><span data-stu-id="9b4b6-132">**OcTerminate**</span></span>](octerminate.md)
</dt> </dl>

 

 
