---
title: Sessions FTP
description: WinINet permet aux applications de parcourir et de manipuler des répertoires et des fichiers sur un serveur FTP. Étant donné que les proxys CERN ne prennent pas en charge FTP, les applications qui utilisent un proxy CERN doivent utiliser la fonction InternetOpenUrl.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031535"
---
# <a name="ftp-sessions"></a>Sessions FTP

WinINet permet aux applications de parcourir et de manipuler des répertoires et des fichiers sur un serveur FTP. Étant donné que les proxys CERN ne prennent pas en charge FTP, les applications qui utilisent un proxy CERN doivent utiliser la fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . Pour plus d’informations sur l’utilisation de [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), consultez [accès direct aux URL](handling-uniform-resource-locators.md).

Pour démarrer une session FTP, utilisez [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) pour créer le descripteur de session.

WinINet vous permet d’effectuer les actions suivantes sur un serveur FTP :

-   Naviguer entre les répertoires.
-   Énumérer, créer, supprimer et renommer des répertoires.
-   Renommez, chargez, téléchargez et supprimez des fichiers.

La navigation est assurée par les fonctions [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) et [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) . Ces fonctions utilisent le descripteur de session créé par un appel précédent à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) pour déterminer le répertoire dans lequel l’application se trouve actuellement, ou pour basculer vers un autre sous-répertoire.

L’énumération des répertoires s’effectue à l’aide des fonctions [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) et [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) . [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) utilise le handle de session créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) pour rechercher le premier fichier qui correspond aux critères de recherche donnés et retourne un handle pour continuer l’énumération de répertoires. [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) utilise le handle retourné par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) pour retourner le fichier suivant qui correspond aux critères de recherche d’origine. L’application doit continuer à appeler [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) jusqu’à ce qu’il n’y ait plus de fichiers restants dans le répertoire.

Utilisez la fonction [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) pour créer des répertoires. Cette fonction utilise le handle de session créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) et crée le répertoire spécifié par la chaîne transmise à la fonction. La chaîne peut contenir un nom de répertoire relatif au répertoire actif, ou un chemin d’accès complet au répertoire.

Pour renommer des fichiers ou des répertoires, l’application peut appeler [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea). Cette fonction remplace le nom d’origine par le nouveau nom passé à la fonction. Le nom du fichier ou du répertoire peut être relatif au répertoire actif ou à un nom complet.

Pour télécharger ou placer des fichiers sur un serveur FTP, l’application peut utiliser [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) ou [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (avec [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)). [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) peut être utilisé si le fichier existe déjà localement, tandis que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) et [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) peuvent être utilisés si les données doivent être écrites dans un fichier sur le serveur FTP.

Pour télécharger ou récupérer des fichiers, l’application peut utiliser [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) ou [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (avec [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)). [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) est utilisé pour récupérer un fichier à partir d’un serveur FTP et le stocker localement, tandis que [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) et [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) peuvent être utilisés pour contrôler l’emplacement des informations téléchargées (par exemple, l’application peut afficher les informations dans une zone d’édition).

Supprimer des fichiers sur un serveur FTP à l’aide de la fonction [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) . Cette fonction supprime un nom de fichier relatif au répertoire actif ou à un nom de fichier complet du serveur FTP. [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requiert un handle de session retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).

## <a name="ftp-function-handles"></a>Handles de fonction FTP

Pour fonctionner correctement, les fonctions FTP nécessitent certains types de descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) . Ces handles doivent être créés dans un ordre spécifique, en commençant par le handle racine créé par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) peut ensuite créer un descripteur de session FTP.

Le diagramme suivant montre les fonctions qui dépendent du descripteur de session FTP retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Les zones grisées représentent des fonctions qui retournent des handles [**HINTERNET**](appendix-a-hinternet-handles.md) , tandis que les zones simples représentent des fonctions qui utilisent le descripteur HINTERNET créé par la fonction sur laquelle ils dépendent.

![fonctions FTP dépendant du descripteur de session FTP retourné par internetconnect](images/ax-wnt06.png)

Le diagramme suivant montre les deux fonctions qui retournent des handles [HINTERNET](appendix-a-hinternet-handles.md) et les fonctions qui en dépendent. Les zones grisées représentent des fonctions qui retournent des handles **HINTERNET** , tandis que les zones simples représentent des fonctions qui utilisent le descripteur **HINTERNET** créé par la fonction sur laquelle ils dépendent.

