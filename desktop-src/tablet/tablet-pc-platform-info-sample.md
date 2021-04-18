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
# <a name="tablet-pc-platform-info-sample"></a>Exemple d’informations sur la plateforme Tablet PC

Ce programme vérifie la présence et la configuration des composants de base de la technologie tactile et du PC MicrosoftTablet. Il détermine si les composants Tablet PC sont activés dans le système d’exploitation, en répertoriant les noms et les informations de version pour les contrôles principaux et le module de reconnaissance vocale et d’écriture manuscrite par défaut.

L’application utilise l’API Windows GetSystemMetrics, en transmettant SM \_ TABLETPC, pour déterminer si l’application s’exécute sur un Tablet PC. SM \_ TABLETPC est défini dans winuser. h.

Un intérêt particulier est la façon dont l’application utilise la collection de regroupements pour fournir des informations sur le module de reconnaissance par défaut. Avant de tenter d’utiliser la collection de regroupements et l’objet de module de reconnaissance, l’application teste la réussite de sa création.

## <a name="components"></a>Composants

À l’aide du module de fusion re-distribuable, certaines parties de l’API de la plateforme Tablet PC peuvent être installées sur des versions non-Tablet de Vista et Windows XP professionnel. L’appel GetSystemMetrics indique uniquement que Windows XP Édition Tablet PC est installé. Une application doit toujours déterminer si un composant donné est disponible. Pour déterminer si un composant de l’API est installé, la méthode appropriée consiste à tenter de créer une instance d’un objet ou d’un contrôle et à vérifier qu’il existe avant de tenter de l’utiliser, comme illustré dans l’exemple suivant.


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



L’application détecte les composants de reconnaissance vocale installés en consultant la clé de registre appropriée :


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



La clé est lue à l’aide de RegQueryValueExW.

Enfin, l’exemple identifie les contrôles qui sont installés.


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



 

 



