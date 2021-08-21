---
description: Spécifie le modèle d’hébergement du fournisseur. La définition de cette propriété entraîne le chargement du fournisseur dans un processus hôte partagé qui a un niveau de privilège spécifié.
ms.assetid: 1e5c778d-cd29-449b-88e2-fe0c90d0edcd
ms.tgt_platform: multiple
title: Hébergement et sécurité du fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce0853b268f3d0bef0c43cbeabc10651885f0bd3b07f79d5c1b29072b560c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050487"
---
# <a name="provider-hosting-and-security"></a>Hébergement et sécurité du fournisseur

La propriété [**HostingModel**](--win32provider.md) dans l’instance **\_ \_ Win32Provider** qui représente votre fournisseur spécifie le modèle d’hébergement du fournisseur. La définition de cette propriété entraîne le chargement du fournisseur dans un processus hôte partagé qui a un niveau de privilège spécifié.

## <a name="shared-provider-host-process"></a>Processus hôte du fournisseur partagé

WMI réside dans un hôte de service partagé avec plusieurs autres services. Pour éviter d’arrêter tous les services en cas d’échec d’un fournisseur, les fournisseurs sont chargés dans un processus hôte distinct nommé « Wmiprvse.exe ». Plusieurs processus portant ce nom peuvent être en cours d’exécution. Chaque peut s’exécuter sous un compte différent avec une sécurité variable. sachez que, à partir de Windows Vista, utilisez la commande [**winmgmt**](winmgmt.md) pour exécuter WMI dans un processus séparé en lui-même à l’aide d’un port fixe. Pour plus d’informations, consultez [connexion à WMI à distance à partir de Vista](connecting-to-wmi-remotely-starting-with-vista.md).

L’hôte partagé peut s’exécuter sous l’un des comptes système suivants dans un processus hôte de Wmiprvse.exe :

-   [LocalSystem](/windows/desktop/Services/localsystem-account)
-   [NetworkService](/windows/desktop/Services/networkservice-account)
-   [LocalService](/windows/desktop/Services/localservice-account)

Un fournisseur peut également être un serveur COM local (.exe) ou auto-hébergé, qui ne nécessite pas d’hôte de fournisseur WMI.

## <a name="setting-the-hosting-model"></a>Définition du modèle d’hébergement

Comme LocalSystem est un compte privilégié, il est recommandé de définir [**HostingModel**](--win32provider.md) sur **NetworkServiceHost** lorsqu’un fournisseur s’exécute dans un processus de Wmiprvse.exe. Le compte NetworkServiceHost est destiné aux services qui ne nécessitent pas de privilèges étendus, mais qui doivent communiquer à distance avec d’autres systèmes.

Si vous ne définissez pas de valeur pour la propriété [**HostingModel**](--win32provider.md) , WMI définit la valeur par défaut **NetworkServiceHostOrSelfHost**. si la valeur **HostingModel** est définie sur **LocalSystemHost**, WMI utilise le suivi pour générer les événements 5603 et 5604 dans le journal des événements Windows. Étant donné que le compte [LocalSystem](/windows/desktop/Services/localsystem-account) local est hautement privilégié, ce paramètre n’est pas recommandé. Vous pouvez afficher ces événements dans la **Observateur d’événements**. Pour plus d’informations, consultez suivi de l' [activité WMI](tracing-wmi-activity.md).

