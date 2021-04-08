---
title: LocalService
description: Installe un objet en tant qu’application de service.
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- Valeur de Registre LocalService COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842794"
---
# <a name="localservice"></a>LocalService

Installe un objet en tant qu’application de service.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a>Notes

En plus de s’exécuter en tant qu’exécutable de serveur local (EXE), un objet COM peut également choisir de s’empaqueter pour s’exécuter en tant qu’application de service lorsqu’il est activé par un client local ou distant. Les services prennent en charge de nombreuses fonctionnalités d’administration utiles et intégrées à l’interface utilisateur, notamment le démarrage, l’arrêt, l’interruption et le redémarrage locaux et distants, ainsi que la possibilité d’établir le serveur pour qu’il s’exécute sous un compte d’utilisateur et une station Windows spécifiques.

Un objet écrit en tant que service est installé pour une utilisation par COM en établissant une valeur **LocalService** et en effectuant une installation de service standard. La valeur **LocalService** doit être définie sur le nom du service, tel que configuré dans **HKEY \_ local \_ machine \\ System \\ CurrentControlSet \\ services**, en tant que valeur par défaut de **reg \_ SZ** .

Lorsque **LocalService** est défini, toute chaîne assignée à [**ServiceParameters**](serviceparameters.md) est passée comme argument de ligne de commande au service lors de son lancement.

La configuration du service est préférable dans de nombreux cas où les fonctionnalités des API de gestion des services locale et distante et de l’interface utilisateur peuvent être utiles pour les services fournis par l’objet. Par exemple, l’utilisation de l’infrastructure administrative existante de l’architecture de service doit être un choix évident si l’objet est de longue durée ou prend en charge des concepts tels que le démarrage, l’arrêt, la réinitialisation ou la suspension.

Les services peuvent être configurés de manière dynamique et peuvent être configurés pour s’exécuter automatiquement lors du démarrage de l’ordinateur, ou pour être lancés à la demande d’une application cliente.

Si vous implémentez des classes en tant que services, vous devez être conscient des points suivants :

-   Cette valeur est utilisée par préférence à la clé [**LocalServer32**](localserver32.md) pour l’activation locale et à distance requestsâ. Si **LocalService** existe et qu’il fait référence à un service valide, la clé **LocalServer32** est ignorée.
-   Actuellement, une seule instance d’une application de service peut s’exécuter à un moment donné sur un ordinateur. Les services COM doivent donc inscrire leurs objets de classe au lancement à l’aide \_ de REGCLS MULTIPLEUSE pour prendre en charge plusieurs clients.
-   Pour lancer et initialiser correctement, les services COM configurés pour s’exécuter automatiquement lorsqu’un ordinateur démarre doivent inclure RPCSS dans leur liste de services dépendants.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> <dt>

[**ServiceParameters**](serviceparameters.md)
</dt> <dt>

[Services](/windows/desktop/Services/services)
</dt> </dl>

 

 