---
description: Pour installer un fichier, une police ou une clé de Registre afin qu’il ne soit pas supprimé lors de la désinstallation du produit, la totalité du composant contenant le fichier, la police ou la clé de registre doit être rendue permanente.
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: Installation des composants permanents, des fichiers, des polices, des clés de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87818c2b9a80d582992dd964daa632575f51e5fa24f17a97af0191277e880df6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105099"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>Installation des composants permanents, des fichiers, des polices, des clés de Registre

Pour installer un fichier, une police ou une clé de Registre afin qu’il ne soit pas supprimé lors de la désinstallation du produit, la totalité du composant contenant le fichier, la police ou la clé de registre doit être rendue permanente. Pour rendre un composant permanent, définissez **msidbComponentAttributesPermanent** dans la colonne attributs de la [table des composants](component-table.md).

Notez que le programme d’installation supprime une clé de registre après avoir supprimé la dernière valeur ou sous-clé sous la clé. Pour éviter qu’une clé de Registre vide ne soit supprimée lors de la désinstallation, écrivez une valeur factice sous la clé que vous avez besoin de conserver, puis entrez + dans la colonne nom de la [table du Registre](registry-table.md).

 

 



