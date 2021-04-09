---
description: Le Windows Installer organise une installation autour des concepts des composants et des fonctionnalités.
ms.assetid: c560441e-89c5-4f82-837b-988c3f404d37
title: Composants et fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b21241c98fbb701bd6a3ef5869045ef8c46da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114178"
---
# <a name="components-and-features"></a>Composants et fonctionnalités

Le Windows Installer organise une installation autour des concepts des composants et des fonctionnalités.

Une fonctionnalité fait partie de la fonctionnalité totale de l’application qu’un utilisateur peut décider d’installer de manière indépendante. Pour plus d’informations, consultez [fonctionnalités de Windows Installer](windows-installer-features.md).

Un composant est une partie de l’application ou du produit à installer. Le programme d’installation installe ou supprime toujours un composant de l’ordinateur d’un utilisateur comme élément cohérent. Les composants sont généralement masqués par l’utilisateur. Quand un utilisateur sélectionne une fonctionnalité à installer, le programme d’installation détermine les composants qui doivent être installés pour fournir cette fonctionnalité. Pour plus d’informations, consultez [Windows Installer Components](windows-installer-components.md).

Les auteurs des packages d’installation doivent décider comment diviser leur application en fonctionnalités et composants. La sélection des fonctionnalités est principalement déterminée par les fonctionnalités de l’application du point de vue de l’utilisateur. Étant donné que les composants doivent être partagés entre les applications, voire entre les produits, il est recommandé que les auteurs suivent une méthode standard pour sélectionner les composants. Pour plus d’informations, consultez [Organisation des applications dans des composants](organizing-applications-into-components.md).

 

 



