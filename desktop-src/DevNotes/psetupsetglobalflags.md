---
description: Désactive les fonctionnalités.
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: pSetupSetGlobalFlags fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535015"
---
# <a name="psetupsetglobalflags-function"></a><span data-ttu-id="8b4c1-103">pSetupSetGlobalFlags fonction)</span><span class="sxs-lookup"><span data-stu-id="8b4c1-103">pSetupSetGlobalFlags function</span></span>

<span data-ttu-id="8b4c1-104">\[Cette fonction n’est pas disponible dans Windows Vista ou Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="8b4c1-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="8b4c1-105">Désactive les fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="8b4c1-105">Disables features.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b4c1-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b4c1-106">Syntax</span></span>


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="8b4c1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b4c1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b4c1-108">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b4c1-108">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b4c1-109">Indicateurs utilisés pour désactiver l’interface utilisateur ou la sauvegarde automatique.</span><span class="sxs-lookup"><span data-stu-id="8b4c1-109">The flags used to disable user interface or automatic backup.</span></span>



| <span data-ttu-id="8b4c1-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b4c1-110">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="8b4c1-111">Signification</span><span class="sxs-lookup"><span data-stu-id="8b4c1-111">Meaning</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <span data-ttu-id="8b4c1-112"><dt>**PSPGF \_**</dt> <dt>0X004</dt> non interactif</span><span class="sxs-lookup"><span data-stu-id="8b4c1-112"><dt>**PSPGF\_NONINTERACTIVE**</dt> <dt>0x004</dt></span></span> </dl> | <span data-ttu-id="8b4c1-113">Défini pour désactiver l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8b4c1-113">Set to disable user interface.</span></span><br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <span data-ttu-id="8b4c1-114"><dt>**PSPGF \_ AUCUNE \_ sauvegarde**</dt> <dt>0x002</dt></span><span class="sxs-lookup"><span data-stu-id="8b4c1-114"><dt>**PSPGF\_NO\_BACKUP**</dt> <dt>0x002</dt></span></span> </dl>               | <span data-ttu-id="8b4c1-115">Défini pour désactiver la sauvegarde automatique.</span><span class="sxs-lookup"><span data-stu-id="8b4c1-115">Set to disable automatic backup.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b4c1-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b4c1-116">Return value</span></span>

<span data-ttu-id="8b4c1-117">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8b4c1-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b4c1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="8b4c1-118">Remarks</span></span>

<span data-ttu-id="8b4c1-119">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8b4c1-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b4c1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b4c1-120">Requirements</span></span>



| <span data-ttu-id="8b4c1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b4c1-121">Requirement</span></span> | <span data-ttu-id="8b4c1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b4c1-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b4c1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8b4c1-123">DLL</span></span><br/> | <dl> <span data-ttu-id="8b4c1-124"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b4c1-124"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
