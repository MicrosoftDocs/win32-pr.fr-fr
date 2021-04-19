---
description: Recharge une configuration IME à partir du Registre HKCU, uniquement dans l’IME japonais.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: reload_config fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: bc9d0d026359036d8847ebaa2542f778de4d5767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534881"
---
# <a name="reload_config-function"></a><span data-ttu-id="57305-103">recharger la \_ fonction de configuration</span><span class="sxs-lookup"><span data-stu-id="57305-103">reload\_config function</span></span>

<span data-ttu-id="57305-104">Recharge une configuration IME à partir du Registre HKCU, uniquement dans l’IME japonais.</span><span class="sxs-lookup"><span data-stu-id="57305-104">Reloads an IME configuration from the HKCU registry, in Japanese IME only.</span></span>

## <a name="syntax"></a><span data-ttu-id="57305-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57305-105">Syntax</span></span>


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a><span data-ttu-id="57305-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57305-106">Parameters</span></span>

<span data-ttu-id="57305-107">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="57305-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="57305-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57305-108">Return value</span></span>

<span data-ttu-id="57305-109">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="57305-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="57305-110">Notes</span><span class="sxs-lookup"><span data-stu-id="57305-110">Remarks</span></span>

<span data-ttu-id="57305-111">Si aucune valeur de Registre n’est présente dans HKCU, la fonction de **\_ configuration de rechargement** écrit les données initiales dans le registre.</span><span class="sxs-lookup"><span data-stu-id="57305-111">If no registry value is present in HKCU, the **reload\_config** function writes initial data to the registry.</span></span>

<span data-ttu-id="57305-112">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="57305-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="57305-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57305-113">Requirements</span></span>



| <span data-ttu-id="57305-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57305-114">Requirement</span></span> | <span data-ttu-id="57305-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="57305-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57305-116">DLL</span><span class="sxs-lookup"><span data-stu-id="57305-116">DLL</span></span><br/> | <dl> <span data-ttu-id="57305-117"><dt>Imejpknl.dll ; </dt> <dt>Imejp98k.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57305-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span></span> </dl> |



 

 
