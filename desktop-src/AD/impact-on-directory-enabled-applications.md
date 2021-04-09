---
title: Impact sur les applications Directory-Enabled
description: Cette rubrique décrit l’impact sur les applications prenant en charge les applications d’annuaire lorsque des décalages de version, des mises à jour partielles ou des collisions se produisent.
ms.assetid: 0aec6fe3-7757-4472-bc18-add2327d4e1b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061818fc791e1c75d440d0c477a321b8c4e5edfb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103940813"
---
# <a name="impact-on-directory-enabled-applications"></a>Impact sur les applications Directory-Enabled

## <a name="version-skew"></a>Décalage de version

La distorsion de version se produit lorsque les applications lisent les mêmes objets de différents réplicas avant qu’une modification n’ait été répliquée. Les applications qui lisent le réplica distant reconnaissent l’objet inchangé. La différence de version est un problème lorsqu’une application ou un ensemble d’applications donné utilise les données de l’annuaire pour interagir.

Par exemple, un service RPC peut publier ses points de terminaison dans l’annuaire à l’aide d’API RPC standard (telles que [**RpcNsBindingExport**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta)). Les clients se connectent au service en recherchant le point de terminaison souhaité dans le répertoire ( [**RpcNsBindingLookupBegin**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), [**RpcNsBindingLookupNext**](/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext), etc.) et en les liant.

Supposons qu’un service RPC ₁ publie des points de terminaison ₁ et qu’il se déplace ensuite vers un autre ordinateur. Le point de terminaison d’origine ₁ est remplacé par E<sub>S2,</sub> reflétant l’adresse du nouvel ordinateur. Les clients lisant les réplicas distants du service d’annuaire ne peuvent pas se connecter au service tant que le point de terminaison mis à jour n’est pas répliqué. Toutefois, le déplacement d’un service d’un ordinateur à un autre est une occurrence rare. par conséquent, cette interruption/ce délai doit rarement être rencontré, en particulier si le déplacement du service est bien planifié.

## <a name="partial-updates"></a>Mises à jour partielles

En général, une mise à jour partielle se produit lorsqu’une application lit un jeu de données alors qu’une autre application écrit dans ce même jeu de données. Il s’agit d’une situation qui peut se produire avec n’importe quelle application dans un système multimaître. Cela peut se produire de nombreuses façons. Vous pouvez avoir plusieurs applications qui écrivent dans le même jeu de données à la fois. Si vous l’examinez de cette façon, le service de réplication d’annuaire est une autre application qui pourrait potentiellement écrire dans le même jeu de données que celui qu’une autre application peut lire. Il peut s’agir d’un problème potentiel pour une application. Toutefois, la fenêtre de temps pendant laquelle une mise à jour partielle peut affecter votre application est relativement petite. Cela devrait rarement s’avérer un problème pour les applications qui ne dépendent pas de la synchronisation de plusieurs objets. Si votre application dépend fortement de la synchronisation d’un ensemble d’objets associé, vous devez prendre en compte les effets d’une mise à jour partielle dans la conception de votre application.

En termes de réplication de répertoires, une mise à jour partielle se produit lorsque les applications lisent le même ensemble d’objets à partir de réplicas différents alors que la réplication est en cours. Les applications au niveau du réplica distant voient certaines des modifications, mais pas toutes.

> [!Note]  
> La fenêtre dans laquelle la mise à jour partielle peut affecter une application est petite : l’application doit commencer à lire des objets pendant que la réplication entrante est en cours, après la réception d’un ou plusieurs objets modifiés associés, mais avant la réception de tous les objets. Le délai entre les mises à jour au niveau du réplica source affecte directement la taille de cette fenêtre : les mises à jour qui se produisent de façon rapprochée dans le temps sont répliquées de façon rapprochée dans le temps. Une mise à jour partielle peut être un problème lorsqu’une application utilise un ensemble d’objets associé.

 

Par exemple, un service d’accès à distance peut utiliser l’annuaire pour stocker des données de stratégie et de profil. Les données de stratégie sont stockées dans un ensemble d’objets et le profil dans un autre jeu. Lorsqu’un utilisateur se connecte au service d’accès à distance, le service d’accès à distance lit la stratégie pour déterminer si l’utilisateur est autorisé à se connecter et, le cas échéant, quel profil appliquer à la session utilisateur. La mise à jour partielle peut affecter le service d’accès à distance de plusieurs façons :

-   Si la stratégie est complexe et se compose de plusieurs objets, le service d’accès à distance peut lire une stratégie partiellement mise à jour, ce qui entraîne un refus incorrect ou l’octroi de service à l’utilisateur, l’impossibilité de traiter la stratégie en raison d’une incohérence interne, et ainsi de suite.
-   Si la stratégie et les profils ont été mis à jour, le service peut traiter correctement la stratégie, mais appliquer un profil obsolète, car les objets de stratégie ont été répliqués, mais pas les objets de profil.
-   Si le profil est complexe et se compose de plusieurs objets, le service peut traiter correctement la stratégie, mais appliquer un profil partiellement mis à jour, car les objets de stratégie ont été répliqués, mais seuls certains objets de profil l’ont fait.

## <a name="collisions"></a>Collisions

Des collisions se produisent lorsque les mêmes attributs d’au moins deux réplicas d’un objet donné sont modifiés au cours du même intervalle de réplication. Le processus de réplication rapproche la collision ; en raison de la réconciliation, un utilisateur ou une application peut « voir » une valeur différente de celle qu’il a écrite.

Voici un exemple simple d’informations sur l’adresse de l’utilisateur : un utilisateur modifie une adresse postale sur le réplica R1 et un administrateur modifie la même adresse postale sur le réplica R2. Une valeur écrite se propage jusqu’à ce qu’une autre valeur soit sélectionnée sur cette valeur par le mécanisme de réconciliation des collisions. Tant qu’une valeur continue à « gagner » par rapport à d’autres valeurs dans le processus de résolution des collisions, la valeur continue à se propager. Enfin, cette valeur « gagnante » sera propagée vers R1, R2 et tous les autres réplicas si aucune autre modification n’est apportée.

La résolution des collisions est un problème pour les applications qui font des hypothèses sur la cohérence interne des objets ou des ensembles d’objets. Par exemple, un service de gestion de l’allocation de bande passante réseau stocke les données de bande passante réseau pour un segment de réseau donné dans l’annuaire d’un objet O1. L’objet contient la bande passante disponible en bits par seconde et la bande passante maximale qu’un utilisateur unique peut réserver. Le service s’attend à ce que la bande passante réservable par l’utilisateur soit toujours inférieure ou égale à la bande passante disponible.

Regardez la séquence d’événements suivante :

-   L’objet dans l’état de réplication complète initial donne la bande passante disponible en tant que 56 kilobits par seconde, et la bande passante réservable par l’utilisateur en tant que 9 600 bits par seconde.
-   Un administrateur sur le réplica R ₁ remplace les valeurs respectivement par 64 Ko et 19 200.
-   Un administrateur sur le réplica R ₂ modifie les valeurs en 10 millions et 1 million respectivement avant l’arrivée de la mise à jour de R ₁.

En supposant que les attributs en question ont des numéros de version identiques lorsque les mises à jour se produisent, il existe une petite possibilité, mais réelle, que l’objet se termine avec une bande passante maximale de 64 Ko et un nombre maximal de 1 million d’utilisateurs pouvant être réservés, si l’application effectue les mises à jour en tant qu’opérations d’écriture distinctes. L’application doit toujours mettre à jour les deux propriétés en une seule opération.

 

 