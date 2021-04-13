---
description: Pour que les fonctions d’installation puissent accéder aux informations contenues dans le fichier INF, vous devez l’ouvrir avec un appel à la fonction SetupOpenInfFile. Cette fonction renvoie un descripteur au fichier INF.
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: Ouverture et fermeture d’un fichier INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529325"
---
# <a name="opening-and-closing-an-inf-file"></a>Ouverture et fermeture d’un fichier INF

Pour que les fonctions d’installation puissent accéder aux informations contenues dans le fichier INF, vous devez l’ouvrir avec un appel à la fonction [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) . Cette fonction renvoie un descripteur au fichier INF.

Si vous ne connaissez pas le nom du fichier INF que vous devez ouvrir, vous pouvez utiliser la fonction [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) pour obtenir la liste des fichiers INF dans un répertoire.

Après avoir ouvert un fichier INF, vous pouvez ajouter des fichiers INF supplémentaires au fichier INF ouvert à l’aide de la fonction [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) . Cette fonction est similaire à une instruction include. Lorsque les fonctions de configuration suivantes font référence à un fichier INF ouvert, elles peuvent également accéder à toutes les informations stockées dans les fichiers ajoutés.

Si vous ne spécifiez pas de fichier INF lors de l’appel à la fonction [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) , **SetupOpenAppendInfFile** ajoute le ou les fichiers spécifiés par la clé **LayoutFile** dans la section **version** du fichier INF ouvert.

Lorsque vous n’avez plus besoin des informations contenues dans le fichier INF, appelez la fonction [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) pour libérer les ressources allouées pendant l’appel à [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea).

 

 



