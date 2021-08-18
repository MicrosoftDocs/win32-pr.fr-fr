---
description: 'Windows Le programme d’installation autorise l’installation d’une instance d’un code de produit par contexte, et les deux types de contexte possibles sont les suivants : MachineUser si un code de produit reste inchangé, une seule instance peut être installée dans le contexte de l’ordinateur et une seule instance peut être installée dans chaque contexte d’utilisateur. Pour que plusieurs instances restent isolées, elles doivent avoir des codes de produit différents et ne peuvent pas partager des données de fichier ou des données non-fichiers. la Windows Installer ne peut pas installer plusieurs instances de produits à l’aide d’installations simultanées. Toutefois, vous pouvez installer plusieurs instances d’un produit si vous disposez d’un package d’installation distinct pour chaque instance d’un produit ou d’un correctif. Chaque package peut ensuite conserver son propre jeu de données et avoir son propre code de produit unique. à partir du programme d’installation exécutant Windows Server 2003 et Windows XP avec Service Pack 1 (SP1), vous pouvez installer plusieurs instances d’un produit à l’aide de transformations de code de produit et d’un package .msi ou d’un correctif. vous pouvez également utiliser les transformations du code du produit pour installer plusieurs instances d’un produit avec Windows 2000 avec Service Pack 4 (SP4) et Windows Installer&\# 160 ; 3,0. La seule façon d’installer plus d’une instance d’un produit avec des versions antérieures du programme d’installation consiste à avoir un package d’installation distinct pour chaque instance. L’utilisation de transformations d’instance réduit considérablement l’effort nécessaire pour prendre en charge plusieurs instances d’un produit. vous pouvez créer un package de Windows Installer de base pour un produit, puis plusieurs transformations d’instances qui modifient le code du produit et gèrent les données pour chaque instance. Pour plus d’informations, consultez Création de plusieurs instances avec des transformations d’instance et installation de plusieurs instances à l’aide de transformations d’instance.'
ms.assetid: 5147ecbd-c395-4a8f-972d-f5c5b2173eff
title: Installation de plusieurs instances de produits et correctifs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6c9f061ef203effc4ec71c386f17a4c92bae957610fdc3a15b0c64a92e1e024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946147"
---
# <a name="installing-multiple-instances-of-products-and-patches"></a>Installation de plusieurs instances de produits et correctifs

Windows Le programme d’installation autorise l’installation d’une instance d’un code de produit par contexte, et les deux types de contexte possibles sont les suivants :

-   Machine
-   Utilisateur

Si un code de produit reste inchangé, une seule instance peut être installée dans le contexte de l’ordinateur et une seule instance peut être installée dans chaque contexte d’utilisateur.

Pour que plusieurs instances restent isolées, elles doivent avoir des codes de produit différents et ne peuvent pas partager des données de fichier ou des données non-fichiers. la Windows Installer ne peut pas installer plusieurs instances de produits à l’aide d' [installations simultanées](concurrent-installations.md). Toutefois, vous pouvez installer plusieurs instances d’un produit si vous disposez d’un package d’installation distinct pour chaque instance d’un produit ou d’un correctif. Chaque package peut ensuite conserver son propre jeu de données et avoir son propre code de produit unique.

à partir du programme d’installation exécutant Windows Server 2003 et Windows XP avec Service Pack 1 (SP1), vous pouvez installer plusieurs instances d’un produit à l’aide de transformations de code de produit et d’un package .msi ou d’un correctif. vous pouvez également utiliser les transformations du code du produit pour installer plusieurs instances d’un produit avec Windows 2000 avec Service Pack 4 (SP4) et Windows Installer 3,0. La seule façon d’installer plus d’une instance d’un produit avec des versions antérieures du programme d’installation consiste à avoir un package d’installation distinct pour chaque instance.

L’utilisation de transformations d’instance réduit considérablement l’effort nécessaire pour prendre en charge plusieurs instances d’un produit. vous pouvez créer un package de Windows Installer de base pour un produit, puis plusieurs transformations d’instances qui modifient le code du produit et gèrent les données pour chaque instance.

Pour plus d’informations, consultez [création de plusieurs instances avec des transformations d’instance](authoring-multiple-instances-with-instance-transforms.md) et [installation de plusieurs instances à l’aide de transformations d’instance](installing-multiple-instances-with-instance-transforms.md).

 

 



