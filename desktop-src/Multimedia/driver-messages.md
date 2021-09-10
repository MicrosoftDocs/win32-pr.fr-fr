---
title: Messages du pilote
description: Messages du pilote
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- pilotes installables, messages
- pilotes installables, messages personnalisés
- messages du pilote
- messages de pilote personnalisés
- pilotes installables, fonction DriverProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368948"
---
# <a name="driver-messages"></a>Messages du pilote

Chaque message de pilote se compose d’un identificateur de message et de paramètres 2 32 bits. L’identificateur de message est une valeur unique que la fonction [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) vérifie pour déterminer l’action à effectuer. La signification des paramètres du message dépend du message. Les paramètres peuvent représenter des valeurs ou des adresses. Dans de nombreux cas, les paramètres ne sont pas utilisés et sont définis sur zéro.

Les messages de pilote peuvent être standard ou personnalisés. Windows envoie des messages de pilote standard, tels que [**DRV \_ OPEN**](drv-open.md), [**drv \_ CLOSE**](drv-close.md)et [**drv \_ configure**](drv-configure.md), à un pilote installable en réponse à une demande d’ouverture, de fermeture ou de configuration du pilote. Les messages standard indiquent au pilote installable de charger ou de décharger ses ressources, d’activer ou de désactiver son fonctionnement, d’ouvrir ou de fermer une instance de pilote et d’afficher une boîte de dialogue de configuration. Certains messages standard, tels que [**DRV \_ Power**](drv-power.md) et [**DRV \_ EXITSESSION**](drv-exitsession.md), notifient au pilote des événements à l’ensemble du système qui affectent le fonctionnement du pilote ou de tout matériel associé.

Les applications et les dll envoient des messages de pilote personnalisés pour indiquer à un pilote installable d’effectuer des actions spécifiques au pilote. Les pilotes installables qui prennent en charge les messages personnalisés doivent inclure un traitement approprié dans la fonction **DriverProc** . Pour éviter les conflits entre les messages de pilote standard et personnalisés, les identificateurs de message personnalisés doivent avoir des valeurs allant de DRV \_ réservé à DRV \_ User. Les messages personnalisés passés à la fonction [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) sont ignorés.

 

 