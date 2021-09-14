---
description: Une fois WMI terminé avec un fournisseur, le fournisseur est déchargé de la mémoire.
ms.assetid: 6116769f-3402-42b3-835d-9bdb0fc27ce0
ms.tgt_platform: multiple
title: Déchargement d’un fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123d8c4f6b9d9155cdc22dc435635466956bdb0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192199"
---
# <a name="unloading-a-provider"></a>Déchargement d’un fournisseur

Une fois WMI terminé avec un fournisseur, le fournisseur est déchargé de la mémoire. La raison principale pour laquelle WMI décharge un fournisseur est de préserver les ressources système. Par conséquent, vous devez ajouter du code qui permet à WMI de décharger votre fournisseur de manière efficace. Le déchargement d’un fournisseur se fait depuis l’intervalle spécifié dans le contrôle du cache jusqu’à deux fois l’intervalle nécessaire pour WMI.

WMI décharge un fournisseur de l’une des manières suivantes :

-   Décharger un fournisseur une fois que le fournisseur a terminé les tâches qui lui sont affectées.
-   Déchargez rapidement tous les fournisseurs lorsque l’utilisateur arrête le système. Notez que WMI décharge les fournisseurs in-process lorsque le service WMI est arrêté à partir de la ligne de commande.

Tandis que le premier scénario est plus courant, vous devez écrire votre fournisseur pour les deux possibilités.

Les sections suivantes sont présentées dans cette rubrique :

