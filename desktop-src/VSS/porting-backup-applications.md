---
description: les fichiers binaires de Windows server 2003 avec Service Pack 1 (SP1) sont compatibles avec Windows Vista et Windows Server 2008. toutefois, les fichiers binaires des versions antérieures de Windows doivent être recompilés.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Portage des applications de sauvegarde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413360"
---
# <a name="porting-backup-applications"></a>Portage des applications de sauvegarde

les fichiers binaires de Windows server 2003 avec Service Pack 1 (SP1) sont compatibles avec Windows Vista et Windows Server 2008. toutefois, les fichiers binaires des versions antérieures de Windows doivent être recompilés.

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a>portage des Applications de sauvegarde Windows XP vers Windows Vista

plusieurs interfaces VSS ont été modifiées depuis Windows XP. au minimum, les applications Windows XP doivent être recompilées à l’aide de fichiers d’en-tête et de bibliothèques du kit de développement logiciel (sdk) VSS 7,2 ou du kit de développement logiciel (sdk) Windows Vista ou Windows Server 2008.

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a>portage des Applications de sauvegarde Windows Server 2003 SP1 vers Windows Vista

les fichiers binaires de Windows server 2003 avec SP1 sont compatibles avec Windows Vista et Windows server 2008. toutefois, la plupart des applications de sauvegarde Windows Server 2003 avec SP1 doivent être mises à jour pour prendre en compte les nouvelles fonctionnalités, qui sont décrites dans les sections suivantes.

## <a name="compiling-backup-applications-for-windows-vista"></a>compilation d’Applications de sauvegarde pour Windows Vista

les Applications qui utilisent des interfaces disponibles dans Windows Server 2003 peuvent être compilées à l’aide de fichiers d’en-tête et de bibliothèques fournis dans le kit de développement logiciel (SDK) VSS 7,2. pour utiliser les nouvelles interfaces, les applications doivent être recompilées à l’aide des fichiers d’en-tête et des bibliothèques inclus dans le kit de développement logiciel (SDK) Windows Vista.

> [!Note]  
> les fichiers binaires compilés à l’aide de Windows Vista ou Windows server 2008 ne sont pas compatibles avec Windows server 2003 avec SP1 ou des versions antérieures de Windows.

 

 

 



