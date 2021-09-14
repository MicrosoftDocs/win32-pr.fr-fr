---
title: Valeurs de retour de SYSMON
description: La liste suivante répertorie les valeurs renvoyées par le moniteur système qui sont définies dans Smonmsg. h.
ms.assetid: f1cc7668-4a6f-4b70-9591-62bd447fe8fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13ce5678c20a1ab8df825a5e3bc5f725d255e459
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008849"
---
# <a name="sysmon-return-values"></a>Valeurs de retour de SYSMON

La liste suivante répertorie les valeurs renvoyées par le moniteur système qui sont définies dans Smonmsg. h.



| Valeur de retour                                       | Description                                                                                                                                                                                                                                  |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SMON \_ état \_ DUPL \_ chemin du compteur \_ (0xC0001388)     | La collection de compteurs contient déjà le compteur spécifié.                                                                                                                                                                               |
| \_État smon \_ aucun \_ \_ objet SYSMON (0xC0001389)      | Les paramètres ne contiennent pas d’objets HTML du moniteur système complets.                                                                                                                                                                        |
| \_Exemples d’États smon \_ insuffisants \_ \_ (0xC000138A)       | Le fichier journal spécifié contient moins de deux échantillons de données.                                                                                                                                                                                 |
| \_ \_ Limite de la taille du fichier journal d’État smon \_ \_ \_ (0xC000138B)  | Le fichier journal spécifié dépasse les limites de taille du contrôle Moniteur système. Si un fichier journal est actuellement sélectionné, sélectionnez activité actuelle comme source de données afin de décharger le fichier journal actuel, puis resélectionnez le fichier journal spécifié. |
| \_ \_ Source de données du fichier journal d’État smon \_ \_ \_ (0xC000138C) | Pour ajouter un nouveau fichier journal à la source de données, le type de source de données doit être changé en un type autre que sysmonLogFiles.                                                                                                                          |
| SMON \_ état \_ DUPL \_ \_ \_ chemin d’accès du fichier journal (0xC000138D)   | La collection de fichiers journaux contient déjà le fichier journal spécifié.                                                                                                                                                                             |



 

Pour obtenir une description des valeurs de retour supplémentaires retournées par le moniteur système, consultez Codes d' [erreur système](/windows/desktop/Debug/system-error-codes) et [codes d’erreur du programme d’assistance des données de performances](/windows/desktop/PerfCtrs/checking-pdh-interface-return-values).

 

 