---
description: Le moniteur d’événements de mise hors tension permet à l’utilisateur ou à l’application de documenter la raison de l’arrêt ou du redémarrage du système.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Moniteur d’événements de mise hors tension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee2deaebde736ed2e0ba72f38e8849cf815b167da68fdddbecb92e713083699b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664359"
---
# <a name="shutdown-event-tracker"></a>Moniteur d’événements de mise hors tension

Le *moniteur d’événements de mise hors tension* permet à l’utilisateur ou à l’application de documenter la raison de l’arrêt ou du redémarrage du système. L’utilisateur est invité à renseigner les informations lors de la sélection de l’option **arrêter** dans le menu **Démarrer** , ou lors de l’utilisation de Shutdown.exe. Les développeurs peuvent inclure un code de raison lors de l’appel des fonctions [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) et [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) . Les informations sont stockées dans le journal des événements.

**Windows XP :** si cette fonctionnalité est activée par défaut à partir de Windows Server 2003, vous devez l’activer sur Windows XP. Pour plus d’informations, consultez la documentation du moniteur d’événements de mise hors tension inclus dans le système ou sur TechNet.

Les fonctions [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) et [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) ont été mises à jour pour prendre en charge les codes de raison de l’arrêt dans le paramètre *dwReason* . Utilisez les valeurs définies dans Reason. h pour construire un code de raison d’arrêt ou définir un code de raison personnalisé. Un code de raison d’arrêt est construit à partir d’un indicateur majeur, d’un drapeau mineur et de deux indicateurs facultatifs. Pour plus d’informations, consultez codes de raison de l' [arrêt du système](system-shutdown-reason-codes.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Moniteur d’événements de mise hors tension (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))
</dt> </dl>

 

 
