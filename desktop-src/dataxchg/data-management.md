---
title: Gestion des données
description: Cette rubrique explique comment les objets mémoire passent des données d’une application à une autre.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Windows Interface utilisateur, échange dynamique de données (DDE)
- échange dynamique de données (DDE), gestion des données
- DDE (échange dynamique de données), gestion des données
- échange de données, échange dynamique de données (DDE)
- Windows Interface utilisateur, échange dynamique de données Management Library (DDEML)
- bibliothèque de gestion des échange dynamique de données (DDEML), gestion des données
- DDEML (bibliothèque de gestion échange dynamique de données), gestion des données
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
- échange dynamique de données (DDE), objets
- DDE (échange dynamique de données), objets
- bibliothèque de gestion des échange dynamique de données (DDEML), objets
- DDEML (bibliothèque de gestion échange dynamique de données), objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85dc9b8ccd82d184866ac9ed28f15bdeac424ec0bf9bd7767a520dea69bc4d11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953739"
---
# <a name="data-management"></a>Gestion des données

étant donné que échange dynamique de données (DDE) utilise des objets mémoire pour transmettre des données d’une application à une autre, la bibliothèque de gestion des échange dynamique de données (DDEML) fournit un ensemble de fonctions que les applications dde peuvent utiliser pour créer et gérer des objets dde.

Toutes les transactions qui impliquent l’échange de données requièrent que l’application fournisse les données pour créer une mémoire tampon locale contenant les données, puis appelle la fonction [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) . Cette fonction alloue un objet DDE, copie les données de la mémoire tampon vers l’objet et retourne un handle de données. Un descripteur de données est une valeur **DWORD** que le Ddeml utilise pour fournir l’accès aux données dans l’objet DDE. Pour partager les données dans un objet DDE, une application transmet le descripteur de données à DDEML et DDEML transmet le descripteur à la fonction de rappel DDE de l’application qui reçoit la transaction de données.

L’exemple suivant montre comment créer un objet DDE et obtenir un descripteur de l’objet. Pendant la transaction [**XTYP \_ ADVREQ**](xtyp-advreq.md) , la fonction de rappel convertit l’heure actuelle en une chaîne ASCII, copie la chaîne dans une mémoire tampon locale, puis crée un objet DDE qui contient la chaîne. La fonction de rappel retourne le descripteur de l’objet DDE (HDDEDATA) au DDEML, qui passe le descripteur à l’application cliente.


```
typedef struct tagTIME 
{ 
    INT     hour;   // 0 - 11 hours for analog clock 
    INT     hour12; // 12-hour format 
    INT     hour24; // 24-hour format 
    INT     minute; 
    INT     second; 
    INT     ampm;   // 0 - AM , 1 - PM 
} TIME; 
 
HDDEDATA EXPENTRY DdeCallback(uType, uFmt, hconv, hsz1, hsz2, 
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
 
    CHAR szBuf[32];
    HRESULT hResult;
    size_t * pcch;
    HRESULT hResult; 
 
    switch (uType) 
    { 
    case XTYP_ADVREQ: 
        if ((hsz1 == hszTime && hsz2 == hszNow) && 
                (uFmt == CF_TEXT)) 
        { 
            // Copy the formatted string to a buffer. 
 
            itoa(tmTime.hour, szBuf, 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.minute < 10)
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
                if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            } 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.minute, &szBuf[*pcch], 10);
            hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), ":"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            if (tmTime.second < 10) 
                hResult = StringCchCat(szBuf, 32/sizeof(TCHAR), "0"); 
            if (FAILED(hResult)
            {
            // TO DO: Write error handler.
                return;
            }
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            itoa(tmTime.second, &szBuf[*pcch], 10);
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            } 
            szBuf[*pcch] = '\0'; 
 
            // Create a global object and return its data handle. 
            hResult = StringCchLength(szBuf, 32/sizeof(TCHAR), pcch);
            if (FAILED(hResult))
            {
            // TO DO: Write error handler.
                return;
            }
            return (DdeCreateDataHandle( 
                idInst, 
                (LPBYTE) szBuf,     // instance identifier 
                *pcch + 1,          // source buffer length 
                0,                  // offset from beginning 
                hszNow,             // item name string 
                CF_TEXT,            // clipboard format 
                0));                // no creation flags 
        } else return (HDDEDATA) NULL; 
 
    // Process other transactions. 
    } 
} 
```



L’application réceptrice obtient un pointeur vers l’objet DDE en passant le descripteur de données à la fonction [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) . Le pointeur retourné par **DdeAccessData** fournit un accès en lecture seule. L’application doit utiliser le pointeur pour passer en revue les données, puis appeler la fonction [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) pour invalider le pointeur. L’application peut copier les données dans une mémoire tampon locale à l’aide de la fonction [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) .

L’exemple suivant obtient un pointeur vers l’objet DDE identifié par le paramètre *hdata* , copie le contenu dans une mémoire tampon locale, puis invalide le pointeur.


```
HDDEDATA hdata; 
LPBYTE lpszAdviseData; 
DWORD cbDataLen; 
DWORD i; 
char szData[32]; 
 
// 
case XTYP_ADVDATA: 
    lpszAdviseData = DdeAccessData(hdata, &cbDataLen); 
    for (i = 0; i < cbDataLen; i++) 
        szData[i] = *lpszAdviseData++; 
    DdeUnaccessData(hdata); 
    return (HDDEDATA) TRUE; 
//
```



En général, lorsqu’une application qui a créé un descripteur de données passe ce handle à DDEML, le descripteur devient non valide dans l’application de création. Cette situation n’est pas un problème si l’application doit partager des données avec une seule application. Toutefois, si une application doit partager les mêmes données avec plusieurs applications, l’application de création doit spécifier l' \_ indicateur HDATA APPOWNED dans [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle). Cela donne la propriété de l’objet DDE à l’application de création et empêche le DDEML d’invalider le descripteur de données. L’application peut ensuite passer le handle de données un nombre quelconque de fois après avoir appelé **DdeCreateDataHandle** une seule fois.

Si une application spécifie l' \_ indicateur HDATA APPOWNED dans le paramètre *AfCmd* de [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), elle doit appeler la fonction [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) pour libérer le handle de mémoire, qu’elle ait passé ou non le descripteur au Ddeml. Avant qu’elle ne se termine, une application doit appeler **DdeFreeDataHandle** pour libérer tout handle de données qu’elle a créé, mais n’a pas réussi à Ddeml.

Une application qui n’a pas encore passé le descripteur d’un objet DDE au DDEML peut ajouter des données à l’objet ou remplacer des données dans l’objet à l’aide de la fonction [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) . En règle générale, une application utilise **DdeAddData** pour remplir un objet DDE non initialisé. Une fois qu’une application a transmis un descripteur de données au DDEML, l’objet DDE identifié par le descripteur ne peut pas être modifié. elle peut uniquement être libérée.

 

 




