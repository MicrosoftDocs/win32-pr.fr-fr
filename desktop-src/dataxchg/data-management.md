---
title: Gestion des données
description: Cette rubrique explique comment les objets mémoire passent des données d’une application à une autre.
ms.assetid: 32919f27-4699-4831-8837-c5160b1daf4e
keywords:
- Interface utilisateur Windows, échange dynamique de données (DDE)
- Échange dynamique de données (DDE), gestion des données
- DDE (échange dynamique de données), gestion des données
- échange de données, échange dynamique de données (DDE)
- Interface utilisateur Windows, bibliothèque de gestion des échange dynamique de données (DDEML)
- Bibliothèque de gestion des échange dynamique de données (DDEML), gestion des données
- DDEML (bibliothèque de gestion échange dynamique de données), gestion des données
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
- Échange dynamique de données (DDE), objets
- DDE (échange dynamique de données), objets
- Bibliothèque de gestion des échange dynamique de données (DDEML), objets
- DDEML (bibliothèque de gestion échange dynamique de données), objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc5178f636cf4b75111d4fc48e17fd144400a91
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380402"
---
# <a name="data-management"></a><span data-ttu-id="774e0-115">Gestion des données</span><span class="sxs-lookup"><span data-stu-id="774e0-115">Data Management</span></span>

<span data-ttu-id="774e0-116">Étant donné que échange dynamique de données (DDE) utilise des objets mémoire pour transmettre des données d’une application à une autre, la bibliothèque de gestion des échange dynamique de données (DDEML) fournit un ensemble de fonctions que les applications DDE peuvent utiliser pour créer et gérer des objets DDE.</span><span class="sxs-lookup"><span data-stu-id="774e0-116">Because Dynamic Data Exchange (DDE) uses memory objects to pass data from one application to another, the Dynamic Data Exchange Management Library (DDEML) provides a set of functions that DDE applications can use to create and manage DDE objects.</span></span>

<span data-ttu-id="774e0-117">Toutes les transactions qui impliquent l’échange de données requièrent que l’application fournisse les données pour créer une mémoire tampon locale contenant les données, puis appelle la fonction [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) .</span><span class="sxs-lookup"><span data-stu-id="774e0-117">All transactions that involve the exchange of data require the application supplying the data to create a local buffer containing the data and then to call the [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) function.</span></span> <span data-ttu-id="774e0-118">Cette fonction alloue un objet DDE, copie les données de la mémoire tampon vers l’objet et retourne un handle de données.</span><span class="sxs-lookup"><span data-stu-id="774e0-118">This function allocates a DDE object, copies the data from the buffer to the object, and returns a data handle.</span></span> <span data-ttu-id="774e0-119">Un descripteur de données est une valeur **DWORD** que le Ddeml utilise pour fournir l’accès aux données dans l’objet DDE.</span><span class="sxs-lookup"><span data-stu-id="774e0-119">A data handle is a **DWORD** value that the DDEML uses to provide access to data in the DDE object.</span></span> <span data-ttu-id="774e0-120">Pour partager les données dans un objet DDE, une application transmet le descripteur de données à DDEML et DDEML transmet le descripteur à la fonction de rappel DDE de l’application qui reçoit la transaction de données.</span><span class="sxs-lookup"><span data-stu-id="774e0-120">To share the data in a DDE object, an application passes the data handle to the DDEML, and the DDEML passes the handle to the DDE callback function of the application that is receiving the data transaction.</span></span>

<span data-ttu-id="774e0-121">L’exemple suivant montre comment créer un objet DDE et obtenir un descripteur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="774e0-121">The following example shows how to create a DDE object and obtain a handle to the object.</span></span> <span data-ttu-id="774e0-122">Pendant la transaction [**XTYP \_ ADVREQ**](xtyp-advreq.md) , la fonction de rappel convertit l’heure actuelle en une chaîne ASCII, copie la chaîne dans une mémoire tampon locale, puis crée un objet DDE qui contient la chaîne.</span><span class="sxs-lookup"><span data-stu-id="774e0-122">During the [**XTYP\_ADVREQ**](xtyp-advreq.md) transaction, the callback function converts the current time to an ASCII string, copies the string to a local buffer, and then creates a DDE object that contains the string.</span></span> <span data-ttu-id="774e0-123">La fonction de rappel retourne le descripteur de l’objet DDE (HDDEDATA) au DDEML, qui passe le descripteur à l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="774e0-123">The callback function returns the handle to the DDE object (HDDEDATA) to the DDEML, which passes the handle to the client application.</span></span>


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



