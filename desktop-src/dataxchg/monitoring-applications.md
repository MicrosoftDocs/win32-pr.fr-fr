---
title: Surveillance des applications de
description: cette rubrique explique comment utiliser les éléments de la bibliothèque de gestion échange dynamique de données pour créer une application qui surveille l’activité d’échange de données dynamiques dans le système.
ms.assetid: 6705dc8e-d1e9-4057-9fa2-42cd5cf818af
keywords:
- Windows Interface utilisateur, échange dynamique de données (DDE)
- échange dynamique de données (DDE), surveillance des applications
- DDE (échange dynamique de données), surveillance des applications
- échange de données, échange dynamique de données (DDE)
- Windows Interface utilisateur, échange dynamique de données Management Library (DDEML)
- bibliothèque de gestion des échange dynamique de données (DDEML), applications de surveillance
- DDEML (bibliothèque de gestion échange dynamique de données), surveillance des applications
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f75685d4caa15e519485b2d8b37983faa35366
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922843"
---
# <a name="monitoring-applications"></a>Surveillance des applications de

les éléments d’API de la bibliothèque de gestion échange dynamique de données (DDEML) peuvent être utilisés pour créer une application qui surveille l’activité de échange dynamique de données (DDE) dans le système. Comme n’importe quelle application DDEML, une application de surveillance DDE contient une fonction de rappel DDE. Le DDEML notifie la fonction de rappel DDE d’une application de surveillance chaque fois qu’un événement DDE se produit, en passant des informations sur l’événement à la fonction de rappel. L’application affiche généralement les informations dans une fenêtre ou les écrit dans un fichier.

Pour recevoir des notifications de DDEML, une application doit être inscrite en tant qu’analyseur DDE en spécifiant l' \_ indicateur de moniteur APPCLASS dans un appel à la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . Dans ce même appel, l’application peut spécifier un ou plusieurs indicateurs d’analyse pour indiquer les types d’événements pour lesquels le DDEML doit notifier la fonction de rappel de l’application. Les indicateurs de surveillance suivants peuvent être spécifiés par une application :



| Indicateur          | Description                                                                                                                                                                                                                                         |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_rappels MF | Notifie la fonction de rappel chaque fois qu’une transaction est envoyée à une fonction de rappel DDE dans le système.                                                                                                                                           |
| \_conv CONV      | Notifie la fonction de rappel lorsqu’une conversation est établie ou terminée.                                                                                                                                                                |
| \_Erreurs MF    | Notifie la fonction de rappel chaque fois qu’une erreur DDEML se produit.                                                                                                                                                                                       |
| \_infos HSZ \_ MF | Notifie la fonction de rappel lorsqu’une application DDEML crée, libère ou incrémente le décompte d’utilisation d’un handle de chaîne ou chaque fois qu’un handle de chaîne est libéré à la suite d’un appel à la fonction [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) . |
| \_liens MF     | Notifie la fonction de rappel chaque fois qu’une boucle de notification est démarrée ou terminée.                                                                                                                                                                         |
| \_POSTMSGS MF  | Notifie la fonction de rappel chaque fois que le système ou une application publie un message DDE.                                                                                                                                                           |
| \_SENDMSGS MF  | Notifie la fonction de rappel chaque fois que le système ou une application envoie un message DDE.                                                                                                                                                           |



 

L’exemple suivant montre comment inscrire une application de surveillance DDE afin que sa fonction de rappel DDE reçoive des notifications de tous les événements DDE.


```
DWORD idInst; 
PFNCALLBACK lpDdeProc; 
hInst = hInstance; 
 
if (DdeInitialize( 
        (LPDWORD) &idInst,  // instance identifier 
        DDECallback,        // pointer to callback function 
        APPCLASS_MONITOR |  // this is a monitoring application 
        MF_CALLBACKS     |  // monitor callback functions 
        MF_CONV          |  // monitor conversation data 
        MF_ERRORS        |  // monitor DDEML errors 
        MF_HSZ_INFO      |  // monitor data handle activity 
        MF_LINKS         |  // monitor advise loops 
        MF_POSTMSGS      |  // monitor posted DDE messages 
        MF_SENDMSGS,        // monitor sent DDE messages 
        0))                 // reserved 
{
    return FALSE; 
}
```



