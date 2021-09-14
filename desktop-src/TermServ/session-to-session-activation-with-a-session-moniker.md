---
title: Activation de session à session avec un moniker de session
description: L’activation de session à session (également appelée activation inter-sessions) permet à un processus client de démarrer (activer) un processus serveur local sur une session spécifiée.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324486"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a>Activation de session à session avec un moniker de session

L’activation de session à session (également appelée activation inter-sessions) permet à un processus client de démarrer (activer) un processus serveur local sur une session spécifiée. Cette fonctionnalité est disponible pour les applications qui sont configurées pour s’exécuter dans le contexte de sécurité de l’utilisateur interactif, également appelé mode d’activation d’objet « RunAs interactive User ». Pour plus d’informations sur les contextes de sécurité, consultez [le contexte de sécurité du client](/windows/desktop/SecAuthZ/the-client-security-context).

DCOM (Distributed COM) permet l’activation d’objets pour chaque session à l’aide d’un [moniker de session](session-monikers.md)fourni par le système. D’autres monikers fournis par le système incluent les [monikers de fichiers](../com/file-monikers.md), les [monikers d’élément](../com/item-monikers.md), les [monikers composites](../com/composite-monikers.md)génériques, les [anti-monikers](../com/anti-monikers.md), les [monikers de pointeur](../com/pointer-monikers.md)et les [monikers d’URL](../com/url-monikers.md).

Pour pouvoir utiliser le moniker de session, l’application DCOM doit être configurée pour s’exécuter en tant qu’utilisateur interactif. Cela peut être défini à l’aide de l’outil d’administration Services de composants, en affichant les propriétés de l’application DCOM et en sélectionnant **l’utilisateur interactif** sous l’onglet **identité** . Pour plus d’informations sur les risques de sécurité possibles associés à la configuration d’une application DCOM pour qu’elle s’exécute en tant qu’utilisateur interactif dans un environnement de Services Bureau à distance, consultez la section « identité de l’application (COM) » de la documentation COM dans le kit de développement logiciel (SDK) de la plateforme.

Si un autre type d’utilisateur est sélectionné pour exécuter l’application, le moniker de session sera ignoré par l’application. Le moniker de session est également ignoré par les applications serveur COM+. Pour plus d’informations sur les autres méthodes permettant de sélectionner le type d’utilisateur pour l’exécution de l’application, consultez la documentation COM dans le kit de développement logiciel (SDK) de plateforme.

Pour créer un moniker de session, vous devez composer l’ID de session de la session Services Bureau à distance avec un moniker de classe qui spécifie l’ID de classe du serveur de traitement.

**Pour créer un moniker de session**

1.  Préfixez le nom d’affichage du moniker de la classe avec le nom complet du moniker de session à l’aide de la syntaxe suivante :

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    où *digits* représente l’ID de session de la session sur laquelle le processus serveur sera démarré, et où *Class ID* représente l’ID de classe du serveur. Notez que l’ID de session est un nombre en base 10.

    pour les ordinateurs qui exécutent Windows XP ou version ultérieure, l’utilisation de la syntaxe suivante entraîne l’envoi par COM de l’activation à la session de console physique active, quel que soit son ID de session :

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  Une fois que vous avez créé le moniker de session, vous pouvez passer le résultat à la fonction [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) ou à la fonction [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) .

Vous pouvez utiliser un moniker de session de la même façon que vous le feriez pour tout autre moniker.

Pour obtenir un exemple de code qui montre comment activer un processus serveur local sur une session spécifiée, consultez [utilisation d’un moniker de session](using-a-session-moniker.md).

Pour plus d’informations sur l’activation d’objets, les monikers fournis par le système et les monikers de classe, consultez la documentation COM dans le kit de développement Platform SDK.

> [!Note]  
> Les processus créés entre les sessions ont une limite supérieure de la taille du bloc d’environnement. Cette limite est d’environ 4 Ko, mais elle peut être plus grande ou plus petite selon les autres informations nécessaires pour créer le processus (par exemple, les noms de fichiers, les répertoires et les paramètres pour le nouveau processus).

 

 

 