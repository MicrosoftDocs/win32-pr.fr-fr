---
description: Cette page répertorie certaines des tâches de programmation couramment effectuées avec l’API de document XPS.
ms.assetid: ced2098f-5462-40d7-a728-4e53f7f41003
title: Tâches courantes de programmation de documents XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7f71614344968bcc68e658021e1f34296a595d9fbf58be2d544c03c3dc428f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846349"
---
# <a name="common-xps-document-programming-tasks"></a>Tâches courantes de programmation de documents XPS

Cette page répertorie certaines des tâches de programmation couramment effectuées avec l’API de document XPS.

## <a name="common-xps-document-tasks"></a>Tâches courantes relatives aux documents XPS

Les exemples de code suivants illustrent certaines des tâches de programmation qui sont couramment exécutées lorsque l’API de document XPS est utilisée pour travailler avec un modèle d’objet XPS.

<dl>

[Initialiser un modèle d’objet XPS](xps-object-model-initialization.md)  
[Créer un modèle d’objet XPS vide](create-a-blank-xps-om.md)  
[Lire un document XPS dans un modèle d’objet XPS](read-an-xps-document-into-an-xps-om.md)  
[Naviguer dans le modèle d’objet XPS](navigate-the-xps-om.md)  
[Écrire du texte dans un modèle d’objet XPS](write-text-to-an-xps-om.md)  
[Dessiner des graphiques dans un modèle d’objet XPS](draw-graphics-in-an-xps-om.md)  
[Placer des images dans un modèle d’objet XPS](place-images-in-an-xps-om.md)  
[Écrire un modèle OM XPS dans un document XPS](write-an-xps-om-to-an-xps-document.md)  
[Imprimer un modèle OM XPS](print-an-xps-om.md)  
[Utilisation des interfaces de collection XPS OM](working-with-xps-object-model-collection-interfaces.md)  
</dl>

## <a name="disclaimer"></a>Clause d'exclusion de responsabilité

Les exemples de code ne sont pas destinés à être des programmes complets et fonctionnels. Les exemples de code qui sont référencés sur cette page, par exemple, n’effectuent pas la vérification des paramètres, la vérification des erreurs ou la gestion des erreurs. Utilisez ces exemples comme point de départ, puis ajoutez le code nécessaire pour créer une application fiable. Pour plus d’informations sur les valeurs de retour **HRESULT** et les stratégies de gestion des erreurs, consultez [gestion des erreurs dans com](../com/error-handling-in-com.md).

Pour pouvoir utiliser des interfaces OM XPS, COM doit être initialisé dans le thread, comme le montre l’exemple de code suivant.


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



Par souci de clarté, ces exemples de code utilisent un modèle d’objet XPS très simple, qui peut ne pas être suffisamment complexe pour votre application. En guise de cas, dans les exemples de code qui ajoutent du contenu à une page, les éléments visuels d’une page sont ajoutés directement à la liste des objets visuels de la page. Toutefois, dans la pratique, vous pouvez regrouper des objets visuels dans des objets canevas, afin que plusieurs objets puissent être traités comme un groupe. Ainsi, pour activer la prise en charge d’un même contenu pour plusieurs tailles de page, vous pouvez regrouper le contenu visuel d’une page dans un objet Canvas unique, puis appliquer une transformation à la zone de dessin pour l’adapter à la taille de page actuelle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs dans COM](../com/error-handling-in-com.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
