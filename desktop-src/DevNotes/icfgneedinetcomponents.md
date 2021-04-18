---
description: Détermine si les composants marqués dans les options sont installés sur le système.
ms.assetid: 5fda917a-9c4b-42a3-8f79-9c609f56eb9f
title: IcfgNeedInetComponents fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgNeedInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: c851ed7d5610d96af636afb60114a51be9c711f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528932"
---
# <a name="icfgneedinetcomponents-function"></a><span data-ttu-id="19057-103">IcfgNeedInetComponents fonction)</span><span class="sxs-lookup"><span data-stu-id="19057-103">IcfgNeedInetComponents function</span></span>

<span data-ttu-id="19057-104">Détermine si les composants marqués dans les options sont installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="19057-104">Determines whether components marked in the options are installed on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="19057-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19057-105">Syntax</span></span>


```C++
HRESULT IcfgNeedInetComponents(
   DWORD  dwfOptions,
   LPBOOL lpfNeedComponents
);
```



## <a name="parameters"></a><span data-ttu-id="19057-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19057-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19057-107">*dwfOptions*</span><span class="sxs-lookup"><span data-stu-id="19057-107">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="19057-108">Combinaison des indicateurs suivants qui spécifient les composants à détecter dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="19057-108">A combination of the following flags that specify which components to detect from the following list.</span></span>



| <span data-ttu-id="19057-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="19057-109">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="19057-110">Signification</span><span class="sxs-lookup"><span data-stu-id="19057-110">Meaning</span></span>                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="19057-111"><dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="19057-111"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="19057-112">Exchange ou Internet Mail est-il nécessaire ?</span><span class="sxs-lookup"><span data-stu-id="19057-112">Is Exchange or Internet mail needed?</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="19057-113"><dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="19057-113"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="19057-114">RAS est-il nécessaire ?</span><span class="sxs-lookup"><span data-stu-id="19057-114">Is RAS needed?</span></span><br/>                       |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="19057-115"><dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="19057-115"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="19057-116">TCP/IP est-il nécessaire ?</span><span class="sxs-lookup"><span data-stu-id="19057-116">Is TCP/IP needed?</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="19057-117">*lpfNeedComponents*</span><span class="sxs-lookup"><span data-stu-id="19057-117">*lpfNeedComponents*</span></span> 
</dt> <dd>

<span data-ttu-id="19057-118">Si cette valeur n’est pas **null**, elle a la valeur **true** en cas de retour si un ou plusieurs composants ne sont pas installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="19057-118">If this value is non-**NULL**, it is **TRUE** on return if one or more components are not installed on the system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19057-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19057-119">Return value</span></span>

<span data-ttu-id="19057-120">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="19057-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="19057-121">Si aucune erreur ne se produit, elle retourne le code d' **erreur de \_ réussite** .</span><span class="sxs-lookup"><span data-stu-id="19057-121">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="19057-122">Notes</span><span class="sxs-lookup"><span data-stu-id="19057-122">Remarks</span></span>

<span data-ttu-id="19057-123">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="19057-123">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="19057-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19057-124">Requirements</span></span>



| <span data-ttu-id="19057-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19057-125">Requirement</span></span> | <span data-ttu-id="19057-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="19057-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19057-127">DLL</span><span class="sxs-lookup"><span data-stu-id="19057-127">DLL</span></span><br/> | <dl> <span data-ttu-id="19057-128"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19057-128"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
