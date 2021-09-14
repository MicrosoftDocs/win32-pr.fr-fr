---
description: Les fonctions suivantes sont utilisées dans la gestion structurée des exceptions.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Fonctions de gestion structurée des exceptions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114578"
---
# <a name="structured-exception-handling-functions"></a>Fonctions de gestion structurée des exceptions

Les fonctions suivantes sont utilisées dans la gestion structurée des exceptions.

-   [**AbnormalTermination**](abnormaltermination.md)

    Indique si le bloc **\_ \_ try** d’un gestionnaire de terminaisons se termine normalement.

-   [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    Inscrit un gestionnaire continue vectorisé.

-   [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    Inscrit un gestionnaire d’exceptions vectorisées.

-   [**GetExceptionCode**](getexceptioncode.md)

    Récupère un code qui identifie le type d’exception qui s’est produit.

-   [**GetExceptionInformation**](getexceptioninformation.md)

    Récupère une description indépendante de l’ordinateur d’une exception et des informations sur l’état de l’ordinateur qui existait pour le thread lorsque l’exception s’est produite.

-   [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    Lève une exception dans le thread appelant.

-   [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    Annule l’inscription d’un gestionnaire de continuation vectorisé.

-   [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    Annule l’inscription d’un gestionnaire d’exceptions vectorisées.

-   [**RtlAddGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    Informe le système d’une table de fonctions dynamiques représentant une région de mémoire contenant du code.

-   [**RtlDeleteGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    Informe le système qu’une table de fonctions dynamiques précédemment signalée n’est plus utilisée.

-   [**RtlGrowFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    Signale que la taille d’une table de fonctions dynamiques a augmenté.

-   [**SetUnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    Permet à une application de remplacer le gestionnaire d’exceptions de niveau supérieur de chaque thread et processus.

-   [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    Passe des exceptions non gérées au débogueur, si le processus est en cours de débogage.

-   [**VectoredHandler**](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    Fonction définie par l’application qui sert de gestionnaire d’exceptions vectorisées.

Les fonctions suivantes sont utilisées uniquement sur les Windows bits 64.

-   [**RtlAddFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    Ajoute une table de fonctions dynamiques à la liste des tables de fonctions dynamiques.

-   [**RtlCaptureContext**](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    Récupère un enregistrement de contexte dans le contexte de l’appelant.

-   [**RtlDeleteFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    Supprime une table de fonctions dynamiques de la liste des tables de fonctions dynamiques.

-   [**RtlInstallFunctionTableCallback**](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    Ajoute une table de fonctions dynamiques à la liste des tables de fonctions dynamiques.

-   [**RtlRestoreContext**](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    Restaure le contexte de l’appelant à l’enregistrement de contexte spécifié.

 

 
