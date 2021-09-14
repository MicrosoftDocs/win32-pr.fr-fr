---
description: Les modules de fusion requièrent rarement une interface utilisateur.
ms.assetid: 53bd2064-09dd-406f-a8ff-7b04f3525b9f
title: Création d’interfaces utilisateur dans les modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2df8781efea35ddd854ef76c2155d4a2ded7f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092437"
---
# <a name="authoring-user-interfaces-in-merge-modules"></a>Création d’interfaces utilisateur dans les modules de fusion

Les modules de fusion requièrent rarement une interface utilisateur. La libération d’un module de fusion qui contient à la fois des composants installables et une interface utilisateur restreint finalement la flexibilité de l’utilisateur du module. La combinaison des composants et de l’interface utilisateur dans un seul module peut empêcher les développeurs d’utiliser leur propre interface utilisateur ou de fournir des installations en mode silencieux. Une meilleure solution consiste à libérer deux modules de fusion, un qui installe silencieusement les composants et un second module facultatif qui contient l’interface utilisateur. Le module avec l’interface utilisateur doit répertorier le module de composant dans sa [table ModuleDependency](moduledependency-table.md). Cette méthode permet aux auteurs de module de fournir une interface utilisateur sans l’imposer aux développeurs.

Lorsque des tables d’interface utilisateur sont utilisées dans des modules de fusion, elles peuvent être fusionnées de la même façon que les autres tables.

 

 



