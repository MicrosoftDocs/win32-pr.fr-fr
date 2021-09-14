---
description: les développeurs de packages de Windows Installer peuvent remarquer que leurs fichiers .msi sont plus volumineux que prévu après des modifications et des enregistrements répétés.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Réduction de la taille d’un fichier .msi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009703"
---
# <a name="reducing-the-size-of-an-msi-file"></a>Réduction de la taille d’un fichier .msi

les développeurs de packages de Windows Installer peuvent remarquer que leurs fichiers .msi sont plus volumineux que prévu après des modifications et des enregistrements répétés. Windows Les fichiers de .msi du programme d’installation sont des fichiers composés qui contiennent des stockages et des flux, et présentent certaines des mêmes limites de stockage que les fichiers de documents OLE. Si vous modifiez et enregistrez le même fichier .msi, cela crée un espace de stockage gaspillé dans le fichier. cela affecte uniquement les auteurs des fichiers de .msi et n’a aucun effet sur les utilisateurs de Windows Installer. Les développeurs peuvent souhaiter supprimer ce gaspillage d’espace de stockage avant d’expédier leur fichier de .msi final.

Pour supprimer l’espace de stockage gaspillé et réduire la taille finale des fichiers .msi, vous disposez des options suivantes.

-   Exportez toutes les tables de la base de données vers des fichiers. IDT, puis importez-les dans une nouvelle base de données. Cela produit le stockage le plus compact possible.
-   Utilisez un utilitaire logiciel pour compacter l’espace de stockage des fichiers de documents OLE.

 

 



