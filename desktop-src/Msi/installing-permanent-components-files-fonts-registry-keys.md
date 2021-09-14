---
description: Pour installer un fichier, une police ou une clé de Registre afin qu’il ne soit pas supprimé lors de la désinstallation du produit, la totalité du composant contenant le fichier, la police ou la clé de registre doit être rendue permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Installation des composants permanents, des fichiers, des polices, des clés de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012041"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>Installation des composants permanents, des fichiers, des polices, des clés de Registre

Pour installer un fichier, une police ou une clé de Registre afin qu’il ne soit pas supprimé lors de la désinstallation du produit, la totalité du composant contenant le fichier, la police ou la clé de registre doit être rendue permanente. Pour rendre un composant permanent, définissez **msidbComponentAttributesPermanent** dans la colonne attributs de la [table des composants](component-table.md).

Notez que le programme d’installation supprime une clé de registre après avoir supprimé la dernière valeur ou sous-clé sous la clé. Pour éviter qu’une clé de Registre vide ne soit supprimée lors de la désinstallation, écrivez une valeur factice sous la clé que vous avez besoin de conserver, puis entrez + dans la colonne nom de la [table du Registre](registry-table.md).

 

 



