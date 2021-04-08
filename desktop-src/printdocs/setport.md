---
description: La fonction SetPort définit l’état associé à un port d’imprimante.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: SetPort, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034464"
---
# <a name="setport-function"></a><span data-ttu-id="2bf58-103">SetPort fonction)</span><span class="sxs-lookup"><span data-stu-id="2bf58-103">SetPort function</span></span>

<span data-ttu-id="2bf58-104">La fonction **SetPort** définit l’état associé à un port d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2bf58-104">The **SetPort** function sets the status associated with a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bf58-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bf58-105">Syntax</span></span>


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a><span data-ttu-id="2bf58-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bf58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bf58-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2bf58-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf58-108">Pointeur vers une chaîne se terminant par zéro qui spécifie le nom du serveur d’impression auquel le port est connecté.</span><span class="sxs-lookup"><span data-stu-id="2bf58-108">Pointer to a zero-terminated string that specifies the name of the printer server to which the port is connected.</span></span> <span data-ttu-id="2bf58-109">Affectez la valeur **null** à ce paramètre si le port se trouve sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="2bf58-109">Set this parameter to **NULL** if the port is on the local machine.</span></span>

</dd> <dt>

<span data-ttu-id="2bf58-110">*pPortName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2bf58-110">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf58-111">Pointeur vers une chaîne se terminant par zéro qui spécifie le nom du port d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2bf58-111">Pointer to a zero-terminated string that specifies the name of the printer port.</span></span>

</dd> <dt>

<span data-ttu-id="2bf58-112">*dwLevel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2bf58-112">*dwLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf58-113">Spécifie le type de structure vers lequel pointe le paramètre *pPortInfo* .</span><span class="sxs-lookup"><span data-stu-id="2bf58-113">Specifies the type of structure pointed to by the *pPortInfo* parameter.</span></span>

<span data-ttu-id="2bf58-114">Cette valeur doit être 3, ce qui correspond à une structure de données de [**port \_ informations \_ 3**](port-info-3.md) .</span><span class="sxs-lookup"><span data-stu-id="2bf58-114">This value must be 3, which corresponds to a [**PORT\_INFO\_3**](port-info-3.md) data structure.</span></span>

</dd> <dt>

<span data-ttu-id="2bf58-115">*pPortInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2bf58-115">*pPortInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bf58-116">Pointeur vers une structure d' [**informations de port \_ \_ 3**](port-info-3.md) qui contient les informations d’état de port à définir.</span><span class="sxs-lookup"><span data-stu-id="2bf58-116">Pointer to a [**PORT\_INFO\_3**](port-info-3.md) structure that contains the port status information to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bf58-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2bf58-117">Return value</span></span>

<span data-ttu-id="2bf58-118">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2bf58-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2bf58-119">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="2bf58-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bf58-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2bf58-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2bf58-121">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="2bf58-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="2bf58-122">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="2bf58-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="2bf58-123">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="2bf58-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="2bf58-124">L’appelant de la fonction **SetPort** doit s’exécuter en tant qu’administrateur.</span><span class="sxs-lookup"><span data-stu-id="2bf58-124">The caller of the **SetPort** function must be executing as an Administrator.</span></span> <span data-ttu-id="2bf58-125">En outre, si l’appelant est un moniteur de port ou un moniteur de langage, il doit appeler [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) pour arrêter l’emprunt d’identité avant d’appeler **SetPort**.</span><span class="sxs-lookup"><span data-stu-id="2bf58-125">Additionally, if the caller is a Port Monitor or Language Monitor, it must call [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) to cease impersonation before it calls **SetPort**.</span></span>

<span data-ttu-id="2bf58-126">Tous les programmes qui appellent **SetPort** doivent disposer d’un accès serveur \_ \_ administrer l’accès au serveur auquel le port est connecté.</span><span class="sxs-lookup"><span data-stu-id="2bf58-126">All programs that call **SetPort** must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="2bf58-127">Lorsque vous définissez une valeur d’état de port d’imprimante avec la valeur de gravité \_ \_ erreur de type état du port \_ , le spouleur d’impression cesse d’envoyer des travaux au port.</span><span class="sxs-lookup"><span data-stu-id="2bf58-127">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="2bf58-128">Le spouleur d’impression reprend l’envoi des travaux au port lorsque l’état du port est effacé par un autre appel à **SetPort**.</span><span class="sxs-lookup"><span data-stu-id="2bf58-128">The print spooler resumes sending jobs to the port when the port status is cleared by another call to **SetPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bf58-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bf58-129">Requirements</span></span>



| <span data-ttu-id="2bf58-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bf58-130">Requirement</span></span> | <span data-ttu-id="2bf58-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bf58-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bf58-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bf58-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2bf58-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bf58-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2bf58-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bf58-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2bf58-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bf58-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2bf58-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="2bf58-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bf58-137"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2bf58-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2bf58-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2bf58-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="2bf58-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bf58-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2bf58-140">DLL</span><span class="sxs-lookup"><span data-stu-id="2bf58-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2bf58-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="2bf58-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="2bf58-142">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="2bf58-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2bf58-143">**SetPortW** (Unicode) et **SetPortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2bf58-143">**SetPortW** (Unicode) and **SetPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="2bf58-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bf58-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bf58-145">Impression</span><span class="sxs-lookup"><span data-stu-id="2bf58-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2bf58-146">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="2bf58-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2bf58-147">**\_Informations sur le port \_ 3**</span><span class="sxs-lookup"><span data-stu-id="2bf58-147">**PORT\_INFO\_3**</span></span>](port-info-3.md)
</dt> </dl>

 

