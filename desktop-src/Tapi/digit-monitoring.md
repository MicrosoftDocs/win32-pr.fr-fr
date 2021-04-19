---
description: L’analyse des chiffres surveille l’appel de chiffres.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Analyse des chiffres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515424"
---
# <a name="digit-monitoring"></a>Analyse des chiffres

L’analyse des chiffres surveille l’appel de chiffres. L’interface TAPI permet aux chiffres d’être signalés selon deux méthodes (modes numériques) :

-   Les chiffres de l’impulsion sont signalés comme des séquences d’impulsions ou de rotation. Pour la détection, ces impulsions se manifestent comme rien de plus que les séquences de clics audibles. Les chiffres de l’impulsion valides sont « 0 » à « 9 ».
-   Les chiffres DTMF sont signalés comme des tonalités DTMF (fréquence multiple de tonalité double). Les chiffres DTMF valides sont « 0 » à « 9 », « A ». 'B', 'C', 'd', ' \* 'et' \# '. Le bord de début et le bas des chiffres DTMF peuvent être surveillés.

Une application peut activer ou désactiver la surveillance des chiffres sur un appel spécifié avec [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits). Lorsque l’analyse des chiffres est activée, les chiffres détectés entraînent la notification de l’application avec le message de [**ligne \_ MONITORDIGITS**](line-monitordigits.md) . Ce message fournit le descripteur d’appel sur lequel le chiffre a été détecté, ainsi que la valeur de chiffre et le mode de chiffre. La portée de l’analyse des chiffres est liée par la durée de vie de l’appel. La surveillance des chiffres sur un appel se termine dès que l’appel *se déconnecte* ou devient *inactif*.

 

 



