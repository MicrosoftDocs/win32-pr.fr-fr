---
title: Gestion des localisateurs de ressources uniformes
description: Une Uniform Resource Locator (URL) est une représentation compacte de l’emplacement et de la méthode d’accès d’une ressource située sur Internet.
ms.assetid: bb59ada6-f49f-412c-a32c-4fb9495b1222
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08157738d99e78ff4d458a3bdd1b1e2e661ce538
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531012"
---
# <a name="handling-uniform-resource-locators"></a>Gestion des localisateurs de ressources uniformes

Une Uniform Resource Locator (URL) est une représentation compacte de l’emplacement et de la méthode d’accès d’une ressource située sur Internet. Chaque URL se compose d’un schéma (HTTP, HTTPs ou FTP) et d’une chaîne spécifique au schéma. Cette chaîne peut également inclure une combinaison d’un chemin d’accès de répertoire, d’une chaîne de recherche ou d’un nom de ressource. Les fonctions WinINet offrent la possibilité de créer, combiner, décomposer et canonicaliser des URL. Pour plus d’informations sur les URL, consultez [RFC-1738 sur les](https://www.ietf.org/rfc/rfc1738.txt) URL (Uniform Resource Locators).

Les fonctions d’URL fonctionnent de manière orientée tâche. Le contenu et le format de l’URL qui est donnée à la fonction ne sont pas vérifiés. L’application appelante doit suivre l’utilisation de ces fonctions pour s’assurer que les données sont au format prévu. Par exemple, la fonction [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) convertit le caractère « % » en séquence d’échappement « %25 » lors de l’utilisation d’aucun indicateur. Si [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) est utilisé sur l’URL canonique, la séquence d’échappement « %25 » est convertie en séquence d’échappement « %2525 », ce qui ne fonctionnerait pas correctement.

-   [Qu’est-ce qu’une URL canonique ?](#what-is-a-canonicalized-url)
-   [Utilisation des fonctions WinINet pour gérer les URL](#using-the-wininet-functions-to-handle-urls)
-   [Canonicalisation des URL](#what-is-a-canonicalized-url)
-   [Combinaison d’URL de base et relatives](#combining-base-and-relative-urls)
-   [Piratage des URL](#cracking-urls)
-   [Création d’URL](#creating-urls)
-   [Accès direct aux URL](#accessing-urls-directly)

## <a name="what-is-a-canonicalized-url"></a>Qu’est-ce qu’une URL canonique ?

Le format de toutes les URL doit respecter la syntaxe et la sémantique acceptées afin d’accéder aux ressources via Internet. La canonicalisation est le processus de mise en forme d’une URL pour suivre cette syntaxe et cette sémantique acceptées.

Les caractères qui doivent être encodés incluent tous les caractères qui n’ont aucun caractère graphique correspondant dans le jeu de caractères codés US-ASCII (hexadécimal 80-FF, qui ne sont pas utilisés dans le jeu de caractères codés US-ASCII, et les valeurs hexadécimales 00-1F et 7F, qui sont des caractères de contrôle), des espaces vides, « % » (qui est utilisé pour encoder d’autres caractères) et des caractères non sûrs (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ \]

## <a name="using-the-wininet-functions-to-handle-urls"></a>Utilisation des fonctions WinINet pour gérer les URL

Le tableau suivant récapitule les fonctions d’URL.



| Fonction                                                   | Description                                        |
|------------------------------------------------------------|----------------------------------------------------|
| [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) | Canonicalizes l’URL.                             |
| [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla)           | Combine des URL de base et relatives.                   |
| [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla)               | Analyse une chaîne d’URL en composants.               |
| [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla)             | Crée une chaîne d’URL à partir de composants.              |
| [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)                 | Commence à récupérer une ressource FTP, HTTP ou HTTPs. |



 

## <a name="canonicalizing-urls"></a>Canonicalisation des URL

La canonicalisation d’une URL est le processus qui convertit une URL, qui peut contenir des caractères non sécurisés tels que des espaces vides, des caractères réservés, etc., dans un format accepté.

La fonction [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) peut être utilisée pour canonicaliser des URL. Cette fonction étant très orientée tâche, l’application doit suivre son utilisation avec précaution. [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) ne vérifie pas que l’URL qui lui est transmise est déjà canonique et que l’URL renvoyée est valide.

Les cinq indicateurs suivants contrôlent la façon dont [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) gère une URL particulière. Les indicateurs peuvent être utilisés en combinaison. Si aucun indicateur n’est utilisé, la fonction encode l’URL par défaut.



| Valeur                     | Signification                                                                                                                                                                                                 |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_mode navigateur \_ ICU        | Ne pas encoder ou décoder les caractères après « \# » ou «  ? » et ne pas supprimer les espaces blancs de fin après «  ? ». Si cette valeur n’est pas spécifiée, l’URL entière est encodée et l’espace blanc de fin est supprimé. |
| décodage ICU \_               | Convertit toutes les séquences% XX en caractères, y compris les séquences d’échappement, avant l’analyse de l’URL.                                                                                                          |
| BIBLIOTHÈQUE de \_ codage des \_ espaces \_ uniquement | Encoder les espaces uniquement.                                                                                                                                                                                     |
| ICU \_ sans \_ codage           | Ne convertissez pas les caractères non sécurisés en séquences d’échappement.                                                                                                                                                   |
| ICU \_ sans \_ méta             | Ne supprimez pas les séquences Meta (telles que « . » et « .. ») de l’URL.                                                                                                                                       |



 

L' \_ indicateur de décodage ICU doit être utilisé uniquement sur les URL canoniques, car il suppose que toutes les séquences% XX sont des codes d’échappement et les convertit en caractères indiqués par le code. Si l’URL contient un symbole « % » qui ne fait pas partie d’un code d’échappement, ICU \_ Decode le traite toujours comme un. Cette caractéristique peut entraîner la création par [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) d’une URL non valide.

Pour utiliser [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) afin de retourner une URL complètement décodée, les indicateurs de décodage ICU \_ et de bibliothèque ICU \_ ne \_ doivent pas être spécifiés. Ce programme d’installation suppose que l’URL passée à [**InternetCanonicalizeUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcanonicalizeurla) a déjà été rendue canonique.

## <a name="combining-base-and-relative-urls"></a>Combinaison d’URL de base et relatives

Une URL relative est une représentation compacte de l’emplacement d’une ressource par rapport à une URL de base absolue. L’URL de base doit être connue de l’analyseur et inclure généralement le schéma, l’emplacement réseau et les parties du chemin d’accès de l’URL. Une application peut appeler [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) pour combiner l’URL relative avec son URL de base. [**InternetCombineUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcombineurla) canonicalizes également l’URL résultante.

## <a name="cracking-urls"></a>Piratage des URL

La fonction [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) sépare une URL en ses composants et retourne les composants indiqués par la structure [**de \_ composants URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) qui est transmise à la fonction.

Les composants qui composent la structure des [**\_ composants d’URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) sont le numéro de schéma, le nom d’hôte, le numéro de port, le nom d’utilisateur, le mot de passe, le chemin d’URL et des informations supplémentaires (tels que les paramètres de recherche). Chaque composant, sauf le schéma et le numéro de port, a un membre de chaîne qui contient les informations et un membre qui contient la longueur du membre de chaîne. Le schéma et les numéros de port ont uniquement un membre qui stocke la valeur correspondante ; elles sont toutes deux retournées sur tous les appels réussis à [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla).

Pour obtenir la valeur d’un composant particulier dans la structure de [**\_ composants URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , le membre qui stocke la longueur de chaîne de ce composant doit être défini sur une valeur différente de zéro. Le membre de chaîne peut être l’adresse d’une mémoire tampon ou la **valeur null**.

Si le membre de pointeur contient l’adresse d’une mémoire tampon, le membre de longueur de chaîne doit contenir la taille de cette mémoire tampon. [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) retourne les informations de composant sous la forme d’une chaîne dans la mémoire tampon et stocke la longueur de chaîne dans le membre de longueur de chaîne.

Si le membre du pointeur est **null**, le membre de longueur de chaîne peut être défini sur n’importe quelle valeur différente de zéro. [**InternetCrackUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcrackurla) stocke l’adresse du premier caractère de la chaîne d’URL qui contient les informations sur le composant et définit la longueur de chaîne sur le nombre de caractères dans la partie restante de la chaîne d’URL qui se rapporte au composant.

Tous les membres de pointeur ayant la valeur **null** avec un membre de longueur différente de zéro pointent vers le point de départ approprié dans la chaîne d’URL. La longueur stockée dans le membre de longueur doit être utilisée pour déterminer la fin des informations du composant individuel.

Pour terminer l’initialisation de la structure des [**\_ composants URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , le membre **dwStructSize** doit être défini sur la taille de la structure des [**\_ composants URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) , en octets.

L’exemple suivant retourne les composants de l’URL dans la zone d’édition, IDC \_ PreOpen1, et retourne les composants à la zone de liste, IDC \_ PreOpenList. Pour afficher uniquement les informations relatives à un composant individuel, cette fonction copie le caractère immédiatement après les informations du composant dans la chaîne et le remplace temporairement par une **valeur null**.


```C++
#include <windows.h>
#include <tchar.h>
#include <strsafe.h>
#include <wininet.h>
#include <stdlib.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  CRACKER_BUFFER_SIZE           MAX_PATH

// For sample source code implementing the InternetErrorOut( ) 
// function referenced below, see the "Handling Errors" topic  
// under "Using WinInet"
extern BOOL WINAPI InternetErrorOut( HWND hWnd, DWORD dwError,
                                     LPCTSTR szFailingFunctionName );

// Forward declaration of listUrlPart helper functions:
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength );
BOOL listURLpart( HWND hDlg, int nListBoxID, 
                  LPTSTR szPartName, int partValue );

// Static list describing the URL Scheme types 
// enumerated in INTERNET_SCHEME:
TCHAR* schemeType[] =
{
  TEXT( "[Partial URL]" ),                //  0
  TEXT( "[Unknown scheme]" ),             //  1
  TEXT( "[Default scheme]" ),             //  2
  TEXT( "FTP" ),                          //  3
  TEXT( "Gopher" ),                       //  4
  TEXT( "HTTP" ),                         //  5
  TEXT( "HTTPS" ),                        //  6
  TEXT( "File" ),                         //  7
  TEXT( "News" ),                         //  8
  TEXT( "MailTo" ),                       //  9
  TEXT( "Socks" ),                        // 10
  TEXT( "JavaScript" ),                   // 11
  TEXT( "VBScript" )                      // 12
};
#define  CRACKER_SCHEME_TYPE_ARRAY_SIZE      13

BOOL WINAPI Cracker( HWND hDlg, int nURLtextBoxId, int nListBoxId )
{
   int i, j;
   TCHAR* failedFunctionName;
   TCHAR URL_buffer[CRACKER_BUFFER_SIZE];

   URL_COMPONENTS URLparts;

   URLparts.dwStructSize = sizeof( URLparts );

   // The following elements determine which components are displayed
   URLparts.dwSchemeLength    = 1;
   URLparts.dwHostNameLength  = 1;
   URLparts.dwUserNameLength  = 1;
   URLparts.dwPasswordLength  = 1;
   URLparts.dwUrlPathLength   = 1;
   URLparts.dwExtraInfoLength = 1;

   URLparts.lpszScheme     = NULL;
   URLparts.lpszHostName   = NULL;
   URLparts.lpszUserName   = NULL;
   URLparts.lpszPassword   = NULL;
   URLparts.lpszUrlPath    = NULL;
   URLparts.lpszExtraInfo  = NULL;

   SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
   if( !GetDlgItemText( hDlg, nURLtextBoxId, 
                        URL_buffer, CRACKER_BUFFER_SIZE ) )
   {
       failedFunctionName = TEXT( "GetDlgItemText" );
       goto CrackerError_01;
   }

   if( FAILED( StringCchLength( URL_buffer, CRACKER_BUFFER_SIZE, 
                                (size_t*) &i ) ) )
   {
       failedFunctionName = TEXT( "StringCchLength" );
       goto CrackerError_01;
   }

   if( !InternetCrackUrl( URL_buffer, (DWORD)_tcslen( URL_buffer ), 0, 
                          &URLparts ) )
   {
       failedFunctionName = TEXT( "InternetCrackUrl" );
       goto CrackerError_01;
   }

   failedFunctionName = TEXT( "listURLpart" );

   i = URLparts.nScheme + 2;
   if( ( i >= 0 ) && ( i < CRACKER_SCHEME_TYPE_ARRAY_SIZE ) )
   {
       StringCchLength( schemeType[i], 
                        CRACKER_BUFFER_SIZE, 
                        (size_t*) &j );
       if( !listURLpart( hDlg, nListBoxId, 
                         TEXT("Scheme type"), 
                         schemeType[i], j ))
           goto CrackerError_01;
   }

   if( !listURLpart( hDlg, nListBoxId, TEXT( "Scheme text" ), 
                     URLparts.lpszScheme, 
                     URLparts.dwSchemeLength ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Host name" ), 
                     URLparts.lpszHostName, 
                     URLparts.dwHostNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Port number" ), 
                     (int) URLparts.nPort ) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "User name" ), 
                     URLparts.lpszUserName, 
                     URLparts.dwUserNameLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Password" ), 
                     URLparts.lpszPassword, 
                     URLparts.dwPasswordLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Path" ), 
                     URLparts.lpszUrlPath, 
                     URLparts.dwUrlPathLength) ||
       !listURLpart( hDlg, nListBoxId, TEXT( "Extra information"), 
                     URLparts.lpszExtraInfo, 
                     URLparts.dwExtraInfoLength))
           goto CrackerError_01;

   return( TRUE );

CrackerError_01:
// For sample source code of the InternetErrorOut( ) function 
// referenced below, see the "Handling Errors" 
// topic under "Using WinInet"
   InternetErrorOut( hDlg, GetLastError( ), failedFunctionName );
   return FALSE;
}

// listURLpart( ) helper function for string parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, LPTSTR part, DWORD partLength )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];
  LPTSTR nextStart;
  size_t nextSize;

  if( partLength == 0 )  // Just skip empty ones
    return( TRUE );

  if( FAILED( StringCchCopyEx( outputBuffer, 
                              (size_t) CRACKER_BUFFER_SIZE,
                               szPartName, &nextStart, 
                               &nextSize, 0 ) ) ||
      FAILED( StringCchCopyEx( nextStart, nextSize, TEXT( ": " ), 
                               &nextStart, &nextSize, 0 ) ) ||
      FAILED( StringCchCopyNEx( nextStart, nextSize, part, 
                                (size_t) partLength,
                                &nextStart, &nextSize, 0 ) ) )
    return( FALSE );

  *nextStart = 0;
  if( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                          (LPARAM)outputBuffer ) < 0 )
    return( FALSE );
  return( TRUE );
}

// listURLpart( ) helper function for numeric parts
BOOL listURLpart( HWND hDlg, int nListBoxId, 
                  LPTSTR szPartName, int partValue )
{
  TCHAR outputBuffer[CRACKER_BUFFER_SIZE];

  if( FAILED( StringCchPrintf( outputBuffer, 
                               (size_t) CRACKER_BUFFER_SIZE,
                               TEXT( "%s: %d" ), szPartName, 
                               partValue ) ) ||
      ( SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 0, 
                            (LPARAM)outputBuffer ) < 0 ) )
    return( FALSE );
  return( TRUE );
}
```



## <a name="creating-urls"></a>Création d’URL

La fonction [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) utilise les informations de la structure de [**\_ composants URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) pour créer un Uniform Resource Locator.

Les composants qui composent la structure des [**\_ composants d’URL**](/windows/desktop/api/Wininet/ns-wininet-url_componentsa) sont le schéma, le nom d’hôte, le numéro de port, le nom d’utilisateur, le mot de passe, le chemin d’URL et des informations supplémentaires (tels que les paramètres de recherche). Chaque composant, à l’exception du numéro de port, a un membre de chaîne qui contient les informations et un membre qui contient la longueur du membre de chaîne.

Pour chaque composant requis, le membre du pointeur doit contenir l’adresse de la mémoire tampon contenant les informations. Le membre de longueur doit avoir la valeur zéro si le membre pointeur contient l’adresse d’une chaîne se terminant par zéro ; le membre de longueur doit être défini sur la longueur de chaîne si le membre pointeur contient l’adresse d’une chaîne qui ne se termine pas par zéro. Le membre pointeur de tous les composants qui ne sont pas obligatoires doit avoir la **valeur null**.

## <a name="accessing-urls-directly"></a>Accès direct aux URL

Les ressources FTP et HTTP sur Internet sont accessibles directement à l’aide des fonctions [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)et [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) . [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) ouvre une connexion à la ressource à l’URL transmise à la fonction. Lorsque cette connexion est établie, il existe deux étapes possibles. Tout d’abord, si la ressource est un fichier, [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) peut la télécharger. Deuxièmement, si la ressource est un répertoire, [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) peut énumérer les fichiers dans le répertoire (sauf en cas d’utilisation de proxys CERN). Pour plus d’informations sur [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), consultez [lecture de fichiers](common-functions.md). Pour plus d’informations sur [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), consultez [recherche du fichier suivant](common-functions.md).

Pour les applications qui doivent fonctionner via un proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) peut être utilisé pour accéder aux répertoires et aux fichiers FTP. Les demandes FTP sont empaquetées pour apparaître comme une requête HTTP, que le proxy CERN accepterait.

[**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilise le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) créé par la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) et l’URL de la ressource. L’URL doit inclure le schéma (http :, FTP :, fichier : \[ pour un fichier local \] ou https : \[ pour Secure Protocol Secure \] ) et l’emplacement réseau (tel que `www.microsoft.com` ). L’URL peut également inclure un chemin d’accès (par exemple,/ISAPI/gomscom.asp ? TARGET =/Windows/Feature/) et nom de la ressource (par exemple, default.htm). Pour les requêtes HTTP ou HTTPs, des en-têtes supplémentaires peuvent être inclus.

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)et [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (URL http ou HTTPS uniquement) peuvent utiliser le descripteur créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pour télécharger la ressource.

Le diagramme suivant illustre les descripteurs à utiliser avec chaque fonction.

![Handles à utiliser avec les fonctions](images/ax-wnt02.png)

Le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) racine créé par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) est utilisé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla). Le descripteur **HINTERNET** créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) peut être utilisé par [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) (non illustré ici) et [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) (URL http ou HTTPS uniquement).

Pour plus d’informations, consultez [**Handles HINTERNET**](appendix-a-hinternet-handles.md).

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 