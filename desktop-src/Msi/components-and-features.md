---
description: le Windows Installer organise une installation autour des concepts des composants et des fonctionnalités.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Composants et fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11cea0d384b3ad2bc3238178ae0f5811c3bad7b501068bcecd35d4c5b36d922a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144555"
---
# <a name="components-and-features"></a>Composants et fonctionnalités

le Windows Installer organise une installation autour des concepts des composants et des fonctionnalités.

Une fonctionnalité fait partie de la fonctionnalité totale de l’application qu’un utilisateur peut décider d’installer de manière indépendante. pour plus d’informations, consultez [fonctionnalités de Windows Installer](windows-installer-features.md).

Un composant est une partie de l’application ou du produit à installer. Le programme d’installation installe ou supprime toujours un composant de l’ordinateur d’un utilisateur comme élément cohérent. Les composants sont généralement masqués par l’utilisateur. Quand un utilisateur sélectionne une fonctionnalité à installer, le programme d’installation détermine les composants qui doivent être installés pour fournir cette fonctionnalité. pour plus d’informations, consultez [Windows Installer components](windows-installer-components.md).

Les auteurs des packages d’installation doivent décider comment diviser leur application en fonctionnalités et composants. La sélection des fonctionnalités est principalement déterminée par les fonctionnalités de l’application du point de vue de l’utilisateur. Étant donné que les composants doivent être partagés entre les applications, voire entre les produits, il est recommandé que les auteurs suivent une méthode standard pour sélectionner les composants. Pour plus d’informations, consultez [Organisation des applications dans des composants](organizing-applications-into-components.md).

 

 