DDEML informe l’application de surveillance d’un événement DDE en envoyant une transaction de [**surveillance \_ XTYP**](xtyp-monitor.md) à la fonction de rappel DDE de l’application. Au cours de cette transaction, DDEML transmet un indicateur d’analyse spécifiant le type d’événement DDE qui s’est produit et un handle vers un objet DDE qui contient des informations détaillées sur l’événement. DDEML fournit un ensemble de structures que l’application peut utiliser pour extraire les informations de l’objet DDE. Il existe une structure correspondante pour chaque type d’événement DDE.



| Structure                                  | Description                                                       |
|--------------------------------------------|-------------------------------------------------------------------|
| [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)     | Contient des informations sur une transaction.                         |
| [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) | Contient des informations sur une conversation.                        |
| [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)   | Contient des informations sur la dernière erreur DDE.                  |
| [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) | Contient des informations sur une boucle de notification.                        |
| [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)   | Contient des informations sur un handle de chaîne.                       |
| [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)   | Contient des informations sur un message DDE qui a été envoyé ou publié. |



 

L’exemple suivant illustre la fonction de rappel DDE d’une application de surveillance DDE qui met en forme les informations relatives à chaque événement de handle de chaîne, puis affiche les informations dans une fenêtre. La fonction utilise la structure [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) pour extraire les informations de l’objet DDE.


```
HDDEDATA CALLBACK DDECallback(uType, uFmt, hconv, hsz1, hsz2, 
    hdata, dwData1, dwData2) 
UINT uType; 
UINT uFmt; 
HCONV hconv; 
HSZ hsz1; 
HSZ hsz2; 
HDDEDATA hdata; 
DWORD dwData1; 
DWORD dwData2; 
{ 
    LPVOID lpData; 
    CHAR *szAction; 
    CHAR szBuf[256]; 
    DWORD cb;
    HRESULT hResult; 
 
    switch (uType) 
    { 
        case XTYP_MONITOR: 
            // Obtain a pointer to the global memory object. 
 
            if (lpData = DdeAccessData(hdata, &cb)) 
            { 
                // Examine the monitor flag. 
 
                switch (dwData2) 
                { 
                    case MF_HSZ_INFO: 
 
#define PHSZS ((MONHSZSTRUCT *)lpData) 
 
                        // The global memory object contains 
                        // string handle data. Use the MONHSZSTRUCT 
                        // structure to access the data. 
 
                        switch (PHSZS->fsAction) 
                        { 
                            // Examine the action flags to determine
                            // the action performed on the handle.
 
                            case MH_CREATE: 
                                szAction = "Created"; 
                                break; 
 
                            case MH_KEEP: 
                                szAction = "Incremented"; 
                                break; 
 
                            case MH_DELETE: 
                                szAction = "Deleted"; 
                                break; 
 
                            case MH_CLEANUP: 
                                szAction = "Cleaned up"; 
                                break; 
 
                            default: 
                                DdeUnaccessData(hdata); 
                                return (HDDEDATA) 0; 
                        } 
 
                        // Write formatted output to a buffer. 
                        hResult = StringCchPrintf(szBuf, 256/sizeof(TCHAR),
                            "Handle %s, Task: %x, Hsz: %lx(%s)", 
                            (LPSTR) szAction, PHSZS->hTask, 
                            PHSZS->hsz, (LPSTR) PHSZS->str);
                        if (FAILED(hResult))
                        {
                        // TO DO: Write error handler.
                            return;
                        } 
                        // Display text or write to a file. 
 
                        break; 
 
#undef PHSZS 
 
                    // Process other MF_* flags. 
 
                    default: 
                        break; 
                } 
            } 
 
            // Free the global memory object. 
 
            DdeUnaccessData(hdata); 
            break; 
 
        default: 
            break; 
    } 
    return (HDDEDATA) 0; 
} 
```



 

 




