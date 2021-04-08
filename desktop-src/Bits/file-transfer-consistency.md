---
title: Cohérence du transfert de fichiers
description: BITS garantit que la version du fichier qu’il transfère est cohérente en fonction de la taille du fichier et de l’horodatage, et non du contenu (le service BITS ne protège pas contre les attaques de l’intercepteur).
ms.assetid: ba82f172-a3ac-49d6-bccd-7d0b68ba66de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533bc0c0db9708528d4ae919572d6e4c1d251ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839361"
---
# <a name="file-transfer-consistency"></a>Cohérence du transfert de fichiers

BITS garantit que la version du fichier qu’il transfère est cohérente en fonction de la taille du fichier et de l’horodatage, et non du contenu (le service BITS ne protège pas contre les attaques de l’intercepteur). Pour vérifier le contenu vous-même, vous pouvez utiliser la méthode [**IBackgroundCopyFile3 :: GetTemporaryName**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-gettemporaryname) pour récupérer le nom du fichier qui contient le contenu téléchargé, vérifier le contenu à l’aide de votre propre mécanisme, puis appeler la méthode [**IBackgroundCopyFile3 :: SetValidationState**](/windows/desktop/api/Bits3_0/nf-bits3_0-ibackgroundcopyfile3-setvalidationstate) pour indiquer à bits si le contenu du fichier est valide. Si vous définissez l’état de validation sur **false** et que le contenu provient du serveur d’origine, le travail passe à l’état d’erreur. Si le contenu provient d’un homologue, le service BITS télécharge le fichier à partir du serveur d’origine.

Pour les téléchargements, si la taille du fichier ou l’horodatage change alors que BITS transfère le fichier, BITS redémarre le transfert de ce fichier uniquement. Par exemple, si le travail de téléchargement contient deux fichiers et que les fichiers sont mis à jour sur le serveur pendant que BITS transfère le deuxième fichier, BITS redémarre le transfert du deuxième fichier uniquement. Le premier fichier, qui a déjà été transféré avec succès, n’est pas mis à jour pour refléter les nouvelles modifications.

Notez que si vous êtes le propriétaire du fichier téléchargé à partir du serveur, vous devez créer une nouvelle URL pour chaque nouvelle version du fichier. Si vous utilisez la même URL pour les nouvelles versions du fichier, certains serveurs proxy peuvent servir des données obsolètes à partir de leur cache, car ils ne vérifient pas avec le serveur d’origine si le fichier est périmé.

Pour les téléchargements, si la taille du fichier ou l’horodatage change pendant le transfert de fichiers, BITS génère une erreur et le travail est placé dans l' \_ État d’erreur d’état de la tâche BG \_ \_ .

Le service BITS ne synchronise pas les demandes de transfert lorsqu’un ou plusieurs utilisateurs demandent que le même fichier soit transféré au même emplacement. BITS transfère le fichier pour chaque demande séparément.

 

 




