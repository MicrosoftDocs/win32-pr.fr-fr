---
description: Considérations sur la sécurité de COM+ CRM
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Considérations sur la sécurité de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110406"
---
# <a name="com-crm-security-considerations"></a>Considérations sur la sécurité de COM+ CRM

Un fichier journal CRM peut contenir des informations sensibles qui doivent être sécurisées. Pour cette raison, si l’application serveur s’exécute sous une identité autre que l’utilisateur interactif lors de la création du fichier journal CRM, le fichier journal CRM est protégé par la sécurité pour cet utilisateur uniquement. Cette fonctionnalité est disponible uniquement sur le système de fichiers NTFS. Si l’identité de l’application serveur est modifiée par la suite, les informations de sécurité du fichier journal CRM ne sont pas automatiquement modifiées. Il peut être modifié manuellement à l’aide des outils d’administration Windows existants. L’alternative consiste simplement à supprimer le fichier journal CRM lorsqu’il est dans un état propre (ce qui est attendu après un arrêt contrôlé de l’application serveur).

En fonctionnement normal, COM+ crée le composant CRM Compensator et appelle l’interface [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) . Toutefois, un utilisateur disposant de privilèges pour créer le compensateur CRM peut appeler l’interface **ICrmCompensator** à des moments inappropriés, ce qui peut entraîner des problèmes de sécurité système. Pour vous protéger contre ces problèmes de sécurité, l’administrateur système peut utiliser la sécurité basée sur les rôles pour limiter le composant CRM Compensator aux seules identités des applications serveur dans lesquelles il s’exécute. Si le composant s’exécute dans une application de bibliothèque, cela inclut toutes les identités des applications serveur.

> [!Note]  
> À partir de Windows Server 2003, afin d’empêcher l’activation à partir de l’extérieur de l’application serveur, il est possible de garantir un système plus sécurisé en marquant le composant CRM Compensator comme privé.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



