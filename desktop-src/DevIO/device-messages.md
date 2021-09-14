---
description: Les messages de l’appareil sont des messages système qui notifient les applications et d’autres fonctionnalités des événements de modification d’appareil.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Messages des appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114333"
---
# <a name="device-messages"></a>Messages des appareils

Les messages de l’appareil sont des messages système qui notifient les applications et d’autres fonctionnalités des événements de modification d’appareil. Ces événements se produisent lorsque le système détecte une modification apportée au matériel système, par exemple lorsque l’utilisateur ancre et déconnecte un ordinateur portable, ou insère ou supprime un appareil tel qu’une carte PCMCIA. Les événements d’appareil peuvent se produire lorsque le système est en cours d’exécution ou lorsque le système reprend l’opération une fois temporairement suspendu.

Pour garantir que les applications ne perdent pas de données lorsque les appareils deviennent indisponibles, le système surveille la configuration matérielle et envoie des messages d’appareil aux applications pour les notifier des modifications et leur permet de préparer les modifications avant qu’elles ne se produisent.

Pour chaque événement d’appareil, le système diffuse un message [**WM \_ DEVICECHANGE**](wm-devicechange.md) à toutes les applications. Dans ce message, le paramètre *wParam* identifie le [type d’événement](device-event-types.md) de l’appareil et le paramètre *lParam* est un pointeur vers des données spécifiques à l’événement.

 

 



