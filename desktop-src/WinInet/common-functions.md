---
title: fonctions courantes (Internet Windows)
description: Les différents protocoles Internet (tels que FTP et http) utilisent plusieurs des mêmes fonctions WinINet pour gérer les informations sur Internet.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7b6a68c2633175eca793f48b2180b7212905762ca0f58290436aa17ae9a728
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132892"
---
# <a name="common-functions-windows-internet"></a>fonctions courantes (Internet Windows)

Les différents protocoles Internet (tels que FTP et http) utilisent plusieurs des mêmes fonctions WinINet pour gérer les informations sur Internet. Ces fonctions courantes gèrent leurs tâches de manière cohérente, quel que soit le protocole auquel elles s’appliquent. Les applications peuvent utiliser ces fonctions pour créer des fonctions à usage général qui gèrent les tâches entre les différents protocoles (telles que la lecture de fichiers pour FTP et http).

Les fonctions courantes gèrent les tâches suivantes :

-   Téléchargement des ressources à partir d’Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)et [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).
-   Configuration des opérations asynchrones ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).
-   Affichage et modification des options ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) et [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).
-   Fermeture de tous les types de handles [**HINTERNET**](appendix-a-hinternet-handles.md) ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).
-   Placement et suppression de verrous sur les ressources ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) et [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).

## <a name="using-common-functions"></a>Utilisation des fonctions courantes

Le tableau suivant répertorie les fonctions courantes incluses dans les fonctions WinINet. Les fonctions courantes peuvent être utilisées sur différents types de descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) ou peuvent être utilisées dans différents types de sessions.