![fonctions FTP qui retournent des handles HINTERNET](images/ax-wnt03.png)

Pour plus d’informations, consultez [Handles HINTERNET](appendix-a-hinternet-handles.md).

## <a name="using-the-wininet-functions-for-ftp-sessions"></a>Utilisation des fonctions WinINet pour les sessions FTP

Les fonctions suivantes sont utilisées pendant les sessions FTP. Ces fonctions ne sont pas reconnues par les proxys CERN. Les applications qui doivent fonctionner par le biais de proxys CERN doivent utiliser [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) et accéder directement aux ressources. Pour plus d’informations sur l’accès direct aux ressources, consultez [accès direct aux URL](handling-uniform-resource-locators.md).



| Fonction                                                 | Description                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | Crée un répertoire sur le serveur. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                  |
| [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | Supprime un fichier du serveur. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                         |
| [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | Démarre l’énumération des fichiers ou la recherche de fichiers dans le répertoire actif. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).        |
| [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | Retourne le répertoire actuel du client sur le serveur. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                   |
| [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | Récupère un fichier du serveur. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                       |
| [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | Initie l’accès à un fichier sur le serveur pour la lecture ou l’écriture. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). |
| [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | Écrit un fichier sur le serveur. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                            |
| [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | Supprime un répertoire sur le serveur. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                      |
| [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | Renomme un fichier sur le serveur. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                                           |
| [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | Modifie le répertoire actuel du client sur le serveur. Cette fonction requiert un handle créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).                   |
| [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | Écrit des données dans un fichier ouvert sur le serveur. Cette fonction requiert un handle créé par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).                                      |



 

### <a name="starting-an-ftp-session"></a>Démarrage d’une session FTP

L’application établit une session FTP en appelant [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) sur un handle créé par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). [**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) a besoin du nom du serveur, du numéro de port, du nom d’utilisateur, du mot de passe et du type de service (qui doit être défini sur Internet \_ service \_ FTP). Pour la sémantique FTP passive, l’application doit également définir l’indicateur [ \_ \_ passive de l’indicateur Internet](api-flags.md) .

Les \_ valeurs de port FTP par défaut Internet \_ \_ et \_ \_ de numéro de port Internet non valides \_ peuvent être utilisées pour le numéro de port. Le \_ port FTP par défaut Internet \_ \_ utilise le port FTP par défaut, mais le type de service doit toujours être défini. \_ \_ Le numéro de port Internet non valide \_ utilise la valeur par défaut pour le type de service indiqué.

Les valeurs du nom d’utilisateur et du mot de passe peuvent être définies sur **null**. Si les deux valeurs sont définies sur **null**, [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilise « Anonymous » pour le nom d’utilisateur et l’adresse de messagerie de l’utilisateur pour le mot de passe. Si seul le mot de passe est défini sur **null**, le nom d’utilisateur passé à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) est utilisé pour le nom d’utilisateur et une chaîne vide est utilisée pour le mot de passe. Si aucune valeur n’est **null**, le nom d’utilisateur et le mot de passe fournis à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) sont utilisés.

### <a name="enumerating-directories"></a>Énumération des répertoires

L’énumération d’un répertoire sur un serveur FTP requiert la création d’un descripteur par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Ce descripteur est une branche du descripteur de session créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) localise le premier fichier ou répertoire sur le serveur et le retourne dans une structure de [**\_ \_ données de recherche Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) . Utilisez [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) jusqu’à ce qu’il retourne l' [**erreur \_ aucun \_ \_ fichier supplémentaire**](wininet-errors.md). Cette méthode recherche tous les fichiers et répertoires suivants sur le serveur. Pour plus d’informations sur [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), consultez [recherche du fichier suivant](common-functions.md).

Pour déterminer si le fichier récupéré par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) ou [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) est un répertoire, vérifiez le membre **dwFileAttributes** de la structure de [**\_ \_ données de recherche Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) pour déterminer s’il est égal au répertoire des attributs de fichier \_ \_ .

Si l’application apporte des modifications sur le serveur FTP ou si le serveur FTP change fréquemment, les indicateurs de rechargement de l' [ \_ indicateur Internet \_ sans \_ cache \_](api-flags.md) et de l' [indicateur de \_ \_ rechargement Internet](api-flags.md) doivent être définis dans [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Ces indicateurs garantissent que les informations de répertoire récupérées à partir du serveur FTP sont à jour.

Une fois que l’application a terminé l’énumération de répertoires, l’application doit effectuer un appel à [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) sur le handle créé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea). Tant que ce handle n’est pas fermé, l’application ne peut pas appeler à nouveau [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) sur le handle de session créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Si un appel à [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) est effectué sur le même handle de session avant la fermeture de l’appel précédent à la même fonction, la fonction échoue et retourne l' [erreur \_ \_ transfert FTP \_ en \_ cours](wininet-errors.md).

L’exemple suivant énumère le contenu d’un répertoire FTP dans un contrôle de zone de liste. Le paramètre *hConnection* est un handle retourné par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après avoir établi une session FTP. Vous trouverez un exemple de code source pour la fonction InternetErrorOut référencée dans cet exemple dans la rubrique [gestion des erreurs](appendix-c-handling-errors.md).


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a>Navigation dans les répertoires

Les fonctions [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) et [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) gèrent la navigation dans les répertoires.

[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) retourne le répertoire actif de l’application sur le serveur FTP. Le chemin d’accès au répertoire à partir du répertoire racine sur le serveur FTP est inclus.

[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) modifie le répertoire de travail sur le serveur. Les informations de répertoire transmises à [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) peuvent être un nom de chemin d’accès partiel ou complet relatif au répertoire actif. Par exemple, si l’application se trouve actuellement dans le répertoire « public/info » et que le chemin d’accès est « FTP/example », [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) remplace le répertoire actif par « public/info/FTP/example ».

L’exemple suivant utilise le handle de session FTP hConnection, qui est retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Le nouveau nom de répertoire est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est transmis dans le paramètre *nDirNameId* . Avant que le répertoire ne soit modifié, la fonction récupère le répertoire actif et le stocke dans la même zone d’édition. Le code de la fonction DisplayFtpDir appelée à la fin est indiqué ci-dessus.


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a>Manipulation de répertoires sur un serveur FTP

WinINet offre la possibilité de créer et de supprimer des répertoires sur un serveur FTP auquel l’application dispose des privilèges nécessaires. Si l’application doit ouvrir une session sur un serveur avec un nom d’utilisateur et un mot de passe spécifiques, les valeurs peuvent être utilisées dans [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) lors de la création du descripteur de session FTP.

La fonction [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) prend un handle de session FTP valide et une chaîne se terminant par un caractère **null** qui contient un chemin d’accès qualifié complet ou un nom relatif au répertoire actif et crée un répertoire sur le serveur FTP.

L’exemple suivant montre deux appels distincts à [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya). Dans les deux exemples, hFtpSession est le descripteur de session créé par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) et le répertoire racine est le répertoire actif.

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

La fonction [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) prend un handle de session et une chaîne se terminant par un caractère **null** qui contient un chemin d’accès qualifié complet ou un nom relatif au répertoire actif et supprime ce répertoire du serveur FTP.

L’exemple suivant montre deux exemples d’appels à [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya). Dans les deux appels, hFtpSession est le descripteur de session créé par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) et le répertoire racine est le répertoire actif. Il existe un répertoire nommé « test » dans le répertoire racine et un répertoire appelé « example » dans le répertoire « test ».

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



