---
description: Paramètres de configuration du localisateur de proxy
ms.assetid: d74a85cf-293e-4322-9aff-55b06d6fda5e
title: Paramètres de configuration du localisateur de proxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3503a90bcccc990865769b6bf02a65fc383511f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114370"
---
# <a name="proxy-locator-configuration-settings"></a>Paramètres de configuration du localisateur de proxy

Cette rubrique décrit les paramètres de configuration pour le localisateur de proxy par défaut. Pour plus d’informations sur la création du localisateur de proxy avec des paramètres de configuration personnalisés, voir [How to configure the proxy Locator](how-to-configure-the-proxy-locator.md).

Le localisateur de proxy peut être configuré pour fonctionner en trois modes : le *mode manuel*, *le mode de détection automatique et le* *mode navigateur*. Les valeurs sont définies dans l’énumération [**MFNET \_ PROXYSETTINGS**](/windows/desktop/api/mfidl/ne-mfidl-mfnet_proxysettings) . L’application peut configurer le mode en définissant la propriété [**MFNETSOURCE \_ PROXYSETTINGS**](mfnetsource-proxysettings-property.md) . Le localisateur de proxy peut également être configuré pour ne pas utiliser de serveur proxy en affectant à cette propriété la valeur **MFNET \_ PROXYSETTING \_ None**. Le serveur proxy n’est pas utilisé si le serveur multimédia est un hôte local ou si l’application demande une adresse de classe A (127. x. x), réservée aux tests de bouclage.

> [!Caution]  
> Un serveur proxy est une barrière de sécurité entre votre intranet et Internet. Si vous n’utilisez pas de serveur proxy, vous risquez d’exposer le réseau à des menaces de sécurité.

 

-   Mode manuel. L’application définit ce mode en affectant à la propriété [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) la valeur **MFNET \_ PROXYSETTING \_ Manual**. L’application doit spécifier les informations de connexion suivantes :

    -   Nom d’hôte du serveur proxy : propriété [**MFNETSOURCE \_ PROXYHOSTNAME**](mfnetsource-proxyhostname-property.md) .
    -   Numéro de port : propriété [**\_ PROXYPORT de MFNETSOURCE**](mfnetsource-proxyport-property.md) .
    -   Indique s’il faut utiliser un serveur proxy pour les adresses locales : [**MFNETSOURCE \_ PROXYBYPASSFORLOCAL**](mfnetsource-proxybypassforlocal-property.md) . Ce paramètre est facultatif. Si ce paramètre n’est pas spécifié, le localisateur de proxy utilise la valeur par défaut **false**.

        > [!Note]  
        > En ignorant le serveur proxy, l’application peut être en mesure de se connecter plus rapidement aux serveurs multimédias sur l’intranet.

         

    -   Liste des adresses de serveur multimédia qui ne nécessitent pas de serveur proxy pour établir une connexion : [**MFNETSOURCE \_ PROXYEXCEPTIONLIST**](mfnetsource-proxyexceptionlist-property.md) Property. Ce paramètre est facultatif.

-   Mode de détection automatique. L’application définit ce mode en affectant à la propriété [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) la valeur **MFNET \_ PROXYSETTING \_ auto**. Dans ce mode, le localisateur de proxy utilise le mécanisme de proxy AutoProxy WinHTTP pour obtenir le nom d’hôte et le numéro de port du serveur proxy. Ces informations de connexion sont récupérées à l’aide du script de proxy automatique WPAD, qui est configuré par l’administrateur de domaine. Pour plus d’informations sur ce mécanisme, consultez le [site Web de Microsoft](../winhttp/winhttp-autoproxy-support.md).

    Le localisateur de proxy met en cache les informations de connexion dans le registre. Dans les appels de détection de proxy suivants, le localisateur de proxy lit les informations de proxy à partir du cache du Registre pour réduire la surcharge impliquée dans la détection automatique. Toutefois, l’application peut forcer la redétection automatique de proxy en définissant la propriété [**MFNETSOURCE \_ PROXYRERUNAUTODETECTION**](mfnetsource-proxyrerunautodetection-property.md) .

-   Mode navigateur. L’application définit ce mode en affectant à la propriété [**MFNETSOURCE \_ PROXYSETTING**](mfnetsource-proxysettings-property.md) la valeur **MFNET \_ PROXYSETTING \_ Browser**. Dans ce mode, le localisateur de proxy utilise les paramètres de proxy de l’application du navigateur. Ce mode est défini par défaut si le protocole est HTTP ou HTTPD.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge du proxy pour les sources réseau](proxy-support-for-network-sources.md)
</dt> </dl>

 

 
