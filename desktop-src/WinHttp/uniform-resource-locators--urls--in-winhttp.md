---
description: Une URL est une représentation compacte de l’emplacement et de la méthode d’accès d’une ressource située sur Internet.
ms.assetid: 940c414d-274f-475c-a50e-7a0853c3c26b
title: URL (Uniform Resource Locators) dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486ed3b17e2cf205f6ac815e87617a84e0ccc4cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034316"
---
# <a name="uniform-resource-locators-urls-in-winhttp"></a>URL (Uniform Resource Locators) dans WinHTTP

Une URL est une représentation compacte de l’emplacement et de la méthode d’accès d’une ressource située sur Internet. Chaque URL se compose d’un schéma (HTTP, HTTPs, FTP ou Gopher) et d’une chaîne spécifique au schéma. Cette chaîne peut également inclure une combinaison d’un chemin d’accès de répertoire, d’une chaîne de recherche ou d’un nom de ressource. Les fonctions des services HTTP Microsoft Windows (WinHTTP) offrent la possibilité de créer, combiner, décomposer et rendre canoniques les URL. Pour plus d’informations, consultez [rfc 1738](https://www.ietf.org/rfc/rfc1738.txt), [Uniform Resource Locators](https://www.ietf.org/rfc/rfc1738.txt) et [RFC 2396](https://www.ietf.org/rfc/rfc2396.txt), [Uniform Resource Identifiers (Uri) : Generic Syntax](https://www.ietf.org/rfc/rfc1738.txt).

## <a name="what-is-a-canonicalized-url"></a>Qu’est-ce qu’une URL canonique ?

La syntaxe et la sémantique des URL spécifiées laissent de l’espace pour la variation et l’erreur. La canonicalisation est le processus qui consiste à normaliser une URL réelle dans un format correct, standard, « canonique ».

Cela implique de coder certains caractères comme des « séquences d’échappement ». Les caractères alphanumériques US-ASCII n’ont pas besoin d’être encodés (les chiffres 0-9, les lettres majuscules A-Z et les lettres minuscules de a à z). La plupart des autres caractères doivent être placés dans une séquence d’échappement, y compris les caractères de contrôle, l’espace, le signe de pourcentage, les « caractères non sécurisés » (<, >, ", \# , {,}, \| , \\ , ^, ~, \[ , \] et') et tous les caractères avec un point de code supérieur à 127.

## <a name="using-the-winhttp-functions-to-handle-urls"></a>Utilisation des fonctions WinHTTP pour gérer les URL

WinHTTP fournit deux fonctions pour la gestion des URL. [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) sépare une URL en ses composants et [**WINHTTPCREATEURL**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) crée une URL à partir de composants.

### <a name="separating-urls"></a>Séparation des URL

La fonction [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) sépare une URL en ses composants et retourne les composants indiqués par la structure [**de \_ composants URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) qui est transmise à la fonction.

Les composants qui composent la structure des [**\_ composants d’URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) sont le numéro de schéma, le nom d’hôte, le numéro de port, le nom d’utilisateur, le mot de passe, le chemin d’URL et des informations supplémentaires, telles que les paramètres de recherche. Chaque composant, sauf le schéma et le numéro de port, a un membre de chaîne qui contient les informations et un membre qui contient la longueur du membre de chaîne. Le schéma et les numéros de port ont uniquement un membre qui stocke la valeur correspondante ; le schéma et le numéro de port sont tous deux renvoyés sur tous les appels réussis à [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl).

Pour récupérer la valeur d’un composant particulier dans la structure de [**\_ composants d’URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) , le membre qui stocke la longueur de chaîne de ce composant doit être défini sur une valeur différente de zéro. Le membre de chaîne peut être un pointeur vers une mémoire tampon ou **null**.

Si le membre de pointeur contient un pointeur vers une mémoire tampon, le membre de longueur de chaîne doit contenir la taille de cette mémoire tampon. La fonction [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) retourne les informations de composant sous la forme d’une chaîne dans la mémoire tampon et stocke la longueur de chaîne dans le membre de longueur de chaîne.

Si le membre de pointeur a la valeur **null**, le membre de longueur de chaîne peut être défini sur n’importe quelle valeur différente de zéro. La fonction [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) stocke un pointeur vers le premier caractère de la chaîne d’URL qui contient les informations sur le composant et définit la longueur de chaîne sur le nombre de caractères dans la partie restante de la chaîne d’URL qui se rapporte au composant.

Tous les membres de pointeur ayant la valeur **null** avec un membre de longueur différente de zéro pointent vers le point de départ approprié dans la chaîne d’URL. La longueur stockée dans le membre de longueur doit être utilisée pour déterminer la fin des informations du composant individuel.

Pour terminer l’initialisation de la structure des [**\_ composants d’URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) correctement, le membre **dwStructSize** doit être défini sur la taille de la structure des [**\_ composants d’URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) .

### <a name="creating-urls"></a>Création d’URL

La fonction [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) utilise les informations de la structure de [**\_ composants URL**](/windows/win32/api/winhttp/ns-winhttp-url_components) décrite précédemment pour créer une URL.

Pour chaque composant requis, le membre pointeur doit contenir un pointeur vers la mémoire tampon qui contient les informations. Le membre de longueur doit avoir la valeur zéro si le membre pointeur contient un pointeur vers une chaîne se terminant par zéro ; le membre de longueur doit être défini sur la longueur de chaîne si le membre pointeur contient un pointeur vers une chaîne qui n’est pas terminée par zéro. Le membre pointeur de tous les composants qui ne sont pas requis doit avoir la valeur **null**.

### <a name="sample-code"></a>Exemple de code

L’exemple de code suivant montre comment utiliser [**WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) et [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) pour désassembler une URL existante, modifier l’un de ses composants et le réassembler en une nouvelle URL.


```C++
  URL_COMPONENTS urlComp;
  LPCWSTR pwszUrl1 = 
    L"https://search.msn.com/results.asp?RS=CHECKED&FORM=MSNH&v=1&q=wininet";
  DWORD dwUrlLen = 0;

  // Initialize the URL_COMPONENTS structure.
  ZeroMemory(&urlComp, sizeof(urlComp));
  urlComp.dwStructSize = sizeof(urlComp);

  // Set required component lengths to non-zero so that they are cracked.
  urlComp.dwSchemeLength    = (DWORD)-1;
  urlComp.dwHostNameLength  = (DWORD)-1;
  urlComp.dwUrlPathLength   = (DWORD)-1;
  urlComp.dwExtraInfoLength = (DWORD)-1;

  // Crack the URL.
  if( !WinHttpCrackUrl( pwszUrl1, (DWORD)wcslen(pwszUrl1), 0, &urlComp ) )
      printf( "Error %u in WinHttpCrackUrl.\n", GetLastError( ) );
  else
  {
    // Change the search information.  New info is the same length.
    urlComp.lpszExtraInfo = L"?RS=CHECKED&FORM=MSNH&v=1&q=winhttp";

    // Obtain the size of the new URL and allocate memory.
    WinHttpCreateUrl( &urlComp, 0, NULL, &dwUrlLen );
    LPWSTR pwszUrl2 = new WCHAR[dwUrlLen];

    // Create a new URL.
    if( !WinHttpCreateUrl( &urlComp, 0, pwszUrl2, &dwUrlLen ) )
      printf( "Error %u in WinHttpCreateUrl.\n", GetLastError( ) );
    else
    {
      // Show both URLs.
      printf( "Old URL:  %S\nNew URL:  %S\n", pwszUrl1, pwszUrl2 );
    }

    // Free allocated memory.
    delete [] pwszUrl2;
  }
```



 

 



