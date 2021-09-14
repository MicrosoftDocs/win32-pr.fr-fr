---
description: Le catalogue COM+ stocke les attributs d’application COM+, les attributs de classe et les attributs au niveau de l’ordinateur. Il garantit la cohérence entre ces attributs et fournit des opérations courantes en plus de ces attributs.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: Le catalogue COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310886"
---
# <a name="the-com-catalog"></a>Le catalogue COM+

Le catalogue COM+ stocke les attributs d’application COM+, les attributs de classe et les attributs au niveau de l’ordinateur. Il garantit la cohérence entre ces attributs et fournit des opérations courantes en plus de ces attributs.

Le catalogue COM+ utilise deux magasins différents, comme suit :

-   La base de données d’inscription COM+
-   registre Windows (**racine des \_ CLASSES \_ HKEY**)

Le catalogue présente une vue logique et unifiée de ces deux magasins et les expose via la bibliothèque d’administration COM+. Cette bibliothèque fournit, via un langage de script, toutes les fonctionnalités de l’outil d’administration Services de composants.

pour les composants COM existants qui ne nécessitent pas de nouveaux services COM+, la recherche s’effectue dans le registre de Windows existant. le catalogue COM+ utilise également le registre Windows pour la bibliothèque de types et l’inscription de proxy/stub d’interface.

## <a name="split-registration"></a>Fractionner l’inscription

pour les nouveaux composants qui sont déjà des composants com existants qui sont utilisés dans l’environnement de services (par exemple, les composants MTS), l’aspect com de base de l’inscription est stocké dans le registre Windows et les nouveaux services et attributs (par exemple, les composants mis en file d’attente) sont stockés dans la base de données d’inscription COM+. C’est ce qu’on appelle une *inscription fractionnée*.

chaque attribut est stocké dans un seul emplacement : le registre Windows ou la base de données d’inscription COM+. les nouveaux composants COM sont inscrits exclusivement dans la base de données d’inscription COM+, avec une certaine duplication dans le registre Windows pour que les outils existants puissent les utiliser.

## <a name="transactional-updates-to-the-catalog"></a>Mises à jour transactionnelles du catalogue

Certaines opérations sur le catalogue sont effectuées de manière transactionnelle. Lorsque vous appelez la bibliothèque d’administration COM+ à partir d’un composant transactionnel, les mises à jour apportées à la base de données d’inscription COM+ se produisent dans la limite de transaction du composant appelant.

toutefois, il n’est pas garanti que les mises à jour qui impliquent des modifications d’autres magasins (telles que le système de fichiers et le registre Windows) soient entièrement transactionnelles. Une transaction abandonnée peut conserver ces magasins dans un état incohérent avec les modifications apportées à l’un ou à la base de données d’inscription COM+.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de packages d’installation pour les applications COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Déploiement de proxys d’application](deploying-application-proxies.md)
</dt> <dt>

[L’utilitaire de réplication COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



