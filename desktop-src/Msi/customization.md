---
description: étant donné que le Windows Installer conserve toutes les informations relatives à l’installation dans une base de données relationnelle, l’installation d’une application ou d’un produit peut être personnalisée pour des groupes d’utilisateurs particuliers en appliquant des opérations de transformation au package.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Personnalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091753"
---
# <a name="customization"></a>Personnalisation

étant donné que le Windows Installer conserve toutes les informations relatives à l’installation dans une base de données relationnelle, l’installation d’une application ou d’un produit peut être personnalisée pour des groupes d’utilisateurs particuliers en appliquant des opérations de transformation au package. Les transformations peuvent être utilisées pour encapsuler les différentes personnalisations d’un package de base requis par différents groupes de travail. Pour plus d’informations, consultez [fusions et transformations](merges-and-transforms.md).

Plusieurs transformations d’un package de base peuvent être appliquées à la volée lors de l’installation. Cela fournit un mécanisme permettant d’affecter efficacement des installations personnalisées à différents groupes d’utilisateurs. Par exemple, cela peut être utile dans les organisations où les services de support technique et de personnel ont besoin de différentes installations d’un produit particulier. Le produit peut être mis à la disposition de tous les membres de l’organisation par une [installation administrative](administrative-installation.md) du package de base sur un point d’installation administratif unique. Chaque groupe de travail peut alors automatiquement recevoir sa personnalisation appropriée au moyen d’une transformation à la volée lors de l’installation du produit.

 

 



