---
title: RunAs
description: Configure une classe pour qu’elle s’exécute sous un compte d’utilisateur spécifique lorsqu’elle est activée par un client distant sans être écrite comme une application de service.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Valeur de Registre RunAs COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106509682"
---
# <a name="runas"></a>RunAs

Configure une classe pour qu’elle s’exécute sous un compte d’utilisateur spécifique lorsqu’elle est activée par un client distant sans être écrite comme une application de service.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a>Notes

La valeur spécifie le nom d’utilisateur et doit être au format *nom d'* utilisateur, *domaine ***\\*** nom* d’utilisateur ou de la chaîne « utilisateur interactif ». Vous pouvez également spécifier les chaînes « NT Authority \\ LocalService » (pour le service local) et « NT Authority \\ NetworkService » (pour service réseau). Vous pouvez également spécifier la chaîne « NT Authority \\ System » lorsque {*AppID \_ GUID*} fait référence à un serveur com déjà démarré ou à une entrée dans la table de classe. Toutefois, vous ne pouvez pas utiliser « NT Authority \\ System » avec un serveur com qui n’est pas déjà démarré. Le mot de passe par défaut pour « NT Authority \\ LocalService », « NT Authority \\ NetworkService » et « NT Authority \\ System » est «» (chaîne vide).

> [!Note]  
> À compter de Windows Vista, un mot de passe vide n’est plus requis pour configurer les paramètres « autorité NT \\ LocalService », « autorité NT \\ NetworkService » et « système d’autorité NT \\ ». 

 

Les classes configurées pour s’exécuter en tant qu’utilisateur particulier ne peuvent pas être inscrites sous une autre identité, donc les appels à [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) avec ce CLSID échouent, sauf si le processus a été lancé par com pour le compte d’une demande d’activation réelle.

Le nom d’utilisateur est extrait de la valeur **runas** sous la clé **AppID** de la classe. Si le nom d’utilisateur est « utilisateur interactif », le serveur est exécuté dans l’identité de l’utilisateur actuellement connecté et est connecté au bureau interactif.

Dans le cas contraire, le mot de passe est récupéré à partir d’une partie du Registre qui est disponible uniquement pour les administrateurs de l’ordinateur et sur le système. Le nom d’utilisateur et le mot de passe sont ensuite utilisés pour créer une session de connexion dans laquelle le serveur est exécuté. Lorsqu’il est lancé de cette manière, l’utilisateur s’exécute avec sa propre station de travail et sa propre station Windows et ne partage pas les handles de fenêtre, le presse-papiers ou d’autres éléments de l’interface utilisateur avec l’utilisateur interactif ou un autre utilisateur s’exécutant dans d’autres comptes d’utilisateur.

Pour établir un mot de passe pour une classe **runas** , vous devez utiliser l’outil d’administration DCOMCNFG installé dans le répertoire système.

Pour les identités **runas** utilisées par les serveurs DCOM, le compte d’utilisateur spécifié dans la valeur doit disposer des droits pour ouvrir une session en tant que tâche. Ce droit peut être ajouté à l’aide de l’outil d’administration stratégie de sécurité locale. Accédez à **stratégies locales** et ouvrez **attribution des droits utilisateur**. Sélectionnez **ouvrir une session en tant que tâche**, puis ajoutez le compte d’utilisateur.

La valeur **runas** n’est pas utilisée pour les serveurs configurés pour être exécutés en tant que services. Les services COM qui doivent s’exécuter sous une identité autre que LocalSystem doivent définir le nom d’utilisateur et le mot de passe appropriés à l’aide de l’applet du panneau de configuration des services ou des fonctions du contrôleur de service. (Pour plus d’informations sur ces fonctions, consultez [services](/windows/desktop/Services/services).)

> [!Note]  
> À compter de Microsoft Windows Server 2003, la classe AppID est lue explicitement à partir de **HKEY \_ local \_ machine \\ Software \\ classes \\ AppID**, qui, contrairement à la plupart des clés de Registre, n’est pas interchangeable avec l' **\_ \_ \\ AppID racine des classes HKEY**.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> </dl>

 

 