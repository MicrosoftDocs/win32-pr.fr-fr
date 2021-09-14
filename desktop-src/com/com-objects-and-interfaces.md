---
title: Objets et interfaces COM
description: Objets et interfaces COM
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126998919"
---
# <a name="com-objects-and-interfaces"></a>Objets et interfaces COM

COM est une technologie qui permet d’interagir avec des objets à travers les limites des processus et des ordinateurs aussi facilement qu’au sein d’un même processus. COM active cela en spécifiant que la seule façon de manipuler les données associées à un objet est d’utiliser une *interface* sur l’objet. Quand ce terme est utilisé dans cette documentation, il fait référence à une implémentation dans le code d’une interface COM compatible binaire qui est associée à un objet.

COM utilise l' *interface* de mot dans un sens différent de celui généralement utilisé dans la programmation de Visual C++. Une interface C++ fait référence à toutes les fonctions prises en charge par une classe et que les clients d’un objet peuvent appeler pour interagir avec elle. Une interface COM fait référence à un groupe prédéfini de fonctions associées qu’une classe COM implémente, mais une interface spécifique ne représente pas nécessairement toutes les fonctions prises en charge par la classe.

La référence à un objet qui *implémente* une interface signifie que l’objet utilise du code qui implémente chaque méthode de l’interface et fournit des pointeurs conformes com à ces fonctions vers la bibliothèque com. COM rend ensuite ces fonctions disponibles à tout client qui demande un pointeur vers l’interface, que le client se trouve à l’intérieur ou à l’extérieur du processus qui implémente ces fonctions.

Pour plus d'informations, voir les rubriques suivantes :

-   [Interfaces et implémentations d’interface](interfaces-and-interface-implementations.md)
-   [Pointeurs d’interface et interfaces](interface-pointers-and-interfaces.md)
-   [IUnknown et héritage d’interface](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 




