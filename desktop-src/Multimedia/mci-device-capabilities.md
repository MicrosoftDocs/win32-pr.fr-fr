---
title: Fonctionnalités de l’appareil MCI
description: Fonctionnalités de l’appareil MCI
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- MCIWndCanConfig macro)
- MCIWndCanEject macro)
- MCIWndCanPlay macro)
- MCIWndCanRecord macro)
- MCIWndCanSave macro)
- MCIWndCanWindow macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195147"
---
# <a name="mci-device-capabilities"></a>Fonctionnalités de l’appareil MCI

MCIWnd comprend les macros suivantes qui vous permettent d’interroger les périphériques MCI pour leurs fonctionnalités.



| Macro                                      | Description                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | Détermine si un appareil dispose d’une boîte de dialogue de configuration pour prendre en charge plusieurs configurations, telles que le périphérique MCIAVI.                   |
| [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | Détermine si un appareil dispose d’une fonction d’éjection contrôlée par logiciel.                                                                       |
| [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | Détermine si un appareil peut lire le contenu existant.                                                                                  |
| [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | Détermine si un appareil peut enregistrer.                                                                                                     |
| [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | Détermine si un appareil peut stocker des données.                                                                                                 |
| [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | Détermine si un appareil prend en charge les commandes de fenêtre MCI (telles que [**Window**](window.md), [**put**](put.md) et [**Where**](where.md)). |



 

Ces macros retournent **true** si l’appareil prend en charge la fonctionnalité spécifique, ou **false** dans le cas contraire.

 

 




