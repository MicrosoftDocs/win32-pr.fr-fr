---
title: Référence haute résolution
description: Référence haute résolution
ms.assetid: 07A2D45E-721C-4DA8-82A5-38B2FB94BC6D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c10bcf5c5297b0adcfceef6853f2292c3fc8b98
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087797"
---
# <a name="high-dpi-reference"></a>Référence haute résolution

## <a name="functions"></a>Fonctions



|                                                                                          |                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Rubrique**                                                                                | **Description**                                                                                                                                                   |
| [**AdjustWindowRectExForDpi**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi)                             | Variante de [AdjustWindowRectEx](/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex) qui retourne des valeurs mises à l’échelle à une résolution spécifique.       |
| [**AreDpiAwarenessContextsEqual**](/windows/desktop/api/Winuser/nf-winuser-aredpiawarenesscontextsequal)                     | Détermine si deux valeurs de [**\_ \_ contexte de reconnaissance PPP**](dpi-awareness-context.md) sont équivalentes.                                                            |
| [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)                           | Active la mise à l’échelle automatique de la zone non cliente de la fenêtre de niveau supérieur spécifiée.                                                                               |
| [**GetAwarenessFromDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getawarenessfromdpiawarenesscontext)       | Récupère la valeur [**de \_ reconnaissance PPP**](/windows/desktop/api/windef/ne-windef-dpi_awareness) à partir d’un [**\_ \_ contexte de sensibilisation PPP**](dpi-awareness-context.md)                                       |
| [**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)                                             | Interroge les informations PPP associées à une analyse.                                                                                                            |
| [**GetDpiForSystem**](/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem)                                               | Retourne la valeur PPP du système.                                                                                                                                           |
| [**GetDpiForWindow**](/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow)                                               | Retourne la valeur PPP actuelle pour la fenêtre spécifiée.                                                                                                                 |
| [**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)                                 | Récupère le mode de virtualisation PPP du processus spécifié.                                                                                                   |
| [**GetSystemMetricsForDpi**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)                                 | Variante de [GetSystemMetrics](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) qui retourne des valeurs mises à l’échelle à une résolution spécifique.         |
| [**GetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getthreaddpiawarenesscontext)                     | Récupère le contexte de détection PPP actif pour le thread actuel.                                                                                                |
| [**GetWindowDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-getwindowdpiawarenesscontext)                     | Récupère le contexte de détection PPP pour une fenêtre.                                                                                                                 |
| [**IsValidDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-isvaliddpiawarenesscontext)                         | Détermine si un [**\_ \_ contexte de détection PPP**](dpi-awareness-context.md) est valide et pris en charge par le système actuel.                                            |
| [**LogicalToPhysicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi) | Convertit un point dans une fenêtre de coordonnées logiques en coordonnées physiques, quelle que soit la prise en compte des PPP de l’appelant.                                   |
| [**PhysicalToLogicalPointForPerMonitorDPI**](/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi) | Convertit un point dans une fenêtre à partir de coordonnées physiques en coordonnées logiques, quelle que soit la prise en compte des PPP de l’appelant.                                   |
| [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)                                 | Définit le mode de virtualisation DPI pour le processus en cours.                                                                                                         |
| [**SetThreadDpiAwarenessContext**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)                     | Modifie le contexte de détection des PPP actifs pour le thread actuel.                                                                                                  |
| [**SystemParametersInfoForDpi**](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)                         | Variante de [SystemParametersInfo](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) qui retourne des valeurs mises à l’échelle à une résolution spécifique.     |
| [**SetProcessDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)                   | Définit le contexte de sensibilisation PPP pour le processus actuel.                                                                                                           |
| [**SetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior)                         | Remplace le comportement par défaut de mise à l’échelle DPI par moniteur d’une boîte de dialogue.                                                                                               |
| [**GetDialogDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior)                         | Récupère le comportement de mise à l’échelle DPI par moniteur d’une boîte de dialogue.                                                                                                       |
| [**SetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior)                     | Remplace le comportement par défaut de mise à l’échelle DPI par moniteur d’une fenêtre enfant dans une boîte de dialogue.                                                                             |
| [**GetDialogControlDpiChangeBehavior**](/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior)                     | Récupère les remplacements de comportement de mise à l’échelle DPI par moniteur d’une fenêtre enfant dans une boîte de dialogue.                                                                           |
| [**OpenThemeDataForDpi**](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedatafordpi)                                       | Variante de [OpenThemeData](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata) qui ouvre des handles de thème associés à une résolution spécifique. |
| [**GetSystemDpiForProcess**](/windows/desktop/api/winuser/nf-winuser-getsystemdpiforprocess)                                 | Récupère la DPI système associée à un processus donné.                                                                                                         |
| [**GetDpiFromDpiAwarenessContext**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)                   | Récupère la résolution à partir d’un handle de [ \_ \_ contexte de détection PPP](dpi-awareness-context.md) donné.                                                                       |
| [**SetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior)                       | Remplace le comportement d’hébergement PPP par défaut du thread actuel.                                                                                                 |
| [**GetThreadDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior)                       | Récupère le comportement d’hébergement PPP du thread actuel.                                                                                                         |
| [**GetWindowDpiHostingBehavior**](/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior)                       | Récupère le comportement d’hébergement PPP de la fenêtre spécifiée.                                                                                                       |



 

