---
description: Lance l’Assistant Passport lorsqu’il est utilisé avec Rundll32.exe.
title: PassportWizardRunDll fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: a858a36caa4af8095fc7023abae5ad918321f53e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203444"
---
# <a name="passportwizardrundll-function"></a><span data-ttu-id="db21e-103">PassportWizardRunDll fonction)</span><span class="sxs-lookup"><span data-stu-id="db21e-103">PassportWizardRunDll function</span></span>

<span data-ttu-id="db21e-104">\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="db21e-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="db21e-105">Il peut être modifié ou non disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="db21e-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="db21e-106">Lance l’Assistant Passport lorsqu’il est utilisé avec Rundll32.exe.</span><span class="sxs-lookup"><span data-stu-id="db21e-106">Launches the Passport Wizard when used with Rundll32.exe.</span></span>

## <a name="syntax"></a><span data-ttu-id="db21e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db21e-107">Syntax</span></span>


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="db21e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db21e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db21e-109">*hwndStub* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db21e-109">*hwndStub* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db21e-110">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="db21e-110">Type: **HWND**</span></span>

<span data-ttu-id="db21e-111">Handle d’une fenêtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="db21e-111">A handle to an owner window.</span></span> <span data-ttu-id="db21e-112">Ce paramètre a généralement la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="db21e-112">This parameter is typically set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="db21e-113">*hAppInstance* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db21e-113">*hAppInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db21e-114">Type : **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="db21e-114">Type: **HINSTANCE**</span></span>

<span data-ttu-id="db21e-115">Handle du fichier bibliothèque, obtenu en tant que valeur de retour de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span><span class="sxs-lookup"><span data-stu-id="db21e-115">A handle to the library file, obtained as a return value from [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span></span>

</dd> <dt>

<span data-ttu-id="db21e-116">*lpszCmdLine* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db21e-116">*lpszCmdLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db21e-117">Type : **LPTStr**</span><span class="sxs-lookup"><span data-stu-id="db21e-117">Type: **LPTSTR**</span></span>

<span data-ttu-id="db21e-118">Données d’argument.</span><span class="sxs-lookup"><span data-stu-id="db21e-118">Argument data.</span></span> <span data-ttu-id="db21e-119">Cette valeur sera toujours vide.</span><span class="sxs-lookup"><span data-stu-id="db21e-119">This value will always be empty.</span></span>

</dd> <dt>

<span data-ttu-id="db21e-120">*nCmdShow* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="db21e-120">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db21e-121">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="db21e-121">Type: **int**</span></span>

<span data-ttu-id="db21e-122">Définit le mode d’affichage de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="db21e-122">Sets the display mode for the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db21e-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db21e-123">Return value</span></span>

<span data-ttu-id="db21e-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="db21e-124">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="db21e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="db21e-125">Remarks</span></span>

<span data-ttu-id="db21e-126">L’Assistant Passport est utilisé pour obtenir un compte Passport par défaut pour Windows.</span><span class="sxs-lookup"><span data-stu-id="db21e-126">The Passport Wizard is used to obtain a default Passport for Windows.</span></span> <span data-ttu-id="db21e-127">Un Passport donne à l’utilisateur un accès personnalisé à tous les sites Web MSN et à d’autres sites compatibles Passport à l’aide de l’adresse de messagerie de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="db21e-127">A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address.</span></span> <span data-ttu-id="db21e-128">L’utilisation de **PassportWizardRunDll** comme point d’entrée dans le fichier Netplwiz.dll via une commande Rundll32 vous permet de lancer l’Assistant Passport à partir d’une ligne de commande comme s’il s’agissait d’un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="db21e-128">Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.</span></span>

<span data-ttu-id="db21e-129">**PassportWizardRunDll** est utilisé uniquement dans le contexte d’une commande Rundll32.exe comme suit :</span><span class="sxs-lookup"><span data-stu-id="db21e-129">**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:</span></span>

<span data-ttu-id="db21e-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span><span class="sxs-lookup"><span data-stu-id="db21e-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span></span>

<span data-ttu-id="db21e-131">L’utilisation d’une fonction de point d’entrée avec Rundll32.exe ne ressemble pas à un appel de fonction normal.</span><span class="sxs-lookup"><span data-stu-id="db21e-131">Using an entry point function with Rundll32.exe does not resemble a normal function call.</span></span> <span data-ttu-id="db21e-132">Le nom de la fonction et le nom du fichier. dll dans lequel elle est stockée sont utilisés uniquement comme paramètres de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="db21e-132">The function name and the name of the .dll file where it is stored are used only as command-line parameters.</span></span> <span data-ttu-id="db21e-133">La définition de fonction présentée sous la syntaxe est un prototype standard pour toutes les fonctions que vous pouvez appeler à l’aide de rundll32.</span><span class="sxs-lookup"><span data-stu-id="db21e-133">The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32.</span></span> <span data-ttu-id="db21e-134">Les valeurs spécifiques pour *hwndStub*, *hAppInstance* et *nCmdShow* ne sont pas fournies par l’utilisateur, mais sont gérées en arrière-plan par rundll32.</span><span class="sxs-lookup"><span data-stu-id="db21e-134">The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32.</span></span> <span data-ttu-id="db21e-135">**PassportWizardRunDll** n’utilise pas la valeur *lpszCmdLine* , donc aucune donnée supplémentaire n’est requise.</span><span class="sxs-lookup"><span data-stu-id="db21e-135">**PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="db21e-136">Spécifications</span><span class="sxs-lookup"><span data-stu-id="db21e-136">Requirements</span></span>



| <span data-ttu-id="db21e-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db21e-137">Requirement</span></span> | <span data-ttu-id="db21e-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="db21e-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db21e-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db21e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="db21e-140">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db21e-140">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="db21e-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db21e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="db21e-142">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db21e-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="db21e-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="db21e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="db21e-144"><dt>Aucun</dt></span><span class="sxs-lookup"><span data-stu-id="db21e-144"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="db21e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="db21e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db21e-146"><dt>Netplwiz.dll (version 5,60 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="db21e-146"><dt>Netplwiz.dll (version 5.60 or later)</dt></span></span> </dl> |



 

 
