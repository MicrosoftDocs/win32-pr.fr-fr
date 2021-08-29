---
title: Sessions HTTP
description: Les ressources sur le Web sont accessibles à l’aide de http.
ms.assetid: 0f307e28-9c38-41e7-9795-7eef08e99a3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ab6e151a726b0d947636818fea9de7946f250ded5adfcd7f145df8945f07b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758959"
---
# <a name="http-sessions"></a>Sessions HTTP

WinINet vous permet d’accéder aux ressources du World Wide Web (WWW). Vous pouvez accéder directement à ces ressources à l’aide de [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour plus d’informations, consultez [accès direct aux URL](handling-uniform-resource-locators.md)).

Les ressources sur le Web sont accessibles à l’aide de http. Les fonctions HTTP gèrent les protocoles sous-jacents, tout en permettant à votre application d’accéder à des informations sur le Web. À mesure que le protocole HTTP évolue, les protocoles sous-jacents sont mis à jour pour maintenir le comportement de la fonction.

Le diagramme suivant montre les relations des fonctions utilisées avec le protocole HTTP. Les zones grisées représentent des fonctions qui retournent des handles [**HINTERNET**](appendix-a-hinternet-handles.md) , tandis que les zones simples représentent des fonctions qui utilisent le descripteur **HINTERNET** créé par la fonction sur laquelle ils dépendent.

![fonctions WinInet utilisées pour http](images/ax-wnt05.png)

