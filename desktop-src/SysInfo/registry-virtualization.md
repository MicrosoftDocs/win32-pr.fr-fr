---
description: La virtualisation du Registre est une technologie de compatibilité des applications qui permet d’effectuer des opérations d’écriture dans le Registre qui ont un impact global pour être redirigées vers des emplacements par utilisateur.
ms.assetid: dace2f65-df60-419a-8be8-ab60668e6396
title: Virtualisation du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642bda46b43fc0b4f7efa60cfcd9e2178643811f
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368540"
---
# <a name="registry-virtualization"></a>Virtualisation du Registre

*La virtualisation du Registre* est une technologie de compatibilité des applications qui permet d’effectuer des opérations d’écriture dans le Registre qui ont un impact global pour être redirigées vers des emplacements par utilisateur. Cette redirection est transparente pour les applications qui lisent ou écrivent dans le registre. il est pris en charge à partir de Windows Vista.

Cette forme de virtualisation est une technologie de compatibilité d’application temporaire. Microsoft a l’intention de la supprimer des versions ultérieures du système d’exploitation Windows à mesure que d’autres applications sont compatibles avec Windows Vista et les versions ultérieures de Windows. Par conséquent, il est important que votre application ne devienne pas dépendante du comportement de la virtualisation du Registre dans le système.

La virtualisation est destinée uniquement à assurer la compatibilité des applications existantes. les Applications conçues pour Windows Vista et les versions ultérieures de Windows ne doivent pas écrire dans des zones système sensibles, ni s’appuyer sur la virtualisation pour résoudre les problèmes. lors de la mise à jour du code existant pour qu’il s’exécute sur Windows Vista et les versions ultérieures de Windows, les développeurs doivent s’assurer que les applications stockent uniquement des données dans des emplacements par utilisateur ou dans des emplacements de% alluserprofile% qui utilisent correctement une liste de contrôle d’accès (ACL).

Pour plus d’informations sur la création d’applications conformes au contrôle de compte d’utilisateur, consultez le [Guide du développeur UAC](/previous-versions/dotnet/articles/aa480150(v=msdn.10)).

## <a name="virtualization-overview"></a>Vue d’ensemble de la virtualisation

avant Windows Vista, les applications étaient généralement exécutées par les administrateurs. Par conséquent, les applications peuvent accéder librement aux fichiers système et aux clés de registre. Si ces applications ont été exécutées par un utilisateur standard, elles échouent en raison de droits d’accès insuffisants. Windows Vista et les versions ultérieures de Windows améliorent la compatibilité des applications pour ces applications en redirigeant automatiquement ces opérations. Par exemple, les opérations du Registre dans le magasin global (**HKEY \_ local \_ machine \\ Software**) sont redirigées vers un emplacement par utilisateur au sein du profil de l’utilisateur, connu sous le nom de « *magasin virtuel* » (classes de l’utilisateur **HKEY \_ \\ <User SID> \_ \\ VirtualStore \\ \\**).

La virtualisation du Registre peut être largement classée dans les types suivants :

<dl> <dt>

<span id="Open_Registry_Virtualization"></span><span id="open_registry_virtualization"></span><span id="OPEN_REGISTRY_VIRTUALIZATION"></span>Ouvrir la virtualisation du Registre
</dt> <dd>

Si l’appelant ne dispose pas d’un accès en écriture à une clé et tente d’ouvrir la clé, la clé est ouverte avec l’accès maximal autorisé pour cet appelant.

Si l' \_ \_ \_ indicateur d’échec sans assistance de la clé Reg \_ est défini pour la clé, l’opération échoue et la clé n’est pas ouverte. Pour plus d’informations, consultez « contrôle de la virtualisation du registre » plus loin dans cette rubrique.

</dd> <dt>

<span id="Write_Registry_Virtualization"></span><span id="write_registry_virtualization"></span><span id="WRITE_REGISTRY_VIRTUALIZATION"></span>Écrire la virtualisation du Registre
</dt> <dd>

Si l’appelant ne dispose pas d’un accès en écriture à une clé et tente d’y écrire une valeur ou de créer une sous-clé, la valeur est écrite dans le magasin virtuel.

Par exemple, si un utilisateur limité tente d’écrire une valeur dans la clé suivante : **HKEY \_ local \_ machine \\ Software** \\ *AppKey1*, Virtualization redirige l’opération d’écriture vers les **classes de HKEY \_ Users \\ <User SID> \_ \\ VirtualStore \\ machine \\** \\ *AppKey1*.

</dd> <dt>

<span id="Read_Registry_Virtualization"></span><span id="read_registry_virtualization"></span><span id="READ_REGISTRY_VIRTUALIZATION"></span>Lire la virtualisation du Registre
</dt> <dd>

Si l’appelant lit à partir d’une clé virtualisée, le registre présente une vue fusionnée des valeurs virtualisées (à partir du magasin virtuel) et des valeurs non virtuelles (du magasin global) à l’appelant.

Par exemple, supposons que **HKEY \_ local \_ machine \\ Software** \\ *AppKey1* contient deux valeurs v1 et v2 et qu’un utilisateur limité écrit une valeur de v3 sur la clé. Lorsque l’utilisateur tente de lire des valeurs à partir de cette clé, la vue fusionnée comprend les valeurs v1 et V2 du magasin global et la valeur v3 du magasin virtuel.

