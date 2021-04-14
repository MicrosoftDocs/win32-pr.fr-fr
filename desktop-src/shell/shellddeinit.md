---
description: Inscrit les services de l’échange dynamique de données interpréteur de commandes (DDE) dans le processus en cours, en avertissant le système que le processus en cours souhaite héberger des objets DDE.
ms.assetid: d7f65d6a-a697-475b-a739-c7950b7f4d5d
title: ShellDDEInit fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellDDEInit
api_type:
- DllExport
api_location:
- Shdocvw.dll
ms.openlocfilehash: cb2f4639d97a99cd063f372e303fd48b7a1d6e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973594"
---
# <a name="shellddeinit-function"></a><span data-ttu-id="ae965-103">ShellDDEInit fonction)</span><span class="sxs-lookup"><span data-stu-id="ae965-103">ShellDDEInit function</span></span>

<span data-ttu-id="ae965-104">Inscrit les services de l’échange dynamique de données interpréteur de commandes (DDE) dans le processus en cours, en avertissant le système que le processus en cours souhaite héberger des objets DDE.</span><span class="sxs-lookup"><span data-stu-id="ae965-104">Registers the Shell Dynamic Data Exchange (DDE) services in the current process, notifying the system that the current process wishes to host DDE objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae965-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae965-105">Syntax</span></span>


```C++
void ShellDDEInit(
  _In_ BOOL init
);
```



## <a name="parameters"></a><span data-ttu-id="ae965-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae965-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae965-107">*init* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae965-107">*init* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae965-108">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="ae965-108">Type: **BOOL**</span></span>

<span data-ttu-id="ae965-109">**True** pour inscrire le processus en cours en tant qu’hôte DDE ; **False** pour annuler son inscription.</span><span class="sxs-lookup"><span data-stu-id="ae965-109">**TRUE** to register the current process as DDE host; **FALSE** to unregister it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae965-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ae965-110">Return value</span></span>

<span data-ttu-id="ae965-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="ae965-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae965-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ae965-112">Remarks</span></span>

<span data-ttu-id="ae965-113">Le processus qui appelle cette fonction agit en tant qu’interpréteur de commandes et est utilisé pour afficher le contenu des dossiers ouverts avec le verbe « Open » [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="ae965-113">The process that calls this function acts as the Shell and is used to view the content of folders opened with the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) 'open' verb.</span></span>

<span data-ttu-id="ae965-114">Cette fonction n’a pas de fichier d’en-tête ou de bibliothèque associé et doit donc être appelée par valeur ordinale.</span><span class="sxs-lookup"><span data-stu-id="ae965-114">This function does not have an associated header or library file so it must be called by ordinal value.</span></span> <span data-ttu-id="ae965-115">Appelez [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Shdocvw.dll) pour obtenir un handle de module.</span><span class="sxs-lookup"><span data-stu-id="ae965-115">Call [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) with the DLL name (Shdocvw.dll) to obtain a module handle.</span></span> <span data-ttu-id="ae965-116">Appelez ensuite [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le numéro ordinal de fonction 118 pour récupérer l’adresse de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ae965-116">Then call [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) with that module handle and the function ordinal number 118 to get the address of the function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae965-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ae965-117">Requirements</span></span>



| <span data-ttu-id="ae965-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae965-118">Requirement</span></span> | <span data-ttu-id="ae965-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae965-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae965-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae965-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ae965-121">Windows XP, applications de bureau Windows 2000 professionnel \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae965-121">Windows XP, Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ae965-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae965-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ae965-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae965-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ae965-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ae965-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae965-125"><dt>Shdocvw.dll (version 6,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="ae965-125"><dt>Shdocvw.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
