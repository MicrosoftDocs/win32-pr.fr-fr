---
description: les actions personnalisées ne doivent pas appeler la fonction SRSetRestorePoint, car cela peut entraîner l’écriture d’un point d’entrée de restauration au milieu d’une installation Windows Installer.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Définition d’un point de restauration à partir d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b30dad9f8f250c0ae82286425d092538ad8324715e632e2c5074e428454f76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628579"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Définition d’un point de restauration à partir d’une action personnalisée

les actions personnalisées ne doivent pas appeler la fonction [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) , car cela peut entraîner l’écriture d’un point d’entrée de restauration au milieu d’une installation Windows Installer.

pour plus d’informations, consultez [Points de restauration du système et le Windows Installer](system-restore-points-and-the-windows-installer.md).

 

 
