---
description: Crée un moniker qui représente un composant matériel et son gestionnaire d’événements associé. La lecture automatique utilise cette fonction pour permettre aux applications d’utiliser des événements de lecture automatique.
title: CreateHardwareEventMoniker fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: c22f01835f9c526e95a4330e6ad35d370421e604
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841240"
---
# <a name="createhardwareeventmoniker-function"></a><span data-ttu-id="dec8e-104">CreateHardwareEventMoniker fonction)</span><span class="sxs-lookup"><span data-stu-id="dec8e-104">CreateHardwareEventMoniker function</span></span>

<span data-ttu-id="dec8e-105">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dec8e-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="dec8e-106">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dec8e-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="dec8e-107">Crée un moniker qui représente un composant matériel et son gestionnaire d’événements associé.</span><span class="sxs-lookup"><span data-stu-id="dec8e-107">Creates a moniker representing a hardware component and its associated event handler.</span></span> <span data-ttu-id="dec8e-108">La lecture automatique utilise cette fonction pour permettre aux applications d’utiliser des événements de lecture automatique.</span><span class="sxs-lookup"><span data-stu-id="dec8e-108">AutoPlay uses this function to allow applications to use AutoPlay events.</span></span>

## <a name="syntax"></a><span data-ttu-id="dec8e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dec8e-109">Syntax</span></span>


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a><span data-ttu-id="dec8e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dec8e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dec8e-111">*CLSID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dec8e-111">*clsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dec8e-112">Type : **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="dec8e-112">Type: **REFCLSID**</span></span>

<span data-ttu-id="dec8e-113">ID de la classe à laquelle le moniker est lié.</span><span class="sxs-lookup"><span data-stu-id="dec8e-113">The ID of the class to which the moniker binds.</span></span>

</dd> <dt>

<span data-ttu-id="dec8e-114">*pszEventHandler* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dec8e-114">*pszEventHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dec8e-115">Type : **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="dec8e-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="dec8e-116">Nom du gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="dec8e-116">The name of the event handler.</span></span>

</dd> <dt>

<span data-ttu-id="dec8e-117">*ppmoniker* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dec8e-117">*ppmoniker* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dec8e-118">Type : **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span><span class="sxs-lookup"><span data-stu-id="dec8e-118">Type: **[**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span></span>

<span data-ttu-id="dec8e-119">Adresse d’une variable pointeur qui reçoit le pointeur d’interface [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) .</span><span class="sxs-lookup"><span data-stu-id="dec8e-119">The address of a pointer variable that receives the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dec8e-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dec8e-120">Return value</span></span>

<span data-ttu-id="dec8e-121">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dec8e-121">Type: **HRESULT**</span></span>

<span data-ttu-id="dec8e-122">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="dec8e-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="dec8e-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="dec8e-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="dec8e-124">Notes</span><span class="sxs-lookup"><span data-stu-id="dec8e-124">Remarks</span></span>

<span data-ttu-id="dec8e-125">Utilisez **CreateHardwareEventMoniker** lors de l’inscription d’applications en cours d’exécution afin que ces applications aient accès aux événements de lecture automatique.</span><span class="sxs-lookup"><span data-stu-id="dec8e-125">Use **CreateHardwareEventMoniker** when registering running applications so that those applications have access to AutoPlay events.</span></span> <span data-ttu-id="dec8e-126">Pour utiliser des événements de lecture automatique dans des applications en cours d’exécution, vous devez d’abord créer un nouveau composant qui implémente l’interface [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) .</span><span class="sxs-lookup"><span data-stu-id="dec8e-126">To use AutoPlay events in running applications, you must first create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span> <span data-ttu-id="dec8e-127">Initialisez cette interface avec la valeur InitCmdLine de l’entrée du gestionnaire particulier sous la clé des **gestionnaires** , car la lecture automatique n’appelle pas la méthode [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) .</span><span class="sxs-lookup"><span data-stu-id="dec8e-127">Initialize this interface with the InitCmdLine value from the particular handler's entry under the **Handlers** key, because AutoPlay does not call the [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method.</span></span>

<span data-ttu-id="dec8e-128">Vous devez appeler **CreateHardwareEventMoniker** pour obtenir un moniker qui représente votre composant et son gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="dec8e-128">You should call **CreateHardwareEventMoniker** to get a moniker that represents your component and its event handler.</span></span> <span data-ttu-id="dec8e-129">Ensuite, utilisez la valeur retournée dans le paramètre *ppmoniker* pour inscrire votre composant dans la table ROT (Running Object Table) comme indiqué dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="dec8e-129">Then, use the value returned in the *ppmoniker* parameter to register your component in the running object table (ROT) as shown in the example.</span></span>

<span data-ttu-id="dec8e-130">Notez que **CreateHardwareEventMoniker** n’est pas défini dans un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="dec8e-130">Note that **CreateHardwareEventMoniker** is not defined in a header file.</span></span> <span data-ttu-id="dec8e-131">Pour l’utiliser dans votre code, vous devez obtenir un handle vers le fichier Shsvcs.dll par le biais d’un appel à [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="dec8e-131">To use it in your code, you must obtain a handle to the Shsvcs.dll file through a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span> <span data-ttu-id="dec8e-132">Vous utilisez ensuite ce handle dans un appel à [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour obtenir une instance de la fonction **CreateHardwareEventMoniker** .</span><span class="sxs-lookup"><span data-stu-id="dec8e-132">You then use that handle in a call to [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain an instance of the **CreateHardwareEventMoniker** function.</span></span>

<span data-ttu-id="dec8e-133">L’appel à [**IRunningObjectTable :: Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) exige que vous entriez les informations **AppID** suivantes dans le registre.</span><span class="sxs-lookup"><span data-stu-id="dec8e-133">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that you enter the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a><span data-ttu-id="dec8e-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="dec8e-134">Requirements</span></span>



| <span data-ttu-id="dec8e-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dec8e-135">Requirement</span></span> | <span data-ttu-id="dec8e-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="dec8e-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dec8e-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dec8e-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dec8e-138">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dec8e-138">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dec8e-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dec8e-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dec8e-140">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dec8e-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="dec8e-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="dec8e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="dec8e-142"><dt>Aucun</dt></span><span class="sxs-lookup"><span data-stu-id="dec8e-142"><dt>None</dt></span></span> </dl>       |
| <span data-ttu-id="dec8e-143">DLL</span><span class="sxs-lookup"><span data-stu-id="dec8e-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dec8e-144"><dt>Shsvcs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dec8e-144"><dt>Shsvcs.dll</dt></span></span> </dl> |



 

 
