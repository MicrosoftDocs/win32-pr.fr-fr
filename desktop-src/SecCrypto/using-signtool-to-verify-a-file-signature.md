---
description: Explique comment utiliser SignTool pour vérifier une signature de fichier.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Utilisation de SignTool pour vérifier une signature de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e91df7a64a8db48d04ceba9df5fbc3fd358058
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "107954922"
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

**SignTool Verify/c** *MyCat.cat* *MyFile.ini*

Pour toute vérification de [SignTool](signtool.md) , vous pouvez récupérer le signataire du certificat. La commande suivante vérifie un fichier système et affiche le certificat du signataire :

**SignTool Verify/v** *MyControl.exe*

[SignTool](signtool.md) retourne le texte de ligne de commande qui indique le résultat de la vérification de signature. En outre, SignTool retourne un code de sortie de zéro pour une exécution réussie, un pour l’échec de l’exécution et deux pour l’exécution qui s’est terminée avec des avertissements.

Pour plus d’informations sur [SignTool](signtool.md), consultez [SignTool](signtool.md).

 

 



