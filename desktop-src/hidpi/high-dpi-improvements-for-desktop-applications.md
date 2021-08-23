---
title: Mixed-Mode de la mise à l’échelle PPP et des API compatibles PPP
description: Mixed-Mode de la mise à l’échelle PPP et des API compatibles PPP
ms.assetid: 44AC0B29-3283-4801-90F5-3E78CCD87B9F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb32de01390f2794b5714bdca5465a5997121c270ded9c170e0b0171fd972542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036220"
---
# <a name="mixed-mode-dpi-scaling-and-dpi-aware-apis"></a>Mixed-Mode de la mise à l’échelle PPP et des API compatibles PPP

## <a name="sub-process-dpi-awareness-support"></a>Prise en charge de la prise en charge de Sub-Process DPI

[**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext) permet l’utilisation de différents modes de mise à l’échelle dpi au sein d’un même processus. avant la Windows 10 mise à jour anniversaire, une prise en charge de windows s dpi était liée au mode de prise en charge dpi à l’échelle du processus (prise en charge de dpi non compatible, compatible avec la résolution système ou Per-Monitor dpi). Mais maintenant, avec **SetThreadDpiAwarenessContext**, les fenêtres de niveau supérieur peuvent avoir un mode de reconnaissance dpi différent de celui du mode de reconnaissance dpi à l’échelle du processus. Cela affecte également les fenêtres enfants, car elles auront toujours le même mode de reconnaissance PPP que leur fenêtre parente.

L’utilisation de **SetThreadDpiAwarenessContext** permet aux développeurs de décider où ils veulent concentrer leurs efforts de développement lorsqu’ils définissent le comportement spécifique aux dpi pour les applications de bureau. Par exemple, la fenêtre de niveau supérieur principale d’une application peut être mise à l’échelle en fonction de l’écran, tandis que les fenêtres de niveau supérieur secondaires peuvent être mises à l’échelle via le système d’exploitation à l’aide d’une mise à l’échelle bitmap.

## <a name="the-dpi-awareness-context"></a>Contexte de détection PPP

Avant la disponibilité de **SetThreadDpiAwarenessContext** , la reconnaissance PPP d’un processus a été définie dans le manifeste du fichier binaire de l’application ou via un appel à [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) pendant l’initialisation du processus. Avec **SetThreadDpiAwarenessContext**, chaque thread peut avoir un contexte de reconnaissance PPP individuel qui peut être différent de celui du mode de reconnaissance PPP à l’échelle du processus. Le contexte de détection PPP d’un thread est représenté par le type * * * * [contexte de détection PPP * \_ \_ *](dpi-awareness-context.md) * * et se comporte comme suit :

-   Un thread peut avoir son contexte de sensibilisation PPP modifié à tout moment.
-   Tous les appels d’API effectués après modification du contexte s’exécutent dans le contexte PPP correspondant (et peuvent être virtualisés).
-   Quand une fenêtre est créée, sa prise en forme PPP est définie comme la reconnaissance DPI du thread appelant à ce moment-là.
-   Lorsque la procédure de fenêtre pour une fenêtre est appelée, le thread bascule automatiquement vers le contexte de détection PPP qui était utilisé lors de la création de la fenêtre.

Un scénario courant pour l’utilisation de **SetThreadDpiAwarenessContext** est le suivant : commencer avec un thread qui s’exécute avec un contexte (par exemple, le **contexte de détection des PPP \_ par la prise en \_ \_ \_ \_ charge** de l’analyse) basculer temporairement vers un autre contexte (prise en charge du **\_ contexte de détection \_ \_ PPP** impossible), créer une fenêtre, puis basculer immédiatement le contexte de thread à son état précédent. La fenêtre créée aura un contexte PPP qui ne **prend \_ pas \_ en \_ charge le contexte de détection PPP**, tandis que le contexte des threads d’appel sera restauré en contexte de **\_ sensibilisation PPP \_ \_ par \_ analyse \_** avec un appel ultérieur à **SetThreadDpiAwarenessContext**. Dans ce scénario, la fenêtre associée au thread appelant s’exécute avec un contexte par moniteur (et, par conséquent, n’est pas étiré par le système d’exploitation), tandis que la fenêtre nouvellement créée ne prend pas en charge la fonction DPI (et par conséquent, la bitmap est automatiquement étirée sur un affichage défini sur >100% de mise à l’échelle).

La figure 1 illustre la façon dont le thread de processus principal s’exécute avec le **\_ contexte de reconnaissance PPP \_ \_ par \_ moniteur**, bascule son contexte sur la **prise en \_ \_ \_ charge du contexte de sensibilisation dpi** et crée une nouvelle fenêtre. La fenêtre qui vient d’être créée s’exécute ensuite avec un contexte de sensibilisation en DPI du contexte de sensibilisation PPP qui ne prend **\_ pas en \_ \_ charge** chaque fois qu’un message est distribué ou que des appels d’API sont effectués à partir de celle-ci. Immédiatement après la création de la nouvelle fenêtre, le thread principal est restauré dans son contexte précédent du **\_ contexte de détection dpi \_ \_ par \_ moniteur**.

