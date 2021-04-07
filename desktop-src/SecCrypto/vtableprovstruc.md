---
description: Contient des pointeurs vers des fonctions de rappel qui peuvent être utilisées par les fonctions du fournisseur de services de chiffrement (CSP).
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: VTableProvStruc, structure (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 99b9344c6951dc93972315d9b4f60752f1484d68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759459"
---
# <a name="vtableprovstruc-structure"></a><span data-ttu-id="5d3c0-103">VTableProvStruc, structure</span><span class="sxs-lookup"><span data-stu-id="5d3c0-103">VTableProvStruc structure</span></span>

<span data-ttu-id="5d3c0-104">La structure **VTableProvStruc** contient des pointeurs vers des fonctions de rappel qui peuvent être utilisées par les fonctions du [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="5d3c0-104">The **VTableProvStruc** structure contains pointers to callback functions that can be used by [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d3c0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d3c0-105">Syntax</span></span>


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a><span data-ttu-id="5d3c0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5d3c0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5d3c0-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="5d3c0-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="5d3c0-108">Valeur **DWORD** qui indique la version de la structure.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-108">A **DWORD** value that indicates the version of the structure.</span></span> <span data-ttu-id="5d3c0-109">Trois versions de cette structure sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-109">Three versions of this structure are used.</span></span> <span data-ttu-id="5d3c0-110">Les versions sont les numéros 1, 2 et 3, et déterminent les membres de la structure qui sont valides.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-110">The versions are number 1, 2, and 3, and determine which members of the structure are valid.</span></span> <span data-ttu-id="5d3c0-111">Les membres de la version 1 sont valides sur tous les systèmes qui prennent en charge cette structure.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-111">Version 1 members are valid on all systems that support this structure.</span></span>

<span data-ttu-id="5d3c0-112">Il s’agit d’un membre de la version 1.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-112">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="5d3c0-113">**FuncVerifyImage**</span><span class="sxs-lookup"><span data-stu-id="5d3c0-113">**FuncVerifyImage**</span></span>
</dt> <dd>

<span data-ttu-id="5d3c0-114">Adresse d’une fonction de rappel [**FuncVerifyImage**](funcverifyimage.md) que le CSP utilise pour vérifier la signature des dll que le CSP chargera.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-114">The address of a [**FuncVerifyImage**](funcverifyimage.md) callback function that the CSP uses to verify the signature of any DLLs that the CSP will load.</span></span> <span data-ttu-id="5d3c0-115">Toutes les dll auxiliaires dans lesquelles un CSP effectue des appels de fonction doivent être signées de la même manière (et avec la même clé) que la DLL CSP principale.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-115">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="5d3c0-116">Pour garantir cette signature, les dll auxiliaires doivent être chargées de manière dynamique à l’aide de la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) .</span><span class="sxs-lookup"><span data-stu-id="5d3c0-116">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="5d3c0-117">Mais avant le chargement de la DLL, la signature de la DLL doit être vérifiée.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-117">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="5d3c0-118">Le fournisseur CSP effectue cette vérification en appelant la fonction **FuncVerifyImage** , comme illustré dans l’exemple ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-118">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

<span data-ttu-id="5d3c0-119">Ce pointeur de fonction peut être stocké et utilisé jusqu’à ce que le contexte CSP soit libéré.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-119">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="5d3c0-120">Il s’agit d’un membre de la version 1.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-120">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="5d3c0-121">**FuncReturnhWnd**</span><span class="sxs-lookup"><span data-stu-id="5d3c0-121">**FuncReturnhWnd**</span></span>
</dt> <dd>

<span data-ttu-id="5d3c0-122">Adresse d’une fonction de rappel [**FuncReturnhWnd**](funcreturnhwnd.md) qui retourne le handle de fenêtre que le fournisseur de services Cloud doit utiliser comme parent ou propriétaire d’une interface utilisateur qui est affichée.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-122">The address of a [**FuncReturnhWnd**](funcreturnhwnd.md) callback function that returns the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span> <span data-ttu-id="5d3c0-123">Les fournisseurs de services de chiffrement qui ne communiquent pas directement avec l’utilisateur et les fournisseurs de services de chiffrement qui utilisent du matériel dédié à cet effet peuvent ignorer cette entrée.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-123">CSPs that do not communicate directly with the user and CSPs that use dedicated hardware for this purpose can ignore this entry.</span></span> <span data-ttu-id="5d3c0-124">Par défaut, ce handle de fenêtre est égal à zéro, mais une application peut définir cette valeur sur une autre valeur à l’aide de la fonction [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) pour définir la propriété **\_ \_ HWND du client pp** .</span><span class="sxs-lookup"><span data-stu-id="5d3c0-124">This window handle is zero by default, but an application can set this to a different value by using the [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) function to set the **PP\_CLIENT\_HWND** property.</span></span>

<span data-ttu-id="5d3c0-125">Ce pointeur de fonction peut être stocké et utilisé jusqu’à ce que le contexte CSP soit libéré.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-125">This function pointer can be stored and used until the CSP context is released.</span></span>

<span data-ttu-id="5d3c0-126">Il s’agit d’un membre de la version 1.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-126">This is a version 1 member.</span></span>

</dd> <dt>

<span data-ttu-id="5d3c0-127">**dwProvType**</span><span class="sxs-lookup"><span data-stu-id="5d3c0-127">**dwProvType**</span></span>
</dt> <dd>

<span data-ttu-id="5d3c0-128">Valeur **DWORD** qui spécifie le type de fournisseur à acquérir.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-128">A **DWORD** value that specifies the type of provider to acquire.</span></span> <span data-ttu-id="5d3c0-129">Les [*types de fournisseurs*](../secgloss/p-gly.md) suivants sont prédéfinis et sont décrits en détail dans [interopérabilité des fournisseurs de services](https://www.bing.com/search?q=CSP+Interoperability)Cloud :</span><span class="sxs-lookup"><span data-stu-id="5d3c0-129">The following [*provider types*](../secgloss/p-gly.md) are predefined and are discussed in detail in [CSP Interoperability](https://www.bing.com/search?q=CSP+Interoperability):</span></span>

-   <span data-ttu-id="5d3c0-130">PROUVER \_ RSA \_ Full</span><span class="sxs-lookup"><span data-stu-id="5d3c0-130">PROV\_RSA\_FULL</span></span>
-   <span data-ttu-id="5d3c0-131">PROUVER \_ RSA \_ SIG</span><span class="sxs-lookup"><span data-stu-id="5d3c0-131">PROV\_RSA\_SIG</span></span>
-   <span data-ttu-id="5d3c0-132">DSS PROVen \_</span><span class="sxs-lookup"><span data-stu-id="5d3c0-132">PROV\_DSS</span></span>
-   <span data-ttu-id="5d3c0-133">\_Fortezza-Fortezza</span><span class="sxs-lookup"><span data-stu-id="5d3c0-133">PROV\_FORTEZZA</span></span>
-   <span data-ttu-id="5d3c0-134">PROUVER \_ MS \_ Exchange</span><span class="sxs-lookup"><span data-stu-id="5d3c0-134">PROV\_MS\_EXCHANGE</span></span>

<span data-ttu-id="5d3c0-135">Il s’agit d’un membre de la version 2.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-135">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="5d3c0-136">**pbContextInfo**</span><span class="sxs-lookup"><span data-stu-id="5d3c0-136">**pbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="5d3c0-137">Pointeur vers un tableau d’informations de contexte.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-137">A pointer to an array of context information.</span></span> <span data-ttu-id="5d3c0-138">Les membres **pbContextInfo** et **cbContextInfo** déterminent ensemble le jeu d’informations utilisé quand une fonction [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) est appelée avec les informations de \_ contexte pp \_ définies.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-138">The **pbContextInfo** and **cbContextInfo** members together determine the information set used when a [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**) function is called with PP\_CONTEXT\_INFO set.</span></span>

<span data-ttu-id="5d3c0-139">Il s’agit d’un membre de la version 2.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-139">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="5d3c0-140">**cbContextInfo**</span><span class="sxs-lookup"><span data-stu-id="5d3c0-140">**cbContextInfo**</span></span>
</dt> <dd>

<span data-ttu-id="5d3c0-141">Valeur **DWORD** qui indique le nombre d’éléments dans le tableau **pbContextInfo** .</span><span class="sxs-lookup"><span data-stu-id="5d3c0-141">A **DWORD** value that indicates the number of elements in the **pbContextInfo** array.</span></span>

<span data-ttu-id="5d3c0-142">Il s’agit d’un membre de la version 2.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-142">This is a version 2 member.</span></span>

</dd> <dt>

<span data-ttu-id="5d3c0-143">**pszProvName**</span><span class="sxs-lookup"><span data-stu-id="5d3c0-143">**pszProvName**</span></span>
</dt> <dd>

<span data-ttu-id="5d3c0-144">Chaîne qui contient le nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-144">A string that contains the name of the provider.</span></span>

<span data-ttu-id="5d3c0-145">Il s’agit d’un membre de la version 3.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-145">This is a version 3 member.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d3c0-146">Notes</span><span class="sxs-lookup"><span data-stu-id="5d3c0-146">Remarks</span></span>

<span data-ttu-id="5d3c0-147">Les pointeurs de la structure **VTableProvStruc** sont uniquement disponibles dans la fonction [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) .</span><span class="sxs-lookup"><span data-stu-id="5d3c0-147">The pointers in the **VTableProvStruc** structure are only available within the [**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**) function.</span></span> <span data-ttu-id="5d3c0-148">Si des membres de la structure sont nécessaires après l’exécution d’un appel à **CPAcquireContext** , des copies des éléments de structure nécessaires doivent être effectuées par le CSP.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-148">If members of the structure are needed after a call to **CPAcquireContext** is completed, copies of the needed structure elements must be made by the CSP.</span></span> <span data-ttu-id="5d3c0-149">Les pointeurs de fonction de cette structure peuvent être stockés et utilisés jusqu’à ce que le contexte du CSP soit libéré.</span><span class="sxs-lookup"><span data-stu-id="5d3c0-149">The function pointers in this structure can be stored and used until the CSP context is released.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d3c0-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d3c0-150">Requirements</span></span>



| <span data-ttu-id="5d3c0-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d3c0-151">Requirement</span></span> | <span data-ttu-id="5d3c0-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d3c0-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5d3c0-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d3c0-153">Minimum supported client</span></span><br/> | <span data-ttu-id="5d3c0-154">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d3c0-154">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d3c0-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d3c0-155">Minimum supported server</span></span><br/> | <span data-ttu-id="5d3c0-156">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d3c0-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5d3c0-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d3c0-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d3c0-158"><dt>Cspdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d3c0-158"><dt>Cspdk.h</dt></span></span> </dl> |
| <span data-ttu-id="5d3c0-159">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="5d3c0-159">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="5d3c0-160">**VTableProvStrucW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="5d3c0-160">**VTableProvStrucW** (Unicode)</span></span><br/>                                          |



 

 
