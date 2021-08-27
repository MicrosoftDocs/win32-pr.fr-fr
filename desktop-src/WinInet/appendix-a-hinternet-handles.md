---
title: Handles HINTERNET
description: Cette section contient des informations sur les handles utilisés par les fonctions WinINet et la hiérarchie dans laquelle elles fonctionnent.
ms.assetid: 8a9788ed-eb25-42cb-b912-8dffa3df1850
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477558887ac484ec0c3645d568bc3d91d29926af887ebadc51cf7e9523da787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051931"
---
# <a name="hinternet-handles"></a>Handles HINTERNET

Cette section contient des informations sur les handles utilisés par les fonctions WinINet et la hiérarchie dans laquelle elles fonctionnent.

-   [À propos des handles HINTERNET](#about-hinternet-handles)
-   [Hiérarchie des handles](#handle-hierarchy)
-   [Hiérarchie FTP](#ftp-hierarchy)
-   [Hiérarchie HTTP](#http-hierarchy)

## <a name="about-hinternet-handles"></a>À propos des handles HINTERNET

Les descripteurs créés et utilisés par les fonctions WinINet sont de type **HINTERNET**. Les fonctions WinINet retournent des handles **HINTERNET** qui ne sont pas interchangeables avec d’autres types de handles. Par conséquent, elles ne peuvent pas être utilisées avec des fonctions telles que [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). De même, les autres types de handle ne peuvent pas être utilisés avec les fonctions WinINet. Par exemple, un handle retourné par [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ne peut pas être passé à [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).

La fonction [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) ferme les handles de type **HINTERNET**. Notez que les valeurs de handle sont recyclées rapidement ; par conséquent, si un handle est fermé et qu’un nouveau descripteur est généré immédiatement, il y a de bonnes chances que le nouveau handle ait la même valeur que celle qui vient d’être fermée.

## <a name="handle-hierarchy"></a>Hiérarchie des handles

Les handles **HINTERNET** sont conservés dans une hiérarchie d’arborescence. Le handle retourné par la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) est le nœud racine. Les handles retournés par la fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) occupent le niveau suivant. Les handles retournés par les fonctions [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)et [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) sont les nœuds terminaux.

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Les handles retournés par, [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)et [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) sont également des nœuds terminaux.

Le diagramme suivant illustre la hiérarchie des handles **HINTERNET** . Chaque zone du diagramme représente une fonction qui retourne un handle **HINTERNET** .

![fonctions qui créent des handles](images/ax-wnt01.png)

Au niveau supérieur se trouve la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , qui crée le handle racine. Le niveau suivant contient les fonctions [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) et [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) . Les fonctions qui utilisent le handle retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) constituent le dernier niveau.

Le diagramme suivant montre les fonctions qui dépendent du handle créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla). Les zones grisées représentent des fonctions qui retournent des handles **HINTERNET** , tandis que les zones simples représentent des fonctions qui utilisent le descripteur **HINTERNET** créé par la fonction associée.

![fonctions qui utilisent le handle InternetOpenUrl](images/ax-wnt02.png)

Les fonctions [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)et [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer) utilisent le descripteur **HINTERNET** créé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

## <a name="ftp-hierarchy"></a>Hiérarchie FTP

Le diagramme suivant montre les fonctions FTP qui dépendent du descripteur de session FTP retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta). Les zones grisées représentent des fonctions qui retournent des handles **HINTERNET** , tandis que les zones simples représentent des fonctions qui utilisent le descripteur **HINTERNET** créé par la fonction sur laquelle ils dépendent.

![fonctions qui utilisent le descripteur de session FTP](images/ax-wnt06.png)

Les fonctions [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya), [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea), [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya), [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)et [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) utilisent toutes le handle **HINTERNET** créé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).

Le diagramme suivant montre les deux fonctions FTP qui retournent des handles et les fonctions qui en dépendent. Les zones grisées représentent des fonctions qui retournent des handles **HINTERNET** , tandis que les zones simples représentent des fonctions qui utilisent le descripteur **HINTERNET** créé par la fonction sur laquelle ils dépendent.

![fonctions qui utilisent le descripteur de ftpopen et ftpfindfirstfile](images/ax-wnt03.png)

La fonction [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) est dépendante du descripteur créé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), tandis que [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) et [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) utilisent le descripteur créé par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).

## <a name="http-hierarchy"></a>Hiérarchie HTTP

Le diagramme suivant montre les relations des fonctions utilisées pour le protocole HTTP. Les zones grisées représentent des fonctions qui retournent des handles **HINTERNET** , tandis que les zones simples représentent des fonctions qui utilisent le descripteur **HINTERNET** créé par la fonction sur laquelle ils dépendent.

![fonctions qui utilisent le handle à partir de httpopenrequest](images/ax-wnt05.png)

Les fonctions [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa), [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa), [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa)et [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) dépendent du handle créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).

Le diagramme suivant montre les fonctions qui utilisent le handle **HINTERNET** créé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) une fois qu’il a été envoyé par [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Les zones grisées représentent des fonctions qui retournent des handles **HINTERNET** , tandis que les zones simples représentent des fonctions qui utilisent le descripteur **HINTERNET** créé par la fonction sur laquelle ils dépendent.

![fonctions qui utilisent le handle après HTTPSendRequest](images/ax-wnt07.png)

Une fois que [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) a utilisé le handle retourné par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), il peut être utilisé par [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable), [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)et [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer).

![fonctions qui utilisent le handle après HttpSendRequestEx](images/ax-wnt08.png)

Une fois que [**HttpSendRequestEx**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequestexa) a utilisé le handle retourné par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), le handle peut être utilisé par [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta), [**InternetReadFileEx**](/windows/desktop/api/Wininet/nf-wininet-internetreadfileexa)et [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile). Une fois [**HttpEndRequest**](/windows/desktop/api/Wininet/nf-wininet-httpendrequesta) appelé, le handle peut être utilisé par [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)et [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable).

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 