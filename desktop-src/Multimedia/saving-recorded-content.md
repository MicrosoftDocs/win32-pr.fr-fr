---
title: Enregistrement du contenu enregistré
description: Enregistrement du contenu enregistré
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- MCIWndSave macro)
- MCIWndSaveDialog macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369287"
---
# <a name="saving-recorded-content"></a>Enregistrement du contenu enregistré

Une fois l’enregistrement terminé, vous pouvez enregistrer le contenu à l’aide de la macro [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) ou [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) , ou en utilisant la fonction [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) avec **MCIWndSave**. La macro **MCIWndSave** enregistre les données dans le fichier associé à la fenêtre MCIWnd. La macro **MCIWndSaveDialog** permet à l’utilisateur de spécifier un nom de fichier et d’enregistrer les données enregistrées dans le fichier spécifié. La fonction **GetSaveFileNamePreview** affiche la boîte de dialogue **Enregistrer** sous pour choisir un fichier et permet à l’utilisateur d’afficher un aperçu (lecture) du fichier. Lorsque le nom d’un fichier existant est spécifié dans la boîte de dialogue **Enregistrer** sous, **GetSaveFileNamePreview** fournit un petit contrôle dans la boîte de dialogue pour permettre à l’utilisateur d’afficher un aperçu du contenu du fichier. Vous pouvez enregistrer les données enregistrées dans un fichier sélectionné avec **GetSaveFileNamePreview** à l’aide de **MCIWndSave**.

 

 




