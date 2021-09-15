---
description: La partie la plus problématique de l’écriture des composants est le traitement des erreurs possibles.
ms.assetid: 12f41eef-9953-4125-8490-07ff64967f95
title: Gestion des erreurs dans COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1979fc49ff8f14bb83b194be7e1787feaf7d86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519320"
---
# <a name="handling-errors-in-com"></a>Gestion des erreurs dans COM+

La partie la plus problématique de l’écriture des composants est le traitement des erreurs possibles. Essayer de déterminer ce qui peut être incorrect et ce qu’il convient de faire peut être difficile dans les meilleures conditions. Les erreurs courantes que votre composant peut vérifier et gérer sont les échecs de connexion réseau, les erreurs de sécurité et les échecs associés à des objets inaccessibles.

En outre, vous pouvez développer vos propres codes d’erreur pour signaler des erreurs spécifiques à l’interface, par exemple lorsqu’une règle d’entreprise a été violée.

Dans le cadre du modèle de programmation COM+, un objet peut (et souvent) appeler des méthodes d’interface sur d’autres objets pour effectuer le travail. Étant donné que les programmeurs peuvent écrire des composants dans différents langages de programmation, COM+ exige que tous les mécanismes de gestion des erreurs soient indépendants du langage, par exemple : les collections HRESULT et [**errorInfo**](errorinfo.md) .

Cette section comprend des rubriques, décrites dans le tableau suivant, qui traitent des techniques de gestion des erreurs dans les applications COM+, des fonctionnalités de COM+ qui affectent le comportement d’échec et des suggestions pour le diagnostic des erreurs COM+.



| Rubrique                                                                                           | Description                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Stratégies de gestion des erreurs dans COM+](strategies-for-handling-errors-in-com-.md)<br/> | Répertorie et décrit les recommandations de base pour la gestion des erreurs dans COM+, y compris quand utiliser les collections HRESULTs et [**errorInfo**](errorinfo.md) .<br/> |
| [Modification des valeurs de retour par COM+](how-com--modifies-return-values.md)<br/>               | Identifie la condition unique dans laquelle COM+ convertit un HRESULT standard en code d’erreur COM+ avant de le renvoyer à l’appelant.<br/>             |
| [Isolation des erreurs et stratégie FailFast](fault-isolation-and-failfast-policy.md)<br/>       | Montre comment l’isolation des erreurs et la stratégie FailFast affectent le comportement de COM+.<br/>                                                                          |
| [Recherche de la source d’une erreur](finding-the-source-of-an-error.md)<br/>                 | Décrit comment vous pouvez diagnostiquer la source et obtenir une description des erreurs d’application. <br/>                                                       |
| [Interprétation des codes d’erreur](interpreting-error-codes.md)<br/>                             | identifie le mécanisme de gestion des erreurs prédominant pour Microsoft Visual C++, le langage Java et Microsoft Visual Basic. <br/>                    |
| [Dépannage](troubleshooting.md)<br/>                                               | Fournit une assistance supplémentaire pour diagnostiquer les erreurs.<br/>                                                                                             |
| [Contacter le support technique](contacting-support.md)<br/>                                         | Identifie les informations importantes de résolution des problèmes que vous devez fournir lorsque vous contactez le support technique.<br/>                                                     |



 

Pour plus d’informations sur la gestion des erreurs associées à différents services COM+, consultez les sections suivantes :

-   [Accélération des transactions en avertissant l’objet racine](speeding-transactions-by-notifying-the-root-object.md)
-   [Gestion des erreurs](handling-errors-in-queued-components.md) (pour les composants en file d’attente)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Débogage des applications COM+](debugging-com--applications.md)
</dt> </dl>

 

 




