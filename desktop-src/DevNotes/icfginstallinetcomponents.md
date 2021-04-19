---
description: Installe les composants système spécifiés.
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: IcfgInstallInetComponents fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541097"
---
# <a name="icfginstallinetcomponents-function"></a><span data-ttu-id="4ff74-103">IcfgInstallInetComponents fonction)</span><span class="sxs-lookup"><span data-stu-id="4ff74-103">IcfgInstallInetComponents function</span></span>

<span data-ttu-id="4ff74-104">Installe les composants système spécifiés.</span><span class="sxs-lookup"><span data-stu-id="4ff74-104">Installs the system components specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ff74-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4ff74-105">Syntax</span></span>


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a><span data-ttu-id="4ff74-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4ff74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ff74-107">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="4ff74-107">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff74-108">Handle de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="4ff74-108">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="4ff74-109">*dwfOptions*</span><span class="sxs-lookup"><span data-stu-id="4ff74-109">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff74-110">Combinaison des indicateurs suivants qui contrôlent l’installation et la configuration.</span><span class="sxs-lookup"><span data-stu-id="4ff74-110">A combination of the following flags that control the installation and configuration.</span></span>



| <span data-ttu-id="4ff74-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ff74-111">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="4ff74-112">Signification</span><span class="sxs-lookup"><span data-stu-id="4ff74-112">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="4ff74-113"><dt>**ICFG \_ INSTALLMAIL**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="4ff74-113"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="4ff74-114">Installez Exchange et la messagerie Internet.</span><span class="sxs-lookup"><span data-stu-id="4ff74-114">Install Exchange and Internet mail.</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="4ff74-115"><dt>**ICFG \_ INSTALLRAS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="4ff74-115"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="4ff74-116">Installez RAS (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="4ff74-116">Install RAS (if needed).</span></span><br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="4ff74-117"><dt>**ICFG \_ INSTALLTCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4ff74-117"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="4ff74-118">Installez TCP/IP (si nécessaire).</span><span class="sxs-lookup"><span data-stu-id="4ff74-118">Install TCP/IP (if needed).</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="4ff74-119">*lpfNeedsRestart*</span><span class="sxs-lookup"><span data-stu-id="4ff74-119">*lpfNeedsRestart*</span></span> 
</dt> <dd>

<span data-ttu-id="4ff74-120">Si cette valeur n’est pas **null**, on retourne la valeur **true** uniquement si Windows doit être redémarré pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="4ff74-120">If this value is non-**NULL**, on return it will be **TRUE** only if Windows must be restarted to complete the installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ff74-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4ff74-121">Return value</span></span>

<span data-ttu-id="4ff74-122">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4ff74-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4ff74-123">Si aucune erreur ne se produit, elle retourne le code d' **erreur de \_ réussite** .</span><span class="sxs-lookup"><span data-stu-id="4ff74-123">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ff74-124">Notes</span><span class="sxs-lookup"><span data-stu-id="4ff74-124">Remarks</span></span>

<span data-ttu-id="4ff74-125">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4ff74-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ff74-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4ff74-126">Requirements</span></span>



| <span data-ttu-id="4ff74-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4ff74-127">Requirement</span></span> | <span data-ttu-id="4ff74-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4ff74-128">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ff74-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4ff74-129">DLL</span></span><br/> | <dl> <span data-ttu-id="4ff74-130"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ff74-130"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
