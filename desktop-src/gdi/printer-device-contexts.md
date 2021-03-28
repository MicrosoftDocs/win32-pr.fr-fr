---
description: Le contrôleur de l’imprimante peut être utilisé lors de l’impression sur une imprimante matricielle, une imprimante jet d’encre, une imprimante laser ou un traceur.
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: Contextes de périphérique d’impression (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972566"
---
# <a name="printer-device-contexts-windows-gdi"></a>Contextes de périphérique d’impression (Windows GDI)

Le contrôleur de l’imprimante peut être utilisé lors de l’impression sur une imprimante matricielle, une imprimante jet d’encre, une imprimante laser ou un traceur. Une application crée un DC d’imprimante en appelant la fonction [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) et en fournissant les arguments appropriés (le nom du pilote d’imprimante, le nom de l’imprimante, le nom du fichier ou du périphérique pour le support de sortie physique et d’autres données d’initialisation). Quand une application a terminé l’impression, elle supprime le DC d’imprimante en appelant la fonction [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) . Une application doit supprimer (au lieu de libérer) un contrôleur de l’imprimante ; la fonction [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) échoue lorsqu’une application tente de l’utiliser pour libérer un contrôleur de périphérique d’imprimante.

Pour plus d’informations, consultez sortie de l' [imprimante](../printdocs/printer-output.md).

 

 
