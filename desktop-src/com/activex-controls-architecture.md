---
title: ActiveX Architecture des contrôles
description: la technologie de contrôle de ActiveX s’appuie sur une base de nombreux objets et interfaces de niveau inférieur dans OLE. Les interfaces exactes disponibles sur un contrôle varient en fonction de ses capacités. Cette section examine de plus près les fonctionnalités qu’un contrôle peut fournir.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cde527bcfc5e683d35da8f267a6cb8b22a85cb6d84e77b905ef30325deb1d850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071239"
---
# <a name="activex-controls-architecture"></a>ActiveX Architecture des contrôles

la technologie de contrôle de ActiveX s’appuie sur une base de nombreux objets et interfaces de niveau inférieur dans OLE. Les interfaces exactes disponibles sur un contrôle varient en fonction de ses capacités. Cette section examine de plus près les fonctionnalités qu’un contrôle peut fournir.

les contrôles ActiveX sont utilisés pour fournir les blocs de construction permettant de créer des interfaces utilisateur dans des applications. Par exemple, un bouton qui lance une action dans l’application conteneur quand l’utilisateur clique dessus est un contrôle simple. Les aspects suivants sont impliqués dans la fourniture de ces blocs de construction d’interface utilisateur :

-   Un contrôle peut être incorporé dans son client de conteneur pour prendre en charge une activité de l’interface utilisateur au sein du client. Ainsi, un contrôle doit fournir une représentation visuelle de lui-même lorsqu’il est incorporé dans le conteneur et doit fournir un moyen d’enregistrer son état, par exemple ses valeurs de propriété et sa position dans son conteneur. Le client doit prendre en charge un conteneur avec des objets incorporés dans celui-ci.
-   En activant le contrôle à l’aide d’un clavier ou d’une souris, l’utilisateur final lance une action dans l’application cliente. Ainsi, un contrôle doit répondre à l’activité du clavier et doit être en mesure de communiquer avec son client pour qu’il puisse notifier son conteneur de ses activités et déclencher des événements dans le client.
-   Le client fournit également un langage de programmation par le biais duquel l’utilisateur final peut lancer des actions fournies par les propriétés et les méthodes du contrôle. Par conséquent, un contrôle doit prendre en charge l’automatisation et un ensemble de fonctionnalités au moment du design plutôt qu’au moment de l’exécution.

En raison de son rôle dans la fourniture des blocs de construction de l’interface utilisateur, un contrôle prend généralement en charge les fonctionnalités dans les domaines suivants à l’aide des technologies OLE, comme indiqué ci-dessous :

<dl> <dt>

<span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Propriétés et méthodes
</dt> <dd>

Comme tout objet OLE, un contrôle peut fournir une grande partie de ses fonctionnalités via un ensemble d’interfaces entrantes avec des propriétés et des méthodes. Le conteneur peut fournir des propriétés ambiantes supplémentaires et peut prendre en charge l’extension des propriétés du contrôle par le biais de l’agrégation. ces fonctionnalités reposent sur l’automatisation OLE, les pages de propriétés, les objets connectables et les technologies de contrôle ActiveX.

</dd> <dt>

<span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Événements
</dt> <dd>

en plus de fournir des propriétés et des méthodes, un contrôle de ActiveX peut également fournir des interfaces sortantes pour notifier son client d’événements. Le client doit prendre en charge la gestion de ces événements. Ces fonctionnalités utilisent l’automatisation OLE et les objets connectables.

</dd> <dt>

<span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Représentation visuelle
</dt> <dd>

Un contrôle peut prendre en charge le positionnement et s’afficher dans son conteneur. Le conteneur positionne le contrôle et détermine sa taille. Ces fonctionnalités utilisent la technologie de document composé, y compris la technologie glisser-déplacer OLE.

</dd> <dt>

<span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Gestion du clavier
</dt> <dd>

Un contrôle peut répondre aux accélérateurs de clavier afin que l’utilisateur final puisse lancer des actions effectuées par le contrôle. Le conteneur gère l’activité du clavier pour tous ses contrôles incorporés. Ces fonctionnalités utilisent les technologies de contrôle et de document composé.

</dd> <dt>

<span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistance
</dt> <dd>

Un contrôle peut enregistrer son état. Le client gère la persistance de ses contrôles incorporés. Ces fonctionnalités utilisent le stockage structuré et les technologies de persistance des objets.

</dd> <dt>

<span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Inscription et licences
</dt> <dd>

En général, un contrôle prend en charge l’inscription automatique et crée un jeu d’entrées de Registre lorsqu’il est instancié. Un contrôle peut également être concédé sous licence pour empêcher toute utilisation non autorisée.

</dd> </dl>

La plupart de ces fonctionnalités impliquent à la fois le contrôle et son conteneur client.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ActiveX Commandes](activex-controls.md)
</dt> </dl>

 

 




