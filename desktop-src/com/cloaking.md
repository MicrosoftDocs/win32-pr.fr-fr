---
title: Masquage (COM)
description: Le masquage est une fonctionnalité de sécurité COM qui détermine l’identité que le client projette sur le serveur lors de l’emprunt d’identité.
ms.assetid: 5b97d9d6-8fa9-4da2-8351-64772227d9a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588651cfa37def4e174ef0f2fdba9b79b0c60ca8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363403"
---
# <a name="cloaking-com"></a>Masquage (COM)

Le masquage est une fonctionnalité de sécurité COM qui détermine l’identité que le client projette sur le serveur lors de l’emprunt d’identité. Lorsque le masquage est défini, le serveur intermédiaire masque sa propre identité et présente l’identité du client au serveur qu’il appelle au nom du client. Directeur l’identité du client qui est affichée par le serveur est l’identité associée au proxy. L’identité du proxy est déterminée par plusieurs facteurs, dont l’un est le type de masquage défini (le cas échéant). Le masquage n’est pas pris en charge par le fournisseur de sécurité Schannel.

Les rubriques suivantes fournissent plus d’informations sur le masquage :

-   [Types de masquage](#types-of-cloaking)
-   [Impact du masquage sur l’identité du client](#how-cloaking-affects-client-identity)
-   [Définir le masquage](#setting-cloaking)
-   [Masquage et niveaux d’emprunt d’identité](#cloaking-and-impersonation-levels)
-   [Scénarios de voilage](#cloaking-scenarios)
-   [Rubriques connexes](#related-topics)

## <a name="types-of-cloaking"></a>Types de masquage

Il existe deux types de masquage : le masquage *statique* et le masquage *dynamique* :

-   Avec le masquage statique (EOAC \_ statique \_ ), le serveur voit le jeton de thread du premier appel d’un client au serveur. Pour le premier appel, si l’identité du proxy a été définie précédemment lors d’un appel à [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), cette identité de proxy est utilisée. Toutefois, si l’identité du proxy n’a pas été définie précédemment, le jeton de thread est utilisé. Si aucun jeton de thread n’est présent, le jeton de processus est utilisé. Pour tous les appels ultérieurs, l’identité définie sur le premier appel est utilisée.
-   Avec le masquage dynamique (EOAC \_ Dynamic \_ voilage), à chaque appel, le jeton de thread actuel (s’il existe un jeton de thread) est utilisé pour déterminer l’identité du client. S’il n’y a aucun jeton de thread, le jeton de processus est utilisé. Cela signifie que les serveurs appelés au nom du client pendant l’emprunt d’identité voient l’identité du client COM à l’origine de l’appel, qui est généralement le comportement souhaité. (Bien sûr, pour que l’emprunt d’identité aboutisse, le client doit avoir donné l’autorité de serveur pour emprunter l’identité en définissant un niveau d’emprunt d’identité approprié. Pour plus d’informations, consultez [niveaux d’emprunt d’identité](impersonation-levels.md).) Ce type de masquage est onéreux.

## <a name="how-cloaking-affects-client-identity"></a>Impact du masquage sur l’identité du client

Lorsqu’un appel chiffré est effectué et que le serveur demande son identité au client, il obtient généralement l’identité associée au proxy. (Parfois, le service d’authentification effectue une traduction à partir de l’identité réelle, mais en général, l’identité du proxy est l’identité que le serveur voit.) Le proxy présente une identité au serveur qui dépend du type de masquage défini et d’autres facteurs.

Pour résumer, l’identité du client est une fonction de l’indicateur de masquage défini, du jeton de processus, de la présence ou de l’absence d’un jeton de thread, et si l’identité du proxy a été définie précédemment. Le tableau suivant indique l’identité du proxy qui en résulte (identité du client) lorsque ces facteurs varient.



| Masquage d’indicateurs                     | Présence du jeton de thread  | Identité du proxy précédemment définie | Identité du proxy (identité du client)                    |
|------------------------------------|------------------------|-------------------------------|-----------------------------------------------------|
| Masquage non défini<br/>        | Ne vous inquiétez pas<br/>  | Ne vous inquiétez pas<br/>         | Traiter le jeton ou l’identité d’authentification<br/> |
| \_ \_ masquage statique EOAC<br/>  | Présent<br/>     | Non<br/>                 | Jeton de thread<br/>                             |
| \_ \_ masquage statique EOAC<br/>  | Présent<br/>     | Oui<br/>                | Identité du proxy actuel<br/>                   |
| \_ \_ masquage statique EOAC<br/>  | Non présent<br/> | Non<br/>                 | Traiter le jeton<br/>                            |
| \_ \_ masquage statique EOAC<br/>  | Non présent<br/> | Oui<br/>                | Identité du proxy actuel<br/>                   |
| \_ \_ voilage dynamique EOAC<br/> | Présent<br/>     | Ne vous inquiétez pas<br/>         | Jeton de thread<br/>                             |
| \_ \_ voilage dynamique EOAC<br/> | Non présent<br/> | Ne vous inquiétez pas <br/>        | Traiter le jeton<br/>                            |



 

L’organigramme suivant illustre le mode de détermination de l’identité du proxy dans différentes situations.

![Diagramme qui montre le déroulement de la détermination de l’identité du proxy.](images/9e8409b7-8475-4824-bdff-cf6b09c139c5.png)

## <a name="setting-cloaking"></a>Définir le masquage

Le masquage est défini en tant qu’indicateur de fonctionnalité dans un appel à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), qui définit le masquage pour l’ensemble du processus. La fonction de masquage est ensuite définie jusqu’à ce que le client la modifie par le biais d’un appel à IClientSecurity ::[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (ou à [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)), qui définit le masquage pour le proxy.

Par défaut, le masquage n’est pas défini. Pour le définir, transmettez \_ EOAC \_ static voiling ou EOAC \_ Dynamic \_ voiling au paramètre *pCapabilities* dans [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket).

Lorsque le masquage statique est activé à l’aide de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), chaque proxy récupère un jeton (thread ou processus) la première fois que vous effectuez un appel sur le proxy. Lorsque le masquage statique est activé à l’aide de [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), le proxy récupère le jeton sur le thread à ce moment-là. Si aucun jeton de thread n’est disponible lors de l’appel de **SetBlanket** , le jeton de processus est utilisé pour l’identité du proxy. Fondamentalement, **SetBlanket** corrige l’identité du proxy.

Avec le masquage dynamique, l’identité du proxy est déterminée de la même façon que le masquage dynamique soit défini à l’aide de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) ou de [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). Le jeton de thread actuel est utilisé, le cas échéant ; dans le cas contraire, le jeton de processus est utilisé.

Si le masquage est défini pour l’ensemble du processus via un appel à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) et que vous souhaitez effectuer des appels avec le jeton de processus, n’empruntez pas l’identité lors des appels.

## <a name="cloaking-and-impersonation-levels"></a>Masquage et niveaux d’emprunt d’identité

Comme indiqué précédemment, la fonctionnalité de voilage détermine l’identité qui est présentée à un serveur lors de l’emprunt d’identité. Le masquage permet à un serveur de projeter une identité autre que la sienne sur un autre serveur qu’il appelle pour le compte du client. Le niveau d’emprunt d’identité indique la quantité d’autorité que le client a donné au serveur.

L’emprunt d’identité sans masquage fonctionne, mais il n’est peut-être pas le meilleur choix car, dans certains cas, le serveur final doit connaître l’identité de l’appelant initial. Cela ne peut pas être effectué sans utiliser le masquage, car il est difficile de s’assurer que seuls les clients autorisés peuvent accéder à un ordinateur distant. Lorsque l’emprunt d’identité est utilisé sans voilage, l’identité présentée à un serveur en aval est celle du processus appelant immédiat.

Toutefois, le masquage n’est pas utile sans emprunt d’identité. Le masquage n’a de sens que lorsque le client a défini un niveau d’emprunt d’identité pour l’emprunt d’identité ou le délégué. (Avec des niveaux d’emprunt d’identité inférieurs, le serveur ne peut pas effectuer d’appels masqués.) La réussite du masquage dépend du nombre de limites de l’ordinateur franchies et du niveau d’emprunt d’identité, qui indique la quantité d’autorité que le serveur doit agir pour le compte du client.

Dans certains cas, il est logique pour le serveur de définir le masquage lorsque le client définit le niveau d’emprunt d’identité sur l' \_ emprunt d’identité RPC C \_ IMP \_ \_ . Toutefois, certaines limitations sont appliquées. Si le client d’origine définit le niveau d’emprunt d’identité sur l' \_ emprunt d’identité RPC C \_ IMP \_ \_ , le serveur intermédiaire (agissant comme un client sur le même ordinateur) peut masquer sur une seule limite d’ordinateur. Cela est dû au fait qu’un jeton d’emprunt d’identité au niveau de l’emprunt d’identité peut être passé sur une seule limite d’ordinateur. Une fois la limite de l’ordinateur franchie, seules les ressources locales sont accessibles. L’identité présentée au serveur dépend du type de masquage défini. Si aucun voilage n’est défini, l’identité présentée à un serveur est celle du processus qui effectue l’appel immédiat.

Pour masquer sur plusieurs limites d’ordinateur, vous devez spécifier à la fois un indicateur de fonctionnalité de masquage approprié et un emprunt d’identité au niveau du délégué. Avec ce type d’emprunt d’identité, les informations d’identification locales et réseau du client sont fournies au serveur, de sorte que le jeton d’emprunt d’identité peut franchir n’importe quel nombre de limites de l’ordinateur. Là encore, l’identité présentée au serveur dépend du type de masquage défini. Si aucun voilage n’est défini avec l’emprunt d’identité au niveau du délégué, l’identité présentée à un serveur est celle du processus à l’origine de l’appel.

Par exemple, supposons que le processus A appelle B et que B appelle C. B a défini le masquage et a a défini le niveau d’emprunt d’identité sur emprunter l’identité. Si A, B et C se trouvent sur le même ordinateur, le passage du jeton d’emprunt d’identité de A à B, puis à C fonctionnera. Toutefois, si A et C se trouvent sur le même ordinateur et que B ne l’est pas, le fait de passer le jeton fonctionne entre A et B, mais pas entre B et C. L’appel de B à C échoue, car B ne peut pas appeler C lors du masquage. Toutefois, si A définit le niveau d’emprunt d’identité à déléguer, le jeton peut être passé de B à C et l’appel peut être réussi.

## <a name="cloaking-scenarios"></a>Scénarios de voilage

Dans l’illustration suivante, le processus A appelle B, appelle C, appelle D lorsque le masquage n’est pas défini. Par conséquent, chaque processus intermédiaire voit l’identité du processus qui l’a appelé.

![Diagramme qui montre le processus lorsque le masquage n’est pas défini.](images/0d2eb6cf-97d6-4c4e-b97e-abad854b1120.png)

Avec le masquage statique, le serveur voit l’identité de proxy qui a été définie lors du premier appel du client au serveur. L’illustration suivante montre un exemple de l’identité de proxy définie lors d’un appel de B à C. Lors d’un appel ultérieur, le processus D voit l’identité de B lorsque le masquage statique est défini par B et C.

![Diagramme qui montre le processus de masquage statique.](images/520938e0-c4a6-4ac1-937d-02baf2007a27.png)

Avec le masquage dynamique, l’identité de l’appelant pendant l’emprunt d’identité est basée sur le jeton de thread actuel, le cas échéant. L’illustration suivante montre la situation dans laquelle B et C définissent le masquage dynamique et que D voit l’identité d’un, en dépit d’un appel antérieur de B à C.

![Diagramme qui montre le processus de masquage dynamique.](images/d0848465-82f3-4d5a-851e-566d7800ada0.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Délégation et emprunt d’identité](delegation-and-impersonation.md)
</dt> </dl>

 

