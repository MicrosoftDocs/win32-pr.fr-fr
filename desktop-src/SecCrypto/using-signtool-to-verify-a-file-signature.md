---
description: Explique comment utiliser SignTool pour vérifier une signature de fichier.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Utilisation de SignTool pour vérifier une signature de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8161d4c890400f3aa33b415e7ac16a5306aa094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518355"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Utilisation de SignTool pour vérifier une signature de fichier

La commande suivante vérifie la signature d’un fichier nommé *MyControl.exe*:

 *MyControl.exe* de vérification de SignTool

Si l’exemple précédent échoue, il se peut que la signature utilise un certificat de signature de code. [SignTool](signtool.md) est par défaut la stratégie de pilote Windows pour la vérification.

La commande suivante vérifie la signature à l’aide de la stratégie de vérification d’authentification par défaut :

**SignTool Verify/pa** *MyControl.exe*

La commande suivante vérifie un fichier système qui peut être signé dans un catalogue :

**Vérification de SignTool/a** *SysFile.dll*

La commande suivante vérifie un fichier système qui est signé dans un catalogue nommé *MyCat.cat*:

**SignTool Verify/c** *MyCat.catMyFile.ini*

Pour toute vérification de [SignTool](signtool.md) , vous pouvez récupérer le signataire du certificat. La commande suivante vérifie un fichier système et affiche le certificat du signataire :

**SignTool Verify/v** *MyControl.exe*

[SignTool](signtool.md) retourne le texte de ligne de commande qui indique le résultat de la vérification de signature. En outre, SignTool retourne un code de sortie de zéro pour une exécution réussie, un pour l’échec de l’exécution et deux pour l’exécution qui s’est terminée avec des avertissements.

Pour plus d’informations sur [SignTool](signtool.md), consultez [SignTool](signtool.md).

 

 



