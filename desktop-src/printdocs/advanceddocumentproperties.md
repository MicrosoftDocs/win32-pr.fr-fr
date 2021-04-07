---
description: La fonction AdvancedDocumentProperties affiche une boîte de dialogue de configuration de l’imprimante pour l’imprimante spécifiée, ce qui permet à l’utilisateur de configurer cette imprimante.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: AdvancedDocumentProperties, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759561"
---
# <a name="advanceddocumentproperties-function"></a><span data-ttu-id="b4300-103">AdvancedDocumentProperties fonction)</span><span class="sxs-lookup"><span data-stu-id="b4300-103">AdvancedDocumentProperties function</span></span>

<span data-ttu-id="b4300-104">La fonction **AdvancedDocumentProperties** affiche une boîte de dialogue de configuration de l’imprimante pour l’imprimante spécifiée, ce qui permet à l’utilisateur de configurer cette imprimante.</span><span class="sxs-lookup"><span data-stu-id="b4300-104">The **AdvancedDocumentProperties** function displays a printer-configuration dialog box for the specified printer, allowing the user to configure that printer.</span></span>

<span data-ttu-id="b4300-105">Cette fonction est un cas particulier de la fonction [**DocumentProperties**](documentproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="b4300-105">This function is a special case of the [**DocumentProperties**](documentproperties.md) function.</span></span> <span data-ttu-id="b4300-106">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="b4300-106">For more details, see the Remarks section.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4300-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4300-107">Syntax</span></span>


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a><span data-ttu-id="b4300-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4300-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4300-109">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4300-109">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4300-110">Handle de la fenêtre parente de la boîte de dialogue de configuration de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b4300-110">A handle to the parent window of the printer-configuration dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="b4300-111">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4300-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4300-112">Handle d’un objet Printer.</span><span class="sxs-lookup"><span data-stu-id="b4300-112">A handle to a printer object.</span></span> <span data-ttu-id="b4300-113">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b4300-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="b4300-114">*pDeviceName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4300-114">*pDeviceName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4300-115">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’appareil pour lequel une boîte de dialogue de configuration de l’imprimante doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="b4300-115">A pointer to a null-terminated string specifying the name of the device for which a printer-configuration dialog box should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="b4300-116">*pDevModeOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b4300-116">*pDevModeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4300-117">Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui contient les données de configuration spécifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b4300-117">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that will contain the configuration data specified by the user.</span></span>

</dd> <dt>

<span data-ttu-id="b4300-118">*pDevModeInput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4300-118">*pDevModeInput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4300-119">Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui contient les données de configuration utilisées pour initialiser les contrôles de la boîte de dialogue de configuration de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b4300-119">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that contains the configuration data used to initialize the controls of the printer-configuration dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4300-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4300-120">Return value</span></span>

<span data-ttu-id="b4300-121">Si la fonction [**DocumentProperties**](documentproperties.md) avec ces paramètres réussit, la valeur de retour de **AdvancedDocumentProperties** est 1.</span><span class="sxs-lookup"><span data-stu-id="b4300-121">If the [**DocumentProperties**](documentproperties.md) function with these parameters is successful, the return value of **AdvancedDocumentProperties** is 1.</span></span> <span data-ttu-id="b4300-122">Sinon, la valeur de retour est zéro.</span><span class="sxs-lookup"><span data-stu-id="b4300-122">Otherwise, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4300-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b4300-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b4300-124">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b4300-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b4300-125">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="b4300-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b4300-126">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="b4300-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b4300-127">Cette fonction peut uniquement afficher la boîte de dialogue Configuration de l’imprimante pour permettre à un utilisateur de la configurer.</span><span class="sxs-lookup"><span data-stu-id="b4300-127">This function can only display the printer-configuration dialog box so a user can configure it.</span></span> <span data-ttu-id="b4300-128">Pour plus de contrôle, utilisez [**DocumentProperties**](documentproperties.md).</span><span class="sxs-lookup"><span data-stu-id="b4300-128">For more control, use [**DocumentProperties**](documentproperties.md).</span></span> <span data-ttu-id="b4300-129">Les paramètres d’entrée de cette fonction sont passés directement à **DocumentProperties** et la valeur *fMode* est définie sur DM \_ dans la \_ mémoire tampon \| DM dans le \_ tampon de sortie de l' \_ invite \| DM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b4300-129">The input parameters for this function are passed directly to **DocumentProperties** and the *fMode* value is set to DM\_IN\_BUFFER \| DM\_IN\_PROMPT \| DM\_OUT\_BUFFER.</span></span> <span data-ttu-id="b4300-130">Contrairement à **DocumentProperties**, cette fonction retourne uniquement 1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="b4300-130">Unlike **DocumentProperties**, this function only returns 1 or 0.</span></span> <span data-ttu-id="b4300-131">Ainsi, vous ne pouvez pas déterminer la taille requise de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en affectant à *pDevMode* la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="b4300-131">Thus, you cannot determine the required size of [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) by setting *pDevMode* to zero.</span></span>

<span data-ttu-id="b4300-132">Une application peut obtenir le nom désigné par le paramètre *pDeviceName* en appelant la fonction [**GetPrinter**](getprinter.md) , puis en examinant le membre **pPrinterName** de la structure d' [**informations d’imprimante \_ \_ 2**](printer-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="b4300-132">An application can obtain the name pointed to by the *pDeviceName* parameter by calling the [**GetPrinter**](getprinter.md) function and then examining the **pPrinterName** member of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4300-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4300-133">Requirements</span></span>



| <span data-ttu-id="b4300-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4300-134">Requirement</span></span> | <span data-ttu-id="b4300-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4300-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4300-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4300-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b4300-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4300-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b4300-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4300-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b4300-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b4300-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b4300-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4300-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4300-141"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b4300-141"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b4300-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4300-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="b4300-143"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4300-143"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b4300-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b4300-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4300-145"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b4300-145"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b4300-146">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="b4300-146">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b4300-147">**AdvancedDocumentPropertiesW** (Unicode) et **AdvancedDocumentPropertiesA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b4300-147">**AdvancedDocumentPropertiesW** (Unicode) and **AdvancedDocumentPropertiesA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b4300-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4300-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4300-149">Impression</span><span class="sxs-lookup"><span data-stu-id="b4300-149">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b4300-150">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="b4300-150">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b4300-151">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="b4300-151">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="b4300-152">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="b4300-152">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="b4300-153">**DocumentProperties**</span><span class="sxs-lookup"><span data-stu-id="b4300-153">**DocumentProperties**</span></span>](documentproperties.md)
</dt> <dt>

[<span data-ttu-id="b4300-154">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="b4300-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="b4300-155">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="b4300-155">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="b4300-156">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b4300-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




