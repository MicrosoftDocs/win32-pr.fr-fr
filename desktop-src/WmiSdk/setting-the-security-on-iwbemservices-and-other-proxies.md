---
description: 'En C++, vous pouvez définir la sécurité sur l’ensemble du processus en appelant CoInitializeSecurity avant de vous connecter à WMI via IWbemLocator :: ConnectServer.'
ms.assetid: 83c04a96-3829-4c07-91a7-06e5b75b2c12
ms.tgt_platform: multiple
title: Définition de la sécurité sur IWbemServices et d’autres proxies
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d593c52091182b1f0580908624e0b4068ed3f8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522425"
---
# <a name="setting-the-security-on-iwbemservices-and-other-proxies"></a>Définition de la sécurité sur IWbemServices et d’autres proxies

En C++, vous pouvez définir la sécurité sur l’ensemble du processus en appelant [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) avant de vous connecter à WMI via [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver). Vous pouvez également modifier le niveau d’authentification, le niveau d’emprunt d’identité ou le service d’authentification dans un appel qui obtient un pointeur vers un proxy WMI, tel que [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) ou [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult). L’appel de [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) vous permet également de modifier le service d’authentification (Kerberos, NTLM ou Negotiate).

Les scripts et les applications de Visual Basic définissent la sécurité des proxies indirectement par le biais d’appels à [**SWbemServices**](swbemservices.md) et d’autres objets Automation. Pour plus d’informations sur la définition et la modification de l’authentification et de l’emprunt d’identité dans le script, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

La modification des niveaux de sécurité ou des services est principalement un problème lors de la connexion à WMI sur un ordinateur distant qui exécute un système d’exploitation différent. Pour plus d’informations, consultez [connexion entre différents systèmes d’exploitation](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection).

Une application cliente se connecte à un proxy WMI à l’aide d’une identité. Une identité est un objet de données qui se compose d’un nom d’utilisateur, d’un mot de passe et de paramètres d’autorité. Pour une application cliente WMI, l’appel à l’interface [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) crée l’identité initiale. La méthode [**ConnectServer**](swbemlocator-connectserver.md) prend l’identité dans un ensemble de trois paramètres, que vous pouvez définir sur **null** pour indiquer l’utilisateur actuel. Vous pouvez également spécifier un paramètre non **null** pour indiquer un utilisateur et un domaine spécifiques. Si l’appel réussit, **ConnectServer** retourne un pointeur via lequel vous pouvez accéder à un large éventail de processus distants, tels qu’un service WMI ou le système d’exploitation Windows directement.

Comme de nombreuses interfaces COM, [**ConnectServer**](swbemlocator-connectserver.md) retourne un pointeur vers un proxy. Un proxy est un objet de données qui représente un processus distant, tel que WMI ou un fournisseur distant. COM utilise un proxy pour permettre aux développeurs d’accéder aux données distantes comme si les données étaient locales.

Les interfaces WMI suivantes utilisent des proxys :

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) (objet de script [**SWbemServices**](swbemservices.md) )
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) (objet de script [**SWbemRefresher**](swbemrefresher.md) )

    L’actualisateur WMI est un cas particulier, car il reçoit un pointeur [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) , dont les paramètres de sécurité doivent être définis correctement. Pour plus d’informations sur l’utilisation des objets actualisateurs, consultez [accès aux données de performances en C++](accessing-performance-data-in-c--.md).

Une fois que vous avez reçu un pointeur vers un processus distant, vous pouvez effectuer l’une des deux opérations suivantes : Si vous savez ce que fait le processus, vous pouvez choisir de définir la sécurité sur le pointeur et d’accéder au processus normalement. C’est le cas avec la plupart des pointeurs vers un service WMI. Pour plus d’informations, consultez [définition des niveaux de sécurité sur une connexion WMI](setting-the-security-levels-on-a-wmi-connection.md). Vous avez également besoin d’accéder à une interface COM différente sur le proxy, telle que [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release), via un appel à l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) sur le proxy.

## <a name="defaults-and-recommendations"></a>Valeurs par défaut et recommandations

La version distribuée du modèle COM (Component Object Model) négocie le service d’authentification par défaut (Kerberos, NTLM ou Negotiate) et vous ne pouvez pas spécifier le service d’authentification par défaut à l’aide de [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). La spécification de la **\_ \_ \_ valeur par défaut de RPC C Authn** dans le paramètre Authentication Service de [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) permet à DCOM de sélectionner le service approprié. Pour les connexions distantes, le service par défaut est Negotiate, qui est le service recommandé pour les applications qui fonctionnent dans les domaines Kerberos et non-Kerberos. Pour les connexions locales, le service d’authentification par défaut est NT LAN Manager (NTLM).

L’exemple de code suivant illustre l’utilisation du service d’authentification par défaut.


```C++
// The pWbemServices variable is of type IWbemServices*

HRESULT hr = CoSetProxyBlanket(
     pWbemServices,                //Proxy
     RPC_C_AUTHN_DEFAULT,          //Authentication service 
     RPC_C_AUTHZ_DEFAULT,          //Authorization service 
     COLE_DEFAULT_PRINCIPAL,       //Server principal name used 
                                       // by authentication service
     RPC_C_AUTHN_LEVEL_DEFAULT,    //Authentication level
     RPC_C_IMP_LEVEL_IMPERSONATE,  //Impersonation level
     COLE_DEFAULT_AUTHINFO,       //Client identity
     EOAC_DEFAULT                  //Capability flags
     );
```



L’exemple de code de cette rubrique requiert la référence et les \# instructions include suivantes.


```C++
#define _WIN32_DCOM
#include <wbemidl.h>
#include <comdef.h>

#pragma comment(lib, "wbemuuid.lib")
```



Pour les scripts, il est recommandé d’utiliser les valeurs par défaut que DCOM sélectionne pour les appels distants. Sur l’ordinateur local, vous ne pouvez pas spécifier un service d’authentification pour les appels à WMI. Pour plus d’informations, consultez [définition du service d’authentification à l’aide de VBScript](setting-the-authentication-service-using-vbscript.md) et [construction d’une chaîne de moniker](constructing-a-moniker-string.md).

 

 
