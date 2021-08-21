---
title: Difxapi.h
description: Cette section contient des rubriques de référence sur l’en-tête difxapi. h.
ms.assetid: 84da7e54-0677-495e-9dc5-aca4ac12c0b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5dcace8f7f8c8ed528849da02016f04e0ca32b2132c7b0587a96872d7cc561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736019"
---
# <a name="difxapih"></a>Difxapi.h

Cette section contient des rubriques de référence sur l’en-tête difxapi. h.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                 | Description                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*DIFLOGCALLBACK*](/previous-versions/windows/hardware/difxapi/diflogcallback)<br/>                     | Une fonction de type **DIFLOGCALLBACK** est une fonction de rappel fournie par l’application qu’une application enregistre en appelant [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback). DIFxAPI appelle la fonction de rappel pour consigner les événements qui se produisent pendant l’opération DIFxAPI.<br/>                        |
| [*DIFXAPILOGCALLBACK*](/previous-versions/windows/hardware/difxapi/difxapilogcallback)<br/>             | Une fonction de type **DIFXAPILOGCALLBACK** est une fonction de rappel fournie par l’application qu’une application enregistre avec difxapi en appelant [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback). DIFxAPI appelle la fonction de rappel pour consigner les événements qui se produisent pendant l’opération DIFxAPI.<br/> |
| [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)<br/>     | La fonction **DIFXAPISetLogCallback** inscrit une fonction de rappel fournie par l’appelant qui difxapi appelle pour consigner des informations sur les événements qui se produisent pendant les opérations difxapi. <br/>                                                                                                            |
| [**DriverPackageGetPath**](/previous-versions/windows/hardware/difxapi/driverpackagegetpath)<br/>       | La fonction **DriverPackageGetPath** récupère le chemin d’accès complet du [fichier INF](/windows-hardware/drivers/install/overview-of-inf-files) pour un package de [pilotes](/windows-hardware/drivers/install/driver-packages)préinstallé.<br/>                                                                                                               |
| [**DriverPackageInstall**](/previous-versions/windows/hardware/difxapi/driverpackageinstall)<br/>       | La fonction **DriverPackageInstall** préinstalle un [package de pilotes](/windows-hardware/drivers/install/driver-packages) , puis installe le pilote dans le système.<br/>                                                                                                                                                 |
| [**DriverPackagePreinstall**](/previous-versions/windows/hardware/difxapi/driverpackagepreinstall)<br/> | La fonction **DriverPackagePreinstall** préinstalle un [package de pilotes](/windows-hardware/drivers/install/driver-packages) pour un [pilote de fonction](/windows-hardware/drivers/kernel/function-drivers) plug-and-Play (PNP) et installe le [fichier INF](/windows-hardware/drivers/install/overview-of-inf-files) pour le package de pilotes dans le répertoire du fichier INF du système.<br/>             |
| [**DriverPackageUninstall**](/previous-versions/windows/hardware/difxapi/driverpackageuninstall)<br/>   | La fonction **DriverPackageUninstall** désinstalle le [package de pilotes](/windows-hardware/drivers/install/driver-packages) spécifié du système et supprime le package de pilotes. <br/>                                                                                                                               |
| [**INSTALLERINFO**](/previous-versions/windows/hardware/difxapi/installerinfo)<br/>                     | La structure INSTALLERINFO contient des informations sur une application que DIFxAPI associe à un [package de pilotes](/windows-hardware/drivers/install/driver-packages). <br/>                                                                                                                                          |
| [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)<br/>           | La fonction **SetDifxLogCallback** inscrit une fonction de rappel fournie par l’appelant qui difxapi appelle pour consigner des informations sur les événements qui se produisent pendant les opérations difxapi. <br/>                                                                                                               |



 

 

 

[Envoyer des commentaires sur cette rubrique à Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Difxapi.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Envoyer des commentaires sur cette rubrique à Microsoft")