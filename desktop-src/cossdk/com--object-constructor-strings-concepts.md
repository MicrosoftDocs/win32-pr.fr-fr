---
description: Les chaînes de constructeur d’objet COM+ sont des chaînes d’initialisation qui sont spécifiées de manière administrative pour un composant.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Concepts des chaînes du constructeur d’objet COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950524"
---
# <a name="com-object-constructor-strings-concepts"></a>Concepts des chaînes du constructeur d’objet COM+

Les chaînes de constructeur d’objet COM+ sont des chaînes d’initialisation qui sont spécifiées de manière administrative pour un composant. Vous pouvez utiliser des chaînes de constructeur d’objet pour écrire un composant unique avec un degré de généralisation qui lui permet d’être personnalisé par la suite pour une tâche particulière. autrement dit, vous pouvez effectuer la construction d’objets paramétrables.

Par exemple, vous pouvez utiliser cette fonctionnalité pour écrire un composant qui détient une connexion ODBC générique et spécifier ultérieurement un DSN exact pour le composant de manière administrative. Si la configuration du système change, vous pouvez modifier la chaîne du constructeur en conséquence.

> [!Note]  
> Les chaînes de constructeur d’objet ne doivent pas être utilisées pour stocker des informations sensibles à la sécurité.

 

Vous pouvez utiliser des chaînes de constructeur d’objet conjointement avec le [regroupement d’objets](com--object-pooling.md) pour obtenir un degré de granularité plus élevé de la façon dont vous regroupez et réutilisez les ressources. Par exemple, vous pouvez créer plusieurs composants distincts, identiques à l’exception des chaînes de constructeur et des CLSID, pour gérer des pools distincts d’objets contenant des connexions utilisables par des groupes de clients distincts. Cela peut être utile si les connexions sont ouvertes d’une manière qui les lie à des rôles de sécurité particuliers, par exemple quand les connexions sont ouvertes avec une authentification spécifique au niveau de la base de données, ce qui les rend non réutilisables dans le cas général.

Pour ce faire, vous pouvez écrire un composant générique unique qui s’appuie sur les chaînes du constructeur de l’objet, à l’aide de [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), puis le recompiler pour produire plusieurs composants personnalisables, chacun avec un CLSID distinct. Vous pouvez ensuite personnaliser de manière administrative chaque composant pour ouvrir une connexion appropriée avec une chaîne de constructeur, les configurer pour qu’ils soient regroupés, et ils seront conservés dans des pools distincts par CLSID.

Vous pouvez spécifier une chaîne de constructeur lorsqu’un composant a été écrit spécifiquement pour reconnaître la chaîne que vous entrez. Les composants peuvent accéder à ces chaînes par programmation à l’aide de [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).

Les chaînes de constructeur sont passées au moment de la création de l’objet uniquement lorsque la construction d’objet est activée administrativement. COM+ appelle la méthode [**IObjectConstruct :: Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) qu’il implémente. Dans cette méthode, vous pouvez accéder à la chaîne du constructeur à l’aide de [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring). Les chaînes vides peuvent être des entrées valides.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mise en pool d’objets COM+](com--object-pooling.md)
</dt> <dt>

[Spécification d’une chaîne de constructeur d’objet pour un composant](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[Utilisation d’une chaîne de constructeur d’objet pour construire un composant](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



