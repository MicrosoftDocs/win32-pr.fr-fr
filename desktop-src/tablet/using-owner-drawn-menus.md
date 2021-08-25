---
description: Utilisation de menus owner-drawn pour la prise en charge des fonctionnalités vocales pour Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Utilisation des menus Owner-Drawn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14e63e3602e31edc506a6c9c070fa0bfcce670ec2248c73d68944a2f83a12f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842799"
---
# <a name="using-owner-drawn-menus"></a>Utilisation des menus Owner-Drawn

Lorsque vous utilisez des menus owner-drawn, vous devez rendre les menus accessibles en vue de la prise en charge des fonctionnalités vocales. Il existe deux façons d'effectuer cette opération :

-   Exposez le nom d’élément de menu à l’aide de la structure MSAAMENUINFO.
-   Fournissez une option pour remplacer les menus graphiques par des menus de texte standard lorsqu’une aide à l’accessibilité est active. Si la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) retourne la **valeur true** avec son paramètre *uiaction* défini sur SPI \_ GETSCREENREADER, utilisez les menus standard. L’application doit surveiller le message WM \_ SETTINGSCHANGE et répondre en interrogeant l’état de cette option et en ajustant son affichage de manière appropriée. par exemple, Microsoft Visual Studio fournit une option permettant d’utiliser des menus standard à la place des menus personnalisés qui sont affichés par défaut.

 

 
