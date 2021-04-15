---
description: Lorsque vous exécutez un script sur un système local qui obtient des données à partir d’un système distant, WMI fournit vos informations d’identification au fournisseur des données sur le système distant.
ms.assetid: e27ff207-b067-47df-9706-e8af51646d28
ms.tgt_platform: multiple
title: Délégation avec WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8a624f3d437d977ff73b3854a59cfd634350e7
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104393867"
---
# <a name="delegating-with-wmi"></a>Délégation avec WMI

Lorsque vous exécutez un script sur un système local qui obtient des données à partir d’un système distant, WMI fournit vos informations d’identification au fournisseur des données sur le système distant. Cela nécessite uniquement un niveau d’emprunt d’identité d' **emprunt d’identité**, car un seul tronçon réseau est requis. Toutefois, si le script se connecte à WMI sur le système distant et tente d’ouvrir un fichier journal sur un autre système distant, le script échoue, sauf si le niveau d’emprunt d’identité est **délégué**. Le niveau d’emprunt d’identité **délégué** est requis par toute opération qui implique plusieurs sauts réseau. Pour plus d’informations sur la sécurité DCOM dans WMI, consultez Définition de la [sécurité des processus des applications clientes](setting-client-application-process-security.md). Pour plus d’informations sur la connexion d’un saut de réseau entre deux ordinateurs, consultez [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md).

**Pour utiliser la délégation pour se connecter à un ordinateur par le biais d’un autre ordinateur**

1.  Activez la délégation dans Active Directory (**Active Directory les utilisateurs et les ordinateurs** dans les **tâches d’administration** du **panneau de configuration** ) sur le contrôleur de domaine. Le compte sur le système distant doit être marqué comme **approuvé pour la délégation** et le compte sur le système local ne doit pas être marqué comme étant **sensible et ne peut pas être délégué**. le système local, le système distant et le contrôleur de domaine doivent être membres du même domaine ou dans des domaines approuvés.

    **Remarque**  L’utilisation de la délégation est un risque pour la sécurité, car elle permet aux processus en dehors de votre contrôle direct d’utiliser vos informations d’identification.

2.  Modifiez votre code de la manière suivante pour indiquer que vous souhaitez utiliser la délégation.

    <dl> <dt>

    <span id="PowerShell"></span><span id="powershell"></span><span id="POWERSHELL"></span>PowerShell
    </dt> <dd>

    Définissez le paramètre *-emprunt d’identité* de l’applet de commande WMI sur **déléguer**.

    </dd> <dt>

    <span id="VBScript"></span><span id="vbscript"></span><span id="VBSCRIPT"></span>VBScript
    </dt> <dd>

    Définissez le paramètre *ImpersonationLevel* à **déléguer** dans l’appel à [SWbemLocator. ConnectServer](swbemlocator-connectserver.md) ou au **délégué** dans la chaîne de [moniker](constructing-a-moniker-string.md) . Vous pouvez également définir l’emprunt d’identité dans un objet [**SWbemSecurity**](swbemsecurity.md).

    </dd> <dt>

    <span id="C__"></span><span id="c__"></span>C++
    </dt> <dd>

    Définissez le paramètre de niveau d’emprunt d’identité sur **RPC \_ C \_ IMP \_ Level \_ Delegate** dans l’appel à [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Pour plus d’informations sur le moment d’effectuer ces appels, consultez [initialisation de com pour une application WMI](initializing-com-for-a-wmi-application.md).

    Pour transmettre l’identité du client aux serveurs COM distants en C++, définissez le masquage dans l’appel à [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket). Pour plus d’informations, consultez [masquage](../com/cloaking.md).

    </dd> </dl>

## <a name="examples"></a>Exemples

L’exemple de code suivant montre une chaîne de moniker qui définit l’emprunt d’identité à **déléguer**. N’oubliez pas que l’autorité doit avoir la valeur Kerberos.


```vb
set objWMIServices = Getobject("winmgmts:{impersonationLevel=Delegate,authority=kerberos:MyDomain\Computer_B}!\\ComputerB\Root\CIMv2")
```



L’exemple de code suivant montre comment définir l’emprunt d’identité sur **Delegate** (une valeur de 4) à l’aide de [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).


```vb
Set objLocator = CreateObject("WbemScripting.SWbemLocator")
Set objWMIService = objLocator.ConnectServer(Computer_B, _
                                             "Root\CIMv2", _
                                             AdminAccount, _
                                             MyPassword, _
                                             "kerberos:Domain\Computer_B")
objWMIService.Security_.ImpersonationLevel = 4
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md)
</dt> <dt>

[Création de processus à distance avec WMI](creating-processes-remotely.md)
</dt> </dl>

 

 
