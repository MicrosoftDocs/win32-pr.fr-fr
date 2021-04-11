---
description: Vous utilisez la sécurité basée sur les rôles pour établir une stratégie d’autorisation, en déterminant le client ou les clients à autoriser et avec quelle autorité. Vous décidez qui doit être en mesure d’effectuer les actions et d’accéder aux ressources.
ms.assetid: 8fc27fe1-e50a-44ba-a595-70b1fe463e24
title: Utilisation de rôles pour l’autorisation du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8ae748ddfec438a79e3d0440a00ed7c2f672aed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110890"
---
# <a name="using-roles-for-client-authorization"></a>Utilisation de rôles pour l’autorisation du client

Vous utilisez la sécurité basée sur les rôles pour établir une stratégie d’autorisation, en déterminant le client ou les clients à autoriser et avec quelle autorité. Vous décidez qui doit être en mesure d’effectuer les actions et d’accéder aux ressources.

Les rôles facilitent cela en agissant comme un mécanisme de contrôle d’accès appelé chaque fois qu’un utilisateur tente d’accéder à une ressource d’application. Un rôle est fondamentalement une liste d’utilisateurs (plus précisément, une catégorie symbolique d’utilisateurs qui partagent le même privilège de sécurité). Lorsque vous affectez un rôle à une ressource d’application, vous accordez l’autorisation d’accès à cette ressource à quiconque est membre de ce rôle.

Par conséquent, vous pouvez définir un privilège de sécurité très particulier en le déclarant comme rôle, puis en attribuant le rôle à des ressources spécifiques. Lorsque l’application est déployée, l’administrateur système peut remplir le rôle avec des utilisateurs et des groupes d’utilisateurs réels. Lorsque l’application est exécutée, COM+ applique la stratégie en effectuant des vérifications de rôle.

Fondamentalement, les rôles aident à protéger votre code, c’est-à-dire les méthodes qui peuvent être appelées par les clients d’une application COM+. L’appartenance à un rôle est vérifiée chaque fois qu’un client tente d’appeler une méthode exposée par un composant dans une application. Si l’appelant est dans un rôle affecté à la méthode appelée, ou à la ressource, l’appel est effectué ; dans le cas contraire, elle échoue.

## <a name="declarative-role-based-security"></a>Sécurité des Role-Based déclaratives

Avec la sécurité basée sur les rôles déclaratives, vous déclarez de façon administrative des rôles (à l’aide de l’outil d’administration Services de composants ou des fonctions d’administration) et les affectez de manière administrative aux ressources de l’application. L’emplacement et la façon dont vous définissez la sécurité déclarative déterminent où les limites de sécurité sont dessinées pour votre application. Pour plus d’informations, consultez [limites de sécurité](security-boundaries.md).

Vous pouvez affecter un rôle donné à l’application entière, à un composant particulier, à une interface particulière dans un composant ou à une méthode particulière sur une interface. Les attributions de rôles sont héritées de la chaîne naturelle d’inclusion, autrement dit, si vous assignez un rôle à un composant, il est implicitement affecté à chaque interface et méthode exposée par ce composant.

Avec la disponibilité des attributions de rôles au niveau de la méthode, vous pouvez protéger efficacement les composants et les interfaces qui n’ont pas été conçus en tenant compte de la sécurité. Toutefois, si les méthodes elles-mêmes ne sont pas sécurisables avec des attributions de rôles déclaratifs, vous devrez peut-être effectuer une vérification de rôle par programme. Il est généralement judicieux de garder à l’esprit la sécurité lorsque vous décidez comment factoriser les fonctionnalités métier par le biais de méthodes. dans le cas contraire, vous pourriez être amené à ajouter du code lié à la sécurité au cours de la dernière minute.

Pour obtenir des procédures détaillées sur la définition de la sécurité basée sur les rôles, consultez Configuration de la [sécurité des Role-Based](configuring-role-based-security.md).

## <a name="programmatic-security"></a>Sécurité par programmation

Dans certains cas, vous souhaiterez peut-être placer la logique de sécurité dans les composants tout en utilisant la sécurité basée sur les rôles. Il se peut que vous ne soyez pas en mesure de prendre en compte toutes les décisions d’accès par le biais de méthodes. Par exemple, vous pouvez avoir une ressource d’application privée, peut-être une base de données particulière, que vous voulez autoriser uniquement certains appelants d’une méthode à accéder tout en excluant d’autres. Vous pouvez également avoir une seule méthode TransferMoney et souhaiter limiter certains appelants en limitant les quantités qu’ils peuvent transférer.

Dans ce cas, vous pouvez effectuer une vérification des rôles dans le code. Une API simple est fournie, ce qui vous permet de vérifier si la sécurité est activée et si un appelant ou un utilisateur particulier se trouve dans un rôle donné. Cette fonctionnalité est disponible uniquement lorsque la sécurité basée sur les rôles est activée. Cela signifie que vous pouvez toujours tirer parti de la sécurité basée sur les rôles déclaratives là où elle suffit, puis vous pouvez l’étendre par programmation à un niveau de granularité plus fin si nécessaire.

En outre, lorsque vous utilisez la sécurité basée sur les rôles, vous disposez d’un accès par programme aux informations relatives à tous les appelants en amont dans la chaîne d’appels à votre composant. Cela s’avère particulièrement utile lorsque vous souhaitez conserver une piste d’audit détaillée.

Pour obtenir une description de la procédure de vérification des rôles dans le code et de l’accès aux informations de contexte d’un appel de sécurité, consultez [sécurité des composants de programmation](programmatic-component-security.md).

## <a name="authorization-and-authentication"></a>Autorisation et authentification

Une autorisation explicite suppose que vous êtes certain que les clients sont réellement ceux qu’ils disent. La vérification de l’identité du client est gérée séparément par un service d’authentification. Sans authentification, vous permettez aux appelants de sur le système honorer. Pour obtenir une description de l’authentification lorsqu’elle a un impact sur les applications COM+, consultez [authentification du client](client-authentication.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception efficace des rôles](designing-roles-effectively.md)
</dt> <dt>

[Limites de sécurité](security-boundaries.md)
</dt> <dt>

[Informations de contexte de l’appel de sécurité](security-call-context-information.md)
</dt> <dt>

[Propriété de contexte de sécurité](security-context-property.md)
</dt> </dl>

 

 