L’exemple suivant crée un répertoire sur le serveur FTP. Le nouveau nom de répertoire est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est transmis dans le paramètre *nDirNameId* . Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP. Le code source de la fonction DisplayFtpDir appelée à la fin est indiqué ci-dessus.


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



L’exemple suivant supprime un répertoire du serveur FTP. Le nom du répertoire à supprimer est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est passé dans le paramètre *nDirNameId* . Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP. Le code source de la fonction DisplayFtpDir appelée à la fin est indiqué ci-dessus.


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a>Obtention de fichiers sur un serveur FTP

Il existe trois méthodes pour récupérer des fichiers à partir d’un serveur FTP :

-   Utilisez [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) et [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Utilisez [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) et [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).
-   Utilisez [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).

Pour plus d’informations sur l’utilisation de la fonction [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) , consultez [lecture de fichiers](common-functions.md).

Si l’URL du fichier est disponible, l’application peut appeler [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pour se connecter à cette URL, puis utiliser [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) pour contrôler le téléchargement du fichier. Cela permet à l’application d’exercer un contrôle plus strict sur le téléchargement et est idéal pour les situations où aucune autre opération ne doit être effectuée sur le serveur FTP. Pour plus d’informations sur l’accès direct aux ressources, consultez [accès direct aux URL](handling-uniform-resource-locators.md).

Si l’application a établi un descripteur de session FTP sur le serveur avec [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), l’application peut appeler [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) avec le nom de fichier existant et avec un nouveau nom pour le fichier stocké localement. L’application peut ensuite utiliser [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) pour télécharger le fichier. Cela permet à l’application d’exercer un contrôle plus strict sur le téléchargement et de conserver la connexion au serveur FTP, si bien que davantage de commandes peuvent être exécutées.

Si l’application n’a pas besoin d’un contrôle strict sur le téléchargement, l’application peut utiliser [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) avec le descripteur de session FTP, le nom de fichier distant et le nom de fichier local pour récupérer le fichier. [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) effectue toutes les tâches de comptabilité et de surcharge associées à la lecture d’un fichier à partir d’un serveur FTP et à son stockage local.

L’exemple suivant récupère un fichier à partir d’un serveur FTP et l’enregistre localement. Le nom du fichier sur le serveur FTP est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est transmis dans le paramètre *nFtpFileNameId* , et le nom local sous lequel le fichier est enregistré est extrait de la zone d’édition dont l’IDC est transmis dans le paramètre *nLocalFileNameId* . Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP.


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a>Placement de fichiers sur un serveur FTP

Il existe deux méthodes pour placer un fichier sur un serveur FTP :

-   Utilisez [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) avec [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).
-   Utilisez [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).

Une application qui doit envoyer des données à un serveur FTP, mais qui n’a pas de fichier local contenant toutes les données, doit utiliser [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) pour créer et ouvrir un fichier sur le serveur FTP. L’application peut ensuite utiliser [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) pour télécharger les informations dans le fichier.

Si le fichier existe déjà localement, l’application peut utiliser [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) pour charger le fichier sur le serveur FTP. [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) effectue toute la surcharge liée au téléchargement d’un fichier local sur un serveur FTP distant.

L’exemple suivant copie un fichier local sur le serveur FTP. Le nom local du fichier est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est transmis dans le paramètre *nLocalFileNameId* , et le nom sous lequel le fichier est enregistré sur le serveur FTP est extrait de la zone d’édition dont l’IDC est transmis dans le paramètre *nFtpFileNameId* . Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP.


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a>Suppression de fichiers d’un serveur FTP

Pour supprimer un fichier d’un serveur FTP, utilisez la fonction [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) . L’application appelante doit disposer des privilèges nécessaires pour supprimer un fichier du serveur FTP.

L’exemple suivant supprime un fichier du serveur FTP. Le nom du fichier à supprimer est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC reçoit le paramètre *nFtpFileNameId* . Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP. Étant donné que cette fonction n’actualise pas les listes de fichiers ou l’affichage des répertoires, le processus appelant doit le faire en cas de suppression réussie.


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a>Attribution d’un nouveau nom aux fichiers et répertoires sur un serveur FTP

Vous pouvez renommer les fichiers et répertoires d’un serveur FTP à l’aide de la fonction [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) . [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accepte deux chaînes se terminant par un caractère **null** qui contiennent des noms complets ou partiels par rapport au répertoire actif. La fonction modifie le nom du fichier désigné par la première chaîne en lui assignant le nom désigné par la deuxième chaîne.

L’exemple suivant renomme un fichier ou un répertoire sur le serveur FTP. Le nom actuel du fichier ou du répertoire est extrait de la zone d’édition de la boîte de dialogue parente dont l’IDC est transmis dans le paramètre *nOldFileNameId* , et le nouveau nom est extrait de la zone d’édition dont l’IDC est passé dans le paramètre *nNewFileNameId* . Le descripteur *hConnection* a été créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après l’établissement d’une session FTP. Étant donné que cette fonction n’actualise pas les listes de fichiers ou l’affichage des répertoires, le processus appelant doit le faire en cas de changement de nom.


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 