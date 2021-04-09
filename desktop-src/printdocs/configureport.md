---
description: La fonction ConfigurePort affiche la boîte de dialogue de configuration du port pour un port sur le serveur spécifié.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: ConfigurePort, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 64f9b3f2e0b0896afdc878477c6e45f8916268a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951951"
---
# <a name="configureport-function"></a><span data-ttu-id="84796-103">ConfigurePort fonction)</span><span class="sxs-lookup"><span data-stu-id="84796-103">ConfigurePort function</span></span>

<span data-ttu-id="84796-104">La fonction **ConfigurePort** affiche la boîte de dialogue de configuration du port pour un port sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="84796-104">The **ConfigurePort** function displays the port-configuration dialog box for a port on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="84796-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84796-105">Syntax</span></span>


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="84796-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84796-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84796-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84796-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84796-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le port spécifié existe.</span><span class="sxs-lookup"><span data-stu-id="84796-108">Pointer to a null-terminated string that specifies the name of the server on which the specified port exists.</span></span> <span data-ttu-id="84796-109">Si ce paramètre a la **valeur null**, le port est local.</span><span class="sxs-lookup"><span data-stu-id="84796-109">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="84796-110">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84796-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84796-111">Handle vers la fenêtre parente de la boîte de dialogue Configuration du port.</span><span class="sxs-lookup"><span data-stu-id="84796-111">Handle to the parent window of the port-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="84796-112">*pPortName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="84796-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84796-113">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du port à configurer.</span><span class="sxs-lookup"><span data-stu-id="84796-113">Pointer to a null-terminated string that specifies the name of the port to be configured.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84796-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84796-114">Return value</span></span>

<span data-ttu-id="84796-115">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="84796-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="84796-116">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="84796-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="84796-117">Notes</span><span class="sxs-lookup"><span data-stu-id="84796-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="84796-118">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="84796-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="84796-119">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="84796-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="84796-120">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="84796-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="84796-121">Avant d’appeler la fonction **ConfigurePort** , une application doit appeler la fonction [**EnumPorts**](enumports.md) pour déterminer les noms de ports valides.</span><span class="sxs-lookup"><span data-stu-id="84796-121">Before calling the **ConfigurePort** function, an application should call the [**EnumPorts**](enumports.md) function to determine valid port names.</span></span>

## <a name="requirements"></a><span data-ttu-id="84796-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84796-122">Requirements</span></span>



| <span data-ttu-id="84796-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84796-123">Requirement</span></span> | <span data-ttu-id="84796-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="84796-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84796-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84796-125">Minimum supported client</span></span><br/> | <span data-ttu-id="84796-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84796-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="84796-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84796-127">Minimum supported server</span></span><br/> | <span data-ttu-id="84796-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84796-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="84796-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="84796-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="84796-130"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84796-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="84796-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="84796-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="84796-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="84796-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="84796-133">DLL</span><span class="sxs-lookup"><span data-stu-id="84796-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84796-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="84796-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="84796-135">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="84796-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="84796-136">**ConfigurePortW** (Unicode) et **ConfigurePortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="84796-136">**ConfigurePortW** (Unicode) and **ConfigurePortA** (ANSI)</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="84796-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84796-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84796-138">Impression</span><span class="sxs-lookup"><span data-stu-id="84796-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="84796-139">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="84796-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="84796-140">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="84796-140">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




