---
title: Stockage Conventions d’affectation des noms d’objets
description: les objets Stockage et stream sont nommés selon un ensemble de conventions.
ms.assetid: 72e87c6a-cce5-4456-8336-c657e65c0a34
keywords:
- Strctd Stockage structurés Stg, notions de base, conventions de nommage des objets de stockage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e828674f4165bdb54dc2ec06748ab4165e75e2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013538"
---
# <a name="storage-object-naming-conventions"></a>Stockage Conventions d’affectation des noms d’objets

les objets Stockage et stream sont nommés selon un ensemble de conventions.

Le nom d’un objet de stockage racine est le nom réel du fichier dans le système de fichiers sous-jacent. Il est conforme aux conventions et aux restrictions imposées par le système de fichiers. Les chaînes de nom de fichier passées aux méthodes et aux méthodes liées au stockage sont passées sur le système de fichiers, non interprétées et inchangées.

Le nom d’un élément imbriqué contenu dans un objet de stockage est géré par l’implémentation de l’objet de stockage particulier. Toutes les implémentations des objets de stockage doivent prendre en charge les noms d’éléments imbriqués 32 caractères de longueur (y compris la marque de fin **null** ), bien que certaines implémentations puissent prendre en charge des noms plus longs. Si l’objet de stockage effectue une conversion de casse quelconque est défini par l’implémentation. Par conséquent, les applications qui définissent des noms d’élément doivent choisir des noms acceptables, que la conversion de casse soit effectuée ou non. L’implémentation COM des fichiers composés prend en charge les noms d’une longueur maximale de 32 caractères et n’effectue aucune conversion de casse.

 

 




