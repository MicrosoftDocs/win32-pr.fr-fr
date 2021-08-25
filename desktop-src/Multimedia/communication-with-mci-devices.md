---
title: Communication avec les périphériques MCI
description: Communication avec les périphériques MCI
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- Périphériques MCI, communication
- MCIWndGetDeviceID macro)
- mciSendCommand fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd04187b948adf144a317a1d9eab80efb60bab8e7b05eaccffeb34722baa98a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785903"
---
# <a name="communication-with-mci-devices"></a>Communication avec les périphériques MCI

Chaque périphérique MCI peut utiliser un ou plusieurs des éléments suivants comme identificateurs :

-   identificateur d’appareil
-   nom de l’appareil
-   un alias
-   nom de fichier du contenu actuellement chargé.

MCIWnd fournit des macros que vous pouvez utiliser pour récupérer ces informations. Vous pouvez ensuite utiliser ces informations pour communiquer via MCI directement avec les périphériques MCI associés à MCIWnd Windows.

Vous pouvez récupérer l’identificateur de l’appareil MCI actuel à l’aide de la macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) . L’identificateur de périphérique MCI est une valeur numérique qui identifie l’instance de l’appareil MCI que votre application utilise. Votre application peut utiliser cet identificateur lors de la communication avec un périphérique MCI à l’aide de la fonction [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) .

Pour récupérer le nom de l’appareil MCI actuel, utilisez la macro [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) . Le nom du périphérique MCI est une chaîne se terminant par un caractère null qui identifie le type d’appareil associé à une fenêtre MCIWnd. Votre application peut utiliser ce nom lors de la communication avec un périphérique MCI à l’aide de **mciSendCommand**.

Vous pouvez récupérer l’alias de l’appareil MCI actuel à l’aide de la macro [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) . Votre application peut utiliser cet alias lors de la communication avec un périphérique MCI à l’aide de la fonction [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .

Enfin, vous pouvez récupérer le nom de fichier utilisé par un périphérique MCI à l’aide de la macro [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) . Le nom de fichier identifie le contenu actuellement associé à une fenêtre MCIWnd. Votre application peut utiliser ce nom de fichier lors de la communication avec un périphérique MCI à l’aide de **mciSendCommand** ou **mciSendString**.

 

 