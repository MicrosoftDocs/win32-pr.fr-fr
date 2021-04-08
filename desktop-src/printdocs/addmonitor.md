---
description: La fonction AddMonitor installe un moniteur de port local et lie les fichiers de configuration, de données et de surveillance.
ms.assetid: 6a556422-5360-42d2-b177-dba0498c06d8
title: AddMonitor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMonitor
- AddMonitorA
- AddMonitorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 40b45c4dc05580837a2cf4a001cf8d18e646e5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035226"
---
# <a name="addmonitor-function"></a><span data-ttu-id="ce129-103">AddMonitor fonction)</span><span class="sxs-lookup"><span data-stu-id="ce129-103">AddMonitor function</span></span>

<span data-ttu-id="ce129-104">La fonction **AddMonitor** installe un moniteur de port local et lie les fichiers de configuration, de données et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="ce129-104">The **AddMonitor** function installs a local port monitor and links the configuration, data, and monitor files.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce129-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce129-105">Syntax</span></span>


```C++
BOOL AddMonitor(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pMonitors
);
```



## <a name="parameters"></a><span data-ttu-id="ce129-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce129-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce129-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce129-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce129-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel l’analyse doit être installée.</span><span class="sxs-lookup"><span data-stu-id="ce129-108">A pointer to a null-terminated string that specifies the name of the server on which the monitor should be installed.</span></span> <span data-ttu-id="ce129-109">Pour les systèmes qui prennent uniquement en charge l’installation locale de moniteurs, cette chaîne doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ce129-109">For systems that support only local installation of monitors, this string should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ce129-110">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce129-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce129-111">Version de la structure vers laquelle *pMonitors* pointe.</span><span class="sxs-lookup"><span data-stu-id="ce129-111">The version of the structure to which *pMonitors* points.</span></span> <span data-ttu-id="ce129-112">Cette valeur doit être 2.</span><span class="sxs-lookup"><span data-stu-id="ce129-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="ce129-113">*pMonitors* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce129-113">*pMonitors* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce129-114">Pointeur vers une structure [**d' \_ informations \_ d’analyse 2**](monitor-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="ce129-114">A pointer to a [**MONITOR\_INFO\_2**](monitor-info-2.md) structure.</span></span> <span data-ttu-id="ce129-115">Si le membre **pEnvironment** de la structure *pMonitors* est **null**, l’environnement actuel de l’appelant (client), et non de la destination (serveur), est utilisé.</span><span class="sxs-lookup"><span data-stu-id="ce129-115">If the **pEnvironment** member of the *pMonitors* structure is **NULL**, the current environment of the caller (client), not of the destination (server), is used.</span></span>

<span data-ttu-id="ce129-116">Notez que l’appel échoue si l’environnement ne correspond pas à l’environnement du serveur, autrement dit, vous pouvez uniquement ajouter une analyse écrite pour l’architecture du serveur.</span><span class="sxs-lookup"><span data-stu-id="ce129-116">Note that the call will fail if the environment does not match the environment of the server, that is, you can only add a monitor that was written for the architecture of the server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce129-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce129-117">Return value</span></span>

<span data-ttu-id="ce129-118">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ce129-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ce129-119">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ce129-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce129-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ce129-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ce129-121">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ce129-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ce129-122">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="ce129-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ce129-123">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="ce129-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ce129-124">L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="ce129-124">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="ce129-125">Avant qu’une application appelle la fonction **AddMonitor** , tous les fichiers requis par le moniteur doivent être copiés dans le répertoire system32.</span><span class="sxs-lookup"><span data-stu-id="ce129-125">Before an application calls the **AddMonitor** function, all files required by the monitor must be copied to the SYSTEM32 directory.</span></span>

<span data-ttu-id="ce129-126">Pour déterminer les moniteurs de port actuellement installés, appelez la fonction [**EnumMonitors**](enummonitors.md) .</span><span class="sxs-lookup"><span data-stu-id="ce129-126">To determine the port monitors that are currently installed, call the [**EnumMonitors**](enummonitors.md) function.</span></span>

<span data-ttu-id="ce129-127">Pour supprimer un moniteur ajouté par **AddMonitor**, appelez la fonction [**DeleteMonitor**](deletemonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="ce129-127">To remove a monitor added by **AddMonitor**, call the [**DeleteMonitor**](deletemonitor.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce129-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce129-128">Requirements</span></span>



| <span data-ttu-id="ce129-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce129-129">Requirement</span></span> | <span data-ttu-id="ce129-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce129-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce129-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce129-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ce129-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce129-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ce129-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce129-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ce129-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce129-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ce129-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce129-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce129-136"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce129-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ce129-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce129-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce129-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce129-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ce129-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ce129-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce129-140"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ce129-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ce129-141">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="ce129-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ce129-142">**AddMonitorW** (Unicode) et **AddMonitorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ce129-142">**AddMonitorW** (Unicode) and **AddMonitorA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="ce129-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce129-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce129-144">Impression</span><span class="sxs-lookup"><span data-stu-id="ce129-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ce129-145">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="ce129-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ce129-146">**DeleteMonitor**</span><span class="sxs-lookup"><span data-stu-id="ce129-146">**DeleteMonitor**</span></span>](deletemonitor.md)
</dt> <dt>

[<span data-ttu-id="ce129-147">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="ce129-147">**EnumMonitors**</span></span>](enummonitors.md)
</dt> <dt>

[<span data-ttu-id="ce129-148">**\_Informations sur le moniteur \_ 2**</span><span class="sxs-lookup"><span data-stu-id="ce129-148">**MONITOR\_INFO\_2**</span></span>](monitor-info-2.md)
</dt> </dl>

 