Définissez la propriété [**HostingModel**](--win32provider.md) des fournisseurs découplés sur « découplé : com ». les fournisseurs créés en ajoutant des classes d’instrumentation à partir de [**Microsoft. Management. Infrastructure**](/previous-versions//hh872326(v=vs.85)) dans le .NET Framework sont des fournisseurs découplés. (**System. Management. Instrumentation** n’est plus pris en charge.) Pour plus d’informations sur la création d’un fournisseur découplé, voir [incorporation d’un fournisseur dans une application](incorporating-a-provider-in-an-application.md).

Le modèle d’hébergement est spécifié dans la propriété [**HostingModel**](--win32provider.md) de l’instance **\_ \_ Win32Provider** qui représente votre fournisseur.

**Pour définir le modèle d’hébergement d’un fournisseur**

1.  Dans le fichier MOF qui définit votre fournisseur, créez une instance de [**\_ \_ Win32Provider**](--win32provider.md).
2.  Attribuez un nom au fournisseur dans la propriété **Name** et affectez l’identificateur de classe (CLSID) de l’objet com du fournisseur à la propriété **CLSID** .

    L’exemple de code suivant affecte un nom à la propriété **Name** et le CSLID de l’objet com Provider à la propriété **CLSID** .

    ``` syntax
    Instance of __Win32Provider as $NewProvider
    {
        Name = "MyProvider";
        Clsid = "{.......}";
    }
    ```

3.  Assignez la valeur de l’hôte partagé appropriée à la propriété [**HostingModel**](--win32provider.md) . Les valeurs de l’hôte partagé, telles que « NetworkServiceHost », sont définies dans la propriété **HostingSpecification** de la classe des [**\_ fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) .

    L’exemple de code suivant affecte une valeur d’hôte partagé à la propriété [**HostingModel**](--win32provider.md) .

    ``` syntax
    HostingModel = "NetworkServiceHost";
    ```

L’exemple de code suivant montre comment inscrire un fournisseur dans NetworkServiceHost.

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost";
}
```

Si vous avez plusieurs fournisseurs, vous pouvez les regrouper dans un hôte de service spécifique en inscrivant votre fournisseur afin qu’il se trouve dans l’instance spécifique.

L’exemple de code suivant inscrit également un fournisseur dans NetworkServiceHost. La [**classe \_ fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) définit des valeurs pour les deux valeurs que combine pour créer la propriété **HostingModel** [**\_ \_ Win32Provider**](--win32provider.md) . Dans l’exemple, la valeur « NetworkServiceHost » provient de la propriété **HostingSpecification** des **\_ fournisseurs msft** et « LocalServiceHost » provient de la propriété **HostingGroup** .

``` syntax
Instance of __Win32Provider as $NewProvider
{
    Name = "MyProvider";
    Clsid = "{.......}";
    HostingModel = "NetworkServiceHost:MySharedHost";
}
```

Des problèmes de développement spéciaux existent pour les fournisseurs qui ne sont pas découplés et qui sont hébergés dans le processus Wmiprvse. Pour plus d’informations, consultez [débogage de fournisseurs](debugging-providers.md).

Si vous écrivez un fournisseur qui contient la propriété ou l’inscription du fournisseur de classe, tous les modèles de thread ne fonctionnent pas. Pour plus d’informations, consultez [choix de l’inscription correcte](choosing-correct-registration.md).

## <a name="hostingmodel-values-for-in-process-providers"></a>Valeurs de HostingModel pour les fournisseurs de In-Process

La liste suivante répertorie les valeurs de modèle d’hébergement du fournisseur à utiliser dans l’instance [**\_ \_ Win32Provider**](--win32provider.md) pour les fournisseurs qui s’exécutent dans un processus de Wmiprvse.exe.



| Valeur dans [ **\_ \_ Win32Provider. HostingModel**](--win32provider.md) | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SelfHost**                                                       | Le fournisseur commence à utiliser l’implémentation du serveur local au lieu de in-process. Le contexte de sécurité du processus dans lequel le fournisseur s’exécute détermine le contexte de sécurité du fournisseur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **LocalSystemHost**                                                | Le fournisseur, s’il est implémenté comme in-process, est chargé dans un hôte de fournisseur partagé s’exécutant dans un contexte [LocalSystem](/windows/desktop/Services/localsystem-account) . à [**partir de Windows**](--win32provider.md) Vista, **LocalSystemHost** n’est plus le modèle d’hébergement par défaut si le modèle d’hébergement d’un fournisseur WMI (**\_ \_ Win32Provider**.**** La propriété HostingModel) n’est pas spécifiée. Pour plus d’informations, consultez [sécurité des modèles d’hébergement](#provider-hosting-and-security).                                                                                                                                                                                                                                                                               |
| **LocalSystemHostOrSelfHost**                                      | Le fournisseur est auto-hébergé ou chargé dans le processus de Wmiprvse.exe s’exécutant sous le compte [LocalSystem](/windows/desktop/Services/localsystem-account) . Comme LocalSystem est un compte doté de privilèges élevés, une entrée est générée dans le journal des événements de sécurité NT pour notifier les administrateurs d’un fournisseur s’exécutant dans cet État approuvé.                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **NetworkServiceHost**                                             | Le fournisseur, s’il est implémenté comme in-process, est chargé dans le processus de Wmiprvse.exe s’exécutant sous le compte [NetworkService](/windows/desktop/Services/networkservice-account) . à [**partir de Windows**](--win32provider.md) Vista, il s’agit du modèle d’hébergement par défaut si le modèle d’hébergement d’un fournisseur WMI (**\_ \_ Win32Provider**.**** La propriété HostingModel) n’est pas spécifiée. Pour plus d’informations, consultez [sécurité des modèles d’hébergement](#provider-hosting-and-security).<br/> **NetworkServiceHost** a des privilèges limités et réduit donc le risque d’une attaque par élévation de privilèges. Si le fournisseur ne fonctionne que sur l’ordinateur local, définissez la propriété [**HostingModel**](--win32provider.md) sur **LocalServiceHost**.<br/> |
| **NetworkServiceHostOrSelfHost**                                   | Le fournisseur est auto-hébergé ou chargé dans le processus de WmiPrvse.exe s’exécutant sous le compte [NetworkService](/windows/desktop/Services/networkservice-account) . **NetworkServiceHostOrSelfHost** est la configuration par défaut lorsque la propriété [**HostingModel**](--win32provider.md) dans **\_ \_ Win32Provider** a la **valeur null**. étant donné que **NetworkServiceHostOrSelfHost** est la valeur par défaut, les fournisseurs de systèmes d’exploitation antérieurs peuvent continuer à fonctionner dans Windows Vista, Windows Server 2008 et les systèmes d’exploitation ultérieurs.                                                                                                                                                                                                                                             |
| **LocalServiceHost**                                               | Le fournisseur, s’il est implémenté comme in-process, est chargé dans le processus de Wmiprvse.exe s’exécutant sous le compte [LocalService](/windows/desktop/Services/localservice-account) . Il s’agit du modèle d’hébergement recommandé pour les services, car LocalService dispose de privilèges limités.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="hostingmodel-values-for-decoupled-providers"></a>Valeurs de HostingModel pour les fournisseurs découplés

La liste suivante répertorie les valeurs du modèle d’hébergement du fournisseur pour les fournisseurs découplés.

<dl> <dt>

<span id="Decoupled_Com"></span><span id="decoupled_com"></span><span id="DECOUPLED_COM"></span>**Découplé : com**
</dt> <dd>

Le fournisseur est un fournisseur découplé hébergé dans un processus distinct qui est un client à WMI.

L’exemple suivant montre le spécificateur FoldIdentity pour la propriété [**HostingModel**](--win32provider.md) définie sur **false**, ce qui permet au fournisseur d’emprunter l’identité du client.

``` syntax
Decoupled:Com:FoldIdentity(FALSE)
```

Si FoldIdentity n’est pas spécifié, la valeur de FoldIdentity est définie par défaut sur **true** . Pour des raisons de sécurité, il est recommandé de ne pas spécifier FoldIdentity (FALSe), car une application non autorisée avec l’emprunt d’identité du délégué peut affecter un domaine entier.

L’exemple suivant montre la propriété [**HostingModel**](--win32provider.md) définie dans la méthode recommandée qui est équivalente à la définition de FOLDIDENTITY (true).

``` syntax
Decoupled:Com
```

</dd> <dt>

<span id="Decoupled_Noncom"></span><span id="decoupled_noncom"></span><span id="DECOUPLED_NONCOM"></span>**Découplé : noncom**
</dt> <dd>

À usage interne uniquement. Non pris en charge.

</dd> </dl>

## <a name="security-of-hosting-models"></a>Sécurité des modèles d’hébergement

Dans la plupart des cas, **LocalSystem** est inutile et le contexte **NetworkServiceHost** est plus approprié. La plupart des fournisseurs WMI doivent emprunter l’identité du contexte de sécurité du client pour effectuer les opérations demandées pour le compte du client WMI. à partir de Windows Vista, un fournisseur WMI qui ne possède pas de définition de modèle d’hébergement et s’exécute comme s’il s’exécutait sous **LocalSystem** ne fonctionnera pas correctement. Pour corriger cette situation, modifiez le modèle d’hébergement attendu et assurez-vous que le code du fournisseur WMI effectue les opérations dans le contexte de sécurité du client en usurpant l’identité du client WMI. LocalSystem est rarement une exigence. Si votre fournisseur doit avoir ce niveau de privilège, spécifiez le modèle d’hébergement avec l’instruction suivante dans le fichier MOF.

``` syntax
HostingModel=LocalSystemHost
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Choix de l’inscription correcte](choosing-correct-registration.md)
</dt> <dt>

[Accès aux espaces de noms WMI](access-to-wmi-namespaces.md)
</dt> <dt>

[Sécurisation des espaces de noms WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Classes de résolution des problèmes et de configuration du fournisseur](provider-configuration-and-troubleshooting-classes.md)
</dt> <dt>

[**\_Fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> </dl>

 

