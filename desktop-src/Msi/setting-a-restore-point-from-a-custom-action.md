---
description: les actions personnalisées ne doivent pas appeler la fonction SRSetRestorePoint, car cela peut entraîner l’écriture d’un point d’entrée de restauration au milieu d’une installation Windows Installer.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Définition d’un point de restauration à partir d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8539c436dbdb960c813b6125557639161dd4a329
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238607"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Définition d’un point de restauration à partir d’une action personnalisée

les actions personnalisées ne doivent pas appeler la fonction [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) , car cela peut entraîner l’écriture d’un point d’entrée de restauration au milieu d’une installation Windows Installer.

pour plus d’informations, consultez [Points de restauration du système et le Windows Installer](system-restore-points-and-the-windows-installer.md).

 

 
