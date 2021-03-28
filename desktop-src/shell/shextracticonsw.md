---
description: Crée un tableau de handles pour les icônes extraites d’un fichier spécifié.
title: SHExtractIconsW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: d82eb48d45210ebf12464708b09fe469d97432db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991625"
---
# <a name="shextracticonsw-function"></a><span data-ttu-id="76eb9-103">SHExtractIconsW fonction)</span><span class="sxs-lookup"><span data-stu-id="76eb9-103">SHExtractIconsW function</span></span>

<span data-ttu-id="76eb9-104">\[**SHExtractIconsW** est disponible via Windows XP Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="76eb9-104">\[**SHExtractIconsW** is available through Windows XP Service Pack 2 (SP2).</span></span> <span data-ttu-id="76eb9-105">Il peut être modifié ou non disponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="76eb9-106">Crée un tableau de handles pour les icônes extraites d’un fichier spécifié.</span><span class="sxs-lookup"><span data-stu-id="76eb9-106">Creates an array of handles to icons extracted from a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="76eb9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76eb9-107">Syntax</span></span>


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a><span data-ttu-id="76eb9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="76eb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76eb9-109">*pszFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-109">*pszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76eb9-110">Type : **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="76eb9-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="76eb9-111">Pointeur vers le nom de fichier à partir duquel extraire les icônes.</span><span class="sxs-lookup"><span data-stu-id="76eb9-111">A pointer to the file name from which to extract the icons.</span></span>

</dd> <dt>

<span data-ttu-id="76eb9-112">*nIconIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-112">*nIconIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76eb9-113">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="76eb9-113">Type: **int**</span></span>

<span data-ttu-id="76eb9-114">Index de la première icône à extraire de la ressource nommée dans *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="76eb9-114">The index of the first icon to extract from the resource named in *pszFileName*.</span></span>

</dd> <dt>

<span data-ttu-id="76eb9-115">*cxIcon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-115">*cxIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76eb9-116">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="76eb9-116">Type: **int**</span></span>

<span data-ttu-id="76eb9-117">Largeur souhaitée de l’icône.</span><span class="sxs-lookup"><span data-stu-id="76eb9-117">The desired width of the icon.</span></span> <span data-ttu-id="76eb9-118">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="76eb9-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="76eb9-119">*cyIcon* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-119">*cyIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76eb9-120">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="76eb9-120">Type: **int**</span></span>

<span data-ttu-id="76eb9-121">Hauteur souhaitée de l’icône.</span><span class="sxs-lookup"><span data-stu-id="76eb9-121">The desired height of the icon.</span></span> <span data-ttu-id="76eb9-122">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="76eb9-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="76eb9-123">*phIcon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-123">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76eb9-124">Type : \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="76eb9-124">Type: \**HICON\** _</span></span>

<span data-ttu-id="76eb9-125">Lorsque cette fonction est retournée, contient un pointeur vers le tableau de handles d’icône.</span><span class="sxs-lookup"><span data-stu-id="76eb9-125">When this function returns, contains a pointer to the array of icon handles.</span></span>

</dd> <dt>

<span data-ttu-id="76eb9-126">_pIconId \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-126">_pIconId\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76eb9-127">Type : \**uint \** _</span><span class="sxs-lookup"><span data-stu-id="76eb9-127">Type: \**UINT\** _</span></span>

<span data-ttu-id="76eb9-128">Lorsque cette fonction est retournée, contient un pointeur vers l’identificateur de ressource de l’icône extraite qui correspond le mieux au périphérique d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="76eb9-128">When this function returns, contains a pointer to the resource identifier of the extracted icon that best fits the current display device.</span></span> <span data-ttu-id="76eb9-129">Si aucun identificateur n’est disponible pour ce format, il contient 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="76eb9-129">If there is no identifier available for this format, it contains 0xFFFFFFFF.</span></span> <span data-ttu-id="76eb9-130">Si aucun identificateur ne peut être obtenu pour une autre raison, retourne la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="76eb9-130">If no identifier can be obtained for any other reason, returns zero.</span></span>

</dd> <dt>

<span data-ttu-id="76eb9-131">_nIcons \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-131">_nIcons\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76eb9-132">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="76eb9-132">Type: **UINT**</span></span>

<span data-ttu-id="76eb9-133">Nombre d’icônes à extraire de la ressource nommée dans *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="76eb9-133">The number of icons to extract from the resource named in *pszFileName*.</span></span> <span data-ttu-id="76eb9-134">Ce paramètre est valide uniquement lorsque la ressource est un fichier. exe ou. dll.</span><span class="sxs-lookup"><span data-stu-id="76eb9-134">This parameter is valid only when the resource is a .exe or .dll file.</span></span>

</dd> <dt>

<span data-ttu-id="76eb9-135">*indicateurs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-135">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76eb9-136">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="76eb9-136">Type: **UINT**</span></span>

<span data-ttu-id="76eb9-137">Indicateurs qui contrôlent cette fonction.</span><span class="sxs-lookup"><span data-stu-id="76eb9-137">The flags that control this function.</span></span> <span data-ttu-id="76eb9-138">Pour connaître les valeurs possibles, consultez le paramètre *fuLoad* de la fonction [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) .</span><span class="sxs-lookup"><span data-stu-id="76eb9-138">For possible values, see the *fuLoad* parameter of the [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76eb9-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="76eb9-139">Return value</span></span>

<span data-ttu-id="76eb9-140">Type : **uint**</span><span class="sxs-lookup"><span data-stu-id="76eb9-140">Type: **UINT**</span></span>

<span data-ttu-id="76eb9-141">Valeur différente de zéro en cas de réussite ; Sinon, zéro.</span><span class="sxs-lookup"><span data-stu-id="76eb9-141">A nonzero value if successful; otherwise, zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="76eb9-142">Notes</span><span class="sxs-lookup"><span data-stu-id="76eb9-142">Remarks</span></span>

<span data-ttu-id="76eb9-143">**SHExtractIconsW** extrait des types de fichiers suivants.</span><span class="sxs-lookup"><span data-stu-id="76eb9-143">**SHExtractIconsW** extracts from the following file types.</span></span>

-   <span data-ttu-id="76eb9-144">Fichier exécutable (.exe)</span><span class="sxs-lookup"><span data-stu-id="76eb9-144">Executable (.exe)</span></span>
-   <span data-ttu-id="76eb9-145">DLL (. dll)</span><span class="sxs-lookup"><span data-stu-id="76eb9-145">DLL (.dll)</span></span>
-   <span data-ttu-id="76eb9-146">Icône (. ico)</span><span class="sxs-lookup"><span data-stu-id="76eb9-146">Icon (.ico)</span></span>
-   <span data-ttu-id="76eb9-147">Curseur (. cur)</span><span class="sxs-lookup"><span data-stu-id="76eb9-147">Cursor (.cur)</span></span>
-   <span data-ttu-id="76eb9-148">Curseur animé (. ani)</span><span class="sxs-lookup"><span data-stu-id="76eb9-148">Animated cursor (.ani)</span></span>
-   <span data-ttu-id="76eb9-149">Bitmap (.bmp)</span><span class="sxs-lookup"><span data-stu-id="76eb9-149">Bitmap (.bmp)</span></span>

<span data-ttu-id="76eb9-150">Extractions à partir de Windows 3. *x* les fichiers exécutables 16 bits (. exe ou. dll) sont également pris en charge.</span><span class="sxs-lookup"><span data-stu-id="76eb9-150">Extractions from Windows 3.*x* 16-bit executable files (.exe or .dll) are also supported.</span></span>

<span data-ttu-id="76eb9-151">Les paramètres *cxIcon* et *cyIcon* spécifient la taille des icônes à extraire.</span><span class="sxs-lookup"><span data-stu-id="76eb9-151">The *cxIcon* and *cyIcon* parameters specify the size of the icons to extract.</span></span> <span data-ttu-id="76eb9-152">Deux tailles peuvent être extraites par le biais de chaque paramètre en fractionnant la valeur entre ses LOWORD et HIWORD.</span><span class="sxs-lookup"><span data-stu-id="76eb9-152">Two sizes can be extracted through each parameter by splitting the value between its LOWORD and HIWORD.</span></span> <span data-ttu-id="76eb9-153">Placez la première taille souhaitée dans le LOWORD du paramètre et la deuxième taille dans le HIWORD.</span><span class="sxs-lookup"><span data-stu-id="76eb9-153">Put the first desired size in the LOWORD of the parameter and the second size in the HIWORD.</span></span> <span data-ttu-id="76eb9-154">Par exemple, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) pour *cxIcon* et *cyIcon* extrait les icônes 24 et 48.</span><span class="sxs-lookup"><span data-stu-id="76eb9-154">For example, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) for both *cxIcon* and *cyIcon* extracts both 24 and 48 sized icons.</span></span>

<span data-ttu-id="76eb9-155">Le processus appelant est responsable de la destruction de toutes les icônes extraites par le biais de cette fonction en appelant la fonction [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) .</span><span class="sxs-lookup"><span data-stu-id="76eb9-155">The calling process is responsible for destroying all icons extracted through this function by calling the [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) function.</span></span>

<span data-ttu-id="76eb9-156">**SHExtractIconsW** n’est pas exporté par nom ou déclaré dans un fichier d’en-tête public.</span><span class="sxs-lookup"><span data-stu-id="76eb9-156">**SHExtractIconsW** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="76eb9-157">Pour l’utiliser, vous devez déclarer un prototype correspondant et utiliser [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour demander un pointeur de fonction à partir de Shell32.dll qui peut être utilisé pour appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="76eb9-157">To use it, you must declare a matching prototype and use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to request a function pointer from Shell32.dll that can be used to call this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="76eb9-158">Spécifications</span><span class="sxs-lookup"><span data-stu-id="76eb9-158">Requirements</span></span>



| <span data-ttu-id="76eb9-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76eb9-159">Requirement</span></span> | <span data-ttu-id="76eb9-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="76eb9-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76eb9-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76eb9-161">Minimum supported client</span></span><br/> | <span data-ttu-id="76eb9-162">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76eb9-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76eb9-163">Minimum supported server</span></span><br/> | <span data-ttu-id="76eb9-164">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76eb9-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="76eb9-165">DLL</span><span class="sxs-lookup"><span data-stu-id="76eb9-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76eb9-166"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="76eb9-166"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="76eb9-167">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="76eb9-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="76eb9-168">**SHExtractIconsW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="76eb9-168">**SHExtractIconsW** (Unicode)</span></span><br/>                                                                      |



 

 
