---
description: Active ou désactive la lecture et l’écriture de secteurs de disque.
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: FveEnableRawAccessW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 5b4a367c3566c1475f856783d800ec43e21071e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860902"
---
# <a name="fveenablerawaccessw-function"></a><span data-ttu-id="ac935-103">FveEnableRawAccessW fonction)</span><span class="sxs-lookup"><span data-stu-id="ac935-103">FveEnableRawAccessW function</span></span>

<span data-ttu-id="ac935-104">Active ou désactive la lecture et l’écriture de secteurs de disque.</span><span class="sxs-lookup"><span data-stu-id="ac935-104">Enables or disables reading and writing of disk sectors.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac935-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac935-105">Syntax</span></span>


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="ac935-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac935-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac935-107">*Nom_volume* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac935-107">*VolumeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac935-108">Identificateur unique du volume de disque.</span><span class="sxs-lookup"><span data-stu-id="ac935-108">A unique identifier for the disk volume.</span></span>

</dd> <dt>

<span data-ttu-id="ac935-109">*Activé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac935-109">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac935-110">Si la **valeur est true**, autorise l’accès au volume brut.</span><span class="sxs-lookup"><span data-stu-id="ac935-110">If **TRUE**, allows access to the raw volume.</span></span> <span data-ttu-id="ac935-111">Si la **valeur est false**, aucun accès au volume brut n’est autorisé.</span><span class="sxs-lookup"><span data-stu-id="ac935-111">If **FALSE**, no access is allowed to the raw volume.</span></span> <span data-ttu-id="ac935-112">Si l’accès brut a déjà été activé, mais que cette valeur est **false**, le volume est remonté et revalidés.</span><span class="sxs-lookup"><span data-stu-id="ac935-112">If raw access has already been enabled but this value is **FALSE**, the volume is remounted and revalidated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac935-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac935-113">Return value</span></span>

<span data-ttu-id="ac935-114">Cette fonction retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="ac935-114">This function returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ac935-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ac935-115">Return code/value</span></span>                                                                                                                                                           | <span data-ttu-id="ac935-116">Description</span><span class="sxs-lookup"><span data-stu-id="ac935-116">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ac935-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ac935-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                           | <span data-ttu-id="ac935-118">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="ac935-118">The function was successful.</span></span><br/>                                            |
| <dl> <span data-ttu-id="ac935-119"><dt>**S \_ FALSe**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="ac935-119"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                        | <span data-ttu-id="ac935-120">Enabled a la **valeur false** et le volume n’était pas déjà en mode d’accès brut.</span><span class="sxs-lookup"><span data-stu-id="ac935-120">Enabled is **FALSE** and the volume was not already in raw access mode.</span></span><br/> |
| <dl> <span data-ttu-id="ac935-121"><dt>**E \_ ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="ac935-121"><dt>**E\_ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl> | <span data-ttu-id="ac935-122">Le volume ne peut pas être verrouillé.</span><span class="sxs-lookup"><span data-stu-id="ac935-122">The volume cannot be locked.</span></span><br/>                                            |



 

## <a name="requirements"></a><span data-ttu-id="ac935-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac935-123">Requirements</span></span>



| <span data-ttu-id="ac935-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac935-124">Requirement</span></span> | <span data-ttu-id="ac935-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac935-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac935-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac935-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac935-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac935-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ac935-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac935-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac935-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac935-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ac935-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ac935-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac935-131"><dt>Fveapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac935-131"><dt>Fveapi.dll</dt></span></span> </dl> |



 

 




