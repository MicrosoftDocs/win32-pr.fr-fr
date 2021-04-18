---
description: Le catalogue COM+ stocke les attributs d’application COM+, les attributs de classe et les attributs au niveau de l’ordinateur. Il garantit la cohérence entre ces attributs et fournit des opérations courantes en plus de ces attributs.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: Le catalogue COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516367"
---
# <a name="the-com-catalog"></a>Le catalogue COM+

Le catalogue COM+ stocke les attributs d’application COM+, les attributs de classe et les attributs au niveau de l’ordinateur. Il garantit la cohérence entre ces attributs et fournit des opérations courantes en plus de ces attributs.

Le catalogue COM+ utilise deux magasins différents, comme suit :

-   La base de données d’inscription COM+
-   Le Registre Windows (**HKEY \_ classes \_ root**)

Le catalogue présente une vue logique et unifiée de ces deux magasins et les expose via la bibliothèque d’administration COM+. Cette bibliothèque fournit, via un langage de script, toutes les fonctionnalités de l’outil d’administration Services de composants.

Pour les composants COM existants qui ne nécessitent pas de nouveaux services COM+, la recherche s’effectue dans le Registre Windows existant. Le catalogue COM+ utilise également le Registre Windows pour la bibliothèque de types et l’inscription de proxy/stub d’interface.

## <a name="split-registration"></a>Fractionner l’inscription

Pour les nouveaux composants qui sont déjà des composants COM existants qui sont utilisés dans l’environnement de services (par exemple, les composants MTS), l’aspect COM de base de l’inscription est stocké dans le Registre Windows et les nouveaux services et attributs (par exemple, les composants mis en file d’attente) sont stockés dans la base de données d’inscription COM+. C’est ce qu’on appelle une *inscription fractionnée*.

Chaque attribut est stocké dans un seul emplacement : le Registre Windows ou la base de données d’inscription COM+. Les nouveaux composants COM sont inscrits exclusivement dans la base de données d’inscription COM+, avec une certaine duplication dans le Registre Windows afin que les outils existants puissent les utiliser.

## <a name="transactional-updates-to-the-catalog"></a>Mises à jour transactionnelles du catalogue

Certaines opérations sur le catalogue sont effectuées de manière transactionnelle. Lorsque vous appelez la bibliothèque d’administration COM+ à partir d’un composant transactionnel, les mises à jour apportées à la base de données d’inscription COM+ se produisent dans la limite de transaction du composant appelant.

Toutefois, il n’est pas garanti que les mises à jour qui impliquent des modifications d’autres magasins (telles que le système de fichiers et le Registre Windows) soient entièrement transactionnelles. Une transaction abandonnée peut conserver ces magasins dans un état incohérent avec les modifications apportées à l’un ou à la base de données d’inscription COM+.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de packages d’installation pour les applications COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Déploiement de proxys d’application](deploying-application-proxies.md)
</dt> <dt>

[L’utilitaire de réplication COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