![Diagramme montrant la prise en action de dpi par moniteur](images/dpi-awareness-context.png)

## <a name="new-dpi-related-apis"></a>Nouvelles API liées à DPI

Outre la prise en charge de différents modes de reconnaissance DPI au sein d’un même processus que **SetThreadDpiAwarenessContext** offre, les fonctionnalités spécifiques à la DPI suivantes ont été ajoutées pour les applications de bureau :<dl> <dd>[EnableNonClientDpiScaling****](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)<dl> <dt>



> [!Note]  
> Le mode de reconnaissance PPP **par moniteur v2** active automatiquement cette fonctionnalité et l’appel de **EnableNonClientDpiScaling** n’est donc pas nécessaire dans les applications qui l’utilisent.

 

L’appel de **EnableNonClientDpiScaling** à partir d’un gestionnaire **\_ NCCREATE** de fenêtre s entraîne la mise à l’échelle automatique de la zone non cliente d’une fenêtre de niveau supérieur pour la résolution PPP. Si la fenêtre de niveau supérieur prend en charge DPI par moniteur (que le processus lui-même soit compatible avec la résolution PPP par moniteur ou que la fenêtre ait été créée au sein d’un thread prenant en charge la résolution PPP), la barre de légende, les barres de défilement, les menus et les barres de menus de ces fenêtres sont mis à l’échelle en fonction de la valeur PPP.
</dt> <dt>

Notez que les zones non clientes d’une fenêtre enfant, telles que les barres de défilement non client d’un contrôle d’édition enfant, ne sont pas automatiquement mises à l’échelle en DPI lorsque cette API est utilisée.
</dt> <dt>

> [!Note]  
> **EnableNonClientDpiScaling** doit être appelé à partir du gestionnaire **WM \_ NCCREATE** .

</dt> </dl> </dd> <dd> <b> API * ForDpi </b>

-   Plusieurs API fréquemment utilisées, telles que [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) , n’ont pas de contexte d’un HWND et n’ont donc aucun moyen de déduire la prise en forme de dpi appropriée pour leurs valeurs de retour. L’appel de ces API à partir d’un thread qui s’exécute dans un autre contexte ou mode de reconnaissance PPP peut retourner des valeurs qui ne sont pas mises à l’échelle pour le contexte du thread appelant. [* * * * GetSystemMetricForDpi * *](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)* *, [* * * * SystemParametersInfoForDpi * *](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)* * et * * * * [AdjustWindowRectExForDpi * *](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * *
-   **GetSystemMetricForDpi** et **SystemParametersInfoForDpi** retournent des valeurs de métriques système à échelle dpi et des valeurs de paramètre système conformément à cette équation :

    
    GetSystemMetrics (...) @ dpi = = GetSystemMetricsForDpi (..., dpi)

    

     

    Par conséquent, l’appel de **GetSystemMetrics** (ou **SystemParametersInfoForDpi**), en cours d’exécution sur un appareil avec une certaine valeur DPI système, retourne la même valeur que leurs variantes prenant en charge dpi (**GetSystemMetricsForDpi** et **SystemParametersInfoForDpi**), étant donné la même valeur DPI que l’entrée.

-   [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi) prend un HWND et calcule la taille requise d’un rectangle de fenêtre d’une manière sensible aux PPP.

</dd> <dd>

</dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow">GetDpiForWindow</a></b><dl> <dt><b>GetDpiForWindow</b> retourne la PPP associée au HWND fourni. La réponse dépend du mode de reconnaissance PPP du HWND :

| Mode de reconnaissance DPI de HWND | Valeur retournée                                                                                                                                                                                                  |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ignore                    | 96                                                                                                                                                                                                            |
| Système                     | La résolution système                                                                                                                                                                                                |
| Per-Monitor                | PPP de l’affichage sur lequel la fenêtre de niveau supérieur associée se trouve principalement <br/> (Si une fenêtre enfant est fournie, la résolution de la fenêtre parente de niveau supérieur correspondante est retournée)<br/> |

</dt> </dl> </dd> <dd><b><a href="/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem">GetDpiForSystem</a></b><dl> <dt>

L’appel de **GetDpiForSystem** est plus efficace que l’appel de [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) et [**GetDeviceCaps**](/windows/desktop/api/wingdi/nf-wingdi-getdevicecaps) pour obtenir la DPI système.
</dt> <dt>

Tout composant pouvant être en cours d’exécution dans une application qui utilise la reconnaissance de la résolution de sous-processus ne doit pas supposer que la résolution du système est statique pendant le cycle de vie du processus. Par exemple, si un thread qui s’exécute sous le **contexte de sensibilisation en dpi ( \_ context awareness \_ \_** context awareness) interroge la résolution du système, la réponse sera 96. Toutefois, si le même thread a basculé vers le contexte de sensibilisation du **\_ système de \_ contexte \_ de sensibilisation PPP** et interrogé à nouveau la résolution du système, la réponse peut être différente. Pour éviter l’utilisation d’une valeur DPI système (et éventuellement obsolète) mise en cache, utilisez **GetDpiForSystem** pour récupérer la résolution système dpi par rapport au mode de reconnaissance dpi du thread appelant. 
</dt> </dl> </dd> </dl>
