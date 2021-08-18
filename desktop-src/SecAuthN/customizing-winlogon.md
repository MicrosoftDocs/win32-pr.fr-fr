---
description: Personnaliser le comportement de Winlogon en implémentant un fournisseur d’informations d’identification.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personnalisation de Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10b2ae1e029bb741a2402a25d8e51f331fdd1cac1e9918dfef3b35b36c8e6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008657"
---
# <a name="customizing-winlogon"></a>Personnalisation de Winlogon

Personnaliser le comportement de [*Winlogon*](/windows/desktop/SecGloss/w-gly) en implémentant un fournisseur d’informations d’identification. Pour plus d’informations sur les fournisseurs d’informations d’identification, consultez [**ICredentialProvider interface**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).

**Windows Server 2003 et Windows XP :** Les fournisseurs d’informations d’identification ne sont pas pris en charge.

les sections suivantes décrivent comment personnaliser Winlogon dans Windows versions antérieures à Windows Vista.

> [!Note]  
> les dll GINA et les packages de notification Winlogon sont ignorés dans Windows Vista.

 

-   [Packages de notification Winlogon](#winlogon-notification-packages)
-   [Stubs GINA](#gina-stubs)
-   [Hooks GINA](#gina-hooks)

## <a name="winlogon-notification-packages"></a>Packages de notification Winlogon

Un package de notification Winlogon est une DLL qui exporte les fonctions qui gèrent les événements Winlogon. Par exemple, lorsqu’un utilisateur se connecte au système, Winlogon appelle chaque package de notification pour fournir des informations sur l’événement. Pour plus d’informations, consultez la page [packages de notification Winlogon](winlogon-notification-packages.md).

## <a name="gina-stubs"></a>Stubs GINA

Un stub [*Gina*](/windows/desktop/SecGloss/g-gly) est une DLL GINA personnalisée qui utilise les implémentations de fonction d’exportation d’une DLL GINA précédemment installée (généralement MsGina.dll). Un stub GINA obtient des pointeurs vers chaque fonction exportée par la DLL GINA précédemment installée. Chaque fonction stub GINA utilise ensuite le pointeur de fonction approprié pour appeler la fonction correspondante dans la DLL GINA installée précédemment.

> [!IMPORTANT]
> Chaque fonction stub GINA doit appeler la fonction correspondante dans le GINA précédemment installé.

 

Une fonction stub GINA peut implémenter des fonctionnalités supplémentaires dans une ou plusieurs de ses fonctions d’exportation. Par exemple, la fonction [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) d’un stub Gina peut vérifier l’heure actuelle avant d’appeler la fonction **WlxLoggedOutSAS** de l' MsGina.dll. Si l’heure actuelle se situe dans une plage spécifique, la fonction stub peut afficher un message qui indique que l’ouverture de session n’est pas autorisée pendant cette période et retourne l' **\_ action SAS wlx \_ \_ aucun** à Winlogon. La fonction **WlxLoggedOutSAS** de l' MsGina.dll est alors appelée uniquement pendant la période autorisée.

L’application GINA stub obtient une table de dispatch pour que Winlogon prenne en charge les fonctions via le paramètre *pWinlogonFunctions* de la fonction [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) . L’application GINA stub peut utiliser cette table de distribution pour appeler les fonctions de prise en charge de Winlogon. Par exemple, une application GINA stub peut appeler la fonction [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) pour déclencher un événement de [*séquence de touches de sécurité*](/windows/desktop/SecGloss/s-gly) (SAS) lorsqu’une [*carte à puce*](/windows/desktop/SecGloss/s-gly) est insérée dans un [*lecteur*](/windows/desktop/SecGloss/r-gly).

Pour plus d’informations sur la création d’un stub GINA, consultez l’exemple Gina stubs dans le \\ \\ \\ répertoire Exemples de sécurité Gina \\ GinaStub d’une installation du kit de développement logiciel (SDK) de plateforme.

> [!Note]  
> Tous les appels entre un GINA et Winlogon doivent se trouver dans un seul thread.

 

## <a name="gina-hooks"></a>Hooks GINA

Un hook GINA est un stub GINA qui, dans son implémentation de la fonction [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) , remplace le pointeur de la fonction de prise en charge [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) dans la table Dispatch par un pointeur vers sa propre implémentation de la fonction **WlxDialogBoxParam** . Par conséquent, chaque fois que la GINA précédemment installée (généralement MsGina.dll) appelle la fonction **WlxDialogBoxParam** , la fonction implémentée par le hook Gina est appelée.

La fonction [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) implémentée par le hook Gina peut remplacer la procédure de rappel [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) qui répond à un événement de boîte de dialogue spécifique.

Cela donne au Hook GINA un contrôle total sur l’apparence et le comportement de toutes les boîtes de dialogue que MsGina.dll crée.

Pour plus d’informations sur la création d’un hook GINA, consultez l’exemple de hooks Gina dans le \\ \\ \\ répertoire Exemples de sécurité Gina \\ GinaHook d’une installation du kit de développement logiciel (SDK) de plateforme.

> [!Note]  
> Tous les appels entre un GINA et Winlogon doivent se trouver dans un seul thread.

 

 

 
