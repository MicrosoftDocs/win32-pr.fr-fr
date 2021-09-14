---
description: La fonction DeviceIoControl fournit une interface de contrôle d’entrée et de sortie de l’appareil (IOCTL) par le biais de laquelle une application peut communiquer directement avec un pilote de périphérique.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Contrôle d’entrée et de sortie de l’appareil (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114373"
---
# <a name="device-input-and-output-control-ioctl"></a>Contrôle d’entrée et de sortie de l’appareil (IOCTL)

La fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) fournit une interface de contrôle d’entrée et de sortie de l’appareil (IOCTL) par le biais de laquelle une application peut communiquer directement avec un pilote de périphérique. La fonction **DeviceIoControl** est une interface à usage général qui peut envoyer des codes de contrôle à un large éventail d’appareils. Chaque code de contrôle représente une opération que le pilote doit effectuer. Par exemple, un code de contrôle peut demander à un pilote de périphérique de retourner des informations sur l’appareil correspondant ou indiquer au pilote d’effectuer une action sur l’appareil, comme la mise en forme d’un disque.

Un certain nombre de codes de contrôle standard sont définis dans les fichiers d’en-tête du kit de développement logiciel (SDK). En outre, les pilotes de périphérique peuvent définir leurs propres codes de contrôle spécifiques à l’appareil. Pour obtenir la liste des codes de contrôle standard inclus dans la documentation du kit de développement logiciel (SDK), consultez la section Notes de [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).

Les types de codes de contrôle que vous pouvez spécifier dépendent de l’appareil accédé et de la plateforme sur laquelle votre application s’exécute. Les applications peuvent utiliser les codes de contrôle standard ou les codes de contrôle spécifiques à l’appareil pour effectuer des opérations d’entrée et de sortie directes sur un lecteur de disquette, un lecteur de disque dur, un lecteur de bande ou un lecteur de CD-ROM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Appeler DeviceIoControl](calling-deviceiocontrol.md)
</dt> </dl>

 

 
