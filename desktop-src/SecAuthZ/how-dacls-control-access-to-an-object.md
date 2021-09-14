---
description: Quand un thread tente d’accéder à un objet sécurisable, le système accorde ou refuse l’accès.
ms.assetid: dc98b23e-ce42-4d4a-a285-c0b7b5e2a478
title: Fonctionnement de AccessCheck
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730cc8f63e7d69bf4cb38344f5eda60861d08a9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011197"
---
# <a name="how-accesscheck-works"></a>Fonctionnement de AccessCheck

Quand un thread tente d’accéder à un objet sécurisable, le système accorde ou refuse l’accès. Si l’objet n’a pas de [*liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ), le système accorde l’accès ; dans le cas contraire, le système recherche les [entrées de Access Control](access-control-entries.md) (ACE) dans la liste DACL de l’objet qui s’appliquent au thread. Chaque entrée du contrôle d’accès dans la liste DACL de l’objet spécifie les droits d’accès autorisés ou refusés pour un [tiers de confiance](trustees.md), qui peut être un compte d’utilisateur, un compte de groupe ou une [*ouverture de session*](/windows/desktop/SecGloss/l-gly).

## <a name="dacls"></a>DACL

Le système compare le tiers de confiance de chaque ACE aux tiers de confiance identifiés dans le [jeton d’accès](access-tokens.md)du thread. Un jeton d’accès contient des [*identificateurs de sécurité*](/windows/desktop/SecGloss/s-gly) (SID) qui identifient l’utilisateur et les comptes de groupe auxquels l’utilisateur appartient. Un jeton contient également un [*SID d’ouverture*](/windows/desktop/SecGloss/l-gly) de session qui identifie la session de connexion en cours. Lors d’une vérification d’accès, le système ignore les SID de groupe qui ne sont pas activés. Pour plus d’informations sur les SID activé, désactivé et refus seul, consultez [attributs SID dans un jeton d’accès](sid-attributes-in-an-access-token.md).

En règle générale, le système utilise le [*jeton d’accès principal*](/windows/desktop/SecGloss/p-gly) du thread qui demande l’accès. Toutefois, si le thread emprunte l’identité d’un autre utilisateur, le système utilise le [*jeton d’emprunt d’identité*](/windows/desktop/SecGloss/i-gly)du thread.

Le système examine chaque entrée de contrôle d’accès dans l’ordre jusqu’à ce que l’un des événements suivants se produise :

-   Une entrée du contrôle d’accès refusé explicitement refuse l’un des [droits d’accès](access-rights-and-access-masks.md) demandés à l’un des tiers de confiance figurant dans le jeton d’accès du thread.
-   Une ou plusieurs ACE access-allowed pour les tiers de confiance figurant dans le jeton d’accès du thread accordent explicitement tous les droits d’accès demandés.
-   Toutes les entrées du contrôle d’accès ont été vérifiées et il existe toujours au moins un droit d’accès demandé qui n’a pas été explicitement autorisé. dans ce cas, l’accès est refusé implicitement.

L’illustration suivante montre comment la liste DACL d’un objet peut autoriser l’accès à un thread tout en refusant l’accès à un autre.

![liste DACL qui accorde différents droits d’accès à différents threads](images/accctrl1.png)

Pour le thread A, le système lit ACE 1 et refuse immédiatement l’accès, car l’ACE avec refus d’accès s’applique à l’utilisateur dans le jeton d’accès du thread. Dans ce cas, le système ne vérifie pas les entrées de contrôle d’intégrité 2 et 3. Pour le thread B, ACE 1 ne s’applique pas, donc le système passe à ACE 2, qui autorise l’accès en écriture et ACE 3 qui autorise l’accès en lecture et en exécution.

Étant donné que le système arrête de vérifier les entrées de contrôle d’accès lorsque l’accès demandé est accordé ou refusé de manière explicite, l’ordre des ACE dans une liste DACL est important. Notez que si l’ordre des entrées de contrôle d’accès est différent dans l’exemple, le système peut avoir accordé l’accès au thread A. Pour les objets système, le système d’exploitation définit un ordre par défaut [des entrées de commande dans une liste DACL](order-of-aces-in-a-dacl.md).

 

 
