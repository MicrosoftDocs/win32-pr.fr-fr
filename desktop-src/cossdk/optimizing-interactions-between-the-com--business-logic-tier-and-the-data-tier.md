---
description: La couche données contient souvent des informations principalement statiques&\# 8212 ; les informations sont conservées sur un support durable.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Optimiser les appels entre la logique métier COM+ et les données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516780"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a>Optimisation des interactions entre le niveau de logique métier COM+ et la couche données

La couche données contient souvent des informations essentiellement statiques : les informations sont conservées sur un support durable. Étant donné que ce niveau englobe des informations qui sont principalement statiques, il est nécessaire d’analyser minutieusement les goulots d’étranglement potentiels. Outre la possibilité évidente de goulots d’étranglement de connexion, les zones réactives peuvent être dues à des enregistrements fréquemment sollicités, à des méthodes d’accès aux données inefficaces et à la nécessité de coordonner l’accès aux systèmes hérités.

## <a name="connecting-to-the-data-tier"></a>Connexion à la couche données

Deux considérations jouent un rôle important dans la conception d’une couche données pour une application COM+ : le regroupement de connexions et l’activation de la [fonction juste-à-temps (JIT) com+](com--just-in-time-activation.md), ainsi que l’utilisation de DSN. Les composants qui établissent des connexions à la couche données doivent utiliser le [regroupement d’objets com+](com--object-pooling.md) défini sur le composant.

Lors de la création de DSN, utilisez les chaînes de constructeur d’objet spécifiées sur le composant au lieu de créer un DSN de fichier. Les noms de sources de fichier sont plus lents qu’une connexion utilisant une chaîne de constructeur d’objet. Les chaînes du constructeur d’objet peuvent être spécifiées dans la feuille de propriétés du composant. Pour plus d’informations, consultez [chaînes de constructeur d’objet com+](com--object-constructor-strings.md).

Si vous utilisez des composants pour accéder à une base de données SQL Server, utilisez le regroupement d’objets COM+ au lieu du regroupement de connexions SQL.

Si votre composant utilise ADO pour extraire plusieurs recordsets, établissez plusieurs connexions pour ce composant. Lorsque ADO Récupère plusieurs recordsets, il crée plusieurs connexions en arrière-plan si vous ne les créez pas. Si vous les créez, vous pouvez les regrouper et avoir davantage de contrôle sur le nombre de connexions utilisées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Optimisation des interactions entre le niveau de logique métier COM+ et la couche présentation](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



