---
description: Cette rubrique explique comment implémenter une DLL pour un filtre DirectShow, à l’aide des classes de base DirectShow.
ms.assetid: d47980d1-6d0c-4b0d-a875-7b072562944a
title: Fabriques de classes et modèles de fabrique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02699a8ff0740ddcf1d86b8514fd45dac9e32ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104553192"
---
# <a name="class-factories-and-factory-templates"></a>Fabriques de classes et modèles de fabrique

Cette rubrique explique comment implémenter une DLL pour un filtre DirectShow, à l’aide des [classes de base DirectShow](directshow-base-classes.md).

Avant qu’un client crée une instance d’un objet COM, il crée une instance de la fabrique de classe de l’objet, à l’aide d’un appel à la fonction [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) . Le client appelle ensuite la méthode **IClassFactory :: CreateInstance** de la fabrique de classes. Il s’agit de la fabrique de classes qui crée réellement le composant et retourne un pointeur vers l’interface demandée. (La fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) combine ces étapes, à l’intérieur de l’appel de fonction.)

L’illustration suivante montre la séquence d’appels de méthode.

![appels de méthode pour créer une fabrique de classes](images/classfactory.png)

[**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) appelle la fonction [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) , qui est définie dans la dll. Cette fonction crée la fabrique de classe et retourne un pointeur vers une interface de la fabrique de classe. DirectShow implémente **DllGetClassObject** pour vous, mais la fonction s’appuie sur votre code d’une façon spécifique. Pour comprendre comment cela fonctionne, vous devez comprendre comment DirectShow implémente les fabriques de classes.

Une fabrique de classe est un objet COM dédié à la création d’un autre objet COM. Chaque fabrique de classe a un type d’objet qu’il crée. Dans DirectShow, chaque fabrique de classes est une instance de la même classe C++, **CClassFactory**. Les fabriques de classes sont spécialisées au moyen d’une autre classe, [**CFactoryTemplate**](cfactorytemplate.md), également appelée *modèle de fabrique*. Chaque fabrique de classe contient un pointeur vers un modèle de fabrique. Le modèle de fabrique contient des informations sur un composant spécifique, telles que l’identificateur de classe (CLSID) du composant, et un pointeur vers une fonction qui crée le composant.

La DLL déclare un tableau global de modèles de fabrique, un pour chaque composant dans la DLL. Quand [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) crée une nouvelle fabrique de classes, il recherche un modèle avec un CLSID correspondant dans le tableau. En supposant qu’il en trouve un, il crée une fabrique de classe qui contient un pointeur vers le modèle correspondant. Lorsque le client appelle **IClassFactory :: CreateInstance**, la fabrique de classe appelle la fonction d’instanciation définie dans le modèle.

L’illustration suivante montre la séquence d’appels de méthode.

![modèles de fabrique de classes dans une dll](images/classfactory2.png)

L’avantage de cette architecture est que vous pouvez définir uniquement quelques éléments spécifiques à votre composant, tels que la fonction d’instanciation, sans implémenter l’ensemble de la fabrique de classes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment créer une DLL de filtre DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
