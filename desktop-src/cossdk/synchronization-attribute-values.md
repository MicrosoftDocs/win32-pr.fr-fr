---
description: L’attribut de synchronisation est une propriété déclarative qui spécifie le type de synchronisation que vous souhaitez attribuer à vos composants lorsqu’ils sont activés.
ms.assetid: 7f044ee5-b99e-4f0c-a680-b1e2672949fc
title: Valeurs d’attribut de synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7867dec9e6494c3e6e3d864e8841785f6c4fac96b2bb54ead0f24b0cbe7ea6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636889"
---
# <a name="synchronization-attribute-values"></a>Valeurs d’attribut de synchronisation

L’attribut de synchronisation est une propriété déclarative qui spécifie le type de synchronisation que vous souhaitez attribuer à vos composants lorsqu’ils sont activés. Lorsque vous incluez l’attribut de synchronisation, COM+ gère les détails de la synchronisation en votre nom ; vous n’avez pas besoin d’effectuer d’autres appels.

En fonction de ses exigences, un objet peut partager la synchronisation de son appelant, exiger une nouvelle synchronisation ou fonctionner sans synchronisation.

COM+ fournit les valeurs d’attribut de synchronisation suivantes :

-   **Désactivé.** Lorsque vous désactivez l’attribut de synchronisation, COM+ ignore les exigences de synchronisation du composant en déterminant le contexte de l’objet. Par conséquent, l’objet peut ou ne peut pas partager le contexte (et la synchronisation) de son appelant.

    En général, vous devez utiliser cette valeur d’attribut lorsque vous savez que le composant n’accède jamais à un gestionnaire de ressources. Lors de la migration de composants COM vers COM+, vous devez désactiver l’attribut de synchronisation pour conserver le même comportement que le composant COM non configuré. Un composant non configuré est un composant COM qui n’a pas été installé dans une application COM+.

-   **Non pris en charge.** Un objet avec cette valeur ne participe jamais à la synchronisation, et ce quel que soit l’état de son appelant. Ce paramètre est disponible uniquement pour les composants qui ne sont pas transactionnels et qui n’utilisent pas le service [d’activation juste-à-temps (JIT) com+](com--just-in-time-activation.md) .

-   **Pris en charge.** Un objet avec cette valeur participe à la synchronisation, le cas échéant. Vous déclarez cette valeur lorsque vous souhaitez qu’un objet partage dans la synchronisation de son appelant, mais ne nécessite pas de synchronisation propre.

    Une bonne raison de définir votre attribut de synchronisation sur pris en charge est que ce paramètre peut être moins onéreux en termes de ressources système. Toutefois, il est plus difficile d’écrire votre composant en raison de la nécessité de le protéger contre les appels simultanés. L’implication de la définition de l’attribut de synchronisation sur pris en charge est que, dans certains cas, une instance de votre objet peut être créée de façon à ce qu’elle ne soit pas synchronisée. Si le modèle de thread du composant est libre ou les deux, vous devez protéger les données de votre instance avec un certain type de mécanisme de verrouillage. Si le modèle de thread est cloisonné (STA), vous n’aurez pas besoin de protéger les données de votre instance.

-   **Obligatoire.** Lorsque vous définissez cet attribut, COM+ garantit que tous les objets créés à partir du composant seront synchronisés. En fait, chaque fois que COM+ crée une instance de votre composant, il n’y a qu’un seul thread à la fois.

    Lorsque COM+ active un objet, il examine l’état de synchronisation de son appelant. Si l’appelant est synchronisé, COM+ transmet la limite de synchronisation de l’appelant pour inclure le nouvel objet. Dans le cas contraire, COM+ commence la synchronisation.

-   **Nécessite New.** Un objet avec cette valeur doit participer à une nouvelle synchronisation, où COM+ gère les contextes et les cloisonnements pour le compte de tous les composants impliqués dans l’appel. COM+ lance automatiquement une nouvelle synchronisation, qui est différente de la synchronisation de l’appelant.

    Une bonne raison de définir votre attribut de synchronisation sur requiert New est que ce paramètre vous permet d’effectuer plus efficacement des appels externes à une instance de votre composant. Toutefois, elle effectue également des appels entre votre objet et l’objet qui l’a créé plus cher en termes de ressources système.

    Par exemple, supposons que votre objet et son objet créateur partagent les mêmes limites de synchronisation. Si le client A appelle l’objet créateur et que le client B appelle votre objet, le deuxième appel devra attendre la fin du premier appel. Si vous définissez requires New, votre objet est créé dans une limite de synchronisation distincte. Dans ce cas, les appels d’autres objets peuvent être traités en même temps. Toutefois, les appels de l’objet créateur à votre objet nécessitent davantage de ressources système, car ils doivent franchir les limites de synchronisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de l’attribut de synchronisation](setting-the-synchronization-attribute.md)
</dt> <dt>

[Dépendances de synchronisation](synchronization-dependencies.md)
</dt> </dl>

 

 



