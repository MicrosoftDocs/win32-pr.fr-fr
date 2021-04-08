---
title: Enregistrement des données capturées dans un nouveau fichier
description: Enregistrement des données capturées dans un nouveau fichier
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- Message WM_CAP_FILE_SAVEAS
- capFileSaveAs macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673166"
---
# <a name="saving-captured-data-to-a-new-file"></a>Enregistrement des données capturées dans un nouveau fichier

Si l’utilisateur souhaite enregistrer les données capturées, l’application doit enregistrer le contenu du fichier de capture dans un autre fichier à l’aide du message de [**fichier d' \_ \_ \_ enregistrement de l’embout WM**](wm-cap-file-saveas.md) (ou de la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ). Ce message ne modifie pas le nom ou le contenu du fichier de capture. Votre application doit spécifier un nom pour le nouveau fichier, car le fichier de capture conserve son nom de fichier d’origine.

En règle générale, un fichier de capture est préalloué pour le plus grand segment de capture prévu, et seule une partie de celui-ci peut être utilisée pour capturer des données. Ce message copie uniquement la partie du fichier de capture contenant les données de capture.

 

 




