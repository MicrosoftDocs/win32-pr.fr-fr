---
description: Cache du proxy AutoProxy
ms.assetid: 087104e8-ab38-4ba4-be70-23a5ea2bb130
title: Cache du proxy AutoProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45d494f1491dd52484a893dbab601ed4870f03badf5f849dca413f9554a8493e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614179"
---
# <a name="autoproxy-cache"></a>Cache du proxy AutoProxy

La fonction [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) effectue une recherche de proxy AutoProxy à la demande pour l’URL spécifiée. Si plusieurs proxies sont retournés, les applications clientes doivent tester chaque proxy avant d’envoyer la demande (pour plus d’informations, consultez la section le [seul serveur proxy est actuellement pris en charge](autoproxy-issues-in-winhttp.md) dans les problèmes liés à proxy dans WinHTTP). Les informations contenues dans cette rubrique s’appliquent aux appels à **WinHttpGetProxyForUrl** lorsque le client spécifie la détection automatique de proxy.

[**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) localise éventuellement l’URL du proxy AutoProxy et télécharge le script du proxy AutoProxy à partir de ce site. WinHttp utilise le script de proxy AutoProxy pour localiser les serveurs proxy. L’URL du proxy et le script du proxy AutoProxy sont mis en cache pour la session spécifiée. Une seule URL et un seul script de proxy AutoProxy sont mis en cache pour chaque session. En règle générale, le script et l’URL du proxy AutoProxy sont mis en cache jusqu’à ce que l’adresse IP associée à l’ordinateur soit modifiée. Si une nouvelle adresse IP est détectée lors d’un appel à **WinHttpGetProxyForUrl**, l’appel tente de localiser une nouvelle URL et un script de proxy et met en cache les résultats. Un seul utilisateur doit être autorisé par session, afin que les données mises en cache ne soient pas partagées avec d’autres utilisateurs sur l’ordinateur. Pour plus d’informations, consultez [vue d’ensemble des sessions WinHTTP](winhttp-sessions-overview.md).

Si le service hors processus est actif lors de l’appel de [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) , l’URL et le script du proxy AutoProxy mis en cache sont disponibles pour l’ensemble de l’ordinateur. Toutefois, si le service out-of-process est utilisé et que l’indicateur **fAutoLogonIfChallenged** dans la structure *pAutoProxyOptions* a la valeur true, l’URL et le script du proxy AutoProxy ne sont pas mis en cache. Par conséquent, l’appel de **WinHttpGetProxyForUrl** avec le membre **FAutoLogonIfChallenged** défini sur **true** entraîne des opérations de surcharge supplémentaires qui peuvent affecter les performances. Les étapes suivantes peuvent être utilisées pour améliorer les performances.

**Pour améliorer les performances**

1.  Appelez [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) avec le paramètre fAutoLogonIfChallenged défini sur **false**. L’URL et le script du proxy AutoProxy sont mis en cache pour les futurs appels à **WinHttpGetProxyForUrl**.
2.  Si l’étape 1 échoue, avec l' **erreur d' \_ \_ \_ échec de connexion WinHTTP**, appelez [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) avec le membre **fAutoLogonIfChallenged** défini sur **true**.

 

 



