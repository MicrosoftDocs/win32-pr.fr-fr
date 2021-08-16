---
title: Propriétés et méthodes
description: Comme tout objet OLE, un contrôle fournit une grande partie de ses fonctionnalités via un ensemble d’interfaces entrantes avec des propriétés et des méthodes.
ms.assetid: 5a0cdb5d-7e27-40e9-94db-cfda853879c6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52dae30453089f235a4e70d7896569ebefcdff9f7f2419b5fc54af88b8563d63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047887"
---
# <a name="properties-and-methods"></a>Propriétés et méthodes

Comme tout objet OLE, un contrôle fournit une grande partie de ses fonctionnalités via un ensemble d’interfaces entrantes avec des propriétés et des méthodes.

Un contrôle expose des propriétés et des méthodes via OLE Automation afin que les conteneurs puissent y accéder sous le contrôle d’un langage de programmation fourni par un conteneur.

Pour prendre en charge l’accès aux propriétés via une interface utilisateur, un contrôle fournit des pages de propriétés, la prise en charge des \_ Propriétés OLEIVERB, la navigation entre les propriétés et la liaison de données par le biais de la modification de propriété notifications.

-   Via les pages de propriétés, un contrôle peut afficher ses propriétés, indépendamment de son conteneur, si nécessaire.
-   En prenant en charge \_ les propriétés OLEIVERB, l’élément propriétés est affiché dans le menu du conteneur. L’utilisateur final peut ensuite sélectionner l’élément **Propriétés** pour afficher les pages de propriétés du contrôle et modifier les propriétés.
-   La navigation par propriété prend en charge un conteneur qui peut afficher les propriétés du contrôle dans le cadre d’une plus grande feuille de propriétés qui peut inclure des propriétés de plusieurs contrôles dans le conteneur.
-   Grâce à la notification de modification de propriété, un contrôle peut informer un client que ses propriétés ont changé, ce qui permet au client d’effectuer les actions nécessaires en conséquence.

Pour plus d'informations, voir les rubriques suivantes :

-   [Propriétés du contrôle](control-properties.md)
-   [Méthodes de contrôle](control-methods.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ActiveX Commandes](activex-controls.md)
</dt> <dt>

[Pages de propriétés et feuilles de propriétés](property-pages-and-property-sheets.md)
</dt> </dl>

 

 