<span data-ttu-id="774e0-124">L’application réceptrice obtient un pointeur vers l’objet DDE en passant le descripteur de données à la fonction [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) .</span><span class="sxs-lookup"><span data-stu-id="774e0-124">The receiving application obtains a pointer to the DDE object by passing the data handle to the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function.</span></span> <span data-ttu-id="774e0-125">Le pointeur retourné par **DdeAccessData** fournit un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="774e0-125">The pointer returned by **DdeAccessData** provides read-only access.</span></span> <span data-ttu-id="774e0-126">L’application doit utiliser le pointeur pour passer en revue les données, puis appeler la fonction [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) pour invalider le pointeur.</span><span class="sxs-lookup"><span data-stu-id="774e0-126">The application should use the pointer to review the data and then call the [**DdeUnaccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeunaccessdata) function to invalidate the pointer.</span></span> <span data-ttu-id="774e0-127">L’application peut copier les données dans une mémoire tampon locale à l’aide de la fonction [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) .</span><span class="sxs-lookup"><span data-stu-id="774e0-127">The application can copy the data to a local buffer by using the [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) function.</span></span>

<span data-ttu-id="774e0-128">L’exemple suivant obtient un pointeur vers l’objet DDE identifié par le paramètre *hdata* , copie le contenu dans une mémoire tampon locale, puis invalide le pointeur.</span><span class="sxs-lookup"><span data-stu-id="774e0-128">The following example obtains a pointer to the DDE object identified by the *hData* parameter, copies the contents to a local buffer, and then invalidates the pointer.</span></span>


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



<span data-ttu-id="774e0-129">En général, lorsqu’une application qui a créé un descripteur de données passe ce handle à DDEML, le descripteur devient non valide dans l’application de création.</span><span class="sxs-lookup"><span data-stu-id="774e0-129">Usually, when an application that created a data handle passes that handle to the DDEML, the handle becomes invalid in the creating application.</span></span> <span data-ttu-id="774e0-130">Cette situation n’est pas un problème si l’application doit partager des données avec une seule application.</span><span class="sxs-lookup"><span data-stu-id="774e0-130">This situation is not a problem if the application must share data with only a single application.</span></span> <span data-ttu-id="774e0-131">Toutefois, si une application doit partager les mêmes données avec plusieurs applications, l’application de création doit spécifier l' \_ indicateur HDATA APPOWNED dans [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle).</span><span class="sxs-lookup"><span data-stu-id="774e0-131">If an application must share the same data with multiple applications, however, the creating application should specify the HDATA\_APPOWNED flag in [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle).</span></span> <span data-ttu-id="774e0-132">Cela donne la propriété de l’objet DDE à l’application de création et empêche le DDEML d’invalider le descripteur de données.</span><span class="sxs-lookup"><span data-stu-id="774e0-132">Doing so gives ownership of the DDE object to the creating application and prevents the DDEML from invalidating the data handle.</span></span> <span data-ttu-id="774e0-133">L’application peut ensuite passer le handle de données un nombre quelconque de fois après avoir appelé **DdeCreateDataHandle** une seule fois.</span><span class="sxs-lookup"><span data-stu-id="774e0-133">The application can then pass the data handle any number of times after calling **DdeCreateDataHandle** only once.</span></span>

<span data-ttu-id="774e0-134">Si une application spécifie l' \_ indicateur HDATA APPOWNED dans le paramètre *AfCmd* de [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), elle doit appeler la fonction [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) pour libérer le handle de mémoire, qu’elle ait passé ou non le descripteur au Ddeml.</span><span class="sxs-lookup"><span data-stu-id="774e0-134">If an application specifies the HDATA\_APPOWNED flag in the *afCmd* parameter of [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle), it must call the [**DdeFreeDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreedatahandle) function to free the memory handle, regardless of whether it passed the handle to the DDEML.</span></span> <span data-ttu-id="774e0-135">Avant qu’elle ne se termine, une application doit appeler **DdeFreeDataHandle** pour libérer tout handle de données qu’elle a créé, mais n’a pas réussi à Ddeml.</span><span class="sxs-lookup"><span data-stu-id="774e0-135">Before it terminates, an application must call **DdeFreeDataHandle** to free any data handle that it created but did not pass to the DDEML.</span></span>

<span data-ttu-id="774e0-136">Une application qui n’a pas encore passé le descripteur d’un objet DDE au DDEML peut ajouter des données à l’objet ou remplacer des données dans l’objet à l’aide de la fonction [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) .</span><span class="sxs-lookup"><span data-stu-id="774e0-136">An application that has not yet passed the handle to a DDE object to the DDEML can add data to the object or overwrite data in the object by using the [**DdeAddData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeadddata) function.</span></span> <span data-ttu-id="774e0-137">En règle générale, une application utilise **DdeAddData** pour remplir un objet DDE non initialisé.</span><span class="sxs-lookup"><span data-stu-id="774e0-137">Typically, an application uses **DdeAddData** to fill an uninitialized DDE object.</span></span> <span data-ttu-id="774e0-138">Une fois qu’une application a transmis un descripteur de données au DDEML, l’objet DDE identifié par le descripteur ne peut pas être modifié. elle peut uniquement être libérée.</span><span class="sxs-lookup"><span data-stu-id="774e0-138">After an application passes a data handle to the DDEML, the DDE object identified by the handle cannot be changed; it can only be freed.</span></span>

 

 




