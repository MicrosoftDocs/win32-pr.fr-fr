---
description: Ce programme vérifie la présence et la configuration des composants de base de la technologie tactile et du PC MicrosoftTablet.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Exemple d’informations sur la plateforme Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d815f21233b1edcc90d456df68b3736c170a5fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534109"
---
# <a name="tablet-pc-platform-info-sample"></a><span data-ttu-id="6a225-103">Exemple d’informations sur la plateforme Tablet PC</span><span class="sxs-lookup"><span data-stu-id="6a225-103">Tablet PC Platform Info Sample</span></span>

<span data-ttu-id="6a225-104">Ce programme vérifie la présence et la configuration des composants de base de la technologie tactile et du PC MicrosoftTablet.</span><span class="sxs-lookup"><span data-stu-id="6a225-104">This program checks the presence and configuration of the MicrosoftTablet PC and Touch Technology core components.</span></span> <span data-ttu-id="6a225-105">Il détermine si les composants Tablet PC sont activés dans le système d’exploitation, en répertoriant les noms et les informations de version pour les contrôles principaux et le module de reconnaissance vocale et d’écriture manuscrite par défaut.</span><span class="sxs-lookup"><span data-stu-id="6a225-105">It determines whether Tablet PC components are enabled in the operating system, listing names and version information for core controls and the default handwriting and speech recognizer.</span></span>

<span data-ttu-id="6a225-106">L’application utilise l’API Windows GetSystemMetrics, en transmettant SM \_ TABLETPC, pour déterminer si l’application s’exécute sur un Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="6a225-106">The application uses the GetSystemMetrics Windows API, passing in SM\_TABLETPC, to determine whether the application running on a Tablet PC.</span></span> <span data-ttu-id="6a225-107">SM \_ TABLETPC est défini dans winuser. h.</span><span class="sxs-lookup"><span data-stu-id="6a225-107">SM\_TABLETPC is defined in WinUser.h.</span></span>

<span data-ttu-id="6a225-108">Un intérêt particulier est la façon dont l’application utilise la collection de regroupements pour fournir des informations sur le module de reconnaissance par défaut.</span><span class="sxs-lookup"><span data-stu-id="6a225-108">Of particular interest is the way the application uses the Recognizers collection to provide information about the default recognizer.</span></span> <span data-ttu-id="6a225-109">Avant de tenter d’utiliser la collection de regroupements et l’objet de module de reconnaissance, l’application teste la réussite de sa création.</span><span class="sxs-lookup"><span data-stu-id="6a225-109">Before attempting to use the Recognizers collection and Recognizer object, the application tests for their successful creation.</span></span>

## <a name="components"></a><span data-ttu-id="6a225-110">Composants</span><span class="sxs-lookup"><span data-stu-id="6a225-110">Components</span></span>

<span data-ttu-id="6a225-111">À l’aide du module de fusion re-distribuable, certaines parties de l’API de la plateforme Tablet PC peuvent être installées sur des versions non-Tablet de Vista et Windows XP professionnel.</span><span class="sxs-lookup"><span data-stu-id="6a225-111">Using the re-distributable merge module, certain parts of the Tablet PC Platform API may be installed on non-Tablet versions of Vista and Windows XP Professional .</span></span> <span data-ttu-id="6a225-112">L’appel GetSystemMetrics indique uniquement que Windows XP Édition Tablet PC est installé.</span><span class="sxs-lookup"><span data-stu-id="6a225-112">The GetSystemMetrics call only indicates that Windows XP Tablet PC Edition is installed.</span></span> <span data-ttu-id="6a225-113">Une application doit toujours déterminer si un composant donné est disponible.</span><span class="sxs-lookup"><span data-stu-id="6a225-113">An application should always determine if a given component is available.</span></span> <span data-ttu-id="6a225-114">Pour déterminer si un composant de l’API est installé, la méthode appropriée consiste à tenter de créer une instance d’un objet ou d’un contrôle et à vérifier qu’il existe avant de tenter de l’utiliser, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="6a225-114">The proper way to determine if a component of the API is installed is to attempt to create an instance of an object or control and check that it exists before attempting to use it, as shown in the following example.</span></span>


```C++
IInkRecognizers* pIInkRecognizers = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkRecognizers,
                              NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IInkRecognizers, 
                              (void **)&pIInkRecognizers);
if (SUCCEEDED(hr)) 
{
  // use the component
} else
{
  // component unavailable
}
```



<span data-ttu-id="6a225-115">L’application détecte les composants de reconnaissance vocale installés en consultant la clé de registre appropriée :</span><span class="sxs-lookup"><span data-stu-id="6a225-115">The application finds out about the installed speech components by looking in the appropriate registry key:</span></span>


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



<span data-ttu-id="6a225-116">La clé est lue à l’aide de RegQueryValueExW.</span><span class="sxs-lookup"><span data-stu-id="6a225-116">The key is read using RegQueryValueExW.</span></span>

<span data-ttu-id="6a225-117">Enfin, l’exemple identifie les contrôles qui sont installés.</span><span class="sxs-lookup"><span data-stu-id="6a225-117">Finally, the sample finds out which controls are installed.</span></span>


```C++
LPCOLESTR gc_wszProgId[NUM_CONTROLS] = {L"InkEd.InkEdit", L"msinkaut.InkOverlay"};
// ...
for (int i = 0, j = 0; i < NUM_CONTROLS; i++)
{
    // Get the component info
    CLSID clsid;
    if (SUCCEEDED(CLSIDFromProgID(gc_wszProgId[i], &clsid)) && GetComponentInfo(clsid, info) == TRUE)
    {
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][0], info.wchName);
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][1], info.wchVersion);
        j++;
    }
}
```



 

 



