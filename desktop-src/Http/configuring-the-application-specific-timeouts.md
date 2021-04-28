---
title: Configuration des délais d’attente spécifiques à l’application
description: Configuration des délais d’attente spécifiques à l’application
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Configuration des délais d’attente spécifiques à l’application HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1cbcdb0b0796820282673c41507f6bfcc0ebd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109737"
---
# <a name="configuring-the-application-specific-timeouts"></a>Configuration des délais d’attente spécifiques à l’application

Les paramètres au niveau de l’API du serveur HTTP s’appliquent à toutes les sessions serveur et tous les groupes d’URL sur l’ordinateur. Ces configurations peuvent être remplacées par l’application en définissant les valeurs de délai d’attente propres à l’application. Les délais d’expiration de la session serveur remplacent les délais d’expiration à l’ensemble de l’API du serveur HTTP et s’appliquent à tous les groupes d’URL créés sous ceux-ci. La configuration de la propriété timeouts sur un groupe d’URL remplace les délais d’expiration de session serveur pour toutes les URL dans le groupe.

Si vous spécifiez zéro pour l’une des minuteries de la structure d' [**\_ informations de limite de dépassement de délai \_ \_ http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) pour un groupe d’URL, l’API du serveur http revient aux délais d’expiration de session du serveur, s’ils existent, ou aux paramètres par défaut de l’API du serveur http si les délais d’expiration de la session serveur n’existent pas. Par exemple, lorsque la propriété délai d’attente du serveur est présente dans un groupe d’URL et que la minuterie **EntityBody** est égale à zéro, le délai d’expiration de la session serveur est utilisé. Si la propriété timeouts n’est pas définie sur une session serveur, la configuration par défaut de l’API du serveur HTTP est utilisée. Pour désactiver un minuteur, définissez la valeur sur **MAXUSHORT**, à l’exception de la minuterie **MinSendRate** qui est définie sur **MAXULONG**.

L’API du serveur HTTP ne peut configurer que le **HeaderWait** spécifique à l’application et les minuteurs **IdleConnection** sont effectifs uniquement après la réception de la première requête. Avant la réception de la première demande, les valeurs de délai d’expiration de l’API du serveur HTTP sont appliquées. Une fois que la première requête a été envoyée et qu’elle est associée à une file d’attente de demandes, les minuteurs **HeaderWait** et **IdleConnection** spécifiques à l’application peuvent être appliqués. Les minuteurs spécifiques à l’application sont appliqués à toutes les demandes suivantes qui arrivent dans la file d’attente des demandes pour une connexion Keep-Alive.

Pour plus d’informations sur la configuration des minuteries, consultez les rubriques [configuration du groupe d’URL](configuring-the-url-group.md) et [configuration de la session serveur](configuring-the-server-session.md) .

 

 