-   [Déchargement d’un fournisseur inactif](#unloading-an-idle-provider)
-   [Accès à la durée d’inactivité d’un fournisseur](#accessing-the-idle-time-for-a-provider)
-   [Déchargement d’un fournisseur qui est également un client WMI](#unloading-a-provider-that-is-also-a-wmi-client)
-   [Déchargement d’un fournisseur pendant l’arrêt](#unloading-a-provider-during-shutdown)
-   [Rubriques connexes](#related-topics)

## <a name="unloading-an-idle-provider"></a>Déchargement d’un fournisseur inactif

WMI effectue les actions suivantes lorsqu’il décharge un fournisseur inactif :

-   Détermine si le fournisseur est inactif.

    WMI utilise la propriété **ClearAfter** pour déterminer la durée pendant laquelle un fournisseur peut rester inactif avant de décharger ce fournisseur. Pour plus d’informations, consultez [accès à la durée d’inactivité d’un fournisseur](#accessing-the-idle-time-for-a-provider).

-   Appelle la méthode [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) du fournisseur.

    Si le fournisseur était un fournisseur pur, alors [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) supprime complètement le fournisseur de la mémoire active. Toutefois, un fournisseur qui n’est pas pur peut continuer à s’exécuter après l’appel de la **version** WMI.

## <a name="accessing-the-idle-time-for-a-provider"></a>Accès à la durée d’inactivité d’un fournisseur

La durée minimale pendant laquelle un fournisseur reste actif est déterminée par la propriété **ClearAfter** . Vous pouvez trouver des **ClearAfter** dans des instances de classes dérivées de la classe système WMI [**\_ \_ CacheControl**](--cachecontrol.md) dans l' \\ espace de noms racine.

La liste suivante décrit les classes qui sont dérivées de [**\_ \_ CacheControl**](--cachecontrol.md), qui contrôle le déchargement du fournisseur :

-   [**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
-   [**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
-   [**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
-   [**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
-   [**\_\_PropertyProviderCacheControl**](--propertyprovidercachecontrol.md)

Vous pouvez modifier la durée minimale pendant laquelle WMI autorise un fournisseur à rester inactif en modifiant la propriété **ClearAfter** dans l’instance de contrôle du cache pour un type de fournisseur spécifique. Par exemple, pour limiter la durée pendant laquelle un fournisseur de propriétés peut rester inactif, vous devez modifier la propriété **ClearAfter** d’une instance [**\_ \_ PropertyProviderCacheControl**](--propertyprovidercachecontrol.md) dans l' \\ espace de noms racine.

## <a name="unloading-a-provider-that-is-also-a-wmi-client"></a>Déchargement d’un fournisseur qui est également un client WMI

Il se peut que votre fournisseur doive rester un client de WMI une fois qu’il a terminé les fonctions du fournisseur, il a été appelé pour fonctionner. Par exemple, un fournisseur Push peut avoir besoin d’émettre des requêtes vers WMI. Pour plus d’informations, consultez Détermination de l' [État d’envoi ou d’extraction](determining-push-or-pull-status.md). Dans ce cas, la propriété **pure** de l’instance [**\_ \_ Win32Provider**](--win32provider.md) qui représente le fournisseur doit avoir la valeur **true**. Si la propriété **pure** a la valeur **false**, le fournisseur prépare le déchargement en appelant [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur tous les points d’interface en attente lorsque WMI appelle la méthode Release de son interface principale. Pour plus d’informations, consultez la section Notes dans [**\_ \_ Win32Provider**](--win32provider.md).

La procédure suivante décrit comment implémenter une méthode Release pour l’interface principale de votre fournisseur.

**Pour décharger un fournisseur**

1.  Libère tous les pointeurs d’interface détenues par WMI lorsque WMI appelle la méthode de [**mise**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en service de l’interface principale de votre fournisseur.

    En général, un fournisseur contient des pointeurs vers les interfaces [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) et [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) fournies dans [**IWbemProviderInit :: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize).

2.  Si la propriété **pure** de l’instance [**\_ \_ Win32Provider**](--win32provider.md) associée est définie sur **false**, le fournisseur peut passer au rôle de l’application cliente après l’appel de la [**version**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)de WMI. Toutefois, WMI ne peut pas décharger un fournisseur qui fonctionne en tant que système client, ce qui augmente la surcharge du système.

    Un fournisseur dont la propriété **pure** a la **valeur true** existe uniquement pour les demandes de service. Par conséquent, ce type de fournisseur ne peut pas assumer le rôle d’une application cliente et WMI peut le décharger.

## <a name="unloading-a-provider-during-shutdown"></a>Déchargement d’un fournisseur pendant l’arrêt

Dans des circonstances normales, l’utilisation des instructions du [déchargement d’un fournisseur qui est également un client WMI](#unloading-a-provider-that-is-also-a-wmi-client) permet à WMI de décharger correctement votre fournisseur. Toutefois, vous pouvez rencontrer des situations où WMI ne peut pas effectuer les procédures de déchargement normales, par exemple lorsque l’utilisateur choisit d’arrêter le système. En utilisant un modèle de transaction de stockage des données, en plus d’implémenter une bonne stratégie de nettoyage, vous pouvez vous assurer que votre fournisseur est correctement déchargé.

L’utilisateur peut arrêter WMI à tout moment. Dans ce cas, WMI ne décharge aucun fournisseur ou n’appelle le point d’entrée [**DllCanUnloadNow**](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) sur aucun fournisseur in-process. En outre, si un fournisseur in-process est au milieu d’un appel de méthode au moment de l’arrêt, WMI peut éventuellement terminer le thread d’exécution au milieu de l’appel. Dans ce cas, WMI n’appelle pas les routines qui gèrent normalement le nettoyage, telles qu’un destructeur d’objet. Au maximum, WMI appellera [**DllMain**](/windows/desktop/Dlls/dllmain) uniquement.

Lorsque le système d’exploitation arrête WMI, le système libère automatiquement toute la mémoire allouée à un fournisseur in-process. Le système d’exploitation ferme également la plupart des ressources détenues par le fournisseur, telles que les descripteurs de fichiers, les handles de fenêtre, etc. Le fournisseur n’a pas besoin d’effectuer une action spécifique pour que cela se produise.

Étant donné que WMI peut s’arrêter au milieu d’un appel, un fournisseur ne doit pas quitter les sources de données dans un état incohérent. Le fait de laisser vos données dans un état incohérent n’est pas un problème pour les fournisseurs en lecture seule. Toutefois, les fournisseurs avec des capacités d’écriture peuvent souhaiter implémenter un certain type de modèle de transaction pour permettre une restauration sécurisée après une fin brutale.

Alors que le système d’exploitation peut libérer des ressources système générales, le système ne libère pas automatiquement toutes les ressources. Par exemple, le système d’exploitation peut ne pas libérer un socket ou une connexion de base de données. Au lieu de cela, le fournisseur devra peut-être nettoyer manuellement ces ressources. Pour éviter ces problèmes, vous pouvez implémenter votre fournisseur hors processus ou vous pouvez ajouter un code de nettoyage.

La solution la plus simple consiste à implémenter votre fournisseur hors processus. Un fournisseur hors processus n’est pas supprimé lorsque WMI s’arrête, bien que WMI libère le fournisseur après un délai d’attente COM. Les fournisseurs pour lesquels les problèmes de robustesse de nettoyage et de terminaison sont plus importants que les performances peuvent être hors processus.

Si vous devez placer le code de nettoyage dans votre fournisseur, vous avez deux options. Un emplacement pour effectuer ce type de nettoyage est [**DllMain**](/windows/desktop/Dlls/dllmain), la fonction de point d’entrée de dll qui est appelée par le système d’exploitation lors du déchargement de la dll. Le code de nettoyage peut être ajouté directement à **DllMain**, en l’exécutant en réponse au **\_ \_ détachement du processus dll**. L’implémentation d’un code de nettoyage dans **DllMain** peut être un peu difficile à organiser, en particulier dans les environnements de programmation tels que MFC ou ATL. Pour plus d’informations, consultez l’article Q148791 de la base de connaissances Microsoft, «*comment fournir votre propre DllMain dans une DLL régulière MFC ».* (Cette ressource n’est peut-être pas disponible dans certaines langues et pays ou régions.)

Vous pouvez également placer le code de nettoyage dans le destructeur d’une classe globale. Pour plus d’informations, consultez déchargement d’un fournisseur. le système d’exploitation Windows n’alloue pas d’objets globaux sur le tas. Au lieu de cela, le système d’exploitation appelle les destructeurs pendant le déchargement de la DLL.

Voici une procédure de nettoyage simple qui peut tenir dans un objet global pour WMI.


```C++
class CMyCleanup
{
    ~CMyCleanup()
    {
        CloseHandle(m_hOpenFile);
        CloseDatabaseConnection(g_hDatabase);
    }
} g_Cleanup;
```



Il existe de nombreuses restrictions quant à ce qui peut être fait dans le code de nettoyage avec l’une ou l’autre approche. Par exemple, ni les threads, ni les dll qui ne sont pas implicitement liés ne sont accessibles de quelque manière que ce soit. En outre, vous ne pouvez pas effectuer d’appels COM dans toutes les circonstances.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition des descripteurs de sécurité espace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Sécurisation de votre fournisseur](securing-your-provider.md)
</dt> <dt>

[Développement d’un fournisseur WMI](developing-a-wmi-provider.md)
</dt> </dl>

 

 