| Fonction                                                         | Description                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | Poursuit l’énumération des fichiers ou la recherche. Requiert un handle créé par la fonction [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .                                                                            |
| [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | Permet à l’utilisateur de placer un verrou sur le fichier utilisé. Cette fonction requiert un handle retourné par la fonction [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) . |
| [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | Récupère la quantité de données disponibles. Requiert un handle créé par la fonction [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .                                                                                    |
| [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | Récupère le paramètre d’une option Internet.                                                                                                                                                                                                            |
| [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | Lit les données d’URL. Requiert un handle créé par la fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .                                                                |
| [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | Définit la position de la lecture suivante dans un fichier. Requiert un handle créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (sur une URL http uniquement) ou un descripteur créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) à l’aide du verbe http obtenir.                 |
| [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | Définit une option Internet.                                                                                                                                                                                                                                |
| [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | Définit une fonction de rappel qui reçoit des informations d’État. Assigne une fonction de rappel au handle [**HINTERNET**](appendix-a-hinternet-handles.md) désigné et à tous les handles dérivés de celui-ci.                                                      |
| [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | Déverrouille un fichier qui a été verrouillé à l’aide de la fonction [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) .                                                                                                                                           |



 

La lecture des fichiers, la recherche du fichier suivant, la manipulation des options et la configuration d’opérations asynchrones sont communes aux fonctions qui prennent en charge divers protocoles et types de descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) .

### <a name="reading-files"></a>Lecture des fichiers

La fonction [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) est utilisée pour télécharger des ressources à partir d’un handle [**HINTERNET**](appendix-a-hinternet-handles.md) retourné par la fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .

[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accepte une variable de pointeur void qui contient l’adresse d’une mémoire tampon et un pointeur vers une variable qui contient la longueur de la mémoire tampon. La fonction retourne les données dans la mémoire tampon et la quantité de données téléchargées dans la mémoire tampon.

Les fonctions WinINet fournissent deux techniques pour télécharger une ressource entière :

-   Fonction [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) .
-   Valeurs de retour de [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).

[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) prend le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (après que [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) a été appelé sur le descripteur) et retourne le nombre d’octets disponibles. L’application doit allouer une mémoire tampon égale au nombre d’octets disponibles, plus 1 pour le caractère **null** de fin, et utiliser cette mémoire tampon avec [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Cette méthode ne fonctionne pas toujours, car [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) vérifie la taille de fichier indiquée dans l’en-tête, et non le fichier réel. Les informations contenues dans le fichier d’en-tête peuvent être obsolètes ou le fichier d’en-tête peut être manquant, car il n’est actuellement pas requis dans toutes les normes.

L’exemple suivant lit le contenu de la ressource accessible par le handle hResource et affiché dans la zone d’édition indiquée par intCtrlID.


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
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

    // Return.
    return TRUE;
}
```



[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) retourne une lecture de zéro octet et se termine avec succès lorsque toutes les données disponibles ont été lues. Cela permet à une application d’utiliser [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) dans une boucle pour télécharger les données et de quitter lorsqu’elle retourne zéro octet de lecture et se termine correctement.

L’exemple suivant lit la ressource à partir d’Internet et affiche la ressource dans la zone d’édition indiquée par intCtrlID. Le handle [**HINTERNET**](appendix-a-hinternet-handles.md) , HINTERNET, a été retourné [**par InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (après envoi par [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a>Recherche du fichier suivant

La fonction [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) est utilisée pour rechercher le fichier suivant dans une recherche de fichiers, à l’aide des paramètres de recherche et du handle [**HINTERNET**](appendix-a-hinternet-handles.md) de [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

Pour effectuer une recherche de fichier, continuez à appeler [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) à l’aide du handle [**HINTERNET**](appendix-a-hinternet-handles.md) retourné par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), ou [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) jusqu’à ce que la fonction échoue avec le message d’erreur étendu erreur, plus [ \_ aucun \_ \_ fichier](wininet-errors.md). Pour récupérer les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

L’exemple suivant affiche le contenu d’un répertoire FTP dans la zone de liste indiquée par lstDirectory. Le handle [**HINTERNET**](appendix-a-hinternet-handles.md) , hConnect, est un handle retourné par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) après avoir établi une session FTP.


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a>Manipulation des options

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) et [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) sont utilisées pour manipuler les options wininet.

[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accepte une variable qui indique l’option à définir, une mémoire tampon destinée à contenir la valeur de l’option et un pointeur qui contient l’adresse de la variable qui contient la longueur de la mémoire tampon.

[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accepte une variable qui indique l’option à récupérer, une mémoire tampon destinée à contenir la valeur de l’option et un pointeur qui contient l’adresse de la variable qui contient la longueur de la mémoire tampon.

### <a name="setting-up-asynchronous-operations"></a>Configuration des opérations asynchrones

Par défaut, les fonctions WinINet fonctionnent de façon synchrone. Une application peut demander une opération asynchrone en définissant l’indicateur [ \_ \_ Async Internet](api-flags.md) dans l’appel à la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) . Tous les appels futurs effectués sur des handles dérivés du handle retourné par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) sont effectués de manière asynchrone.

Le raisonnement pour les opérations asynchrones et synchrones consiste à permettre à une application monothread de maximiser son utilisation du processeur sans devoir attendre la fin de l’exécution des e/s réseau. Par conséquent, en fonction de la demande, l’opération peut s’effectuer de façon synchrone ou asynchrone. L’application doit vérifier le code de retour. Si une fonction retourne **false** ou **null**, et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne \_ des erreurs d’e/s \_ en attente, la demande a été effectuée de façon asynchrone et l’application est rappelée avec la \_ demande d’État Internet \_ \_ terminée lorsque la fonction est terminée.

Pour commencer l’opération asynchrone, l’application doit définir l’indicateur [ \_ \_ Async Internet Flag](api-flags.md) dans son appel à [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). L’application doit ensuite inscrire une fonction de rappel valide à l’aide de [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).

Une fois qu’une fonction de rappel est inscrite pour un handle, toutes les opérations sur ce handle peuvent générer des indications d’État, à condition que la valeur de contexte qui a été fournie lors de la création du handle ne soit pas égale à zéro. La spécification d’une valeur de contexte zéro force une opération à se terminer de façon synchrone, même si l' [ \_ indicateur Internet \_ Async](api-flags.md) a été spécifié dans [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).

Les indications d’État fournissent à l’application des commentaires sur la progression des opérations réseau, telles que la résolution d’un nom d’hôte, la connexion à un serveur et la réception de données. Trois indications d’État à usage spécial peuvent être effectuées pour un descripteur :

-   \_ \_ La fermeture du descripteur d’État Internet \_ est la dernière indication d’État effectuée pour un descripteur.
-   \_ \_ Le descripteur d’État Internet \_ créé indique le moment où le descripteur est initialement créé.
-   La \_ \_ demande d’État Internet \_ est terminée indique qu’une opération asynchrone est terminée.

L’application doit vérifier la structure des [**\_ \_ résultats Async Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) pour déterminer si l’opération a réussi ou échoué après avoir reçu une indication de la \_ demande d’État Internet \_ \_ terminée.

L’exemple suivant montre un exemple de fonction de rappel et un appel à [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) pour inscrire la fonction en tant que fonction de rappel.


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a>Fermeture des handles HINTERNET

Tous les descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) peuvent être fermés à l’aide de la fonction [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) . Les applications clientes doivent fermer tous les descripteurs **HINTERNET** dérivés du descripteur **HINTERNET** qu’ils essaient de fermer avant d’appeler [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) sur le descripteur.

L’exemple suivant illustre la hiérarchie des handles.


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a>Verrouillage et déverrouillage des ressources

La fonction [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) permet à une application de s’assurer que la ressource mise en cache associée au descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) qui lui est passée ne disparaît pas du cache. Si un autre téléchargement tente de valider une ressource qui a la même URL que le fichier verrouillé, le cache évite de supprimer le fichier en procédant à une suppression sécurisée. Une fois que l’application a appelé la fonction [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) , le cache reçoit l’autorisation de supprimer le fichier.

Si l' [indicateur \_ Internet \_ aucun \_ cache \_ Write](api-flags.md) ou indicateur de [ \_ \_ \_ cache](api-flags.md) de l’indicateur Internet n’a pas été défini, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) crée un fichier temporaire avec l’extension tmp, sauf si le descripteur est connecté à une ressource HTTPS. Si la fonction accède à une ressource https et qu' \_ \_ aucune écriture dans le cache n’est définie pour l’indicateur Internet \_ (ou le cache de l' \_ \_ indicateur Internet \_ \_ ), [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) échoue.

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 
