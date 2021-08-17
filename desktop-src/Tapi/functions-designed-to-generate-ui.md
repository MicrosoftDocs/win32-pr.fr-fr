---
description: Supposons, dans le cadre d’un exemple, que l’application appelle la fonction TAPI lineConfigDialog, qui est conçue pour ouvrir une boîte de dialogue permettant de configurer les options du fournisseur de services relatives à l’appareil de ligne spécifié.
ms.assetid: a388d192-a327-4e67-968b-344d80c19fb1
title: Fonctions conçues pour générer l’interface utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e7aeda54d4c04a144b2786b56f32d13c51ab39c5274204485151caecc2db1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140612"
---
# <a name="functions-designed-to-generate-ui"></a>Fonctions conçues pour générer l’interface utilisateur

Supposons, dans le cadre d’un exemple, que l’application appelle la fonction TAPI [**lineConfigDialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) , qui est conçue pour ouvrir une boîte de dialogue permettant de configurer les options du fournisseur de services relatives à l’appareil de ligne spécifié. En réponse à cet appel, TAPI demande à TAPISRV d’appeler [**TSPI \_ providerUIIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) dans le fournisseur de services de téléphonie, en obtenant le nom de la dll de l’interface utilisateur TSP.

Dans le contexte de l’application, TAPI charge la DLL de l’interface utilisateur TSP et appelle la fonction [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) avec les paramètres fournis par l’application, et inclut un pointeur vers la fonction [*DllCallbackProc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) TAPI. La DLL de l’interface utilisateur TSP affiche la boîte de dialogue Configuration, en appelant la fonction *DllCallbackProc* si nécessaire pour obtenir du fournisseur de services de téléphonie les informations à afficher. Chaque fois que la fonction *DllCallbackProc* est appelée, TAPI demande à tapisrv d’appeler la fonction [**TSPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) du fournisseur de services de téléphonie, en passant le bloc de paramètres à partir de la dll de l’interface utilisateur et en renvoyant le bloc de paramètres à la dll de l’interface utilisateur. La DLL de l’interface utilisateur transmet toutes les modifications de configuration au fournisseur de services de téléphonie en appelant *DllCallbackProc*.

Une fois la fonction terminée, la DLL de l’interface utilisateur retourne (dans ce cas) [**TUISPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog). L’interface TAPI appelle la fonction [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) pour libérer la dll de l’interface utilisateur et retourne à l’application.

 

 
