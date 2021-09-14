---
description: Accès au catalogue COM+
ms.assetid: 1322a3fe-faee-4971-949f-5e0d2dfe469b
title: Accès au catalogue COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2de7c87da1744e23b384199dce68628fd77d5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013031"
---
# <a name="accessing-the-com-catalog"></a>Accès au catalogue COM+

Le catalogue COM+ est le magasin de données sous-jacent qui contient toutes les données de configuration COM+. Chaque fois que vous effectuez une administration COM+, vous lisez et écrivez des données stockées dans le catalogue. La seule façon dont vous pouvez accéder au catalogue est d’utiliser l’outil d’administration Services de composants ou la bibliothèque comadmin.

Le catalogue COM+ fournit une couche d’abstraction sur les détails réels de l’emplacement et de la façon dont les données de configuration COM+ sont stockées. La plupart des données sont stockées dans la base de données d’inscription COM+ (ou RegDB), qui contient les données de tous les composants configurés installés dans les applications COM+. Cette base de données est utilisée au moment de l’exécution de l’application pour fournir des données de configuration à COM+ afin d’activer correctement les objets dans un contexte approprié, ce qui permet aux services d’être fournis pour les objets selon leur configuration. Le RegDB lui-même est un gestionnaire de ressources transactionnelles qui utilise des transactions DTC via le [Gestionnaire de ressources de compensation](com--compensating-resource-manager.md). Lorsque vous apportez des modifications de configuration persistantes, elles sont validées de façon transactionnelle. La seule façon d’accéder à RegDB est d’utiliser le catalogue COM+, à l’aide des objets comadmin ou de l’outil d’administration Services de composants.

Sur chaque ordinateur, un serveur de catalogue COM+ s’exécute en tant que composant dans l’application système. Le serveur de catalogue contrôle l’accès aux données de catalogue stockées sur son ordinateur. en effet, le serveur de catalogue est un moteur de requête qui vous permet de lire et d’écrire des données dans le catalogue de cet ordinateur. Lorsque vous lancez l’administration par programme en instanciant un objet [**COMAdminCatalog**](comadmincatalog.md) , cet objet ouvre une session avec le serveur de catalogue local. Les demandes de regroupements ou d’éléments de collection sur le catalogue local sont gérées par le serveur de catalogue local. Lorsque vous vous connectez à un ordinateur distant, vous communiquez avec le serveur de catalogue sur cet ordinateur.

## <a name="security-considerations-in-administration"></a>Considérations relatives à la sécurité dans l’administration

Pour modifier des données sur le catalogue COM+, vous devez disposer de l’autorité en tant qu’administrateur. Pour utiliser l’outil d’administration Services de composants afin de modifier les données de configuration, vous devez être membre du rôle Administrateurs affecté à l’application système sur l’ordinateur que vous essayez d’administrer. De même, pour modifier des données à l’aide des objets comadmin, votre code doit être exécuté avec l’autorité administrateur. Autrement dit, une application ou un script utilisant les objets comadmin doit s’exécuter sous un compte d’utilisateur qui est affecté au rôle Administrateurs sur l’application système sur l’ordinateur qu’il tente d’administrer. L’application peut accéder et modifier les informations du catalogue uniquement dans la mesure où le compte sous lequel elle s’exécute dispose de cette autorité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vue d’ensemble des objets comadmin](overview-of-the-comadmin-objects.md)
</dt> <dt>

[Description Résumé des classes comadmin](summary-description-of-the-comadmin-classes.md)
</dt> </dl>

 

 