## <a name="types"></a>Types



|                                                                            |                                                                                        |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| **Rubrique**                                                                  | **Description**                                                                        |
| [**\_reconnaissance dpi**](/windows/desktop/api/windef/ne-windef-dpi_awareness)                                    | Représente les modes de virtualisation en coordonnées PPP.                                        |
| [**\_contexte de détection PPP \_**](dpi-awareness-context.md)                   | Jeton qui représente un mode de virtualisation PPP et les comportements associés.           |
| [**comportements de modification de la \_ résolution de contrôle de boîte de dialogue \_ \_ \_**](/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors) | Décrit les remplacements du comportement de mise à l’échelle DPI par moniteur pour les fenêtres enfants dans les boîtes de dialogue. |
| [**comportements de modification de la résolution de dialogue \_ \_ \_**](/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors)      | Décrit les remplacements du comportement de mise à l’échelle DPI par moniteur pour les boîtes de dialogue.                      |
| [**\_type de résolution de l’analyse \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-monitor_dpi_type)                 | Représente le type de DPI associé à une analyse.                                  |
| [**\_détection des PPP de processus \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)                   | Représente le mode de virtualisation de la coordonnée PPP d’un processus.                        |
| [**\_comportement d’hébergement PPP \_**](/windows/win32/api/windef/ne-windef-dpi_hosting_behavior)                    | Représente le comportement d’hébergement PPP pour une fenêtre.                                      |



 

## <a name="messages"></a>Messages



|                                                                    |                                                                                                                                         |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Rubrique**                                                          | **Description**                                                                                                                         |
| [**\_DPICHANGED WM**](wm-dpichanged.md)                            | Avertit une fenêtre de niveau supérieur que son PPP a changé.                                                                                   |
| [**\_DPICHANGED WM \_ BEFOREPARENT**](wm-dpichanged-beforeparent.md) | Avertit une fenêtre enfant que la valeur PPP associée à la fenêtre qui la contient a changé. Remis avant la notification de la fenêtre parente. |
| [**\_DPICHANGED WM \_ AFTERPARENT**](wm-dpichanged-afterparent.md)   | Avertit une fenêtre enfant que la valeur PPP associée à la fenêtre qui la contient a changé. Remis après notification de la fenêtre parente.  |
| [**\_GETDPISCALEDSIZE WM**](wm-getdpiscaledsize.md)                | Permet aux fenêtres de niveau supérieur d’être redimensionnées de manière *non linéaire* en réponse aux modifications PPP.                                                           |



 

 

 
