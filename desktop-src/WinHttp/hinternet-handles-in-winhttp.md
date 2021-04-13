---
description: Les services HTTP Microsoft Windows (WinHTTP) utilisent des handles pour effectuer le suivi des paramètres et des informations requis lors de l’utilisation du protocole HTTP.
ms.assetid: 0bd82860-1347-40c8-ae77-c4d865c109be
title: Descripteurs HINTERNET dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf374675ad6f2114dd48e0a3ff1db50cd0dd7f9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560987"
---
# <a name="hinternet-handles-in-winhttp"></a>Descripteurs HINTERNET dans WinHTTP

Les services HTTP Microsoft Windows (WinHTTP) utilisent des handles pour effectuer le suivi des paramètres et des informations requis lors de l’utilisation du protocole HTTP. Chaque descripteur conserve les informations pertinentes pour une session HTTP, une connexion avec un serveur HTTP ou une ressource spécifique. Cette rubrique décrit les différents types de descripteurs, les conventions d’affectation de noms pour ces handles et leur structure hiérarchique.

-   [À propos des handles HINTERNET](#about-hinternet-handles)
-   [Descripteurs de nommage](#naming-handles)
-   [Hiérarchie des handles](#handle-hierarchy)
-   [Explication de la hiérarchie des handles](#explanation-of-the-handle-hierarchy)

## <a name="about-hinternet-handles"></a>À propos des handles HINTERNET

Les handles qui sont créés et utilisés par WinHTTP sont appelés Handles **HINTERNET** . Les fonctions WinHTTP retournent des handles **HINTERNET** qui ne sont pas interchangeables avec d’autres Handles, donc ils ne peuvent pas être utilisés avec des fonctions telles que [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) ou [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle). De même, les autres Handles ne peuvent pas être utilisés avec les fonctions WinHTTP. Par exemple, un handle retourné par [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ne peut pas être passé à [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata). Ces handles **HINTERNET** ne peuvent pas être fermés lorsqu’un appel d’API utilisant le descripteur est en cours. Pour éviter une condition de concurrence, les applications doivent protéger le descripteur et l’empêcher d’être fermé tant que l’appel d’API est en cours.

Les fonctions Microsoft Win32 Internet (WinInet) utilisent également des handles **HINTERNET** . Toutefois, les handles utilisés dans les fonctions WinInet ne peuvent pas être modifiés avec les handles utilisés dans les fonctions WinHTTP. Pour plus d’informations sur WinInet, consultez [à propos de WinInet](/windows/desktop/WinInet/about-wininet).

La fonction [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle) ferme les handles WinHTTP **HINTERNET** .

## <a name="naming-handles"></a>Descripteurs de nommage

Dans la documentation WinHTTP, les descriptions des fonctions dans l’interface de programmation d’applications (API) et l’exemple de code illustrent la création et l’utilisation de différents types de descripteurs **HINTERNET** . Pour assurer le suivi des différents types de handles disponibles, le nom de ces descripteurs est cohérent. Le tableau suivant présente les identificateurs utilisés par Convention dans la documentation.



| Type de handle       | Handle de création de fonction                                                                                                          | Identificateur |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------|------------|
| Handle générique    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen), [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)ou [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) | hInternet  |
| Handle de session    | [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen)                                                                                                | hSession   |
| Handle de connexion | [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect)                                                                                          | hConnect   |
| Handle de demande    | [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest)                                                                                  | hRequest   |



 

## <a name="handle-hierarchy"></a>Hiérarchie des handles

Les handles **HINTERNET** sont conservés dans une hiérarchie. Le handle retourné par [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen) est le descripteur de **HINTERNET** de session. L’appel de **WinHttpOpen** initialise les fonctions WinHTTP et commence un contexte de session qui gère les informations et paramètres utilisateur pendant toute la durée de vie du handle de session. [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) spécifie un serveur HTTP ou https cible et crée un handle de **HINTERNET** de connexion. Par défaut, le handle de connexion hérite des paramètres pour le handle de session. Chaque ressource spécifiée avec un appel à [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest) est affectée à un descripteur de **HINTERNET** de requête.

Le diagramme suivant illustre la hiérarchie des handles **HINTERNET** . Chaque zone du diagramme représente une fonction WinHTTP qui retourne un handle **HINTERNET** .

![fonctions qui créent des handles](images/art-winhttp2.png)

Après avoir fermé un handle, l’application doit être préparée à recevoir des notifications de rappel sur le descripteur jusqu’à ce que la valeur finale du **\_ handle d’état de rappel \_ \_ \_ WinHTTP** soit retournée pour indiquer que le handle est complètement fermé.

Un descripteur de session est appelé le parent d’un handle de connexion qu’il a utilisé pour créer ; de même, le descripteur de connexion et son descripteur de session parent sont les parents de tous les descripteurs de demande que le handle de connexion est utilisé pour créer.

Lorsqu’un descripteur parent est fermé, les enfants qu’il a sont invalidés indirectement, même s’ils ne se ferment pas eux-mêmes, et les demandes ultérieures qui les utilisent échouent avec l’erreur erreur **\_ \_ handle non valide**. Les demandes asynchrones en attente ne peuvent pas être exécutées correctement.

Le diagramme suivant montre les fonctions qui utilisent le handle **HINTERNET** créé par [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest). Les zones ombrées représentent des fonctions WinHTTP qui créent des handles et les zones simples affichent les fonctions qui utilisent ces handles **HINTERNET** . Le diagramme est également organisé pour indiquer l’ordre dans lequel les fonctions WinHTTP sont normalement appelées.

![fonctions qui créent des handles](images/art-winhttp2.png)

## <a name="explanation-of-the-handle-hierarchy"></a>Explication de la hiérarchie des handles

Tout d’abord, un descripteur de session est créé avec [**WinHttpOpen**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopen). [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect) requiert le descripteur de session comme premier paramètre et retourne un handle de connexion pour un serveur spécifié. Un handle de demande est créé par [**WinHttpOpenRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpopenrequest), qui utilise le handle de connexion créé par [**WinHttpConnect**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpconnect). Si l’application choisit d’ajouter des en-têtes supplémentaires à la demande, ou si elle est nécessaire pour que l’application définisse des informations d’identification pour l’authentification, [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) et [**WinHttpSetCredentials**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetcredentials) peuvent être appelés à l’aide de ce handle de demande. La demande est envoyée par [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest), qui utilise le handle de demande. Après l’envoi de la demande, des données supplémentaires peuvent être envoyées au serveur à l’aide de [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata), ou l’application peut passer directement à [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) pour indiquer qu’aucune information supplémentaire n’est envoyée au serveur. À ce stade, en fonction de l’objectif de l’application, le descripteur de demande peut être utilisé pour appeler [**WinHttpQueryHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryheaders), [**WinHttpQueryAuthSchemes**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryauthschemes)ou récupérer une ressource avec [**WinHttpQueryDataAvailable**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpquerydataavailable) et [**WinHttpReadData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreaddata).

 

 
