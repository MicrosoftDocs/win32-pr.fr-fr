---
title: Utilisation de TBS
description: Chaque commande soumise au TBS est associée à une entité spécifique. Pour ce faire, vous devez créer un ou plusieurs contextes pour une entité, qui sont ensuite associés à chaque commande suivante soumise par cette entité.
ms.assetid: 609f1e95-9868-4e34-8758-71306ac4e51f
keywords:
- TPM base services TBS, exemples
- Services de base du module de plateforme sécurisée (TPM), utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 189d047e6cf969887e390ac7dad1cfc8cdbfa4f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940013"
---
# <a name="using-tbs"></a>Utilisation de TBS

La fonctionnalité des services de base du module de plateforme sécurisée est divisée en quatre zones fonctionnelles :

-   [Virtualisation des ressources](resource-virtualization.md)
-   [Planification des commandes](command-scheduling.md)
-   [Gestion de l’alimentation](power-management.md)
-   [Blocage des commandes](command-blocking.md)

Pour vous assurer que les différentes entités ne peuvent pas accéder aux ressources de l’autre, chaque commande soumise à la TBS est associée à une entité spécifique. Pour ce faire, vous devez créer un ou plusieurs contextes pour une entité, qui sont ensuite associés à chaque commande suivante soumise par cette entité. Chaque commande comprend un objet Context, qui permet au TBS d’exécuter des commandes TPM dans le contexte approprié. Tous les objets créés par les commandes sont vidés du module de plateforme sécurisée (TPM) lorsque le contexte est fermé.

Une entité crée le contexte avant d’accéder au service TBS et de maintenir le contexte jusqu’à ce que l’exécution des accès TBS soit terminée. Par exemple, dans le cas d’un TSS, la fonctionnalité de services de base (TCS) du TSS crée un contexte TBS au démarrage, et conserve ce contexte actif jusqu’à ce qu’il s’arrête.

Pour Windows Server 2008 et Windows Vista, le service TBS restreint l’accès à l’API TBS aux comptes administrateurs, NT autorité \\ LocalService et autorité NT \\ NetworkService. Par défaut, ces comptes sont les seuls à pouvoir se connecter à TBS et à créer des contextes. Les restrictions d’accès peuvent être modifiées en créant un **accès** à la clé de Registre avec un nom de valeur de Registre String (**reg \_ SZ**) **SecurityDescriptor** <dl> <dt>

Type de données
</dt> <dd>REG_SZ</dd> </dl> under it as follows:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         TPM
            Access
               SecurityDescriptor = SecurityDescriptor
```

Exemple :

**O :BAG : BAD : (A ;; 0 x00000001;;; BA) (A ;; 0 x00000001;;; NS) (A ;; 0 x00000001;;; LS**

Par défaut, le nombre maximal de contextes pris en charge par le TBS est de 25. Ce nombre peut être modifié en créant ou en modifiant une valeur de Registre **DWORD** nommée **MaxContexts** sous **HKEY \_ local \_ machine** \\ **Software** \\ **Microsoft** \\ **TPM**. L’utilisation du contexte TBS en temps réel peut être observée à l’aide de l’outil Analyseur de performances pour suivre le nombre de contextes TBS.

Pour Windows 8, Windows Server 2012 et versions ultérieures, le TBS autorise l’accès aux utilisateurs et aux administrateurs standard. Les clés de Registre **SecurityDescriptor** et **MaxContexts** sont devenues obsolètes. Pour Windows 8, Windows Server 2012 et versions ultérieures, le TBS restreint l’accès à certaines commandes à l’aide du blocage de commande.

Pour Windows 10, la version 1607, le TBS autorise l’accès à partir des applications AppContainer. Pour chaque version de module de plateforme sécurisée, les clés **BlockedAppContainerCommands** et **AllowedW8AppContainerCommands** ont été ajoutées avec les listes de correspondance des commandes TPM bloquées et autorisées, respectivement.

Pour Windows 10, version 1803, les clés de Registre sous **AllowedW8AppContainerCommands** ne sont plus prises en charge.

 

 




