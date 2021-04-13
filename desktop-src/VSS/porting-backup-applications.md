---
description: Les fichiers binaires de Windows Server 2003 avec Service Pack 1 (SP1) sont compatibles avec Windows Vista et Windows Server 2008. Toutefois, les fichiers binaires des versions antérieures de Windows doivent être recompilés.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Portage des applications de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528708"
---
# <a name="porting-backup-applications"></a>Portage des applications de sauvegarde

Les fichiers binaires de Windows Server 2003 avec Service Pack 1 (SP1) sont compatibles avec Windows Vista et Windows Server 2008. Toutefois, les fichiers binaires des versions antérieures de Windows doivent être recompilés.

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a>Portage des applications de sauvegarde Windows XP vers Windows Vista

Plusieurs interfaces VSS ont été modifiées depuis Windows XP. Au minimum, les applications Windows XP doivent être recompilées à l’aide de fichiers d’en-tête et de bibliothèques du kit de développement logiciel (SDK) VSS 7,2 ou du kit de développement logiciel (SDK) Windows Vista ou Windows Server 2008.

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a>Portage des applications de sauvegarde Windows Server 2003 SP1 vers Windows Vista

Les fichiers binaires de Windows Server 2003 avec SP1 sont compatibles avec Windows Vista et Windows Server 2008. Toutefois, la plupart des applications de sauvegarde Windows Server 2003 avec SP1 doivent être mises à jour pour prendre en compte les nouvelles fonctionnalités, qui sont décrites dans les sections suivantes.

## <a name="compiling-backup-applications-for-windows-vista"></a>Compilation d’applications de sauvegarde pour Windows Vista

Les applications qui utilisent des interfaces disponibles dans Windows Server 2003 peuvent être compilées à l’aide de fichiers d’en-tête et de bibliothèques fournis dans le kit de développement logiciel (SDK) VSS 7,2. Pour utiliser les nouvelles interfaces, les applications doivent être recompilées à l’aide des fichiers d’en-tête et des bibliothèques inclus dans le kit de développement logiciel (SDK) Windows Vista.

> [!Note]  
> Les fichiers binaires compilés à l’aide de Windows Vista ou Windows Server 2008 ne sont pas compatibles avec Windows Server 2003 avec SP1 ou des versions antérieures de Windows.

 

 

 



