---
description: Chaque enregistrement de la table IsolatedComponent associe le composant spécifié dans la \_ colonne application du composant (généralement un .exe) au composant spécifié dans la \_ colonne partagé du composant (généralement une DLL partagée).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Table IsolatedComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011997"
---
# <a name="isolatedcomponent-table"></a>Table IsolatedComponent

Chaque enregistrement de la table IsolatedComponent associe le composant spécifié dans la \_ colonne application du composant (généralement un .exe) au composant spécifié dans la \_ colonne partagé du composant (généralement une DLL partagée). L' [action IsolateComponents](isolatecomponents-action.md) installe une copie du composant \_ partagé dans un emplacement privé pour une utilisation par l’application de composant \_ . Cela isole l’application du composant des \_ autres copies du composant \_ partagé qui peuvent être installées dans un emplacement partagé sur l’ordinateur. Consultez [composants isolés](isolated-components.md).

Pour lier un composant \_ partagé à plusieurs applications de composant \_ , incluez un enregistrement distinct pour chaque paire dans la table IsolatedComponents. Le programme d’installation copie les fichiers du composant \_ partagé dans le répertoire de chaque application de composant \_ installée.

La table IsolatedComponent contient les colonnes suivantes.



| Colonne                 | Type                         | Clé | Nullable |
|------------------------|------------------------------|-----|----------|
| Composant \_ partagé      | [Identificateur](identifier.md) | O   | N        |
| Application de composant \_ | [Identificateur](identifier.md) | O   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Composant \_ partagé
</dt> <dd>

Clé étrangère dans la [table des composants](component-table.md). Composant qui contient le fichier partagé, généralement une DLL. La DLL doit être le fichier de clé pour ce composant. Il doit s’agir d’un composant différent de celui indiqué dans la \_ colonne application du composant.

Le composant partagé contrôle l’inscription de toutes les copies isolées du composant et doit avoir l’indicateur **msidbComponentAttributesSharedDllRefCount** défini dans la colonne attributs de la table des composants. Cela permet de s’assurer que le programme d’installation peut gérer la durée de vie du composant partagé.

</dd> <dt>

<span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Application de composant \_
</dt> <dd>

Clé étrangère dans la [table des composants](component-table.md). Composant qui contient l' .exe qui charge le fichier partagé. Le .exe doit être le fichier de clé pour ce composant. Il doit s’agir d’un composant différent de celui indiqué dans la \_ colonne partagé du composant.

</dd> </dl>

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE62](ice62.md)  
[ICE66](ice66.md)  
[ICE97](ice97.md)  
</dl>

 

 



