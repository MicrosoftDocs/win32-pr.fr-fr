---
description: lorsque vous accédez à un serveur Windows Management Instrumentation (WMI) à l’aide d’un script, vous pouvez choisir entre les protocoles d’authentification NTLM (NT LAN Manager) ou Kerberos.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Définition du service d’authentification à l’aide de VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bd2cf444560aac7ebce96b52d9abaa528bdcaa76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403583"
---
# <a name="setting-the-authentication-service-using-vbscript"></a>Définition du service d’authentification à l’aide de VBScript

lorsque vous accédez à un serveur Windows Management Instrumentation (WMI) à l’aide d’un script, vous pouvez choisir entre les protocoles d’authentification NTLM (NT LAN Manager) ou Kerberos. La spécification de Kerberos n’est pas requise, sauf lors de l’utilisation de la délégation. Pour plus d’informations, consultez [connexion à un troisième ordinateur-délégation](connecting-to-a-3rd-computer-delegation.md).

Étant donné que les versions de système d’exploitation diffèrent dans le service d’authentification qu’elles utilisent, il est recommandé de ne pas spécifier de valeur pour le champ autorité lors de la connexion à un système distant. Au lieu de cela, autorisez le système d’exploitation et la version distribuée du modèle COM (Component Object Model) à sélectionner NTLM ou Kerberos. Si un service d’authentification est spécifié, la syntaxe requiert le nom principal du serveur, qui est le nom de l’ordinateur cible plutôt que le contrôleur de domaine.

Vous pouvez utiliser le paramètre Authority uniquement avec les connexions aux serveurs WMI distants. La tentative de connexion échoue si vous tentez de définir des niveaux d’autorisation dans le cadre d’un moniker ou d’un appel à [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) pour une connexion locale.

Procédez comme suit pour spécifier le service d’authentification que vous souhaitez utiliser dans le paramètre *strAuthority* de la méthode [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) ou de la connexion de chaîne [moniker](constructing-a-moniker-string.md) .

**Pour spécifier l’authentification NTLM ou Kerberos avec l’API de script pour WMI**

1.  Si le paramètre *strAuthority* commence par la chaîne « Kerberos : », WMI suppose que la chaîne fait référence à un nom de principal Kerberos et que l’authentification Kerberos est utilisée. Si le paramètre *strAuthority* commence par la chaîne « ntlmdomain : », WMI utilise l’authentification NTLM à la place.
2.  Vous pouvez également utiliser la partie autorité d’un moniker pour spécifier le type d’authentification utilisé pour la connexion à WMI. Pour utiliser l’authentification Kerberos lors de l’utilisation d’un moniker, incluez la chaîne « Authority = Kerberos : » suivie du nom principal. Pour utiliser l’authentification NTLM, incluez la chaîne « Authority = ntlmdomain : » suivie du nom de domaine NTLM.

    L’exemple suivant montre un moniker qui demande l’authentification Kerberos à l’aide de l’entité « MyDomain \\ Server ».

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    En revanche, l’exemple suivant montre un moniker qui demande l’authentification NTLM à l’aide du domaine « mydomain ».

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



