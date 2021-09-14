---
title: Configuration d’un pilote pouvant être installé
description: Configuration d’un pilote pouvant être installé
ms.assetid: c81f4bcb-38c6-42f1-a50d-1f700c6a3c37
keywords:
- pilotes installables, configuration
- Configuration des pilotes installables
- OpenDriver fonction)
- SendDriverMessage fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ad0ad16d719152dba0dc0b2ca6224122831a0ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416861"
---
# <a name="configuring-an-installable-driver"></a>Configuration d’un pilote pouvant être installé

Pour indiquer à un pilote installable d’effectuer des tâches utiles, vous devez ouvrir le pilote à l’aide de la fonction [OpenDriver](/windows/win32/api/mmiscapi/nf-mmiscapi-opendriver) et lui envoyer des messages à l’aide de la fonction [SendDriverMessage](/windows/win32/api/mmiscapi/nf-mmiscapi-senddrivermessage) . L’exemple suivant montre comment demander au pilote d’afficher sa boîte de dialogue de configuration.


```C++
LONG MyConfigureDriver()
{
    HDRVR hdrvr;
    DRVCONFIGINFO dci;
    LONG lRes;

    // Open the driver (no additional parameters needed this time).
    if ((hdrvr = OpenDriver(L"\\samples\\sample.drv", 0, 0)) == 0) {
        // Can't open the driver
        return DRVCNF_CANCEL;
    }

    // Make sure driver has a configuration dialog box.
    if (SendDriverMessage(hdrvr, DRV_QUERYCONFIGURE, 0, 0) != 0) {
        // Set the DRVCONFIGINFO structure and send the message
        dci.dwDCISize = sizeof (dci);
        dci.lpszDCISectionName = (LPWSTR)0;
        dci.lpszDCIAliasName = (LPWSTR)0;
        lRes = SendDriverMessage(hdrvr, DRV_CONFIGURE, 0, (LONG)&dci);
     }

    // Close the driver (no additional parameters needed this time).
    CloseDriver(hdrvr, 0, 0);

    return lRes;
}
 
```



 

 