---
title: Inscription du serveur DLL pour l’activation du remplacement
description: Inscription du serveur DLL pour l’activation du remplacement
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363583"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a>Inscription du serveur DLL pour l’activation du remplacement

Un serveur DLL est chargé dans un processus de substitution dans les conditions suivantes :

-   Il doit y avoir une valeur AppID spécifiée sous la clé CLSID dans le registre, et une clé [AppID](appid-key.md) correspondante.
-   Dans un appel d’activation, le bit du [**\_ \_ serveur local CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) est défini et la clé CLSID ne spécifie pas [LocalServer32](localserver32.md), [LocalServer](localserver.md)ou [LocalService](localservice.md). Si d’autres bits **CLSCTX** sont définis, l' [**algorithme de traitement**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)pour les indicateurs d’exécution in-process, local ou distant est suivi.
-   La clé CLSID contient la sous-clé [InprocServer32](inprocserver32.md) .
-   La DLL proxy/stub spécifiée dans la clé **InprocServer32** existe.
-   La valeur [DllSurrogate](dllsurrogate.md) existe sous la clé **AppID** .

S’il existe une valeur **LocalServer**, **LocalServer32** ou **LocalService** indiquant l’existence d’un fichier exe, le service ou le serveur exe est toujours lancé en priorité pour le chargement d’un serveur dll dans un processus de substitution.

La valeur nommée **DllSurrogate** doit être spécifiée pour que l’activation de substitution se produise. L’activation fait référence aux appels à l’une des fonctions d’activation suivantes :

-   [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

Pour lancer une instance du substitut fourni par le système, définissez la valeur de **DllSurrogate** sur une chaîne vide ou sur **null**. Pour spécifier le lancement d’un substitut personnalisé, définissez la valeur sur le chemin d’accès du substitut.

Si [RemoteServerName](remoteservername.md) et **DllSurrogate** sont tous les deux spécifiés pour le même AppID, la valeur **RemoteServerName** est ignorée et la valeur **DllSurrogate** provoque une activation sur l’ordinateur local. Pour l’activation de substitution à distance, spécifiez **RemoteServerName** mais pas **DllSurrogate** sur le client, puis spécifiez **DllSurrogate** sur le serveur.

Un serveur DLL conçu pour s’exécuter toujours seul dans son propre processus de substitution est mieux configuré avec un AppID égal à son CLSID. Sous **AppID**, il vous suffit de spécifier une valeur nommée **DllSurrogate** avec une valeur de chaîne vide.

Il est préférable de configurer un serveur de DLL conçu pour s’exécuter seul dans son propre processus de substitution et pour traiter plusieurs clients sur un réseau avec une valeur [runas](runas.md) spécifiée sous la clé de Registre **AppID** . Si le **runas** spécifie « utilisateur interactif » ou une identité d’utilisateur spécifique dépend de l’interface utilisateur, de la sécurité et de la configuration requise du serveur. Lorsqu’une valeur **runas** est spécifiée, une seule instance du serveur est chargée pour le service de tous les clients, quelle que soit l’identité du client. En revanche, ne configurez pas le serveur avec **runas** si l’intention est de faire en sorte qu’une instance du serveur dll s’exécute en substitution pour traiter chaque identité de client distant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration requise du serveur DLL](dll-server-requirements.md)
</dt> <dt>

[Partage de substitution](surrogate-sharing.md)
</dt> </dl>

 

 