---
description: à compter de Windows Server 2008 et Windows Vista, l’API WinHTTP a été améliorée pour inclure les fonctionnalités suivantes.
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: nouveautés de Windows Server 2008 et Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e474bbfa32d8f82737df4be6f537ca0a6f1bc870e2028d7dcdb1f418adb7120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071699"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>nouveautés de Windows Server 2008 et Windows Vista

à compter de Windows Server 2008 et Windows Vista, l’API WinHTTP a été améliorée pour inclure les fonctionnalités suivantes.

## <a name="greater-than-4-gb-upload"></a>Télécharger supérieure à 4 go.

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) peut envoyer uniquement 4 Go de données en raison des limitations de la taille du paramètre de longueur totale DWORD. Pour permettre aux applications d’envoyer plus de 4 Go de données, l’en-tête Content-Length est ajouté à la demande en spécifiant des données aussi volumineuses qu’un grand \_ entier (2 ^ 64 octets). Pour plus d’informations, consultez **WinHttpSendRequest**. Cette fonctionnalité n’est pas prise en charge sur l’objet com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="transfer-encoding-header"></a>En-tête Transfer-Encoding

L’en-tête Transfer-Encoding permet aux applications d’envoyer des données segmentées au serveur. Lorsque l’en-tête Transfer-Encoding est présent dans la demande, l’application envoie la demande avec un corps d’entité de longueur égale à zéro dans l’appel à [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). Le corps d’entité est envoyé dans les appels suivants à [**WinHttpWriteData**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata). Cette fonctionnalité n’est pas prise en charge sur l’objet com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>Récupération de la liste des émetteurs de certificats clients SSL

L’application peut récupérer la liste d’émetteurs de certificats client SSL lorsque [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) échoue avec un **certificat d’authentification de \_ \_ client WinHTTP \_ \_ \_ nécessaire**. Une nouvelle option, **l' \_ option \_ WinHTTP \_ \_ \_ liste d’émetteurs de certificats client**, permet aux applications de récupérer la liste d’émetteurs de certificats et de filtrer la liste pour le certificat optimal. Pour plus d’informations, consultez les rubriques [**indicateurs d’option**](option-flags.md) et [récupération de la liste d’émetteurs pour l’authentification du client SSL](ssl-in-winhttp.md) . Cette fonctionnalité n’est pas prise en charge sur l’objet com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="optional-client-certificates"></a>Certificats clients facultatifs

Lorsque [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) échoue avec une erreur que le certificat d' **\_ authentification du client WinHTTP a \_ \_ \_ \_ requis**, le serveur n’a peut-être pas besoin du certificat client SSL. Le serveur peut être en mesure de rétablir une autre forme d’authentification ou d’autoriser le client à poursuivre l’accès anonyme. L’application définit l’option de **\_ \_ \_ \_ contexte de certificat client de l’option WinHTTP** et spécifie une macro que WinHTTP utilise pour déterminer si le certificat client est requis. Pour plus d’informations, consultez [**indicateurs d’option**](option-flags.md). Cette fonctionnalité n’est pas prise en charge sur l’objet com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="source-and-destination-ip-addresses"></a>Adresses IP source et de destination

Quand [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) se termine, l’application peut récupérer l’adresse IP et le port source et de destination de la demande qui a généré la réponse. Une nouvelle structure est fournie pour recevoir les adresses source et de destination lorsque l’option d’informations de connexion de l' **\_ option \_ \_ WinHTTP** est définie. Pour plus d’informations, consultez [**indicateurs d’option**](option-flags.md). Cette fonctionnalité n’est pas prise en charge sur l’objet com [**IWinHttpRequest**](iwinhttprequest-interface.md) .

## <a name="additional-ssl-client-authentication-errors"></a>Erreurs d’authentification du client SSL supplémentaires

Des erreurs d’authentification du client SSL supplémentaires fournissent des informations supplémentaires sur le certificat client SSL. **Erreur \_ le certificat du \_ client winhttp \_ \_ aucune \_ \_ clé privée** et erreur le certificat winhttp certificat du client de **\_ \_ \_ \_ \_ \_ clé privée d’accès** n’est nouveau pour Windows Server 2008 et Windows Vista. L’objet com [**IWinHttpRequest**](iwinhttprequest-interface.md) retourne ces erreurs dans un HRESULT.

 

 