Notez que les valeurs virtuelles ont priorité sur les valeurs globales quand elles sont présentes. Dans l’exemple ci-dessus, même si le magasin global comportait la valeur v3 sous cette clé, la valeur v3 serait toujours renvoyée à l’appelant à partir du magasin virtuel. Si v3 devait être supprimé du magasin virtuel, v3 serait retourné à partir du magasin global. En d’autres termes, si v3 devait être supprimé des **classes de HKEY \_ Users \\ <User SID> \_ \\ VirtualStore \\ machine \\ Software** \\ *AppKey1* mais **HKEY \_ local \_ machine \\ Software** \\ *AppKey1* avait une valeur v3, cette valeur serait retournée par le magasin global.

</dd> </dl>

## <a name="registry-virtualization-scope"></a>Étendue de la virtualisation du Registre

La virtualisation du Registre est activée uniquement pour les éléments suivants :

-   processus interactifs 32 bits.
-   Clés dans **HKEY \_ local \_ machine \\ Software**.
-   Clés dans lesquelles un administrateur peut écrire. (si un administrateur ne peut pas écrire dans une clé, l’application aurait échoué sur les versions précédentes de Windows même si elle a été exécutée par un administrateur.)

La virtualisation du Registre est désactivée pour les éléments suivants :

-   processus 64 bits.
-   Processus qui ne sont pas interactifs, tels que les services.

    Notez que l’utilisation du Registre comme mécanisme de communication entre processus (IPC) entre un service (ou tout autre processus pour lequel la virtualisation n’est pas activée) et une application ne fonctionnera pas correctement si la clé est virtualisée. Par exemple, si un service antivirus met à jour ses fichiers de signature en fonction d’une valeur définie par une application, le service ne mettra jamais à jour ses fichiers de signature, car le service lit à partir du magasin global, mais l’application écrit dans le magasin virtuel.

-   Processus qui empruntent l’identité d’un utilisateur. Si un processus tente une opération en usurpant l’identité d’un utilisateur, cette opération ne sera pas virtualisée.
-   Les processus en mode noyau, tels que les pilotes.
-   Processus dont l' **requestedExecutionLevel** est spécifié dans leurs manifestes.
-   clés et sous-clés **de \_ hkey \_ local \\ machine \\ Classes software Classes**, **hkey \_ local \_ machine \\ software \\ microsoft \\ Windows** et **hkey \_ local \_ machine \\ software \\ microsoft \\ Windows NT**.

## <a name="controlling-registry-virtualization"></a>Contrôle de la virtualisation du Registre

En plus de contrôler la virtualisation au niveau de l’application à l’aide de **requestedExecutionLevel** dans le manifeste, un administrateur peut activer ou désactiver la virtualisation sur une base par clé pour les clés dans **HKEY \_ local \_ machine \\ Software**. Pour ce faire, utilisez l’option indicateurs de l’utilitaire de ligne de commande Reg.exe avec les indicateurs figurant dans le tableau suivant.



| Indicateur                         | Signification                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_échec de \_ la \_ désinstallation de la clé de Registre \_ | Cet indicateur désactive la virtualisation open Registry. Si cet indicateur est défini et qu’une opération d’ouverture échoue sur une clé pour laquelle la virtualisation est activée, le registre ne tente pas de rouvrir la clé. Si cet indicateur est désactivé, le registre tente de rouvrir la clé avec un \_ accès maximal autorisé au lieu de l’accès demandé.                                                                   |
| \_clé Reg \_ non \_ virtualiser   | Cet indicateur désactive la virtualisation du registre d’écriture. Si cet indicateur est défini et si une opération de création de clé ou de valeur définie échoue parce que l’appelant ne dispose pas des droits d’accès suffisants à la clé parente, le registre fait échouer l’opération. Si cet indicateur est désactivé, le registre tente d’écrire la clé ou la valeur dans le magasin virtuel. L’appelant doit disposer de la clé \_ Read Right sur la clé parente. |
| \_ \_ indicateur recurse de clé de Registre \_      | Si cet indicateur est défini, les indicateurs de virtualisation du Registre sont propagés à partir de la clé parente. Si cet indicateur est désactivé, les indicateurs de virtualisation du registre ne sont pas propagés. La modification de cet indicateur affecte uniquement les nouvelles clés de descendant créées après la modification de l’indicateur. Elle ne définit pas ou n’efface pas ces indicateurs pour les clés descendantes existantes.                                                                  |



 

L’exemple suivant illustre l’utilisation de l’utilitaire de ligne de commande Reg.exe avec l’option FLAGs pour interroger l’état des indicateurs de virtualisation pour une clé.

``` syntax
C:\>reg flags HKLM\Software\AppKey1 QUERY

HKEY_LOCAL_MACHINE\Software\AppKey1

        REG_KEY_DONT_VIRTUALIZE: CLEAR
        REG_KEY_DONT_SILENT_FAIL: CLEAR
        REG_KEY_RECURSE_FLAG: CLEAR

The operation completed successfully.
```

Chaque fois que l’audit est activé sur une clé qui est virtualisée, un nouvel événement d’audit de virtualisation est généré pour indiquer que la clé est virtualisée (en plus des événements d’audit habituels). Les administrateurs peuvent utiliser ces informations pour surveiller l’état de la virtualisation sur leurs systèmes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main avec le contrôle de compte d’utilisateur](/previous-versions/windows/it-pro/windows-vista/cc507861(v=technet.10))
</dt> <dt>

[Comprendre et configurer le contrôle de compte d’utilisateur](/previous-versions/windows/it-pro/windows-vista/cc709628(v=ws.10))
</dt> <dt>

[Meilleures pratiques et recommandations pour les développeurs pour les applications dans un environnement de moindre privilège](/previous-versions/dotnet/articles/aa480150(v=msdn.10))
</dt> </dl>

 

 
