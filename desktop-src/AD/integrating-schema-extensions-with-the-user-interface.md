---
title: Intégration des extensions de schéma avec l’interface utilisateur
description: Les outils d’administration de Active Directory Domain Services utilisent une architecture commune pour connecter l’interface utilisateur d’administration au schéma d’annuaire.
ms.assetid: 62cf9f9d-7091-4cff-9995-5934dfa3e97e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c23d951ec51d7453ee92cf90ddcb28ddb8219d3056b1edb96d16bf15494fe956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187208"
---
# <a name="integrating-schema-extensions-with-the-user-interface"></a>Intégration des extensions de schéma avec l’interface utilisateur

Les outils d’administration de Active Directory Domain Services utilisent une architecture commune pour connecter l’interface utilisateur d’administration au schéma d’annuaire. La pièce maîtresse de cette architecture est la classe d’objets **displaySpecifier** . Les spécificateurs d’affichage et leur utilisation sont décrits en détail dans [extension de l’interface utilisateur pour les objets d’annuaire](extending-the-user-interface-for-directory-objects.md).

Quand vous créez une classe en sous-classant une classe existante, vous pouvez tirer parti de l’interface utilisateur existante pour la superclasse en copiant le spécificateur d’affichage de la superclasse. Un moyen simple de copier le spécificateur d’affichage d’une classe consiste à l’exporter dans un fichier LDIF à l’aide de LDIFDE, de modifier le nom unique et le CN, puis d’importer le fichier LDIF modifié. Si la sous-classe possède des attributs supplémentaires, vous devrez fournir des pages de propriétés supplémentaires pour prendre en charge la modification. Si la sous-classe a des propriétés requises supplémentaires, vous devrez fournir des pages d’extension de boîte de dialogue de création, car l’interface utilisateur fournie par la superclasse n’a aucun moyen de créer ces nouveaux attributs.

 

 




