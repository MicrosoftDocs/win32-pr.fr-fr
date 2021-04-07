---
title: Catégories de composants et fonctionnement
description: Catégories de composants et fonctionnement
ms.assetid: efbf4a25-3c73-4d09-a172-6676c6d6501b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf8065584ae2dc83e470428b7345eb2d9321d32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939658"
---
# <a name="component-categories-and-how-they-work"></a>Catégories de composants et fonctionnement

Les catégories de composants identifient les zones de fonctionnalités prises en charge et requises par un composant logiciel, une entrée de Registre est utilisée pour chaque catégorie ou zone de fonctionnalités identifiée. Chaque catégorie de composant est identifiée par un identificateur global unique (GUID). lorsqu’un contrôle est installé, il s’inscrit lui-même en tant que contrôle dans le registre système à l’aide de l’ID de catégorie de composant pour le contrôle, consultez [auto-inscription pour les contrôles](self-registration-for-controls.md). Au sein de l’auto-enregistrement des contrôles, il inscrira également les catégories de composants qu’il implémente, ainsi que les catégories de composants qu’il requiert qu’un conteneur prenne en charge pour pouvoir héberger correctement le contrôle.

Lorsqu’un conteneur de contrôle offre à l’utilisateur des contrôles à insérer, il permet uniquement à l’utilisateur de sélectionner et d’instancier les contrôles qui pourront fonctionner correctement dans cet environnement. Par exemple, si le conteneur de contrôle ne prend pas en charge la liaison de liaison, le conteneur ne permet pas à l’utilisateur de sélectionner et d’instancier les contrôles qui ont une entrée dans le registre, ce qui signifie qu’ils ont besoin de la catégorie de composant DataBinding. Une boîte de dialogue commune pour l’insertion de contrôles et les API pour gérer les entrées de Registre sont disponibles.

Les catégories de composants ne sont pas cumulatives ni exclusives. un contrôle peut nécessiter une combinaison de catégories de composants pour fonctionner. Un contrôle qui n’a pas d’entrées requises pour les catégories de composants peut être supposé pouvoir fonctionner dans n’importe quel conteneur de contrôle et ne nécessite pas de fonctionnalité spécifique d’un conteneur de contrôle pour fonctionner.

Les catégories de composants suivantes sont identifiées ici, si nécessaire, des spécifications plus détaillées des catégories peuvent être disponibles.

-   Relation contenant-contenu de contrôle [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) .
-   Liaison de liaison simple via l’interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) .
-   Liaison de liaison avancée (prise en charge par les interfaces DataBinding supplémentaires de VB 4.0).
-   Interfaces privées Visual Basices- [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat), [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol)
-   Contrôles prenant en charge Internet.
-   Contrôles sans fenêtre.

Il ne s’agit pas d’une liste définitive des catégories ; d’autres catégories sont susceptibles d’être définies à l’avenir à mesure que de nouvelles spécifications sont identifiées. Une liste à jour des catégories de composants est disponible auprès de Microsoft. Cette liste reflète les catégories de composants qui ont été identifiées par Microsoft et d’autres qui concernent les fournisseurs qui ont informé Microsoft.

Il est important de se souvenir que les contrôles doivent tenter de travailler dans autant d’environnements que possible. Si possible, le contrôle doit dégrader ses fonctionnalités lorsqu’il est placé dans un conteneur qui ne prend pas en charge certaines interfaces. L’objectif des catégories de composants est d’empêcher une situation où le contrôle est placé dans un environnement inapproprié et le contrôle ne peut pas accomplir sa tâche souhaitée. En règle générale, un contrôle doit se dégrader de manière appropriée lorsque les interfaces ne sont pas présentes, un contrôle peut choisir d’indiquer à l’utilisateur une boîte de message indiquant que certaines fonctionnalités ne sont pas disponibles ou de documenter clairement les fonctionnalités requises d’un conteneur de contrôle pour des performances optimales.

Notez que les contrôles et les conteneurs plus anciens n’utilisent pas les catégories de composants et s’appuient plutôt sur le mot clé de contrôle présent sur le contrôle dans le registre. Pour être reconnu par les anciens contrôles Container qui peuvent souhaiter inscrire le mot clé Control dans le registre, les développeurs de contrôles doivent vérifier que le contrôle peut être hébergé correctement dans ces conteneurs avant de procéder ainsi. Les conteneurs qui utilisent des catégories de composants peuvent correctement les utiliser pour héberger des contrôles plus anciens, car la DLL de catégorie de composants gère le mappage, une catégorie distincte existe pour les ControlV1 CATID de contrôles plus anciens, \_ afin qu’un conteneur puisse éventuellement les exclure si nécessaire.

Comme les catégories de composants sont identifiées par des GUID, il est possible que les conteneurs qui offrent des fonctionnalités spécifiques disposent de leurs propres ID de catégorie, générés à l’aide d’un outil de génération de GUID. Toutefois, cela peut compromettre l’avantage de l’interopérabilité des contrôles et des conteneurs, c’est pourquoi il est préférable d’utiliser chaque catégorie de composants existante. Les fournisseurs sont encouragés à consulter ensemble lorsqu’ils définissent de nouvelles catégories de composants pour s’assurer qu’ils répondent aux exigences courantes de la place de marché et suivent l’esprit de l’interopérabilité des contrôles ActiveX.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Catégories de composant](component-categories.md)
</dt> </dl>

 

 