Pour plus d’informations, consultez [Handles HINTERNET](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-to-access-the-www"></a>Utilisation des fonctions WinINet pour accéder au Web

-   [Initiation d’une connexion au Web](#initiating-a-connection-to-the-www)
-   [Ouverture d’une demande](#opening-a-request)
-   [Ajout d’en-têtes de demande](#adding-request-headers)
-   [Envoi d’une demande](#sending-a-request)
-   [Publication des données sur le serveur](#posting-data-to-the-server)
-   [Obtention d’informations sur une demande](#getting-information-about-a-request)
-   [Téléchargement des ressources à partir du Web](#downloading-resources-from-the-www)

Les fonctions suivantes sont utilisées pendant les sessions HTTP pour accéder au Web.



| Fonction                                               | Description                                                                                                                                                                                  |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) | Ajoute des en-têtes de requête HTTP au descripteur de requête HTTP. Cette fonction requiert un handle créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                 |
| [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)             | Ouvre un handle de requête HTTP. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                                                         |
| [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa)                 | Interroge les informations relatives à une requête HTTP. Cette fonction requiert un handle créé par la fonction [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . |
| [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)             | Envoie la requête HTTP spécifiée au serveur HTTP. Cette fonction requiert un handle créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).                                                  |
| [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg)           | Affiche des boîtes de dialogue prédéfinies pour les conditions d’erreur Internet courantes. Cette fonction requiert le handle utilisé dans l’appel à [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).                     |



 

### <a name="initiating-a-connection-to-the-www"></a>Initiation d’une connexion au Web

Pour démarrer une connexion au Web, l’application doit appeler la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) sur le [**HINTERNET**](appendix-a-hinternet-handles.md) racine retourné par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) doit établir une session http en déclarant le type de \_ service http du service Internet \_ . Pour plus d’informations sur l’utilisation de [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), consultez [utilisation de internetconnect](enabling-internet-functionality.md).

### <a name="opening-a-request"></a>Ouverture d’une demande

La fonction [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ouvre une requête HTTP et retourne un descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) qui peut être utilisé par les autres fonctions http. Contrairement aux autres fonctions ouvertes (telles que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) n’envoie pas la requête à Internet lorsqu’elle est appelée. La fonction [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) envoie la demande et établit une connexion sur le réseau.

[**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) accepte un descripteur de session http créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) et un verbe http, un nom d’objet, une chaîne de version, un point d’interconnexion, des types d’acceptation, des indicateurs et une valeur de contexte.

Le verbe HTTP est une chaîne à utiliser dans la demande. Les verbes HTTP courants utilisés dans les demandes sont les suivants : obtient, PUT et poster. Si cette valeur est définie sur **null**, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) utilise la valeur par défaut obten.

Le nom de l’objet est une chaîne qui contient le nom de l’objet cible du verbe HTTP spécifié. Il s’agit généralement d’un nom de fichier, d’un module exécutable ou d’un spécificateur de recherche. Si le nom d’objet fourni est une chaîne vide, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) recherche la page par défaut.

La chaîne de version doit contenir la version HTTP. Si ce paramètre a la **valeur null**, la fonction utilise « http/1.1 ».

Le référent spécifie l’adresse du document à partir duquel le nom de l’objet a été obtenu. Si ce paramètre a la **valeur null**, aucun référent n’est spécifié.

La chaîne terminée par le caractère **null** qui contient les types Accept indique les types de contenu acceptés par l’application. Si ce paramètre a la **valeur null** , cela signifie qu’aucun type de contenu n’est accepté par l’application. Si une chaîne vide est fournie, l’application indique qu’elle accepte uniquement les documents de type "" Text/ \* "". La valeur « "Text/ \* " » indique des documents texte uniquement, et non des images ou d’autres fichiers binaires.

Les valeurs d’indicateur contrôlent la mise en cache, les cookies et les problèmes de sécurité. Pour Microsoft Network (MSN), NTLM et d’autres types d’authentification, définissez l’indicateur de maintien de la [ \_ \_ \_ connexion à l’indicateur Internet](api-flags.md) .

Si l' [indicateur \_ \_ Async de l’indicateur Internet](api-flags.md) a été défini dans l’appel à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), une valeur de contexte différente de zéro doit être définie pour une opération asynchrone appropriée.

L’exemple suivant est un exemple d’appel à [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

`hHttpRequest = HttpOpenRequest( hHttpSession, "GET", "", NULL, "", NULL, 0, 0);`

### <a name="adding-request-headers"></a>Ajout d’en-têtes de demande

La fonction [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) permet aux applications d’ajouter un ou plusieurs en-têtes de demande à la requête initiale. Cette fonction permet à une application d’ajouter des en-têtes de format libre supplémentaires au handle de requête HTTP. elle est destinée à être utilisée par des applications sophistiquées qui requièrent un contrôle précis sur la requête envoyée au serveur HTTP.

[**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) a besoin d’un handle de requête http créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), d’une chaîne qui contient les en-têtes, de la longueur des en-têtes et des modificateurs.

### <a name="sending-a-request"></a>Envoi d’une demande

[**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) établit une connexion à Internet et envoie la demande au site spécifié. Cette fonction requiert un handle [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) peut également envoyer des en-têtes supplémentaires ou des informations facultatives. Les informations facultatives sont généralement utilisées pour les opérations qui écrivent des informations sur le serveur, telles que PUT et poster.

Une fois que [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) a envoyé la demande, l’application peut utiliser les fonctions [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)et [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) sur le handle [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) pour télécharger les ressources du serveur.

### <a name="posting-data-to-the-server"></a>Publication des données sur le serveur

Pour la publication de données sur un serveur, le verbe HTTP dans l’appel à [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) doit être de type « publication » ou « put ». L’adresse de la mémoire tampon qui contient les données de publication doit ensuite être passée au paramètre *lpOptional* dans [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Le paramètre *dwOptionalLength* doit être défini sur la taille des données.

Vous pouvez également utiliser la fonction [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) pour envoyer des données sur un handle [**HINTERNET**](appendix-a-hinternet-handles.md) envoyé à l’aide de [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa).

### <a name="getting-information-about-a-request"></a>Obtention d’informations sur une demande

[**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) permet à une application de récupérer des informations sur une requête http. La fonction requiert un handle [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), une valeur de niveau d’information et une longueur de mémoire tampon. [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) accepte également une mémoire tampon qui stocke les informations et un index d’en-tête de base zéro qui énumère plusieurs en-têtes portant le même nom.

### <a name="downloading-resources-from-the-www"></a>Téléchargement des ressources à partir du Web

Après avoir ouvert une demande avec [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et l’avoir envoyée au serveur [**avec HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), l’application peut utiliser les fonctions [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)et [**INTERNETSETFILEPOINTER**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) pour télécharger la ressource à partir du serveur http.

L’exemple suivant télécharge une ressource. La fonction accepte le descripteur de la fenêtre active, le numéro d’identification d’une zone d’édition et un handle [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et envoyé par [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Elle utilise [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) pour déterminer la taille de la ressource, puis la télécharge à l’aide de [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Le contenu est ensuite affiché dans la zone d’édition.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR lpszData;    // buffer for the data
    DWORD  dwSize;       // size of the data available
    DWORD  dwDownloaded; // size of the downloaded data
    DWORD  dwSizeSum=0;  // size of the data in the textbox
    LPTSTR lpszHolding;  // buffer to merge the textbox data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            printf("InternetQueryDataAvailable failed (%d)\n", GetLastError());
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,
                                 (LPVOID)lpszData,
                                 dwSize,
                                 &dwDownloaded))
            {
                printf("InternetReadFile failed (%d)\n", GetLastError());
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the data buffer
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];

                // Check if there has been any data written
                // to the textbox.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the textbox if any
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding,
                                   dwSizeSum);

                    // Add a null terminator at the end of the
                    // textbox data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string.
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + dwDownloaded + 1;
                LPTSTR* ppszDestEnd = 0;
                size_t* pcchRemaining = 0;

                // Add the new data to the holding buffer
                HRESULT hr = StringCchCatEx(lpszHolding,
                                            cchDest,
                                            lpszData,
                                            ppszDestEnd,
                                            pcchRemaining,
                                            STRSAFE_NO_TRUNCATION);

                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the textbox.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to the
                    // textbox data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                        break;
                    else
                    {
                    //  TODO: Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    return TRUE;
}
```



> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 