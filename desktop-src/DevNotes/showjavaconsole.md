---
description: La fonction ShowJavaConsole est une aide au débogage pour les développeurs Java. Les applets (ou tout autre code Java) s’exécutant dans Internet Explorer peuvent l’utiliser pour afficher des messages d’erreur et d’autres informations.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: ShowJavaConsole fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540468"
---
# <a name="showjavaconsole-function"></a><span data-ttu-id="1bf0c-104">ShowJavaConsole fonction)</span><span class="sxs-lookup"><span data-stu-id="1bf0c-104">ShowJavaConsole function</span></span>

<span data-ttu-id="1bf0c-105">La fonction **ShowJavaConsole** est une aide au débogage pour les développeurs Java.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-105">The **ShowJavaConsole** function is a debugging aid for Java developers.</span></span> <span data-ttu-id="1bf0c-106">Les applets (ou tout autre code Java) s’exécutant dans Internet Explorer peuvent l’utiliser pour afficher des messages d’erreur et d’autres informations.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-106">Applets (or other Java code) running within Internet Explorer can use it to display error messages and other information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bf0c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bf0c-107">Syntax</span></span>


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a><span data-ttu-id="1bf0c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bf0c-108">Parameters</span></span>

<span data-ttu-id="1bf0c-109">Cette fonction n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-109">This function has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="1bf0c-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1bf0c-110">Return value</span></span>

<span data-ttu-id="1bf0c-111">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bf0c-112">Notes</span><span class="sxs-lookup"><span data-stu-id="1bf0c-112">Remarks</span></span>

<span data-ttu-id="1bf0c-113">L’appel de **ShowJavaConsole** entraîne l’affichage de la fenêtre de la console Java par la machine virtuelle Java.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-113">Calling **ShowJavaConsole** causes the Java virtual machine (VM) to display the Java console window.</span></span> <span data-ttu-id="1bf0c-114">La fenêtre de la console Java elle-même peut afficher la sortie du débogage à partir du code Java qui s’exécute dans le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-114">The Java console window itself can display debugging output from Java code running in the calling process.</span></span> <span data-ttu-id="1bf0c-115">En règle générale, cela ne peut être utilisé que par une application hébergeant la machine virtuelle Java.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-115">Typically, this would be used only by an application hosting the Java VM.</span></span> <span data-ttu-id="1bf0c-116">Il n’existe qu’une seule fenêtre de console Java par processus. plusieurs appels à l’API entraînent l’affichage de la même fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-116">There is only a single Java console window per process; multiple calls to the API result in the same window being displayed.</span></span> <span data-ttu-id="1bf0c-117">En d’autres termes, si la fenêtre de console est déjà affichée, rien ne se produit. Si la fenêtre n’a pas été affichée ou si l’utilisateur l’a fermée, la fenêtre s’affiche.</span><span class="sxs-lookup"><span data-stu-id="1bf0c-117">In other words, if the console window is already displayed, nothing happens; if the window has not been displayed, or the user has closed it, then the window pops up.</span></span>

<span data-ttu-id="1bf0c-118">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="1bf0c-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1bf0c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bf0c-119">Requirements</span></span>



| <span data-ttu-id="1bf0c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bf0c-120">Requirement</span></span> | <span data-ttu-id="1bf0c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bf0c-121">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1bf0c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="1bf0c-122">DLL</span></span><br/> | <dl> <span data-ttu-id="1bf0c-123"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1bf0c-123"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
