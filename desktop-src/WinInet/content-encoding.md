---
title: Encodage du contenu
description: À compter de Windows Server 2008 et Windows Vista, l’application peut diriger WinINet pour effectuer le décodage de contenu pour les schémas d’encodage de contenu gzip et deflate.
ms.assetid: 136f22a6-e5ca-41c5-8651-6e132655d268
keywords:
- Encodage du contenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b089ae2aa4cbacdfc9b6ebefe5cbdfc1bfc10e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031724"
---
# <a name="content-encoding"></a>Encodage du contenu

Comme spécifié dans les applications de protocole HTTP (RFC 2616) peuvent demander que le serveur retourne les réponses HTTP dans un format encodé. Avant Windows Server 2008 et Windows Vista, les demandes avec encodage de contenu étaient envoyées à l’application à des fins de traitement à leur niveau. À compter de Windows Server 2008 et Windows Vista, l’application peut diriger WinINet pour effectuer le décodage de contenu pour les schémas d’encodage de contenu gzip et deflate.

Pour activer le décodage du contenu, l’application définit l’option de décodage demandant à ce que WinINet effectue le décodage en son nom. Toutefois, l’activation du décodage ne garantit pas que WinINet effectue le décodage du contenu et que l’application doit être préparée à gérer le décodage. WinINet supprime l’en-tête Content-Encoding de la réponse lorsque le décodage du contenu est correctement effectué. Les applications sont censées gérer le décodage du contenu, que l’option de décodage soit activée ou désactivée lorsque l’en-tête Content-Encoding est présent dans la réponse.

Lorsque le décodage est activé, l’application doit spécifier la liste des encodages pris en charge dans l’en-tête Accept-Encoding de la requête. Toutefois, l’en-tête Accept-Encoding n’oblige pas le serveur à envoyer une réponse encodée. WinINet envoie les réponses qui ne correspondent pas à la liste des encodages acceptables à l’application.

La liste suivante décrit les conditions dans lesquelles WinINet effectue le décodage du contenu lorsque l’option est activée :

-   L’en-tête Accept-Encoding doit être présent dans la demande et doit spécifier les schémas d’encodage gzip, deflate ou gzip et deflate.
-   Le schéma d’encodage spécifié dans l’en-tête Content-Encoding doit correspondre à l’un des schémas d’encodage spécifiés dans l’en-tête Accept-Encoding.
-   L’en-tête Content-Encoding dans la réponse spécifie un seul schéma d’encodage.
-   La réponse ne doit contenir qu’un seul en-tête Content-Encoding. WinINet décode le contenu encodé avec un seul schéma d’encodage.
-   L’en-tête Cache-Control ne doit pas contenir la directive no-Transform.
-   L’en-tête Content-Range ne doit pas être présent dans la réponse.

## <a name="setting-the-decompression-option"></a>Définition de l’option de décompression

L’option de décodage peut être définie sur le descripteur de session, le handle de demande ou le handle de connexion. Handle sur lequel l’option de décodage est définie, définit la portée de l’option de décodage. Par exemple, la définition du décodage sur la session permet de décoder une partie des connexions et des demandes créées sous ce descripteur.

Pour définir l’option de décodage, l’application appelle [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) avec le descripteur retourné par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta). L’option **Internet \_ encodage \_ http \_** est spécifiée dans le paramètre *valeur dwOption* et le paramètre *lpBuffer* pointe vers une variable booléenne définie sur true. Pour désactiver le décodage, l’application appelle **InternetSetOption** avec l’option **Internet \_ \_ \_ décodage http** et la variable booléenne définie sur false.

Lorsque l’option de décodage est définie, WinINet effectue le décodage sur la demande lorsque l’application appelle [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile). Si WinINet rencontre une erreur lors du décodage du contenu, l’appel à **InternetReadFile** échoue avec une **erreur le \_ \_ décodage Internet \_ a échoué**. Lorsque le décodage échoue, l’application dispose de deux options : elle peut supprimer l’en-tête Accept-Encoding et renvoyer la demande, ou il peut définir l’option **Internet \_ \_ \_ décodage http** de la demande sur false, puis renvoyer la demande. Si l’option de décodage est définie sur false, l’application doit vérifier l’en-tête Content-Encoding et effectuer tout décodage au niveau de l’application.

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 