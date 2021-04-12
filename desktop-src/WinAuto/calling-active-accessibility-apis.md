---
title: Appel d’API Active Accessibility
description: Microsoft Active Accessibility fournit des interfaces de programmation d’applications (API) pour les clients et les serveurs.
ms.assetid: c40441d2-7294-4c76-8b42-08ed66eccb7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209a239495fddbcaf2275f095abc889295568b3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031383"
---
# <a name="calling-active-accessibility-apis"></a>Appel d’API Active Accessibility

Microsoft Active Accessibility fournit des interfaces de programmation d’applications (API) pour les clients et les serveurs. La plupart d’entre elles sont implémentées dans la bibliothèque de liens dynamiques de Microsoft Active Accessibility, Oleacc.dll, mais [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)et [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent) sont implémentées dans user32.dll, qui est un composant fondamental du système d’exploitation Microsoft Windows.

Les ordinateurs qui exécutent Windows 95 ou Microsoft Windows NT 4,0 ne disposent pas de Oleacc.dll et de la version correcte de user32.dll installée, car Microsoft Active Accessibility a été incorporé dans les versions suivantes de Windows. Par conséquent, les applications qui s’exécutent sur ces plateformes sont explicitement liées à Oleacc.dll au moment de l’exécution à l’aide de la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) au lieu de s’appuyer sur les bibliothèques d’importation. Active Accessibility 1,3 prend en charge Windows 95 et Microsoft Windows NT 4,0. Les versions antérieures de Windows ne sont pas prises en charge par Microsoft Active Accessibility.

Les applications serveur utilisent la fonction [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour récupérer l’adresse d’une fonction de Active Accessibility Microsoft, puis effectuer l’appel via un pointeur de fonction. Si vous appelez une fonction implémentée dans Oleacc.dll, les applications serveur utilisent le handle retourné par [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) dans l’appel à **GetProcAddress**. Si vous appelez une fonction définie dans user32.dll, les applications serveur appellent [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) en spécifiant « User32 » et utilisent le handle de module retourné dans l’appel à **GetProcAddress**.

Par exemple, si une application utilise [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent), elle appelle [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) à l’aide du handle de module de user32.dll pour obtenir l’adresse de la fonction. Si l’appel réussit (ce qui signifie que cette version de Windows prend en charge Microsoft Active Accessibility), l’application définit un indicateur qui indique qu’il est possible d’appeler **NotifyWinEvent** en toute sécurité. L’adresse reçue de **GetProcAddress** est stockée dans une variable de pointeur de fonction et utilisée dans le code.

 

 