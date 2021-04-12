---
description: Lorsque vous effectuez des appels en dehors du processus appelant ou à un service WMI distant, WMI utilise la version distribuée du modèle COM (Component Object Model).
ms.assetid: 261b4f18-5de5-4e06-a887-f5afd9c45511
ms.tgt_platform: multiple
title: Configuration de l’authentification dans WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0293d74c528e7c1c0e77a1ffb9f5f9ee7dfd5f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203728"
---
# <a name="setting-authentication-in-wmi"></a>Configuration de l’authentification dans WMI

Lorsque vous effectuez des appels en dehors du processus appelant ou à un service WMI distant, WMI utilise la version distribuée du modèle COM (Component Object Model). Les appels hors processus et distants sont effectués par le biais de proxies, qui requièrent l’authentification des informations d’identification du processus appelant.

Vous définissez le niveau d’authentification lors de la connexion à un ordinateur et à un espace de noms WMI. Pour vous connecter à WMI, appelez [**IWbemLocator :: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) en C++. Dans les scripts ou les Visual Basic, vous vous connectez à WMI à l’aide de SWbemLocator. ConnectServer ou de la chaîne de [moniker](constructing-a-moniker-string.md) . La sécurité DCOM et WMI requièrent tous deux des niveaux d’authentification lors de la connexion entre les ordinateurs. Le niveau requis varie selon le système d’exploitation que vous connectez. Pour plus d’informations, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

WMI s’exécute normalement dans un hôte de service partagé et partage la même authentification que les autres processus de l’hôte. Pour exécuter le processus WMI avec un autre niveau d’authentification, exécutez WMI avec la commande [**winmgmt**](winmgmt.md) avec le commutateur **/standalonehost** et définissez le niveau d’authentification pour WMI en général. Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).

Pour plus d’informations et des exemples de code sur la façon de définir l’authentification pour les connexions WMI, consultez [définition du service d’authentification à l’aide de VBScript](setting-the-authentication-service-using-vbscript.md) et définition de l' [authentification à l’aide de C++](setting-authentication-using-c-.md). Ces rubriques contiennent également des tables qui répertorient les constantes d’authentification pour C++ et les scripts.

## <a name="using-proxies-in-wmi"></a>Utilisation de proxies dans WMI

Pour définir l’authentification d’un proxy, appelez la fonction [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) . Pour plus d’informations et pour obtenir un exemple de code, consultez [définition de la sécurité sur IWbemServices et d’autres proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

L' [API com pour](com-api-for-wmi.md) les objets WMI suivante utilisent des proxys directement en C++ ou C# pour appeler hors processus ou un service WMI distant :

-   [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)
-   [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

Les objets de script, tels que [**SWbemObject**](swbemobject.md), [**SWbemServices**](swbemservices.md)et [**SWbemRefresher**](swbemrefresher.md) , n’utilisent pas directement les proxys. Au lieu de cela, les objets de script représentent un wrapper ou une couche qui appelle l' [API com pour](com-api-for-wmi.md) les objets WMI listés ci-dessus. Pour plus d’informations et pour obtenir un exemple de code de configuration de l’authentification dans les scripts, consultez [définition du niveau de sécurité de processus par défaut à l’aide de VBScript](setting-the-default-process-security-level-using-vbscript.md).

 

 
